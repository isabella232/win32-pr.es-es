---
description: Se llama desde un sombreador de posicionamiento cualquiera para rechazar el acierto y finalizar el sombreador.
ms.assetid: ''
title: Función IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696126"
---
# <a name="ignorehit-function"></a><span data-ttu-id="1a04f-103">Función IgnoreHit</span><span class="sxs-lookup"><span data-stu-id="1a04f-103">IgnoreHit function</span></span>

<span data-ttu-id="1a04f-104">Se llama desde un [sombreador de posicionamiento cualquiera](any-hit-shader.md) para rechazar el acierto y finalizar el sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a04f-104">Called from an [any hit shader](any-hit-shader.md) to reject the hit and end the shader.</span></span> <span data-ttu-id="1a04f-105">La búsqueda de aciertos continúa sin confirmar la distancia y los atributos para el acierto actual.</span><span class="sxs-lookup"><span data-stu-id="1a04f-105">The hit search continues on without committing the distance and attributes for the current hit.</span></span>  <span data-ttu-id="1a04f-106">La llamada a [**ReportHit**](reporthit-function.md) en el [sombreador de intersección](intersection-shader.md), si hay alguna, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="1a04f-106">The [**ReportHit**](reporthit-function.md) call in the [intersection shader](intersection-shader.md), if there is one, will return false.</span></span>  <span data-ttu-id="1a04f-107">Se conservan las modificaciones realizadas en la carga de Ray hasta este punto en el sombreador de posicionamiento any.</span><span class="sxs-lookup"><span data-stu-id="1a04f-107">Any modifications made to the ray payload up to this point in the any hit shader are preserved.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a04f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a04f-108">Syntax</span></span>

```
void IgnoreHit();

```


## <a name="return-value"></a><span data-ttu-id="1a04f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a04f-109">Return Value</span></span>

<span data-ttu-id="1a04f-110">**void**</span><span class="sxs-lookup"><span data-stu-id="1a04f-110">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="1a04f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a04f-111">Remarks</span></span>

<span data-ttu-id="1a04f-112">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="1a04f-112">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="1a04f-113">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="1a04f-113">**Any Hit Shader**</span></span>](any-hit-shader.md)




## <a name="see-also"></a><span data-ttu-id="1a04f-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a04f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a04f-115">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="1a04f-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




