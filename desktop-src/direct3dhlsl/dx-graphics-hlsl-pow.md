---
title: pow
description: Devuelve el valor especificado elevado a la potencia especificada.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- HLSL de Pow
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488210"
---
# <a name="pow"></a>pow

Devuelve el valor especificado elevado a la potencia especificada.



| *RET* Pow (*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor especificado.<br/> |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[con \] la potencia especificada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Parámetro *x* elevado a la potencia del parámetro *y* .

## <a name="remarks"></a>Observaciones

La función intrínseca de el HLSL de **Pow** calcula *x*<sup>y</sup>.



| X      | Y      | Resultado                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | cualquiera    | NAN                                                                         |
| >0 | = = 0   | 1                                                                           |
| = = 0   | >0 | 0                                                                           |
| = = 0   | < 0 | inf                                                                         |
| >0 | < 0 | 1/X<sup>-y</sup>                                                            |
| = = 0   | = = 0   | Depende del procesador de gráficos concreto<br/> 0, 1 o NAN<br/> |



 

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *y*   | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí ( \_ solo vs 1 \_ 1) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

