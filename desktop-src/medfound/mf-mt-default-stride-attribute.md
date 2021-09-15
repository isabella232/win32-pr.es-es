---
description: Paso de superficie predeterminado, para un tipo de medio de vídeo sin comprimir. Stride es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474156"
---
# <a name="mf_mt_default_stride-attribute"></a>Atributo MF \_ MT \_ DEFAULT \_ STRIDE

Paso de superficie predeterminado, para un tipo de medio de vídeo sin comprimir. Stride es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como **un valor INT32.**

## <a name="remarks"></a>Observaciones

El valor del atributo se almacena como **UINT32,** pero se debe convertir en un valor entero de 32 bits con signo. Stride puede ser negativo.

Stride es positivo para las imágenes de arriba a abajo y negativo para las imágenes de abajo hacia arriba.

Este atributo proporciona el intervalo para una *representación contigua* de la imagen en memoria; Es decir, una representación sin bytes de relleno adicionales después de cada fila. Si un búfer multimedia admite la interfaz [**IMF2DBuffer,**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) use el método [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para obtener el paso real de la superficie, que podría incluir bytes de relleno adicionales.

Para obtener más información sobre el paso de superficie, vea [Image Stride](image-stride.md).

Para obtener un ejemplo de cómo calcular el paso predeterminado, vea [Búferes de vídeo sin comprimir.](uncompressed-video-buffers.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



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

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Image Stride](image-stride.md)
</dt> </dl>

 

 




