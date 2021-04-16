---
description: Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Propiedad MFPKEY_LOOKAHEAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696943"
---
# <a name="mfpkey_lookahead-property"></a>\_Propiedad de búsqueda anticipada MFPKEY

Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCLookAhead

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Cuando el códec usa la búsqueda anticipada, puede codificar el vídeo de forma más eficaz.

El objeto de escritor del SDK de Windows Media Format espera que el códec codifique cada ejemplo inmediatamente. Como resultado, esta característica no funciona correctamente en el software que utiliza el objeto de escritor (incluido Windows Media Encoder y Windows Media Player). Cualquier extensión de unidad de datos asociada con fotogramas de vídeo se adjuntará al fotograma de salida incorrecto. El número de fotogramas por los que las extensiones de unidad de datos se colocan de forma no es igual al número de fotogramas de la búsqueda anticipada que se usan.

Los valores de búsqueda anticipada válidos van de 0 a 16 fotogramas. El valor recomendado es 16.

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

 

 




