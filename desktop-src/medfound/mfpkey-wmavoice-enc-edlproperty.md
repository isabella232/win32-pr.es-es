---
description: Especifica las partes del contenido que se codificarán como música mediante el códec de voz.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ffc9f68c7122897c9f5032e9ac0e4fc93c596b5ce65f18d44fb6af6dff2dd2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713725"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>Propiedad MFPKEY \_ WMAVOICE \_ ENC \_ EDL

Especifica las partes del contenido que se codificarán como música mediante el códec de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>Tipo de datos

VT \_ BSTR

## <a name="default-value"></a>Valor predeterminado

Ningún valor predeterminado. Si no se establece esta propiedad, el códec usará el valor de la propiedad [ \_ MFPKEY WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) para determinar cómo codificar el contenido.

## <a name="remarks"></a>Comentarios

Puede usar esta propiedad si el modo automático del códec no proporciona resultados satisfactorios.

Este valor es una cadena delimitada por comas que contiene al menos cuatro enteros. El primer entero es el número de versión; use siempre 1 para este valor. El segundo entero es el número de secciones que se deben codificar como música. Después del segundo entero hay varios pares de valores que representan intervalos en milisegundos, un par por cada sección de contenido que debe codificarse como música.

Por ejemplo, "1,2,100,200,500,600" informa al codificador de que use la versión 1 con 2 secciones de música. La primera sección de música comienza en 100 ms y termina en 200 ms. La segunda sección de música comienza en 500 ms y termina en 600 ms.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




