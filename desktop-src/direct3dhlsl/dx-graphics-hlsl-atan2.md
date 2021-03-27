---
title: ATAN2 (Corecrt \_ Math. h)
description: Devuelve el arcotangente de dos valores (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- HLSL de ATAN2
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280310"
---
# <a name="atan2"></a>atan2

Devuelve el arcotangente de dos valores (x, y).



| *RET* ATAN2 (*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el valor y.<br/> |
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor x.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Arco tangente de (y, x).

## <a name="remarks"></a>Observaciones

Los signos de los  parámetros x *e y se* usan para determinar el cuadrante de los valores devueltos en el intervalo de-π a π. La función intrínseca de HLSL **ATAN2** está bien definida para cada punto que no sea el origen, aunque *y* sea igual a 0 y *x* no sea igual a 0.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

