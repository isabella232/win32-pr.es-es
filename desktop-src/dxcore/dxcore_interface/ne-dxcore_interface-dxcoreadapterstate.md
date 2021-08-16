---
title: DXCoreAdapterState
description: Define constantes que especifican tipos de estados de adaptador dxcore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6878aaccb61fd164fcf834561fcf70f13d2609de595687b6ef6301778c87f81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367085"
---
# <a name="dxcoreadapterstate-enum"></a>Enumeración DXCoreAdapterState

Define constantes que especifican tipos de estados de adaptador dxcore. Pase una de estas constantes al método [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) para recuperar el elemento de estado del adaptador para un tipo de estado; pase una constante al [método IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) para establecer la información de un adaptador para un elemento de estado.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Constantes

### <a name="isdriverupdateinprogress"></a>IsDriverUpdateInProgress

Especifica el estado del adaptador <em>IsDriverUpdateInProgress,</em> que cuando indica que se ha iniciado una actualización del controlador en el adaptador, pero aún no `true` se ha completado. Si la actualización del controlador ya se ha completado, el adaptador se habrá invalidado y la llamada a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) devolverá <b>un HRESULT</b> de <b>DXGI_ERROR_DEVICE_REMOVED</b>.

Al llamar [a QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el elemento de estado <em>IsDriverUpdateInProgress</em> tiene el tipo <b>uint8_t</b>, que representa un valor booleano.

<b>Importante</b>. Este elemento de estado no es compatible con [SetState.](./nf-dxcore_interface-idxcoreadapter-setstate.md)

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

Especifica el estado del <em>adaptador AdapterMemoryBudget,</em> que recupera o solicita el presupuesto de memoria del adaptador en el adaptador.

Al llamar [a QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el estado del adaptador <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> para *outputBuffer.*

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState,](./nf-dxcore_interface-idxcoreadapter-setstate.md) [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)