---
description: Establece el identificador del conjunto de parámetros de secuencia (SPS) en la unidad de capa de abstracción de red (NAL) de SPS de la secuencia de bits H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Propiedad CODECAPI_AVEncH264SPSID (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153678"
---
# <a name="codecapi_avench264spsid-property"></a>\_Propiedad AVEncH264SPSID de CODECAPI

Establece el identificador del conjunto de parámetros de secuencia (SPS) en la unidad de capa de abstracción de red (NAL) de SPS de la secuencia de bits H. 264.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>Valor de propiedad

Especifica el valor del **\_ identificador de \_ conjunto \_ de parámetros SEQ** en la unidad nal de SPS. El elemento de sintaxis **Seq \_ Parameter \_ set \_ ID** identifica el conjunto de parámetros Sequence. El flujo de bits resultante se puede concatenar con otros flujos de bits para generar un flujo de bits más largo que contenga varios conjuntos de parámetros de secuencia con distintos identificadores de SPS.

El intervalo válido es 0 31, tal y como se especifica en la especificación H. 264/AVC.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

