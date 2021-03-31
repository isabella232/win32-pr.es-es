---
title: SystemMonitor. MaximumScale (propiedad)
description: Recupera o establece el valor máximo del eje vertical (Y) del gráfico.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Propiedad MaximumScale SysMon
- Propiedad MaximumScale SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996259"
---
# <a name="systemmonitormaximumscale-property"></a>SystemMonitor. MaximumScale (propiedad)

Recupera o establece el valor máximo del eje vertical (Y) del gráfico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor máximo positivo del eje vertical del gráfico. El valor máximo predeterminado de la escala vertical es 100. El valor más bajo en el que se puede establecer el valor máximo es uno más que el valor de [**MinimumScale**](systemmonitor-minimumscale.md) . El valor más alto en el que puede establecer el valor máximo es 999.999.999.

## <a name="remarks"></a>Observaciones

El control ajusta automáticamente la posición de los números de escala que se muestran en la escala vertical según el tamaño del control mostrado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





