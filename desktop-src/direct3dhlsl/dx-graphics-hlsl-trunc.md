---
title: trunc (Corecrt \_ Math. h)
description: Trunca un valor de punto flotante al componente entero.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- truncar HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998460"
---
# <a name="trunc"></a>trunc

Trunca un valor de punto flotante al componente entero.



| RET trunc (*x*) |
|----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] la entrada especificada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

El valor de entrada se trunca a un componente entero.

## <a name="remarks"></a>Observaciones

Esta función trunca un valor de punto flotante al componente entero. Dado un valor de punto flotante de 1,6, la función trunc devolvería 1,0, donde la función [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) devolvería 2,0.

## <a name="type-description"></a>Descripción del tipo



| Nombre | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                          |
| direcc  | El mismo tipo que la entrada x                                                                                           | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | Mismas dimensiones que la entrada x |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos | sí       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

