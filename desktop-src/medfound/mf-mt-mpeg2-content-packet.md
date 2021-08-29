---
description: Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica si los paquetes de transporte contienen encabezados de paquete de contenido.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: MF_MT_MPEG2_CONTENT_PACKET atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc650c28b6d02fdcbdedafcd2e173a501a763fbcfe4fa86a17c5cc98e0cdceba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012915"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>Atributo MF \_ MT \_ MPEG2 \_ CONTENT \_ PACKET

Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica si los paquetes de transporte contienen encabezados de paquete de contenido.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Valor                                                                                                | Significado                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | No se agregan encabezados de paquetes de contenido.<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | A intervalos de entre 200 y 1000 milisegundos, se agrega un encabezado content packet de 14 bytes al principio del paquete de transporte, tal como se define en el estándar Association of Radio Industries and Businesses (ARIB).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




