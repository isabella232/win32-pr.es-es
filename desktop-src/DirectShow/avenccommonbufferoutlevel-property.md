---
description: Especifica el nivel final del búfer de codificación, en bits, al final del proceso de codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Propiedad AVEncCommonBufferOutLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666140"
---
# <a name="avenccommonbufferoutlevel-property"></a>Propiedad AVEncCommonBufferOutLevel

Especifica el nivel final del búfer de codificación, en bits, al final del proceso de codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonBufferOutLevel**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo de valores lineal. Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

La propiedad solo está disponible si la duración de la codificación se define de antemano mediante la propiedad [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) o la propiedad [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) .

En el vídeo MPEG, esta propiedad define el llenado del comprobador de búfer de vídeo (VBV) al final del proceso de codificación. Admite la concatenación de flujos durante la codificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




