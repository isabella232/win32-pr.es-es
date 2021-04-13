---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Describe un grupo de segmentos de memoria para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420857"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a><span data-ttu-id="ec2b5-103">Estructura DXCoreAdapterMemoryBudgetNodeSegmentGroup</span><span class="sxs-lookup"><span data-stu-id="ec2b5-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup structure</span></span>

<span data-ttu-id="ec2b5-104">Describe un grupo de segmentos de memoria para un adaptador.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-104">Describes a memory segment group for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec2b5-105">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a><span data-ttu-id="ec2b5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec2b5-106">Members</span></span>

### <a name="nodeindex"></a><span data-ttu-id="ec2b5-107">nodeIndex</span><span class="sxs-lookup"><span data-stu-id="ec2b5-107">nodeIndex</span></span>

<span data-ttu-id="ec2b5-108">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="ec2b5-108">Type: **uint32_t**</span></span>

<span data-ttu-id="ec2b5-109">Especifica el adaptador físico del dispositivo para el que se consulta la información de memoria del adaptador.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-109">Specifies the device's physical adapter for which the adapter memory information is queried.</span></span> <span data-ttu-id="ec2b5-110">En el caso de una operación de un solo adaptador, establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-110">For single-adapter operation, set this to zero.</span></span> <span data-ttu-id="ec2b5-111">Si hay varios nodos de adaptador, establézcalo en el índice del nodo (el adaptador físico del dispositivo) para el que desea consultar la información de memoria del adaptador (consulte sistemas de [varios adaptadores](../../direct3d12/multi-engine.md)).</span><span class="sxs-lookup"><span data-stu-id="ec2b5-111">If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter systems](../../direct3d12/multi-engine.md)).</span></span>

### <a name="segmentgroup"></a><span data-ttu-id="ec2b5-112">segmentGroup</span><span class="sxs-lookup"><span data-stu-id="ec2b5-112">segmentGroup</span></span>

<span data-ttu-id="ec2b5-113">Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span><span class="sxs-lookup"><span data-stu-id="ec2b5-113">Type: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span></span>

<span data-ttu-id="ec2b5-114">Especifica la agrupación de segmentos de memoria del adaptador que desea consultar.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-114">Specifies the adapter memory segment grouping that you want to query about.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec2b5-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec2b5-115">See also</span></span>

[<span data-ttu-id="ec2b5-116">Referencia de DXCore</span><span class="sxs-lookup"><span data-stu-id="ec2b5-116">DXCore Reference</span></span>](../dxcore-reference.md)

[<span data-ttu-id="ec2b5-117">Uso de DXCore para enumerar adaptadores</span><span class="sxs-lookup"><span data-stu-id="ec2b5-117">Using DXCore to enumerate adapters</span></span>](../dxcore-enum-adapters.md)

[<span data-ttu-id="ec2b5-118">Sistemas de varios adaptadores</span><span class="sxs-lookup"><span data-stu-id="ec2b5-118">Multi-adapter systems</span></span>](../../direct3d12/multi-engine.md)