---
title: Mostrar
description: Devuelve un vector de reflexión mediante un rayo de incidente y una superficie normal.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- reflejar HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793594"
---
# <a name="reflect"></a>Mostrar

Devuelve un vector de reflexión mediante un rayo de incidente y una superficie normal.



| refleje *RET* (*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Configur*<br/> | \[en \] un vector de incidente de punto flotante.<br/> |
| <span id="n"></span><span id="N"></span>*n*<br/> | \[en \] un vector normal de punto flotante.<br/>   |



 

## <a name="return-value"></a>Valor devuelto

Un vector de reflexión de punto flotante.

## <a name="remarks"></a>Observaciones

Esta función calcula el vector de reflexión mediante la siguiente fórmula: v = i-2 \* n \* punto (i n).

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *n*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *i* |
| *direcc* | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *i* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos | sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

