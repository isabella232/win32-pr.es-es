---
title: Propiedad SystemMonitor. MinimumScale
description: Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Propiedad MinimumScale SysMon
- Propiedad MinimumScale SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490468"
---
# <a name="systemmonitorminimumscale-property"></a>Propiedad SystemMonitor. MinimumScale

Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor mínimo positivo del eje vertical del gráfico. El valor mínimo predeterminado de la escala vertical es 0. El valor más alto en el que se puede establecer el valor mínimo es uno menos que el valor [**MaximumScale**](systemmonitor-maximumscale.md) .

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

[**SystemMonitor. MaximumScale**](systemmonitor-maximumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





