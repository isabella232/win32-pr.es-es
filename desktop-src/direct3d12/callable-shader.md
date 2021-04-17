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
# <a name="callable-shader"></a><span data-ttu-id="451cf-103">Sombreador al que se puede llamar</span><span class="sxs-lookup"><span data-stu-id="451cf-103">Callable Shader</span></span>

<span data-ttu-id="451cf-104">Sombreador que se invoca desde otro sombreador con la función intrínseca [**CallShader**](callshader-function.md) .</span><span class="sxs-lookup"><span data-stu-id="451cf-104">A shader that is invoked from another shader with the [**CallShader**](callshader-function.md) intrinsic.</span></span>

<span data-ttu-id="451cf-105">Hay una estructura de parámetros proporcionada en el sitio de llamada **CallShader** que debe coincidir con la estructura de parámetros utilizada en el sombreador al que apunta el índice solicitado en la tabla del sombreador al que se puede llamar a través del método [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .</span><span class="sxs-lookup"><span data-stu-id="451cf-105">There is a parameter structure supplied at the **CallShader** call site that must match the parameter structure used in the callable shader pointed to by the requested index into the callable shader table supplied through the [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) method.</span></span>  <span data-ttu-id="451cf-106">El sombreador al que se puede llamar debe declarar este parámetro como *INOUT*.</span><span class="sxs-lookup"><span data-stu-id="451cf-106">The callable shader must declare this parameter as *inout*.</span></span>  <span data-ttu-id="451cf-107">Además, el sombreador invocable puede leer índices de inicio y entradas de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="451cf-107">Additionally, the callable shader may read launch index and dimension inputs.</span></span> <span data-ttu-id="451cf-108">Para obtener más información, vea [**intrínsecos de valor del sistema**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span><span class="sxs-lookup"><span data-stu-id="451cf-108">For more information, see [**System Value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span></span> 


## <a name="shader-type-attribute"></a><span data-ttu-id="451cf-109">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="451cf-109">Shader Type attribute</span></span>


```
[shader("callable")]
```



## <a name="example"></a><span data-ttu-id="451cf-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="451cf-110">Example</span></span>

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




