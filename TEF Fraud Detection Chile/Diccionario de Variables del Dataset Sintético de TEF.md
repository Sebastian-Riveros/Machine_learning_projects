## Diccionario de Variables de Dataset Sintético de TEF (Transferencias Electrónicas de Fondos)

Este documento describe cada una de las columnas presentes en el dataset sintético de Transferencias Electrónicas de Fondos (TEF).

| Variable | Tipo de Dato | Descripción |
|---|---|---|
| `transaction_id` | String | Identificador único de la transacción. |
| `timestamp` | Datetime | Fecha y hora en que se realizó la transacción. |
| `sender_id` | String | Identificador único del usuario que envía la transacción. |
| `receiver_id` | String | Identificador único del usuario o comerciante que recibe la transacción. Puede ser un `USER_XXXXXX`, `MERCHANT_XXXXXX`, `MULA_ACC_XXXXXX`, `MULA_CARD_CLONE_XXXXXX`. |
| `amount` | Float | Monto de la transacción en CLP. |
| `currency` | String | Moneda de la transacción (siempre 'CLP' en este dataset). |
| `transaction_type` | String | Tipo de transacción (ej. 'TRANSFERENCIA', 'PAGO_COMERCIO', 'PAGO_SERVICIO', 'PAGO_CUENTA'). |
| `sender_bank` | String | Banco al que pertenece el emisor de la transacción. |
| `sender_balance_before` | Float | Saldo del emisor antes de la transacción. |
| `sender_balance_after` | Float | Saldo del emisor después de la transacción. |
| `receiver_balance_before` | Float | Saldo del receptor antes de la transacción. Para comerciantes, este valor es 0. |
| `receiver_balance_after` | Float | Saldo del receptor después de la transacción. Para comerciantes, este valor es 0. |
| `is_fraud` | Integer (0 o 1) | Indicador binario: 1 si la transacción es fraudulenta, 0 si es legítima. |
| `fraud_type` | String | Tipo específico de fraude si `is_fraud` es 1 (ej. 'Vishing/Phishing', 'SIM_Swapping', 'Autofraude', 'Billeteras_D', 'Apertura_Na', 'Clonacion_T'). 'None' si no es fraude. |
| `sender_location_lat` | Float | Latitud de la ubicación desde donde se originó la transacción del emisor. |
| `sender_location_lon` | Float | Longitud de la ubicación desde donde se originó la transacción del emisor. |
| `receiver_location_lat` | Float | Latitud de la ubicación del receptor de la transacción. |
| `receiver_location_lon` | Float | Longitud de la ubicación del receptor de la transacción. |
| `distance_from_home` | Float | Distancia en kilómetros entre la ubicación de la transacción del emisor y su ubicación 'hogar' registrada. |
| `time_since_last_transaction` | Float | Tiempo en horas transcurrido desde la última transacción del emisor. Es 0 para la primera transacción de un usuario o si es instantánea. |
| `sender_device_id` | String | Identificador del dispositivo utilizado por el emisor. |
| `receiver_device_id` | String | Identificador del dispositivo utilizado por el receptor. Puede ser 'N/A' si el receptor es un comerciante o si el dispositivo no es relevante para el tipo de receptor. |
| `sender_ip_address` | String | Dirección IP desde la que se originó la transacción del emisor. |
| `receiver_ip_address` | String | Dirección IP del receptor. Puede ser 'N/A' si el receptor es un comerciante o si la IP no es relevante para el tipo de receptor. |
| `sender_account_age` | Integer | Antigüedad de la cuenta del emisor en días. |
| `sender_avg_daily_transactions` | Float | Promedio de transacciones diarias del emisor. |
| `sender_avg_daily_amount` | Float | Promedio del monto diario transaccionado por el emisor. |
| `sender_recent_account_changes` | String | Indicadores de cambios recientes en la cuenta del emisor (ej. 'phone_number_change', 'new_device_login', 'unusual_ip_address', 'identity_theft_flag', 'new_account_opened_recently', 'unusual_transaction_pattern', 'card_compromised_flag'). 'none' si no hay cambios. |
| `sender_communication_channel_flag` | String | Indicador de comunicación sospechosa asociada al emisor (ej. 'suspicious_call_preceding_transfer', 'phishing_email_reported', 'fake_bank_contact', 'potential_self_initiated'). 'none' si no hay comunicación sospechosa. |
|`last_24h_count`| int64 | Transacciones en las últimas 24 horas por emisor
| `avg_amount_last_7d`| float64 | Monto promedio en los últimos 7 días por emisor
| `amount_vs_avg`| float64 | Desvío de monto respecto a promedio diario
|`recent_tx_ratio`| float64 | Ratio transacciones recientes / promedio diario
| `sender_balance_delta` | float64|Cambio de balance sender / receiver
| `receiver_balance_delta`| float64 | Cambio de balance receiver / sender
| `distance_sender_receiver`| float64 | Distancia entre sender y receiver

#==============================================================================================================================
