---
title: DXCoreSegmentGroup
description: Define constantes que especifican la agrupación de segmentos de memoria de un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720152"
---
# <a name="dxcoresegmentgroup-enum"></a><span data-ttu-id="cd7bc-103">Enumeración DXCoreSegmentGroup</span><span class="sxs-lookup"><span data-stu-id="cd7bc-103">DXCoreSegmentGroup enum</span></span>

<span data-ttu-id="cd7bc-104">Define constantes que especifican la agrupación de segmentos de memoria de un adaptador.</span><span class="sxs-lookup"><span data-stu-id="cd7bc-104">Defines constants that specify an adapter's memory segment grouping.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd7bc-105">Syntax</span></span>

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a><span data-ttu-id="cd7bc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="cd7bc-106">Constants</span></span>

### <a name="local"></a><span data-ttu-id="cd7bc-107">Local</span><span class="sxs-lookup"><span data-stu-id="cd7bc-107">Local</span></span>

<span data-ttu-id="cd7bc-108">Especifica una agrupación de segmentos que se considera que son locales para el adaptador y representa la memoria más rápida disponible para la GPU.</span><span class="sxs-lookup"><span data-stu-id="cd7bc-108">Specifies a grouping of segments that is considered local to the adapter, and represents the fastest memory available to the GPU.</span></span> <span data-ttu-id="cd7bc-109">La aplicación debe tener como destino el grupo de segmentos local como el tamaño de destino de su espacio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="cd7bc-109">Your application should target the local segment group as the target size for its working set.</span></span>

### <a name="nonlocal"></a><span data-ttu-id="cd7bc-110">No locales</span><span class="sxs-lookup"><span data-stu-id="cd7bc-110">NonLocal</span></span>

<span data-ttu-id="cd7bc-111">Especifica una agrupación de segmentos que se considera no local en el adaptador y puede tener un rendimiento más lento que el grupo de segmentos local.</span><span class="sxs-lookup"><span data-stu-id="cd7bc-111">Specifies a grouping of segments that is considered non-local to the adapter, and may have slower performance than the local segment group.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd7bc-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd7bc-112">See also</span></span>

<span data-ttu-id="cd7bc-113">[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="cd7bc-113">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>