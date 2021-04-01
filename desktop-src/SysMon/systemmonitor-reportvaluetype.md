---
title: Propiedad SystemMonitor. ReportValueType
description: Recupera o establece un valor que determina si el histograma y las vistas de informe representan el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor del contador promedio o mínimo.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Propiedad ReportValueType SysMon
- Propiedad ReportValueType SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996350"
---
# <a name="systemmonitorreportvaluetype-property"></a>Propiedad SystemMonitor. ReportValueType

Recupera o establece un valor que determina si el histograma y las vistas de informe representan el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor del contador promedio o mínimo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Valor de propiedad

Determina si el histograma y las vistas de informe representan el último valor muestreado durante el intervalo de muestreo o un valor calculado del intervalo de muestreo. Para obtener los valores posibles, vea [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Observaciones

SYSMON omite este valor y usa [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) si [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) no es [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) o **DisplayTypeConstants.sysmonReport**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





