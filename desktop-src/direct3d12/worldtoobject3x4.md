---
description: Matriz que se va a transformar de espacio mundial en el espacio de objeto.
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
ms.openlocfilehash: 6274b1d4d18aff0464d933c20f7b8052f3389e5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677241"
---
# <a name="worldtoobject3x4"></a><span data-ttu-id="ee20d-103">WorldToObject3x4</span><span class="sxs-lookup"><span data-stu-id="ee20d-103">WorldToObject3x4</span></span>

<span data-ttu-id="ee20d-104">Matriz que se va a transformar de espacio mundial en el espacio de objeto.</span><span class="sxs-lookup"><span data-stu-id="ee20d-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="ee20d-105">El espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.</span><span class="sxs-lookup"><span data-stu-id="ee20d-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee20d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee20d-106">Syntax</span></span>

```
void WorldToObject3x4();

```




## <a name="remarks"></a><span data-ttu-id="ee20d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee20d-107">Remarks</span></span>

<span data-ttu-id="ee20d-108">La matriz es una transposición de la matriz **WorldToObject4x3** .</span><span class="sxs-lookup"><span data-stu-id="ee20d-108">The matrix is a transposition of **WorldToObject4x3** matrix.</span></span>

<span data-ttu-id="ee20d-109">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="ee20d-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="ee20d-110">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="ee20d-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="ee20d-111">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="ee20d-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="ee20d-112">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="ee20d-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="ee20d-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee20d-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee20d-114">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="ee20d-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




