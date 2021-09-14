---
title: ddy
description: Devuelve el derivado parcial del valor especificado con respecto a la coordenada Y del espacio de pantalla.
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- ddy HLSL
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888305"
---
# <a name="ddy"></a>ddy

Devuelve el derivado parcial del valor especificado con respecto a la coordenada Y del espacio de pantalla.



| *ret* ddy(*x*) |
|----------------|



 

Esta función calcula el derivado parcial con respecto a la coordenada Y del espacio de pantalla. Para calcular el derivado parcial con respecto a la coordenada X del espacio en pantalla, use la [**función ddx.**](dx-graphics-hlsl-ddx.md)

Esta función solo se admite en sombreadores de píxeles.

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Derivado parcial del *parámetro x.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí                                       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                                  | sí                                       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)                   | sí                                       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                   | sí en ps \_ 2 \_ x; no se admite en ps \_ 2 \_ 0. |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                   | no                                        |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

