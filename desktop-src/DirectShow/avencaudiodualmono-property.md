---
description: 'Propiedad AVEncAudioDualMono: especifica si el audio de 2 canales se codifica como estéreo o mono dual.'
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Propiedad AVEncAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7255177290ebbe15104d0264a821e9c17ecdf90b605fbaab435f6d39c577548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052825"
---
# <a name="avencaudiodualmono-property"></a>AvEncAudioDualMono, propiedad

Especifica si el audio de 2 canales está codificado como estéreo o mono dual.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncAudioDualMono**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVEncAudioDualMono.**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)

## <a name="remarks"></a>Comentarios

Esta propiedad no se aplica a los codificadores de audio MPEG. Para audio MPEG, use [**la propiedad AVEncMPACodingMode.**](avencmpacodingmode-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

