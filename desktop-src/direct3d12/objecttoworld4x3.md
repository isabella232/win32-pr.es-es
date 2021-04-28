---
description: 'ObjectToWorld4x3: matriz para transformar del espacio de objetos al espacio del mundo.'
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
ms.openlocfilehash: bc91c6e98aceb13af3f589f873a4b96c2b1843c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098303"
---
# <a name="objecttoworld4x3"></a><span data-ttu-id="2743e-103">ObjectToWorld4x3</span><span class="sxs-lookup"><span data-stu-id="2743e-103">ObjectToWorld4x3</span></span>

<span data-ttu-id="2743e-104">Matriz para transformar del espacio del objeto al espacio del mundo.</span><span class="sxs-lookup"><span data-stu-id="2743e-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="2743e-105">Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.</span><span class="sxs-lookup"><span data-stu-id="2743e-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2743e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2743e-106">Syntax</span></span>

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a><span data-ttu-id="2743e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2743e-107">Remarks</span></span>

<span data-ttu-id="2743e-108">La matriz es una transformación de **la matriz ObjectToWorld3x4.**</span><span class="sxs-lookup"><span data-stu-id="2743e-108">The matrix is a transposition of **ObjectToWorld3x4** matrix.</span></span>

<span data-ttu-id="2743e-109">Se puede llamar a esta función desde los siguientes tipos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2743e-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="2743e-110">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="2743e-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="2743e-111">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="2743e-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="2743e-112">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="2743e-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="2743e-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2743e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2743e-114">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="2743e-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




