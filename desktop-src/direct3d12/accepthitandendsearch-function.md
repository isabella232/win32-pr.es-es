---
description: Se usa en cualquier sombreador de posicionamiento para confirmar el acierto actual y, a continuación, detener la búsqueda de más visitas para el rayo.
ms.assetid: ''
title: Función AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648165"
---
# <a name="accepthitandendsearch-function"></a><span data-ttu-id="adbb8-103">Función AcceptHitAndEndSearch</span><span class="sxs-lookup"><span data-stu-id="adbb8-103">AcceptHitAndEndSearch function</span></span>

<span data-ttu-id="adbb8-104">Se usa en [cualquier sombreador de posicionamiento](any-hit-shader.md) para confirmar el acierto actual y, a continuación, detener la búsqueda de más visitas para el rayo.</span><span class="sxs-lookup"><span data-stu-id="adbb8-104">Used in an [any hit shader](any-hit-shader.md) to commit the current hit and then stop searching for more hits for the ray.</span></span> <span data-ttu-id="adbb8-105">Si hay un sombreador de intersección en ejecución, se detiene la ejecución.</span><span class="sxs-lookup"><span data-stu-id="adbb8-105">If there is an intersection shader running, it's execution stops.</span></span>  <span data-ttu-id="adbb8-106">La ejecución pasa al [sombreador de posicionamiento más cercano](closest-hit-shader.md), si está habilitado, con el golpe más cercano registrado hasta el momento.</span><span class="sxs-lookup"><span data-stu-id="adbb8-106">Execution passes to the [closest hit shader](closest-hit-shader.md), if enabled, with the closest hit recorded so far.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbb8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="adbb8-107">Syntax</span></span>

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a><span data-ttu-id="adbb8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="adbb8-108">Return Value</span></span>

<span data-ttu-id="adbb8-109">**void**</span><span class="sxs-lookup"><span data-stu-id="adbb8-109">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="adbb8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="adbb8-110">Remarks</span></span>

<span data-ttu-id="adbb8-111">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="adbb8-111">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="adbb8-112">**Sombreador al que se puede llamar**</span><span class="sxs-lookup"><span data-stu-id="adbb8-112">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="adbb8-113">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="adbb8-113">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="adbb8-114">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="adbb8-114">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="adbb8-115">**Sombreador de generación de rayos**</span><span class="sxs-lookup"><span data-stu-id="adbb8-115">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="adbb8-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="adbb8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adbb8-117">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="adbb8-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




