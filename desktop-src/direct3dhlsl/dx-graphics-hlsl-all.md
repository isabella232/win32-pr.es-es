---
title: todo
description: Determina si todos los componentes del valor especificado son distintos de cero.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- todo HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984086"
---
# <a name="all"></a>todo

Determina si todos los componentes del valor especificado son distintos de cero.



| *RET* todo (*x*) |
|----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

**True** si todos los componentes del parámetro *x* son distintos de cero; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Esta función es similar a [**cualquier**](dx-graphics-hlsl-any.md) función intrínseca de HLSL. La función **any** determina si alguno de los componentes del valor especificado es distinto de cero, mientras que la función **All** determina si todos los componentes del valor especificado son distintos de cero.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Tamaño |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | cualquiera  |
| *direcc* | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md)                            | [**bool**](/windows/desktop/WinProg/windows-data-types)                                                                                 | 1    |



 

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

 

