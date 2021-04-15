---
title: Enumeración DODownloadCostPolicy
description: Especifica el identificador de las opciones de directivas de costos asociadas a la propiedad **DODownloadProperty_CostPolicy** .
keywords:
- Enumeración DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421983"
---
# <a name="dodownloadcostpolicy-enumeration"></a>Enumeración DODownloadCostPolicy

La enumeración **DODownloadCostPolicy** especifica el identificador de las opciones de directivas de costos asociadas a la propiedad **DODownloadProperty_CostPolicy** .

## <a name="syntax"></a>Sintaxis

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a>Constantes

| Requisito | Value |
|-|-|
| DODownloadCostPolicy_Always | La descarga se ejecuta independientemente del costo. |
| DODownloadCostPolicy_Unrestricted | Descarga se ejecuta a menos que imponga costos o límites de tráfico. |
| DODownloadCostPolicy_Standard | Descarga se ejecuta a menos que no esté sujeto a un recargo ni a un agotamiento cercano. |
| DODownloadCostPolicy_NoRoaming | La descarga se ejecuta a menos que la conectividad esté sujeta a suplementos móviles. |
| DODownloadCostPolicy_NoSurcharge | Descarga se ejecuta a menos que esté sujeto a un suplemento. |
| DODownloadCostPolicy_NoCellular | Descarga se ejecuta a menos que la red sea móvil. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DeliveryOptimizationDownloadTypes. h |
