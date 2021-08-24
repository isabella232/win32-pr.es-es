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
ms.openlocfilehash: 2932f82cf6d9e8b2071446b63f84e60727aff2da2213461d3c1194b2811fe1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854975"
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

## <a name="remarks"></a>Comentarios

Los signos de los *parámetros x* e *y* se usan para determinar el cuadrante de los valores devueltos dentro del intervalo de -π para π. La función intrínseca HLSL **atan2** está bien definida para cada punto distinto del origen, incluso si *y* es igual a 0 y *x* no es igual a 0.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | Sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

