---
description: Contiene la marca de tiempo de descodificación (DTS) para el ejemplo.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d72ea69f487efe24148fa8ce60ad05eb7a124673f02a78e70c67f604a51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241486"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>Atributo MFSampleExtension \_ DecodeTimestamp

Contiene la marca de tiempo de descodificación (DTS) para el ejemplo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

El valor del atributo es dts en unidades de 100 nanosegundos. DTS se define en algunos estándares de codificación, incluido MPEG. DtS especifica cuándo se debe descodificar la imagen codificada. Si el vídeo codificado contiene fotogramas B, dts puede diferir del tiempo de presentación, ya que las imágenes B aparecen fuera del orden temporal en la secuencia de bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> </dl>

 

 




