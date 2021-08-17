---
title: Propiedad SystemMonitor.ReportValueType
description: Recupera o establece un valor que determina si el gráfico histograma y vistas de informe representa el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor promedio o mínimo del contador.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- ReportValueType, propiedad SysMon
- Propiedad ReportValueType SysMon , clase SystemMonitor
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
ms.openlocfilehash: 95282c48ac30b13af07c124ea21f36f91c7ae658b10d290a109fdd1dcc7a5ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955013"
---
# <a name="systemmonitorreportvaluetype-property"></a>Propiedad SystemMonitor.ReportValueType

Recupera o establece un valor que determina si el gráfico histograma y vistas de informe representa el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor promedio o mínimo del contador.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Valor de propiedad

Determina si el gráfico de vistas Histograma e Informe es el último valor muestreado durante el intervalo de muestreo o un valor calculado a partir del intervalo de muestreo. Para obtener los valores posibles, [**vea ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Comentarios

SYSMON omite este valor y usa [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) si [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) noDisplayTypeConstants.sys [**monHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) **oDisplayTypeConstants.sysmonReport**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





