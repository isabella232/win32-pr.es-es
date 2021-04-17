---
description: Especifica el número máximo de muestras PCM adicionales que podrían devolverse al final de después de descodificar un archivo.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Propiedad MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715879"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>\_Propiedad MaxNumPCMSamplesWithPaddedSilence del descodificador de MFPKEY \_

Especifica el número máximo de muestras PCM adicionales que podrían devolverse al final de después de descodificar un archivo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

2048

## <a name="remarks"></a>Observaciones

Esta propiedad se puede utilizar para calcular el silencio artificial que se inserta entre las canciones a medida que se introducen en el descodificador una tras otra.

En el caso de los descodificadores de Windows Media Audio 10 Professional y Windows Media Audio 9 sin pérdida de, esta propiedad siempre es igual a 0.

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

 

 
