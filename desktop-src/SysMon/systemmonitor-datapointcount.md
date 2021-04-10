---
title: Propiedad SystemMonitor. DataPointCount
description: Recupera o establece el número de puntos de datos mostrados en un gráfico de líneas.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Propiedad DataPointCount SysMon
- Propiedad DataPointCount SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996163"
---
# <a name="systemmonitordatapointcount-property"></a>Propiedad SystemMonitor. DataPointCount

Recupera o establece el número de puntos de datos mostrados en un gráfico de líneas.

## <a name="syntax"></a>Sintaxis


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de puntos de datos mostrados en la vista de un gráfico de líneas. El valor predeterminado es 100 puntos de datos. El intervalo válido de valores es de 2 a 1.000.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se usa si [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) es **sysmonCurrentActivity**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





