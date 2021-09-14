---
title: WINBIO_CAPABILITY constantes (Winbio \_ types.h)
description: Subtipos de sensor de huella digital.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfd98b4831d5e3dfa13aea365d6ed9ddd30960ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071155"
---
# <a name="winbio_capability-constants"></a>Constantes DE FUNCIONALIDAD DE WINBIO \_

Los siguientes subtipos de sensor de huella digital son valores DE CAPACIDADES DE **\_ WINBIO** que se pueden usar como máscara de bits para el parámetro *Capabilities* de la estructura ESQUEMA DE [**UNIDAD WINBIO. \_ \_**](winbio-unit-schema.md) Se refieren a las funcionalidades del sensor incorporado.




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt><dt>0x00000001</dt></dl> | El sensor puede capturar datos biométricos.<br /> | 
| <span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt><dt>0x00000002</dt></dl> | El sensor puede hacer coincidir los datos biométricos con una identidad.<br /> | 
| <span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt><dt>0x00000004</dt></dl> | El sensor contiene una base de datos incorporada.<br /> | 
| <span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt><dt>0x00000008</dt></dl> | El sensor puede realizar el procesamiento biométrico.<br /> | 
| <span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt><dt>0x00000010</dt></dl> | El sensor puede cifrar datos biométricos.<br /> | 
| <span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt><dt>0x00000020</dt></dl> | El sensor puede actuar como un panel del mouse. Actualmente no se admite.<br /> | 
| <span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt><dt>0x00000040</dt></dl> | El sensor contiene una luz indicadora.<br /> | 
| <span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt><dt>0x00000080</dt></dl> | El adaptador del sensor administra su propia conexión con el hardware biométrico.<br /><blockquote>[!Note]<br />Esta constante solo se aplica a Windows 10 y versiones posteriores.</blockquote><br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                                                                                  |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluye Winbio.h para aplicaciones cliente o Adaptadores de \_ Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> <dt>

[**ESQUEMA DE \_ UNIDAD \_ WINBIO**](winbio-unit-schema.md)
</dt> </dl>

 

 





