---
description: 'ObjectToWorld3x4: matriz para la transformación del espacio de objetos al espacio del mundo.'
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107743"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="7cae0-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="7cae0-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="7cae0-104">Matriz para transformar del espacio de objetos al espacio del mundo.</span><span class="sxs-lookup"><span data-stu-id="7cae0-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="7cae0-105">Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.</span><span class="sxs-lookup"><span data-stu-id="7cae0-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cae0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cae0-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="7cae0-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cae0-107">Remarks</span></span>

<span data-ttu-id="7cae0-108">La matriz es una retorsión de **la matriz ObjectToWorld4x3.**</span><span class="sxs-lookup"><span data-stu-id="7cae0-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="7cae0-109">Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:</span><span class="sxs-lookup"><span data-stu-id="7cae0-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="7cae0-110">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="7cae0-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="7cae0-111">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="7cae0-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="7cae0-112">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="7cae0-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="7cae0-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7cae0-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cae0-114">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="7cae0-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




