---
title: Propiedad SystemMonitor.MinimumScale
description: Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- SysMon, propiedad MinimumScale
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
ms.openlocfilehash: afeafadde962f01db0dc828cb0e0346e6d93fb121a0166637ba0d67b947d36e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955283"
---
# <a name="systemmonitorminimumscale-property"></a>Propiedad SystemMonitor.MinimumScale

Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor mínimo positivo del eje vertical del gráfico. El valor mínimo predeterminado de la escala vertical es 0. El valor más alto en el que puede establecer el valor mínimo es uno menor que [**el valor MaximumScale.**](systemmonitor-maximumscale.md)

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

[**SystemMonitor.MaximumScale**](systemmonitor-maximumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





