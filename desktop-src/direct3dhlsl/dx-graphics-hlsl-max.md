---
title: max
description: Selecciona el mayor de x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- max HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360520"
---
# <a name="max"></a>max

Selecciona el mayor de x e y.



| ret max(x, y) |
|---------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor de entrada x.<br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] El valor de entrada y.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Parámetro *x* o *y,* lo que sea el valor más grande.


## <a name="remarks"></a>Observaciones

Los desnormales se controlan de la siguiente manera:

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| F           | src0 | src0 o src1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F significa número finito-real.


## <a name="type-description"></a>Descripción del tipo

| Nombre | Entrada o salida      | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | cualquiera                          |
| y    | in          | igual que la entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | las mismas dimensiones que la entrada x |
| Ret  | Tipo de valor devuelto | igual que la entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | las mismas dimensiones que la entrada x |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (frente \_ a \_ 1 1 y ps \_ 1 \_ 4) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Especificación funcional de DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
