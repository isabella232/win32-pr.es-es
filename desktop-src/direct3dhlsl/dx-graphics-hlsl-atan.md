---
title: atan
description: Devuelve el arcotangente del valor especificado.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- HLSL de atan
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792051"
---
# <a name="atan"></a>atan

Devuelve el arcotangente del valor especificado.



| *RET* atan (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Arco tangente del parámetro *x* . Este valor está dentro del intervalo de-π/2 a π/2.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

