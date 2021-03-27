---
title: ldexp (Corecrt, \_ Math. h)
description: Devuelve el resultado de multiplicar el valor especificado por dos, elevado a la potencia del exponente especificado.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- HLSL de ldexp
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914757"
---
# <a name="ldexp"></a>ldexp

Devuelve el resultado de multiplicar el valor especificado por dos, elevado a la potencia del exponente especificado.



| *RET* ldexp (*x*, *exp*) |
|-------------------------|



 

Esta función usa la siguiente fórmula: *x* \* 2 <sup>exp</sup>

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/>       | \[en \] el valor especificado.<br/>    |
| <span id="exp"></span><span id="EXP"></span>*consumo*<br/> | \[en \] el exponente especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Resultado de multiplicar el parámetro *x* por dos, elevado a la potencia del parámetro *exp* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *exp* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí ( \_ solo vs 1 \_ 1) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

