---
title: ENUMERACIÓN DODownloadCostPolicy
description: Especifica el identificador de las opciones de directivas de costo asociadas a **la DODownloadProperty_CostPolicy** propiedad .
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566805"
---
# <a name="dodownloadcostpolicy-enumeration"></a>ENUMERACIÓN DODownloadCostPolicy

La **enumeración DODownloadCostPolicy** especifica el identificador de las opciones de directivas de costo asociadas a **la DODownloadProperty_CostPolicy** propiedad .

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
| DODownloadCostPolicy_Unrestricted | La descarga se ejecuta a menos que imponga costos o límites de tráfico. |
| DODownloadCostPolicy_Standard | La descarga se ejecuta a menos que no esté sujeto a un sobrecargo ni a un agotamiento próximo. |
| DODownloadCostPolicy_NoRoaming | La descarga se ejecuta a menos que esa conectividad esté sujeta a los suplementos de itinerancia. |
| DODownloadCostPolicy_NoSurcharge | La descarga se ejecuta a menos que esté sujeto a un sobrecargo. |
| DODownloadCostPolicy_NoCellular | La descarga se ejecuta a menos que la red esté en telefonía móvil. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |
