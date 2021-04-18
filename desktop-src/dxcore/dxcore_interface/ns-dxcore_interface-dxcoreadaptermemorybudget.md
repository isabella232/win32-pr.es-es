---
title: DXCoreAdapterMemoryBudget
description: Describe el presupuesto de memoria para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488198"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>Estructura DXCoreAdapterMemoryBudget

Especifica el estado del adaptador de <em>AdapterMemoryBudget</em> , que recupera o solicita el presupuesto de memoria del adaptador en el adaptador. Establecer (solicitar) un presupuesto representa la memoria física mínima necesaria para reservar, en bytes, en el adaptador. Se recomienda establecer una reserva de adaptador con el fin de indicar la cantidad de memoria física que no puede tener la aplicación. Este valor ayuda al sistema operativo (SO) a minimizar rápidamente el impacto de las grandes situaciones de presión de memoria.

Al llamar a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el estado del adaptador de <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo **DXCoreAdapterMemoryBudget** para *outputBuffer*.

Al llamar a [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), el estado del adaptador de <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo **uint64_t** para *inputData*.

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

Especifica el presupuesto de memoria del adaptador proporcionado por el sistema operativo, en bytes, que la aplicación debe tener como destino. Si *currentUsage* es mayor que el *presupuesto*, es posible que la aplicación incurra en intermitencias o penalizaciones de rendimiento debidas a la actividad en segundo plano por parte del sistema operativo, que está diseñada para proporcionar a otras aplicaciones un uso equitativo de la memoria del adaptador.

### <a name="currentusage"></a>currentUsage

Tipo: **uint64_t**

Especifica el uso de memoria actual del adaptador de la misma en bytes.

### <a name="availableforreservation"></a>availableForReservation

Tipo: **uint64_t**

Especifica la cantidad de memoria del adaptador, en bytes, que la aplicación tiene disponible para reserva. Para reservar esta memoria del adaptador, la aplicación debe llamar a [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) con el *Estado* establecido en [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).

### <a name="currentreservation"></a>currentReservation

Tipo: **uint64_t**

Especifica la cantidad de memoria del adaptador, en bytes, reservada por la aplicación. El sistema operativo usa la reserva como una sugerencia para determinar el espacio de trabajo mínimo de la aplicación. La aplicación debe intentar asegurarse de que se puede recortar el uso de memoria del adaptador para cumplir este requisito.

## <a name="see-also"></a>Vea también

[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)