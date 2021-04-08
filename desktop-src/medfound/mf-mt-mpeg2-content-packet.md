---
description: Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica si los paquetes de transporte contienen encabezados de paquetes de contenido.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: MF_MT_MPEG2_CONTENT_PACKET atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911190"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>\_Atributo de \_ \_ paquete de contenido MF MT MPEG2 \_

Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica si los paquetes de transporte contienen encabezados de paquetes de contenido.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                                                | Significado                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | No se agregan encabezados de paquetes de contenido.<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | A intervalos de 200 a 1.000 milisegundos, se agrega un encabezado de paquete de contenido de 14 bytes al principio del paquete de transporte, tal como se define en la Asociación del estándar de industrias y empresas de radio (ARIB).<br/> |



 

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

 

 




