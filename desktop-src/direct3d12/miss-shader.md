---
description: Sombreador que se invoca cuando no se encuentran ni se aceptan intersecciones de rayo.
ms.assetid: ''
title: Sombreador de errores
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696130"
---
# <a name="miss-shader"></a>Sombreador de errores

Sombreador que se invoca cuando no se encuentran ni se aceptan intersecciones de rayo. Esto es útil para el sombreado de fondo o cielo.  El sombreador de errores puede usar [**CallShader**](callshader-function.md) y **TraceRay** para programar más trabajo.

El sombreador de errores debe incluir un parámetro de carga con tipo definido por el usuario que coincida con el proporcionado a [**TraceRay**](traceray-function.md).


## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("miss")]
```



## <a name="example"></a>Ejemplo

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




