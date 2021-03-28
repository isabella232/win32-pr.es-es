---
title: max
description: Selecciona el mayor de x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- HLSL máx.
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421153"
---
# <a name="max"></a>max

Selecciona el mayor de x e y.



| RET máx. (x, y) |
|---------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor de entrada x.<br/> |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el valor de entrada y.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Parámetro *x* o *y* , el que sea el valor más grande.


## <a name="remarks"></a>Observaciones

Las desnormalizaciones se controlan de la siguiente manera:

| src0 SRC1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| F           | src0 | src0 o SRC1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F significa número finito-real.


## <a name="type-description"></a>Descripción del tipo

| Nombre | Entrada o salida      | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Tamaño                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | cualquiera                          |
| y    | in          | igual que la entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada x |
| direcc  | Tipo de valor devuelto | igual que la entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada x |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible                   |
|------------------------------------------------------------------------------------|-----------------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (vs \_ 1 \_ 1 y PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Especificación funcional de DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
