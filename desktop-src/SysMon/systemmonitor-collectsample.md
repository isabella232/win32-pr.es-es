---
title: SystemMonitor CollectSample, método
description: Muestrea un valor para cada contador del objeto Counters.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Método CollectSample SysMon
- Método CollectSample SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, método CollectSample
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
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490990"
---
# <a name="systemmonitorcollectsample-method"></a>SystemMonitor:: CollectSample (método)

Muestrea un valor para cada contador del objeto [**counters**](counters.md) .

## <a name="syntax"></a>Sintaxis


```VB
Sub CollectSample()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Llame a **CollectSample** solo si [**ManualUpdate**](systemmonitor-manualupdate.md) es true y va a tomar muestras de los valores de contador de la actividad actual del equipo no usar este método al realizar el muestreo desde un archivo de registro. El gráfico o informe se actualiza con el nuevo valor. Tenga en cuenta que algunos tipos de gráficos necesitan dos muestras para representar gráficamente los datos, por ejemplo, el gráfico de líneas.

Para recibir una notificación cuando se ha recopilado el ejemplo, implemente el evento [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





