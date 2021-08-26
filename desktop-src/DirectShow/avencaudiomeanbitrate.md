---
description: Especifica la velocidad de bits media de la secuencia de audio codificada, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: Propiedad AVEncAudioMeanBitRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7b0d1ad6cfde3aee4ec9c747feb8d692c3917332808e40e3d5f76e3d01ce21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079475"
---
# <a name="avencaudiomeanbitrate-property"></a>Propiedad AVEncAudioMeanBitRate

Especifica la velocidad de bits media de la secuencia de audio codificada, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>Valor de propiedad

Los codificadores pueden implementar esta propiedad como un conjunto enumerado o como un intervalo lineal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




