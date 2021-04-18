---
description: Matriz que se va a transformar del espacio de objeto a espacio universal.
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 613b4c403f235819845114e7019e07051a25ec80
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714809"
---
# <a name="objecttoworld4x3"></a><span data-ttu-id="20c61-103">ObjectToWorld4x3</span><span class="sxs-lookup"><span data-stu-id="20c61-103">ObjectToWorld4x3</span></span>

<span data-ttu-id="20c61-104">Matriz que se va a transformar del espacio de objeto a espacio universal.</span><span class="sxs-lookup"><span data-stu-id="20c61-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="20c61-105">El espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.</span><span class="sxs-lookup"><span data-stu-id="20c61-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c61-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20c61-106">Syntax</span></span>

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a><span data-ttu-id="20c61-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20c61-107">Remarks</span></span>

<span data-ttu-id="20c61-108">La matriz es una transposición de la matriz **ObjectToWorld3x4** .</span><span class="sxs-lookup"><span data-stu-id="20c61-108">The matrix is a transposition of **ObjectToWorld3x4** matrix.</span></span>

<span data-ttu-id="20c61-109">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="20c61-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="20c61-110">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="20c61-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="20c61-111">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="20c61-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="20c61-112">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="20c61-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="20c61-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="20c61-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c61-114">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="20c61-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




