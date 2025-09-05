Acceso a link descarga del Dataset: https://www.kaggle.com/datasets/sebastinriverossalas/fraude-transaccin-electrnica-de-fondos-tef-chile

Este es un Dataset Sintético creado a partir de una revisión exhaustiva sobre el panorama de fraudes bancarios asociados principalmente a transacciones electrónicas de fondos (TEF) en Chile. 

El Dataset incluye:

Variables de Transacción Base: Incluye los datos esenciales de cualquier transacción (amount, sender_bank, timestamp), que son la base para cualquier análisis de comportamiento.
Características de Comportamiento: Variables como sender_avg_daily_transactions, sender_avg_daily_amount, time_since_last_transaction, y las características desagregadas (last_24h_count, avg_amount_last_7d) son cruciales. El fraude a menudo se detecta como una anomalía en el patrón de comportamiento del usuario, y estas variables capturan precisamente eso.
Características Geográficas y de Dispositivo: La inclusión de coordenadas de ubicación, distance_from_home, sender_device_id, y sender_ip_address es fundamental. El fraude de tipo SIM_Swapping o Clonacion_T a menudo se correlaciona con transacciones desde ubicaciones o dispositivos inusuales.
Indicadores de Fraude Específicos: Las variables categóricas como sender_recent_account_changes y sender_communication_channel_flag simulan alertas internas o reportes que una institución financiera podría tener. Estas son características de alto valor predictivo.
Balance delta: Las variables sender_balance_delta y receiver_balance_delta son excelentes características de ingeniería que capturan el cambio neto en los saldos, lo cual es un indicador directo del flujo de fondos y esencial para modelar este tipo de datos.
Manejo del Desbalance de Clases: La columna target "is_fraud" tiene un mean de 0.02199, lo que indica que aproximadamente el 2.2% de las transacciones son fraudulentas (gran parte asociadas a Banco Estado). Siendo un porcentaje realista para los datasets de fraude financiero, que suelen tener una alta tasa de desbalance.
Finalmente, el objetivo es ofrecer una representación realista de los fraudes asociados a TEF's en Chile. A pesar de ser sintético, su estructura y las relaciones entre las variables lo hacen un excelente recurso educativo para estudiantes y profesionales que deseen practicar la detección de fraudes bancarios.
