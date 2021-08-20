---
title: Propiedad SystemMonitor.UpdateInterval
description: Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que recopila los datos del contador y actualiza el gráfico o informe.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Propiedad UpdateInterval SysMon
- Propiedad UpdateInterval SysMon , clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c6f9d20a6a9b88d3764e013468747968a71690cf5e4a31603a88acd9e7e33e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954530"
---
# <a name="systemmonitorupdateinterval-property"></a>Propiedad SystemMonitor.UpdateInterval

Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que recopila los datos del contador y actualiza el gráfico o informe.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a>Valor de propiedad

Tiempo, en segundos, que SYSMON espera antes de la próxima vez que recopile los datos del contador y actualice el gráfico o informe. El intervalo mínimo es 1 segundo (este también es el valor predeterminado). El valor máximo es 1 000 000.

## <a name="remarks"></a>Comentarios

Esta propiedad solo es relevante cuando [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) está establecido en False.

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

 

 





