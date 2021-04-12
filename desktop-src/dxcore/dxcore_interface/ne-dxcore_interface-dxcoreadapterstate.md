---
title: DXCoreAdapterState
description: Define constantes que especifican los tipos de Estados del adaptador de DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359115"
---
# <a name="dxcoreadapterstate-enum"></a><span data-ttu-id="fea38-103">Enumeración DXCoreAdapterState</span><span class="sxs-lookup"><span data-stu-id="fea38-103">DXCoreAdapterState enum</span></span>

<span data-ttu-id="fea38-104">Define constantes que especifican los tipos de Estados del adaptador de DXCore.</span><span class="sxs-lookup"><span data-stu-id="fea38-104">Defines constants that specify kinds of DXCore adapter states.</span></span> <span data-ttu-id="fea38-105">Pase una de estas constantes al método [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) para recuperar el elemento de estado del adaptador para un tipo de estado; Pase una constante al método [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) para establecer la información de un adaptador para un elemento de estado.</span><span class="sxs-lookup"><span data-stu-id="fea38-105">Pass one of these constants to the [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) method to set an adapter's info for a state item.</span></span>

## <a name="syntax"></a><span data-ttu-id="fea38-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fea38-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a><span data-ttu-id="fea38-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="fea38-107">Constants</span></span>

### <a name="isdriverupdateinprogress"></a><span data-ttu-id="fea38-108">IsDriverUpdateInProgress</span><span class="sxs-lookup"><span data-stu-id="fea38-108">IsDriverUpdateInProgress</span></span>

<span data-ttu-id="fea38-109">Especifica el estado del adaptador de <em>IsDriverUpdateInProgress</em> , que `true` indica que se ha iniciado una actualización del controlador en el adaptador, pero que aún no se ha completado.</span><span class="sxs-lookup"><span data-stu-id="fea38-109">Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed.</span></span> <span data-ttu-id="fea38-110">Si ya se ha completado la actualización del controlador, se habrá invalidado el adaptador y la llamada a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) devolverá un <b>valor HRESULT</b> de <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span><span class="sxs-lookup"><span data-stu-id="fea38-110">If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span></span>

<span data-ttu-id="fea38-111">Al llamar a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el elemento de estado <em>IsDriverUpdateInProgress</em> tiene el tipo <b>uint8_t</b>, que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="fea38-111">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.</span></span>

<span data-ttu-id="fea38-112"><b>Importante</b>.</span><span class="sxs-lookup"><span data-stu-id="fea38-112"><b>Important</b>.</span></span> <span data-ttu-id="fea38-113">Este elemento de estado no es compatible con [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span><span class="sxs-lookup"><span data-stu-id="fea38-113">This state item is not supported for [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span></span>

### <a name="adaptermemorybudget"></a><span data-ttu-id="fea38-114">AdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="fea38-114">AdapterMemoryBudget</span></span>

<span data-ttu-id="fea38-115">Especifica el estado del adaptador de <em>AdapterMemoryBudget</em> , que recupera o solicita el presupuesto de memoria del adaptador en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="fea38-115">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span>

<span data-ttu-id="fea38-116">Al llamar a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el estado del adaptador de <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> para *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="fea38-116">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.</span></span>

## <a name="see-also"></a><span data-ttu-id="fea38-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="fea38-117">See also</span></span>

<span data-ttu-id="fea38-118">[IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="fea38-118">[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>