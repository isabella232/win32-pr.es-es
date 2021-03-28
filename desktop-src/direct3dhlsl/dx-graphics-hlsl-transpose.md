---
title: transponer
description: Transpone la matriz de entrada especificada.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- transponer HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420824"
---
# <a name="transpose"></a>transponer

Transpone la matriz de entrada especificada.



| RET (*x*) |
|--------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                             |
|--------------------------------------------------------|-----------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] la matriz especificada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor transpuesto del parámetro *x* .

## <a name="remarks"></a>Observaciones

Si las dimensiones de la matriz de origen son *columnas* de *filas* , la matriz resultante es *filas* de *columnas* .

## <a name="type-description"></a>Descripción del tipo



| Nombre | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Tamaño                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| *x*  | [**matrices**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | cualquiera                                                                                    |
| direcc  | [**matrices**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | filas = el mismo número de columnas que la entrada *x*, columnas = el mismo número de filas que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos | sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

