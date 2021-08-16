---
title: Propiedad SystemMonitor.MaximumScale
description: Recupera o establece el valor máximo del eje vertical (Y) del gráfico.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- SysMon, propiedad MaximumScale
- Propiedad MaximumScale SysMon , clase SystemMonitor
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
ms.openlocfilehash: 176ebab3b2879b3d158310ec61fa9e65df45f8b502029ede1c58c2c1dd33f225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882034"
---
# <a name="systemmonitormaximumscale-property"></a>Propiedad SystemMonitor.MaximumScale

Recupera o establece el valor máximo del eje vertical (Y) del gráfico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor máximo positivo del eje vertical del gráfico. El valor máximo predeterminado de la escala vertical es 100. El valor más bajo en el que puede establecer el valor máximo es uno más que [**el valor MinimumScale.**](systemmonitor-minimumscale.md) El valor máximo en el que puede establecer el valor máximo es 999 999 999 999.

## <a name="remarks"></a>Comentarios

El control ajusta automáticamente la posición de los números de escala mostrados en la escala vertical según el tamaño del control mostrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





