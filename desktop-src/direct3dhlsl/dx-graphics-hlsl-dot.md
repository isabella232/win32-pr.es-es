---
title: dot
description: Devuelve el producto escalar de dos vectores.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- dot HLSL
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888260"
---
# <a name="dot"></a>dot

Devuelve el producto escalar de dos vectores.



| *ret* dot(*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] el primer vector.<br/>  |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] El segundo vector.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Producto de punto del *parámetro x* y el *parámetro y* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| *x*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | cualquiera                             |
| *y*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | las mismas dimensiones que la entrada *x* |
| *Ret* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | 1                               |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

