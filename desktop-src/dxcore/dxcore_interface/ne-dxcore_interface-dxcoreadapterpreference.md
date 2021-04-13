---
title: DXCoreAdapterPreference
description: Define constantes que especifican las preferencias del adaptador de DXCore que se van a usar como criterios de ordenación de lista.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421142"
---
# <a name="dxcoreadapterpreference-enum"></a><span data-ttu-id="e2821-103">Enumeración DXCoreAdapterPreference</span><span class="sxs-lookup"><span data-stu-id="e2821-103">DXCoreAdapterPreference enum</span></span>

## <a name="description"></a><span data-ttu-id="e2821-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2821-104">Description</span></span>

<span data-ttu-id="e2821-105">Define constantes que especifican las preferencias del adaptador de DXCore que se van a usar como criterios de ordenación de lista.</span><span class="sxs-lookup"><span data-stu-id="e2821-105">Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.</span></span> <span data-ttu-id="e2821-106">Puede ordenar una lista de adaptadores de DXCore pasando una matriz de **DXCoreAdapterPreference** a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="e2821-106">You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2821-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2821-107">Syntax</span></span>

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a><span data-ttu-id="e2821-108">Campos de enumeración</span><span class="sxs-lookup"><span data-stu-id="e2821-108">Enum fields</span></span>

### <a name="hardware"></a><span data-ttu-id="e2821-109">Hardware</span><span class="sxs-lookup"><span data-stu-id="e2821-109">Hardware</span></span>

<span data-ttu-id="e2821-110">Especifica una preferencia para los adaptadores de hardware (en contraposición a los adaptadores de software).</span><span class="sxs-lookup"><span data-stu-id="e2821-110">Specifies a preference for hardware adapters (as opposed to software adapters).</span></span>

### <a name="minimumpower"></a><span data-ttu-id="e2821-111">MinimumPower</span><span class="sxs-lookup"><span data-stu-id="e2821-111">MinimumPower</span></span>

<span data-ttu-id="e2821-112">Especifica una preferencia para la GPU con alimentación mínima (como un procesador de gráficos integrado o iGPU).</span><span class="sxs-lookup"><span data-stu-id="e2821-112">Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).</span></span>

### <a name="highperformance"></a><span data-ttu-id="e2821-113">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="e2821-113">HighPerformance</span></span>

<span data-ttu-id="e2821-114">Especifica una preferencia para la GPU de mayor rendimiento, como un procesador de gráficos externo (xGPU), si está disponible, o el procesador de gráficos discretos (dGPU) si está disponible.</span><span class="sxs-lookup"><span data-stu-id="e2821-114">Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2821-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2821-115">See also</span></span>

<span data-ttu-id="e2821-116">[IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e2821-116">[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>