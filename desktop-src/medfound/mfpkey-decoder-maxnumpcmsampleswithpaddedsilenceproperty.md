---
description: Especifica el número máximo de muestras de PCM adicionales que se pueden devolver al final de después de lacoding de un archivo.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572749"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>MFPKEY \_ Decoder \_ MaxNumPCMSamplesWithPaddedSilence (Propiedad)

Especifica el número máximo de muestras de PCM adicionales que se pueden devolver al final de después de lacoding de un archivo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

2048

## <a name="remarks"></a>Observaciones

Esta propiedad se puede usar para calcular el silencio artificial que se inserta entre las canciones a medida que se introducen en el descodificador una tras otra.

Para los descodificadores sin pérdida Windows Media Audio 10 Professional y Windows Media Audio 9, esta propiedad siempre es igual a 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
