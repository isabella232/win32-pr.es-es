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
# <a name="dxcoreadapterstate-enum"></a>Enumeración DXCoreAdapterState

Define constantes que especifican los tipos de Estados del adaptador de DXCore. Pase una de estas constantes al método [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) para recuperar el elemento de estado del adaptador para un tipo de estado; Pase una constante al método [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) para establecer la información de un adaptador para un elemento de estado.

## <a name="syntax"></a>Sintaxis

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Constantes

### <a name="isdriverupdateinprogress"></a>IsDriverUpdateInProgress

Especifica el estado del adaptador de <em>IsDriverUpdateInProgress</em> , que `true` indica que se ha iniciado una actualización del controlador en el adaptador, pero que aún no se ha completado. Si ya se ha completado la actualización del controlador, se habrá invalidado el adaptador y la llamada a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) devolverá un <b>valor HRESULT</b> de <b>DXGI_ERROR_DEVICE_REMOVED</b>.

Al llamar a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el elemento de estado <em>IsDriverUpdateInProgress</em> tiene el tipo <b>uint8_t</b>, que representa un valor booleano.

<b>Importante</b>. Este elemento de estado no es compatible con [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

Especifica el estado del adaptador de <em>AdapterMemoryBudget</em> , que recupera o solicita el presupuesto de memoria del adaptador en el adaptador.

Al llamar a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el estado del adaptador de <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> para *outputBuffer*.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)