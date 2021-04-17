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
# <a name="miss-shader"></a><span data-ttu-id="3a103-103">Sombreador de errores</span><span class="sxs-lookup"><span data-stu-id="3a103-103">Miss Shader</span></span>

<span data-ttu-id="3a103-104">Sombreador que se invoca cuando no se encuentran ni se aceptan intersecciones de rayo.</span><span class="sxs-lookup"><span data-stu-id="3a103-104">A shader that is invoked when no ray intersections are found or accepted.</span></span> <span data-ttu-id="3a103-105">Esto es útil para el sombreado de fondo o cielo.</span><span class="sxs-lookup"><span data-stu-id="3a103-105">This is useful for background or sky shading.</span></span>  <span data-ttu-id="3a103-106">El sombreador de errores puede usar [**CallShader**](callshader-function.md) y **TraceRay** para programar más trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a103-106">The miss shader may use [**CallShader**](callshader-function.md) and **TraceRay** to schedule more work.</span></span>

<span data-ttu-id="3a103-107">El sombreador de errores debe incluir un parámetro de carga con tipo definido por el usuario que coincida con el proporcionado a [**TraceRay**](traceray-function.md).</span><span class="sxs-lookup"><span data-stu-id="3a103-107">The miss shader must include a user-defined structure typed payload parameter matching the one supplied to [**TraceRay**](traceray-function.md).</span></span>


## <a name="shader-type-attribute"></a><span data-ttu-id="3a103-108">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3a103-108">Shader Type attribute</span></span>


```
[shader("miss")]
```



## <a name="example"></a><span data-ttu-id="3a103-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a103-109">Example</span></span>

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

 

 




