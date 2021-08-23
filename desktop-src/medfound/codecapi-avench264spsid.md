---
description: Establece el identificador del conjunto de parámetros de secuencia (SPS) en la unidad de capa de abstracción de red (NAL) de SPS de la secuencia de bits H.264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da06e431a3747e676e3934ac9a261e1d0e1ec37e18bacf01f8a3e623c4257488
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664665"
---
# <a name="codecapi_avench264spsid-property"></a>Propiedad CODECAPI \_ AVEncH264SPSID

Establece el identificador del conjunto de parámetros de secuencia (SPS) en la unidad de capa de abstracción de red (NAL) de SPS de la secuencia de bits H.264.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>Valor de propiedad

Especifica el valor de **seq \_ parameter set \_ id \_ en** la unidad NAL de SPS. El **elemento de \_ sintaxis seq parameter \_ set \_ id** identifica el conjunto de parámetros de secuencia. La secuencia de bits resultante se puede concatenar con otras secuencias de bits para generar una secuencia de bits más larga que contenga varios conjuntos de parámetros de secuencia con distintos identificadores de SPS.

El intervalo válido es 0 31, como se especifica en la especificación H.264/AVC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

