---
title: faceforward
description: Voltea la superficie normal (si es necesario) para cara en una dirección opuesta a i; Devuelve el resultado en n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- HLSL de faceforward
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149365"
---
# <a name="faceforward"></a>faceforward

Voltea la superficie normal (si es necesario) para cara en una dirección opuesta a i; Devuelve el resultado en n.



| *RET* faceforward (*n*, *i*, *ng*) |
|-----------------------------------|



 

Esta función usa la siguiente fórmula:-*n*  signo (punto (*i*, *ng*)).

## <a name="parameters"></a>Parámetros



| Elemento                                                      | Descripción                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*n*<br/>    | \[en \] el vector de la superficie de punto flotante normal.<br/>                                           |
| <span id="i"></span><span id="I"></span>*Configur*<br/>    | \[en \] un vector de incidente de punto flotante que apunta de la posición de la vista a la posición del sombreado.<br/> |
| <span id="ng"></span><span id="NG"></span>*natural*<br/> | \[en \] un vector normal de superficie de punto flotante.<br/>                                                       |



 

## <a name="return-value"></a>Valor devuelto

Vector normal de superficie de punto flotante que está orientado A la dirección de la vista.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *i*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *n* |
| *natural*  | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *n*   |
| *direcc* | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *n*   |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible             |
|------------------------------------------------------------------------------------|-----------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 y PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

