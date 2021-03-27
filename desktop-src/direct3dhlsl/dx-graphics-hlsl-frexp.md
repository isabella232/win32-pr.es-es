---
title: frexp ((Corecrt, \_ Math. h)
description: Devuelve la mantisa y el exponente del valor de punto flotante especificado.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- HLSL de frexp (
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003810"
---
# <a name="frexp"></a>frexp

Devuelve la mantisa y el exponente del valor de punto flotante especificado.



| *RET* frexp ((*x*, *exp*) |
|-------------------------|



 

El valor devuelto es la mantisa y el valor devuelto por el parámetro *exp* es el exponente.

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/>       | \[en \] el valor de punto flotante especificado. Si el parámetro *x* es 0, esta función devuelve 0 para la mantisa y el exponente.<br/> |
| <span id="exp"></span><span id="EXP"></span>*consumo*<br/> | \[\]el exponente devuelto del parámetro *x* .<br/>                                                                                   |



 

## <a name="return-value"></a>Valor devuelto

La mantisa del parámetro *x* .

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
| Modelador [modelo 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador más altos | sí                 |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | sí ( \_ solo PS 2 \_ x) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | no                  |



 

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

