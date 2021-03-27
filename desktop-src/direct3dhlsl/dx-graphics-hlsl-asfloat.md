---
title: asfloat
description: Interpreta el patrón de bits de x como un número de punto flotante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- Interfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997133"
---
# <a name="asfloat"></a>asfloat

Interpreta el patrón de bits de *x* como un número de punto flotante.



| RET asfloat (*x*) |
|------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor de entrada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

La entrada se interpreta como un número de punto flotante.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | cualquiera                            |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                                                                                | mismas dimensiones que la entrada *x* |



 

## <a name="function-overloads"></a>Sobrecargas de función

<dl> ' Float <x> asfloat ( <x> valor float); `  
` Float <x> asfloat ( <x> valor int); `  
` Float <x> asfloat ( <x> valor uint); '
</dl>

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | no        |



 

## <a name="remarks"></a>Observaciones

Los compiladores anteriores permitieron incorrectamente `asfloat(bool)` , pero tenga en cuenta que no se admiten las entradas bool.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

