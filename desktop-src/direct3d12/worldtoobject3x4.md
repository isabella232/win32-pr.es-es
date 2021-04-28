---
description: 'WorldToObject3x4: matriz para la transformación del espacio del mundo al espacio de objetos.'
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: cc7bf7dc2f06102b9b23eafd45655f12816c8359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105252"
---
# <a name="worldtoobject3x4"></a><span data-ttu-id="6d240-103">WorldToObject3x4</span><span class="sxs-lookup"><span data-stu-id="6d240-103">WorldToObject3x4</span></span>

<span data-ttu-id="6d240-104">Matriz para la transformación del espacio del mundo al espacio de objetos.</span><span class="sxs-lookup"><span data-stu-id="6d240-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="6d240-105">Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.</span><span class="sxs-lookup"><span data-stu-id="6d240-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d240-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d240-106">Syntax</span></span>

```
void WorldToObject3x4();

```




## <a name="remarks"></a><span data-ttu-id="6d240-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d240-107">Remarks</span></span>

<span data-ttu-id="6d240-108">La matriz es una contracción **de la matriz WorldToObject4x3.**</span><span class="sxs-lookup"><span data-stu-id="6d240-108">The matrix is a transposition of **WorldToObject4x3** matrix.</span></span>

<span data-ttu-id="6d240-109">Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:</span><span class="sxs-lookup"><span data-stu-id="6d240-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="6d240-110">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="6d240-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="6d240-111">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="6d240-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="6d240-112">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="6d240-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="6d240-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6d240-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d240-114">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="6d240-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




