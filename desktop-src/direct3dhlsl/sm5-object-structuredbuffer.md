---
title: StructuredBuffer
description: Búfer de solo lectura, que puede tomar un tipo T que es una estructura .
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- StructuredBuffer HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963531"
---
# <a name="structuredbuffer"></a>StructuredBuffer

Búfer de solo lectura, que puede tomar un tipo T que es una estructura .



| Método                                                             | Descripción                            |
|--------------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-structuredbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.          |
| [**Carga**](structuredbuffer-load.md)                              | Lee los datos del búfer.                     |
| [**Operador\[\]**](sm5-object-structuredbuffer-operatorindex.md)  | Devuelve una variable de recurso de solo lectura. |



 

El formato UAV enlazado a este recurso debe crearse con el formato DXGI \_ FORMAT \_ UNKNOWN.

Para obtener más información sobre los [búferes estructurados,](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)consulte el material de información general.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                            | Compatible |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Disponible para sombreadores de cálculo y píxeles en Direct3D 11 en algunos dispositivos Direct3D 10).<br/> | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

