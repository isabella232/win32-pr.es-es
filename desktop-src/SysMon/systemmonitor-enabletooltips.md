---
title: Propiedad SystemMonitor.EnableToolTips
description: Recupera o establece un valor que determina si se muestra una sugerencia de herramientas cuando el mouse mantiene el mouse sobre un contador en una de las vistas de gráfico (no se admite para la vista de informe).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Propiedad EnableToolTips SysMon
- Propiedad EnableToolTips SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374854"
---
# <a name="systemmonitorenabletooltips-property"></a>Propiedad SystemMonitor.EnableToolTips

Recupera o establece un valor que determina si se muestra una sugerencia de herramientas cuando el mouse mantiene el mouse sobre un contador en una de las vistas de gráfico (no se admite para la vista de informe).

## <a name="syntax"></a>Sintaxis


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True muestra una sugerencia de herramienta con la información del contador; de lo contrario, False.

## <a name="remarks"></a>Observaciones

En el caso de los gráficos de líneas, la información sobre herramientas se ancla al punto de datos más cercano al mouse. En el caso de los gráficos de barras y los histogramas, la información sobre herramientas representa el valor de datos total de la barra, no un punto dentro de la barra.

La información sobre herramientas contiene información diferente basada en el origen de datos. Para los archivos de registro, la información sobre herramientas contiene la ruta de acceso del contador, el valor del contador, la marca de tiempo, el número de muestras de datos incluidas en el punto de datos y los valores de datos mínimo y máximo.

Para la actividad en tiempo real, la sugerencia de la herramienta contiene la ruta de acceso del contador, el valor del contador y la marca de tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





