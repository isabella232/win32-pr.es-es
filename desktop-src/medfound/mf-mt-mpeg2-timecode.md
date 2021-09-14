---
description: Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica que los paquetes de transporte contienen un código de tiempo de 4 bytes.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257847"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>Atributo \_ \_ TIMECODE DE MF MT MPEG2 \_

Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica que los paquetes de transporte contienen un código de tiempo de 4 bytes.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                                                | Significado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | No se agrega ningún código de hora.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Se agrega un código de tiempo de 4 bytes al principio de cada paquete de transporte. Este código de tiempo es necesario para algunos estándares de televisión digital.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




