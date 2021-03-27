---
title: cruzadas
description: Devuelve el producto cruzado de dos vectores 3D de punto flotante.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- HLSL cruzado
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997157"
---
# <a name="cross"></a>cruzadas

Devuelve el producto cruzado de dos vectores 3D de punto flotante.



| *RET* cruzada (*x*, *y*) |
|-----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el primer punto flotante, Vector 3D.<br/>  |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el segundo punto flotante, Vector 3D.<br/> |



 

## <a name="return-value"></a>Valor devuelto

El producto cruzado del parámetro *x* y el parámetro *y* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *y*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *direcc* | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | 3    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible             |
|------------------------------------------------------------------------------------|-----------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 y PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

