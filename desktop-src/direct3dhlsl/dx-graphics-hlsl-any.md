---
title: cualquiera
description: Determina si alguno de los componentes del valor especificado es distinto de cero.
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- cualquier HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984083"
---
# <a name="any"></a>cualquiera

Determina si alguno de los componentes del valor especificado es distinto de cero.



| *RET* any (*x*) |
|----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

**True** si alguno de los componentes del parámetro *x* es distinto de cero; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Esta función es similar a la función intrínseca de HLSL [**All**](dx-graphics-hlsl-all.md) . La función **any** determina si alguno de los componentes del valor especificado es distinto de cero, mientras que la función **All** determina si todos los componentes del valor especificado son distintos de cero.

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

 

