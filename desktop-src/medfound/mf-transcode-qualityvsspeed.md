---
description: Especifica un número entre 0 y 100 que indica el equilibrio entre la calidad de codificación y la velocidad de codificación.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: MF_TRANSCODE_QUALITYVSSPEED atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7498cd319f347d8509f42e1713e1b2e267b32406eceb073ea9ca1e4cb4ea8d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604675"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>Atributo \_ MF TRANSCODE \_ QUALITYVSSPEED

Especifica un número entre 0 y 100 que indica el equilibrio entre la calidad de codificación y la velocidad de codificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor de esta propiedad tiene el intervalo siguiente.



| Valor                                                                          | Significado                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | Codificación más rápida y de menor calidad.<br/>  |
| <dl> <dt>100</dt> </dl> | Codificación más lenta y de mayor calidad.<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo tiene el mismo valor GUID que la propiedad [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) definida para [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)y tiene la misma interpretación.

La aplicación puede establecer este atributo en el perfil de transcodificación antes de compilar la topología de transcodificación para Windows códecs multimedia. El valor debe estar en el intervalo de 0 a 100. Para la secuencia de vídeo, el generador de topologías de transcodificación asigna un valor al valor especificado por la aplicación y proporciona el valor asignado a la propiedad **MFPKEY \_ COMPLEXITYEX** del codificador. Los valores inferiores permiten al codificador usar algoritmos de codificación menos complicados. El uso de algoritmos más sencillos genera una salida de menor calidad, pero el proceso de codificación es más rápido y requiere menos potencia de procesamiento.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodificación de API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
