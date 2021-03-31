---
title: Propiedad SystemMonitor. UpdateInterval
description: Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que recopila datos de contador y actualiza el gráfico o el informe.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Propiedad UpdateInterval SysMon
- Propiedad UpdateInterval SysMon, clase SystemMonitor
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
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996315"
---
# <a name="systemmonitorupdateinterval-property"></a>Propiedad SystemMonitor. UpdateInterval

Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que recopila datos de contador y actualiza el gráfico o el informe.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a>Valor de propiedad

Período de tiempo, en segundos, que SYSMON espera antes de la próxima vez que recopila datos de contador y actualiza el gráfico o el informe. El intervalo mínimo es 1 segundo (este también es el valor predeterminado). El valor máximo es 1 millón.

## <a name="remarks"></a>Observaciones

Esta propiedad solo es relevante cuando [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) se establece en false.

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

 

 





