---
title: WINBIO_BIOMETRIC_SENSOR_SUBTYPE constantes (Winbio \_ types.h)
description: Especifique una máscara de bits para incorporar funcionalidades de sensor.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08cb98e4645b3e65a5dd56d60450acbc0d949ea673afec25baba6d335217ffa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911038"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a>Constantes DE \_ \_ SUBTIPO DE SENSOR \_ BIOMÉTRICO WINBIO

Las siguientes constantes se pueden usar como máscara de bits para el parámetro *Capabilities* de la [**estructura DE ESQUEMA \_ DE \_ UNIDAD WINBIO.**](winbio-unit-schema.md) Se refieren a las funcionalidades del sensor incorporado.



| Constante                                                                                                                                                                                                            | Descripción                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <dt>**SUBTIPO DE SENSOR WINBIO \_ \_ \_ DESCONOCIDO**</dt> </dl>     | No se conocen los subtipos de sensor.<br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <dt>**DESLIZAMIENTO DEL \_ SUBTIPO DEL SENSOR DE FP \_ \_ DE WINBIO \_**</dt> </dl> | El sensor admite deslizamientos de huellas digitales.<br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <dt>**WINBIO \_ FP \_ SENSOR \_ SUBTYPE \_ TOUCH**</dt> </dl> | El sensor admite toques de dedo.<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> <dt>

[**ESQUEMA DE \_ UNIDAD \_ WINBIO**](winbio-unit-schema.md)
</dt> </dl>

 

 





