---
title: smoothstep (
description: Devuelve una interpolación Smooth Hermite entre 0 y 1, si x está en el intervalo \ min, Max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- HLSL de smoothstep (
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983995"
---
# <a name="smoothstep"></a>smoothstep (

Devuelve una interpolación Smooth Hermite entre 0 y 1, si *x* está en el intervalo \[ *min*, *Max* \] .



| *RET* smoothstep ((*min*, *Max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*minuto*<br/> | \[en \] el intervalo mínimo del parámetro *x* .<br/> |
| <span id="max"></span><span id="MAX"></span>*máx.*<br/> | \[en \] el intervalo máximo del parámetro *x* .<br/> |
| <span id="x"></span><span id="X"></span>*x1*<br/>       | \[en \] el valor especificado que se va a interpolar.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si *x* es menor que *min*; 1 si *x* es mayor que el *máximo*; de lo contrario, un valor comprendido entre 0 y 1 si *x* está en el intervalo \[ *min*, *Max* \] .

## <a name="remarks"></a>Observaciones

Use la función intrínseca **smoothstep (** HLSL para crear una transición fluida entre dos valores. Por ejemplo, puede usar esta función para mezclar dos colores sin problemas.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *min* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *max* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
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

 

