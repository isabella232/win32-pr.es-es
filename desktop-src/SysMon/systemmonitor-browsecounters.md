---
title: Método SystemMonitor BrowseCounters
description: Muestra el cuadro de diálogo Agregar contadores.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Método BrowseCounters SysMon
- Método BrowseCounters SysMon, interfaz SystemMonitor
- SystemMonitor interface SysMon , BrowseCounters (método)
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e88d493ea0e4e1a9312191533162c8eb5a94cfb4233d17d21bb7217a136d403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882931"
---
# <a name="systemmonitorbrowsecounters-method"></a>SystemMonitor::BrowseCounters (método)

Muestra el **cuadro de diálogo Agregar** contadores.

## <a name="syntax"></a>Sintaxis


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este cuadro de diálogo permite al usuario seleccionar contadores de rendimiento locales o remotos de una lista de objetos de rendimiento. Los contadores seleccionados se agregan a la [**colección Contadores**](counters.md) y se muestran en el gráfico o informe.

Para recibir una notificación cuando se agrega un contador, implemente el [**evento OnCounterAdded.**](systemmonitor-oncounteradded.md)

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

[**Counters.Add**](counters-add.md)
</dt> </dl>

 

 





