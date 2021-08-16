---
title: Propiedad SystemMonitor.DataPointCount
description: Recupera o establece el número de puntos de datos que se muestran en un gráfico de líneas.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- SysMon, propiedad DataPointCount
- Propiedad SysMon de DataPointCount , objeto SystemMonitor
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
ms.openlocfilehash: 3d7d1212f3f1467c0fb505e84dffdd9cc6bb381c19d8ccc34ad38ee46562ec6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882630"
---
# <a name="systemmonitordatapointcount-property"></a>Propiedad SystemMonitor.DataPointCount

Recupera o establece el número de puntos de datos que se muestran en un gráfico de líneas.

## <a name="syntax"></a>Syntax


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de puntos de datos que se muestran en la vista de un gráfico de líneas. El valor predeterminado es 100 puntos de datos. El intervalo válido de valores es de 2 a 1000.

## <a name="remarks"></a>Comentarios

Esta propiedad solo se usa si [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) es **sysmonCurrentActivity**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





