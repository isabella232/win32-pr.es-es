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
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071169"
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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> <dt>

[**ESQUEMA DE \_ UNIDAD \_ WINBIO**](winbio-unit-schema.md)
</dt> </dl>

 

 





