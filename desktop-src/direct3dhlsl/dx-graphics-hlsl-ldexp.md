---
title: ldexp (Corecrt \_ math.h)
description: Devuelve el resultado de multiplicar el valor especificado por dos, elevado a la potencia del exponente especificado.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- ldexp HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888236"
---
# <a name="ldexp"></a>ldexp

Devuelve el resultado de multiplicar el valor especificado por dos, elevado a la potencia del exponente especificado.



| *ret* ldexp(*x*, *exp*) |
|-------------------------|



 

Esta función usa la siguiente fórmula: *x* \* 2 <sup>exp</sup>

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[en \] El valor especificado.<br/>    |
| <span id="exp"></span><span id="EXP"></span>*Exp*<br/> | \[en \] El exponente especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Resultado de multiplicar el parámetro *x* por dos, elevado a la potencia del *parámetro exp.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *exp* | igual que la entrada *x*                                                                                              | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *Ret* | igual que la entrada *x*                                                                                              | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo \_ frente a \_ 1 1) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

