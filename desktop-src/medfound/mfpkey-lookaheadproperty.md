---
description: Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: MFPKEY_LOOKAHEAD propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268988"
---
# <a name="mfpkey_lookahead-property"></a>Propiedad LOOKAHEAD de MFPKEY \_

Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCLookAhead

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Cuando el códec usa lookahead, puede codificar el vídeo de forma más eficaz.

El objeto de escritor del SDK Windows Media Format espera que el códec encodifique cada ejemplo inmediatamente. Como resultado, esta característica no funciona correctamente en el software que usa el objeto de escritor (incluidos Windows Media Encoder y Reproductor de Windows Media). Las extensiones de unidad de datos asociadas a fotogramas de vídeo se asociarán al fotograma de salida incorrecto. El número de fotogramas por los que las extensiones de unidad de datos están fuera de lugar es igual al número de fotogramas de lookahead que se usan.

Los valores válidos de la apariencia oscilan entre 0 y 16 fotogramas. El valor recomendado es 16.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




