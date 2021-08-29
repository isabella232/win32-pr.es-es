---
title: DXCoreAdapterMemoryBudget
description: Describe el presupuesto de memoria de un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2cbe109d4c7f6c03389ec9e51c9468c601730890220fde2dea72aed476093f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118689"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>DxCoreAdapterMemoryBudget (estructura)

Especifica el estado <em>del adaptador AdapterMemoryBudget,</em> que recupera o solicita el presupuesto de memoria del adaptador en el adaptador. Establecer (solicitar) un presupuesto representa la memoria física mínima necesaria para reservar, en bytes, en el adaptador. Se recomienda establecer una reserva de adaptador para indicar la cantidad de memoria física sin la que la aplicación no puede pasar. Este valor ayuda al sistema operativo (SO) a minimizar rápidamente el impacto de situaciones de presión de memoria de gran tamaño.

Al llamar [a QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el estado del adaptador <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo **DXCoreAdapterMemoryBudget** para *outputBuffer.*

Al llamar [a SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), el estado del adaptador <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo **uint64_t** *para inputData*.

## <a name="syntax"></a>Sintaxis

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a>Miembros

### <a name="budget"></a>budget

Tipo: **uint64_t**

Especifica el presupuesto de memoria del adaptador proporcionado por el sistema operativo, en bytes, que la aplicación debe tener como destino. Si *currentUsage* es mayor que el presupuesto *,* la aplicación puede incurrir en errores o penalizaciones de rendimiento debido a la actividad en segundo plano por parte del sistema operativo, que está diseñado para proporcionar a otras aplicaciones un uso justo de la memoria del adaptador.

### <a name="currentusage"></a>currentUsage

Tipo: **uint64_t**

Especifica el uso actual de la memoria del adaptador de applicaton, en bytes.

### <a name="availableforreservation"></a>availableForReservation

Tipo: **uint64_t**

Especifica la cantidad de memoria del adaptador, en bytes, que la aplicación tiene disponible para la reserva. Para reservar esta memoria del adaptador, la aplicación debe llamar a [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) con el estado *establecido* en [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).

### <a name="currentreservation"></a>currentReservation

Tipo: **uint64_t**

Especifica la cantidad de memoria del adaptador, en bytes, reservada por la aplicación. El sistema operativo usa la reserva como sugerencia para determinar el espacio de trabajo mínimo de la aplicación. La aplicación debe intentar asegurarse de que el uso de memoria del adaptador se puede recortar para cumplir este requisito.

## <a name="see-also"></a>Consulte también

[Referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)