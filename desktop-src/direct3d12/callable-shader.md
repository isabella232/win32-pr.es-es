---
description: Sombreador que se invoca desde otro sombreador con el intrínseco CallShader.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966875"
---
# <a name="callable-shader"></a>Sombreador al que se puede llamar

Sombreador que se invoca desde otro sombreador con [**el intrínseco CallShader.**](callshader-function.md)

Hay una estructura de parámetros proporcionada en el sitio de llamada de **CallShader** que debe coincidir con la estructura de parámetros utilizada en el sombreador al que se puede llamar al que apunta el índice solicitado en la tabla de sombreador a la que se puede llamar proporcionada a través del método [**DispatchRays.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays)  El sombreador al que se puede llamar debe declarar este parámetro *como de entrada.*  Además, el sombreador al que se puede llamar puede leer entradas de índice y dimensión de inicio. Para obtener más información, vea [**Intrínsecos de valor del sistema.**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md) 


## <a name="shader-type-attribute"></a>Atributo Tipo de sombreador


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

 

 




