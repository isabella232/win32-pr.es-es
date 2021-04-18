---
description: Dirección del espacio de objeto del rayo actual.
ms.assetid: ''
title: ObjectRayDirection
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectRayDirection
api_type:
- NA
ms.openlocfilehash: 1cc291a33f91bf7fc0565596bdd075a86e193246
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714811"
---
# <a name="objectraydirection"></a><span data-ttu-id="70d9f-103">ObjectRayDirection</span><span class="sxs-lookup"><span data-stu-id="70d9f-103">ObjectRayDirection</span></span>

<span data-ttu-id="70d9f-104">Dirección del espacio de objeto del rayo actual.</span><span class="sxs-lookup"><span data-stu-id="70d9f-104">The object-space direction for the current ray.</span></span> <span data-ttu-id="70d9f-105">El espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.</span><span class="sxs-lookup"><span data-stu-id="70d9f-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d9f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70d9f-106">Syntax</span></span>

```
float3 ObjectRayDirection();

```



## <a name="remarks"></a><span data-ttu-id="70d9f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70d9f-107">Remarks</span></span>

<span data-ttu-id="70d9f-108">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="70d9f-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="70d9f-109">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="70d9f-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="70d9f-110">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="70d9f-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="70d9f-111">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="70d9f-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="70d9f-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="70d9f-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d9f-113">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="70d9f-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




