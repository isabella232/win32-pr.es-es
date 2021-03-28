---
title: rcp
description: Calcula un recíproco rápido, aproximado y por componente.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- HLSL de RCP
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792297"
---
# <a name="rcp"></a>rcp

Calcula un recíproco rápido, aproximado y por componente.



| *RET* RCP (*x*) |
|----------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

\[en \] el valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Recíproco del parámetro *x* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                      | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types) o [ **Double**](/windows/desktop/WinProg/windows-data-types) | cualquiera                            |
| *direcc* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types) o [ **Double**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 