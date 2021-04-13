---
title: Propiedad SystemMonitor. MonitorDuplicateInstances
description: Recupera o establece un valor que determina si se pueden supervisar varias instancias de un contador.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Propiedad MonitorDuplicateInstances SysMon
- Propiedad MonitorDuplicateInstances SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422211"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a>Propiedad SystemMonitor. MonitorDuplicateInstances

Recupera o establece un valor que determina si se pueden supervisar varias instancias de un contador.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True indica que se pueden supervisar varias instancias de un contador (true es el valor predeterminado). False indica que solo se puede supervisar una instancia de un contador.

## <a name="remarks"></a>Observaciones

El monitor de sistema anexa \# n a cada nombre de instancia, excepto el primero, si existen varias instancias. El número de serie, n, comienza con uno y se incrementa en uno por cada nueva instancia. Por ejemplo, si especifica " \\ Process ( \* ) \\ % Processor Time", la colección de contadores debe contener varias instancias de svchost. La primera vez será svchost, la siguiente repetición será svchost \# 1, etc.

Las instancias duplicadas se supervisan solo si se usa el carácter comodín ( \* ) para el nombre de instancia. Si especificó " \\ Process (svchost) \\ % Processor Time", se supervisará la primera instancia encontrada de svchost, no todas las instancias de svchost.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





