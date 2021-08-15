---
title: WINBIO_SENSOR_MODE constantes (Winbio \_ types.h)
description: Establezca el modo del adaptador del sensor.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8f0cb4592931629e6feec4fff4a6ac3e5986d3b199afee719dd8dae67a9580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909333"
---
# <a name="winbio_sensor_mode-constants"></a>Constantes DEL \_ MODO SENSOR DE WINBIO \_

Los valores siguientes se usan en la [**función SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) para establecer el modo del adaptador del sensor.



| Constante                                                                                                                                                                                                        | Descripción                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**MODO DESCONOCIDO \_ DEL SENSOR \_ \_ WINBIO**</dt> </dl>          | No se conoce el modo de funcionamiento.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**MODO BÁSICO \_ DEL SENSOR \_ \_ WINBIO**</dt> </dl>                | Utilice el sensor en modo básico. El sensor actúa solo como un dispositivo de captura. No se usan las funcionalidades de procesamiento o almacenamiento incorporadas que existan.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**MODO AVANZADO \_ DEL SENSOR \_ \_ WINBIO**</dt> </dl>       | Utilice el sensor en modo avanzado. El sensor puede capturar ejemplos y realizar funciones de coincidencia y almacenamiento.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**MODO DE \_ NAVEGACIÓN DEL SENSOR \_ \_ WINBIO**</dt> </dl> | Utilice el sensor como panel del mouse. Actualmente no se admite.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**MODO DE \_ SUSPENSIÓN DEL SENSOR \_ \_ WINBIO**</dt> </dl>                | Utilice el sensor en modo de suspensión.<br/>                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





