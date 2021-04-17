---
description: Sombreador que se invoca desde otro sombreador con la función intrínseca CallShader.
ms.assetid: ''
title: Sombreador al que se puede llamar
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714789"
---
# <a name="callable-shader"></a>Sombreador al que se puede llamar

Sombreador que se invoca desde otro sombreador con la función intrínseca [**CallShader**](callshader-function.md) .

Hay una estructura de parámetros proporcionada en el sitio de llamada **CallShader** que debe coincidir con la estructura de parámetros utilizada en el sombreador al que apunta el índice solicitado en la tabla del sombreador al que se puede llamar a través del método [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .  El sombreador al que se puede llamar debe declarar este parámetro como *INOUT*.  Además, el sombreador invocable puede leer índices de inicio y entradas de dimensiones. Para obtener más información, vea [**intrínsecos de valor del sistema**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md). 


## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("callable")]
```



## <a name="example"></a>Ejemplo

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




