---
title: Propiedad SystemMonitor. ChartScroll
description: Recupera o establece un valor que determina si el gráfico de líneas se desplaza en la vista.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Propiedad ChartScroll SysMon
- Propiedad ChartScroll SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996494"
---
# <a name="systemmonitorchartscroll-property"></a>Propiedad SystemMonitor. ChartScroll

Recupera o establece un valor que determina si el gráfico de líneas se desplaza en la vista.

## <a name="syntax"></a>Sintaxis


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si el gráfico de líneas se desplaza continuamente de derecha a izquierda; en caso contrario, false si el gráfico de líneas se dibuja de izquierda a derecha y se ajusta en sí mismo en la vista. False es la opción predeterminada.

## <a name="remarks"></a>Observaciones

Este valor se omite si [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) no es [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





