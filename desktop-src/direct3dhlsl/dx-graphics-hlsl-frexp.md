---
title: frexp (Corecrt \_ math.h)
description: Devuelve la mantisa y el exponente del valor de punto flotante especificado.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
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
ms.openlocfilehash: 0f77ab30f525c37fcb2243bb6f634722420836f3893a4550edbb6604c8769773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276625"
---
# <a name="frexp"></a>frexp

Devuelve la mantisa y el exponente del valor de punto flotante especificado.



| *ret* frexp(*x*, *exp*) |
|-------------------------|



 

El valor devuelto es la mantisa y el valor devuelto por *el parámetro exp* es el exponente.

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[en \] El valor de punto flotante especificado. Si el *parámetro x* es 0, esta función devuelve 0 para la mantisa y el exponente.<br/> |
| <span id="exp"></span><span id="EXP"></span>*Exp*<br/> | \[out \] El exponente devuelto del *parámetro x.*<br/>                                                                                   |



 

## <a name="return-value"></a>Valor devuelto

Mantisa del *parámetro x.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *exp* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *Ret* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador superiores | sí                 |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | sí (solo ps \_ 2 \_ x) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | no                  |



 

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

