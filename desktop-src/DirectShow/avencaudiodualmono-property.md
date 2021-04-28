---
description: 'Propiedad AVEncAudioDualMono: especifica si el audio de 2 canales está codificado como estéreo o mono dual.'
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Propiedad AVEncAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096583"
---
# <a name="avencaudiodualmono-property"></a>Propiedad AVEncAudioDualMono

Especifica si el audio de 2 canales está codificado como estéreo o mono dual.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncAudioDualMono**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVEncAudioDualMono.**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)

## <a name="remarks"></a>Comentarios

Esta propiedad no se aplica a los codificadores de audio MPEG. Para el audio MPEG, use [**la propiedad AVEncMPACodingMode.**](avencmpacodingmode-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones de escritorio de Windows 2000 Professional \[ \| para aplicaciones para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones de escritorio de Windows 2000 Server \[ \| para aplicaciones para UWP\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

