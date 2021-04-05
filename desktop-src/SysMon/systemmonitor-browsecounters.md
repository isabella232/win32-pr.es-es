---
title: SystemMonitor BrowseCounters, método
description: Muestra el cuadro de diálogo Agregar contadores.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Método BrowseCounters SysMon
- Método BrowseCounters SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, método BrowseCounters
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
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078828"
---
# <a name="systemmonitorbrowsecounters-method"></a>SystemMonitor:: BrowseCounters (método)

Muestra el cuadro de diálogo **Agregar contadores** .

## <a name="syntax"></a>Sintaxis


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este cuadro de diálogo permite al usuario seleccionar contadores de rendimiento locales o remotos en una lista de objetos de rendimiento. Los contadores seleccionados se agregan a la colección de [**contadores**](counters.md) y se muestran en el gráfico o el informe.

Para recibir una notificación cuando se agrega un contador, implemente el evento [**OnCounterAdded**](systemmonitor-oncounteradded.md) .

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

[**Counters. Add**](counters-add.md)
</dt> </dl>

 

 





