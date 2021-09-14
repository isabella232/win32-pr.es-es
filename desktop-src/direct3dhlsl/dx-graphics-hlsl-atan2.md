---
title: atan2 (Corecrt \_ math.h)
description: Devuelve la arcotangente de dos valores (x,y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964703"
---
# <a name="atan2"></a>atan2

Devuelve la arcotangente de dos valores (x,y).



| *ret* atan2(*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] el valor y.<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] el valor x.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Arco tangente de (y,x).

## <a name="remarks"></a>Observaciones

Los signos de *los parámetros x* e *y* se usan para determinar el cuadrante de los valores devueltos dentro del intervalo de -π para π. La función intrínseca HLSL **atan2** está bien definida para cada punto distinto del origen, incluso si *y* es igual a 0 y *x* no es igual a 0.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | igual que la entrada *x*                                                                                              | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

