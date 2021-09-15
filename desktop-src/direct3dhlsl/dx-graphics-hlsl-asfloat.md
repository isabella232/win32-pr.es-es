---
title: asfloat
description: Interpreta el patrón de bits de x como un número de punto flotante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 901b64099547060305bab6db43cbe75b3fdb8d9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568364"
---
# <a name="asfloat"></a>asfloat

Interpreta el patrón de bits *de x* como un número de punto flotante.



| ret asfloat(*x*) |
|------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor de entrada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Entrada interpretada como un número de punto flotante.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                                                                                | las mismas dimensiones que la entrada *x* |



 

## <a name="function-overloads"></a>Sobrecargas de función

<dl> `float&lt;x&gt; asfloat(float&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(int&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(uint&lt;x&gt; value);`  
</dl>

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | no        |



 

## <a name="remarks"></a>Observaciones

Los compiladores anteriores permitían incorrectamente , pero tenga en cuenta que no se admiten entradas `asfloat(bool)` bool.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

