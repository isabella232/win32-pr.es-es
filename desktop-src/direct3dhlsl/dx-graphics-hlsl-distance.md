---
title: distancia
description: Devuelve una distancia escalar entre dos vectores.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- distance HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888281"
---
# <a name="distance"></a>distancia

Devuelve una distancia escalar entre dos vectores.



| *ret* distance(*x*, *y*) |
|--------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El primer vector de punto flotante que se comparará.<br/>  |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] El segundo vector de punto flotante que se comparará.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor escalar de punto flotante que representa la distancia entre el parámetro *x* y *el parámetro y.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *y*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *Ret* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

