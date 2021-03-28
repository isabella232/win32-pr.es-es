---
title: StructuredBuffer
description: Un búfer de solo lectura, que puede tomar un tipo T que es una estructura.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- HLSL de StructuredBuffer
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997072"
---
# <a name="structuredbuffer"></a>StructuredBuffer

Un búfer de solo lectura, que puede tomar un tipo T que es una estructura.



| Método                                                             | Descripción                            |
|--------------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-structuredbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.          |
| [**Carga**](structuredbuffer-load.md)                              | Lee los datos del búfer.                     |
| [**Operador\[\]**](sm5-object-structuredbuffer-operatorindex.md)  | Devuelve una variable de recurso de solo lectura. |



 

El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.

Para obtener más información sobre los [búferes estructurados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte el material de información general.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                            | Compatible |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador de mayor nivel modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponibles para los sombreadores de cálculo y de píxeles en Direct3D 11 en algunos dispositivos de Direct3D 10).<br/> | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores.



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

