---
title: faceforward
description: Invierte la superficie normal (si es necesario) a la cara en una dirección opuesta a i; devuelve el resultado en n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- FACEFORWARD HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964655"
---
# <a name="faceforward"></a>faceforward

Invierte la superficie normal (si es necesario) a la cara en una dirección opuesta a i; devuelve el resultado en n.



| *ret* faceforward(*n*, *i*, *ng*) |
|-----------------------------------|



 

Esta función usa la fórmula siguiente: -*n*  sign(dot(*i*, *ng*)).

## <a name="parameters"></a>Parámetros



| Elemento                                                      | Descripción                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*N*<br/>    | \[en \] Vector normal de superficie de punto flotante resultante.<br/>                                           |
| <span id="i"></span><span id="I"></span>*i*<br/>    | \[en Un vector de incidente de punto flotante que apunta desde la posición de vista a la posición \] de sombreado.<br/> |
| <span id="ng"></span><span id="NG"></span>*Ng*<br/> | \[en \] Un vector normal de superficie de punto flotante.<br/>                                                       |



 

## <a name="return-value"></a>Valor devuelto

Vector normal de superficie de punto flotante orientado a la dirección de la vista.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *i*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *n* |
| *Ng*  | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *n*   |
| *Ret* | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *n*   |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible             |
|------------------------------------------------------------------------------------|-----------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 y ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

