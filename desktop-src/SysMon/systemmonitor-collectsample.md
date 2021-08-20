---
title: Método SystemMonitor CollectSample
description: Muestrea un valor para cada contador en el objeto Counters.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Método SysMon de CollectSample
- Método CollectSample SysMon, interfaz SystemMonitor
- SystemMonitor interface SysMon , CollectSample (método)
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6416abcf0601726aca30a9ea29c7f2d219210e4a81d6fef20625798676604ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956134"
---
# <a name="systemmonitorcollectsample-method"></a>SystemMonitor::CollectSample (método)

Muestrea un valor para cada contador del [**objeto Counters.**](counters.md)

## <a name="syntax"></a>Sintaxis


```VB
Sub CollectSample()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Llame a **CollectSample** solo si [**ManualUpdate**](systemmonitor-manualupdate.md) es True y los valores de contador de muestreo de la actividad actual del equipo no usan este método al realizar el muestreo desde un archivo de registro. El gráfico o informe se actualiza con el nuevo valor. Tenga en cuenta que algunos tipos de gráficos necesitan dos ejemplos para representar los datos, por ejemplo, el gráfico de líneas.

Para recibir una notificación cuando se haya recopilado el ejemplo, implemente el [**evento OnSampleCollected.**](-systemmonitor-onsamplecollected.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





