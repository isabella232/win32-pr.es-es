---
title: faceforward
description: Voltea la superficie normal (si es necesario) a la cara en una dirección opuesta a i; devuelve el resultado en n.
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
ms.openlocfilehash: 253d581ef5ea2eddac55c63245039f1ccda6c0e73032468d1598fb919e850a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950385"
---
# <a name="faceforward"></a>faceforward

Voltea la superficie normal (si es necesario) a la cara en una dirección opuesta a i; devuelve el resultado en n.



| *ret* faceforward(*n*, *i*, *ng*) |
|-----------------------------------|



 

Esta función usa la siguiente fórmula: -*n*  sign(dot(*i*, *ng*)).

## <a name="parameters"></a>Parámetros



| Elemento                                                      | Descripción                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*N*<br/>    | \[en \] El vector normal de superficie de punto flotante resultante.<br/>                                           |
| <span id="i"></span><span id="I"></span>*i*<br/>    | \[en \] Un vector de incidente de punto flotante que apunta desde la posición de vista a la posición de sombreado.<br/> |
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
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | Sí                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 y ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

