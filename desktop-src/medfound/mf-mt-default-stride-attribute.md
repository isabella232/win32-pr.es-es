---
description: Paso de superficie predeterminado, para un tipo de medio de vídeo sin comprimir. Stride es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e130918f62d6ff986ced7dd6449dcc2d381a00fc0d7c0342eeb4afcc03833bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035243"
---
# <a name="mf_mt_default_stride-attribute"></a>Atributo MF \_ MT \_ DEFAULT \_ STRIDE

Paso de superficie predeterminado, para un tipo de medio de vídeo sin comprimir. Stride es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un **valor INT32.**

## <a name="remarks"></a>Comentarios

El valor del atributo se almacena como **UINT32,** pero se debe convertir en un valor entero de 32 bits con signo. Stride puede ser negativo.

Stride es positivo para las imágenes de arriba abajo y negativo para las imágenes de abajo hacia arriba.

Este atributo proporciona el intervalo para una *representación contigua* de la imagen en memoria; es decir, una representación sin bytes de relleno adicionales después de cada fila. Si un búfer multimedia es compatible con la interfaz [**IMF2DBuffer,**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) use el método [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para obtener el paso real de la superficie, lo que podría incluir bytes de relleno adicionales.

Para obtener más información sobre el paso de superficie, vea [Image Stride](image-stride.md).

Para obtener un ejemplo de cómo calcular el paso predeterminado, vea [Búferes de vídeo sin comprimir.](uncompressed-video-buffers.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> <dt>

[Image Stride](image-stride.md)
</dt> </dl>

 

 




