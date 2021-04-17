---
title: Propiedad SystemMonitor. ShowTimeAxisLabels
description: Recupera o establece un valor que determina si el eje horizontal (X) de la vista de gráfico contiene etiquetas.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Propiedad ShowTimeAxisLabels SysMon
- Propiedad ShowTimeAxisLabels SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665941"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a>Propiedad SystemMonitor. ShowTimeAxisLabels

Recupera o establece un valor que determina si el eje horizontal (X) de la vista de gráfico contiene etiquetas.

## <a name="syntax"></a>Sintaxis


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si el valor es true, se aplicarán etiquetas al eje x. Un valor de false no lo será. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

SYSMON omite esta propiedad para los gráficos de barras, informes e histogramas.

En el caso de los gráficos de líneas, SYSMON usa la hora a la que se muestreó el valor del contador como etiqueta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





