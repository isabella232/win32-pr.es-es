---
description: STRIDE Surface predeterminado, para un tipo de medio de vídeo sin comprimir. STRIDE es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275948"
---
# <a name="mf_mt_default_stride-attribute"></a>MF \_ MT \_ default \_ STRIDE (atributo)

STRIDE Surface predeterminado, para un tipo de medio de vídeo sin comprimir. STRIDE es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Se trata como un valor **INT32** .

## <a name="remarks"></a>Observaciones

El valor del atributo se almacena como **UINT32**, pero debe convertirse en un valor entero con signo de 32 bits. STRIDE puede ser negativo.

STRIDE es positivo para las imágenes de arriba abajo y negativo para las imágenes ascendentes.

Este atributo proporciona el intervalo para una representación *contigua* de la imagen en memoria; es decir, una representación sin bytes de relleno adicionales después de cada fila. Si un búfer multimedia admite la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use el método [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para obtener el paso real de la superficie, que puede incluir bytes de relleno adicionales.

Para obtener más información sobre el intervalo de superficie, consulte [STRIDE](image-stride.md)de la imagen.

Para obtener un ejemplo de cómo calcular el intervalo predeterminado, consulte [búferes de vídeo sin comprimir](uncompressed-video-buffers.md).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Intervalo de imagen](image-stride.md)
</dt> </dl>

 

 




