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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964675"
---
# <a name="cross"></a>cruzadas

Devuelve el producto cruzado de dos vectores 3D de punto flotante.



| *ret* cross(*x*, *y*) |
|-----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] el primer vector 3D de punto flotante.<br/>  |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] el segundo punto flotante, vector 3D.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Producto cruzado del parámetro *x* y *el parámetro y* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *y*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *Ret* | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | 3    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible             |
|------------------------------------------------------------------------------------|-----------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 y ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

