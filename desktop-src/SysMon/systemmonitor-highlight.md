---
title: SystemMonitor. Highlight (propiedad)
description: Recupera o establece un valor que indica si los valores de los contadores seleccionados se resaltan en el gráfico.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Resaltar propiedad SysMon
- Resaltar propiedad SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad Highlight
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905266"
---
# <a name="systemmonitorhighlight-property"></a>SystemMonitor. Highlight (propiedad)

Recupera o establece un valor que indica si los valores de los contadores seleccionados se resaltan en el gráfico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True indica que los valores de los contadores seleccionados se resaltan en el gráfico; en caso contrario, false. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Para seleccionar uno o varios contadores, puede establecer el valor de [**peritem. Selected**](counteritem-selected.md) en true o el usuario puede seleccionar los contadores de la lista de contadores que se muestran en la leyenda.

**Antes de Windows Vista:** No puede seleccionar contadores mediante programación y el usuario puede seleccionar un solo contador de la lista de contadores que se muestra en la leyenda.

El resaltado puede ser negro o blanco, dependiendo del valor de la propiedad [**BackColor**](systemmonitor-backcolor.md) . El resaltado se establece automáticamente en el color que proporcionará el contraste suficiente entre el color de resaltado y el color de fondo.

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

[**Contraelemento. seleccionado**](counteritem-selected.md)
</dt> </dl>

 

 





