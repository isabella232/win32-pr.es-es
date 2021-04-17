---
description: Invoca otro sombreador desde dentro de un sombreador.
ms.assetid: ''
title: Función CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714812"
---
# <a name="callshader-function"></a><span data-ttu-id="64752-103">Función CallShader</span><span class="sxs-lookup"><span data-stu-id="64752-103">CallShader function</span></span>

<span data-ttu-id="64752-104">Invoca otro sombreador desde dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="64752-104">Invokes another shader from within a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="64752-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64752-105">Syntax</span></span>
<span data-ttu-id="64752-106">Esta definición de función intrínseca es equivalente a la siguiente plantilla de función:</span><span class="sxs-lookup"><span data-stu-id="64752-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a><span data-ttu-id="64752-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64752-107">Parameters</span></span>

`ShaderIndex`

<span data-ttu-id="64752-108">Entero sin signo que representa el índice en la tabla de [sombreador](callable-shader.md) al que se puede llamar especificada en la llamada a [**DispatchRays**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.</span><span class="sxs-lookup"><span data-stu-id="64752-108">An unsigned integer representing the index into the [callable shader](callable-shader.md) table specified in the call to [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.</span></span>

`Parameter`

<span data-ttu-id="64752-109">Parámetros definidos por el usuario que se van a pasar al sombreador al que se puede llamar.</span><span class="sxs-lookup"><span data-stu-id="64752-109">The user-defined parameters to pass to the callable shader.</span></span>  <span data-ttu-id="64752-110">Esta estructura de parámetro debe coincidir con la estructura de parámetros utilizada en el sombreador al que se llama en la tabla de sombreador.</span><span class="sxs-lookup"><span data-stu-id="64752-110">This parameter structure must match the parameter structure used in the callable shader pointed to in the shader table.</span></span>


## <a name="return-value"></a><span data-ttu-id="64752-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64752-111">Return Value</span></span>

<span data-ttu-id="64752-112">**void**</span><span class="sxs-lookup"><span data-stu-id="64752-112">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="64752-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64752-113">Remarks</span></span>

<span data-ttu-id="64752-114">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="64752-114">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="64752-115">**Sombreador al que se puede llamar**</span><span class="sxs-lookup"><span data-stu-id="64752-115">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="64752-116">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="64752-116">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="64752-117">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="64752-117">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="64752-118">**Sombreador de generación de rayos**</span><span class="sxs-lookup"><span data-stu-id="64752-118">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="64752-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="64752-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64752-120">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="64752-120">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




