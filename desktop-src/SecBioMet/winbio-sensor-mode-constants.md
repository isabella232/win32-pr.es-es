---
title: Constantes de WINBIO_SENSOR_MODE (Winbio \_ Types. h)
description: Establezca el modo de adaptador de sensor.
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
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803902"
---
# <a name="winbio_sensor_mode-constants"></a>Constantes de modo de \_ sensor de WINBIO \_

Los valores siguientes se usan en la función [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) para establecer el modo de adaptador de sensor.



| Constante                                                                                                                                                                                                        | Descripción                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**\_modo desconocido del sensor de WINBIO \_ \_**</dt> </dl>          | No se conoce el modo operativo.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**\_modo básico del sensor de WINBIO \_ \_**</dt> </dl>                | Use el sensor en modo básico. El sensor actúa únicamente como un dispositivo de captura. No se utiliza ninguna funcionalidad de almacenamiento o procesamiento incorporado que exista.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**\_modo avanzado del sensor de WINBIO \_ \_**</dt> </dl>       | Use el sensor en modo avanzado. El sensor puede capturar ejemplos y realizar funciones de almacenamiento y búsqueda de coincidencias.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**\_modo de \_ navegación del sensor de WINBIO \_**</dt> </dl> | Use el sensor como almohadilla del mouse. Actualmente no se admite.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**\_modo de \_ suspensión del sensor de WINBIO \_**</dt> </dl>                | Use el sensor en modo de suspensión.<br/>                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





