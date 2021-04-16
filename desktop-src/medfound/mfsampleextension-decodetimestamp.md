---
description: Contiene la marca de tiempo de descodificación (DTS) para el ejemplo.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696684"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>\_Atributo DecodeTimestamp de MFSampleExtension

Contiene la marca de tiempo de descodificación (DTS) para el ejemplo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

El valor del atributo es el DTS en unidades 100-nanosegundos. El DTS se define en algunos estándares de codificación, incluido MPEG. El DTS especifica cuándo se debe descodificar la imagen codificada. Si el vídeo codificado contiene fotogramas B, el DTS puede diferir del tiempo de presentación, ya que las imágenes B aparecen fuera del orden temporal en el fragmentada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> </dl>

 

 




