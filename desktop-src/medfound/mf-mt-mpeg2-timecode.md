---
description: Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica que los paquetes de transporte contienen un código de tiempo de 4 bytes.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277689"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>\_Atributo de \_ código de tiempo MF MT MPEG2 \_

Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica que los paquetes de transporte contienen un código de tiempo de 4 bytes.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                                                | Significado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | No se agrega código de tiempo.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Se agrega un código de tiempo de 4 bytes al principio de cada paquete de transporte. Este código de tiempo es necesario para algunos estándares de televisión digital.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




