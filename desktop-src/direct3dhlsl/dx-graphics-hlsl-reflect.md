---
title: Reflejar
description: Devuelve un vector de reflexión mediante un rayo de incidente y una superficie normal.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- reflect HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2abc7100eae846fc3d2f21b013676aa3dbc64574a7e8cdb8a14dc492ceb33f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725949"
---
# <a name="reflect"></a>Reflejar

Devuelve un vector de reflexión mediante un rayo de incidente y una superficie normal.



| *ret* reflect(*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*i*<br/> | \[en \] Un punto flotante, vector de incidente.<br/> |
| <span id="n"></span><span id="N"></span>*N*<br/> | \[en \] Un vector normal de punto flotante.<br/>   |



 

## <a name="return-value"></a>Valor devuelto

Vector de reflexión de punto flotante.

## <a name="remarks"></a>Comentarios

Esta función calcula el vector de reflexión mediante la fórmula siguiente: v = i - 2 \* n \* dot(i n) .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *n*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *i* |
| *Ret* | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *i* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador superiores | Sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

