---
description: Especifica las partes de contenido que el códec de voz debe codificar como música.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: Propiedad MFPKEY_WMAVOICE_ENC_EDL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812631"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>MFPKEY \_ WMAVOICE \_ enc \_ EDL (propiedad)

Especifica las partes de contenido que el códec de voz debe codificar como música.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>Tipo de datos

VT \_ BSTR

## <a name="default-value"></a>Valor predeterminado

Ningún valor predeterminado. Si no se establece esta propiedad, el códec usará el valor de la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) para determinar cómo codificar el contenido.

## <a name="remarks"></a>Observaciones

Puede usar esta propiedad si el modo automático del códec no da resultados satisfactorios.

Este valor es una cadena delimitada por comas que contiene al menos cuatro enteros. El primer entero es el número de versión; Use siempre 1 para este valor. El segundo entero es el número de secciones que se deben codificar como música. Después del segundo entero hay un número de pares de valores que representan rangos en milisegundos, un par para cada sección de contenido que debe codificarse como música.

Por ejemplo, "1, 2100200500600" informa al codificador que use la versión 1 con 2 secciones de música. La primera sección de música comienza en 100 ms y termina en 200 ms. La segunda sección Music comienza en 500 ms y termina en 600 ms.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




