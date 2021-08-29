---
title: Propiedad SystemMonitor.MonitorDuplicateInstances
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
ms.openlocfilehash: da6f8e9f85dcc865bb9a0733b7a1160582772754b5a2cabd1aa7b80452e6f42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881787"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a>Propiedad SystemMonitor.MonitorDuplicateInstances

Recupera o establece un valor que determina si se pueden supervisar varias instancias de un contador.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True indica que se pueden supervisar varias instancias de un contador (True es el valor predeterminado). False indica que solo se puede supervisar una instancia de un contador.

## <a name="remarks"></a>Comentarios

El Monitor de sistema \# anexa n a cada nombre de instancia, excepto el primero, si existen varias instancias. El número de serie, n, comienza con uno y se incrementa en uno para cada nueva instancia. Por ejemplo, si especifica \\ "Process( ) % Processor Time", la colección de contadores debe contener \* varias instancias de \\ svchost. La primera repetición será svchost, la siguiente será svchost \# 1, y así sucesivamente.

Las instancias duplicadas solo se supervisan si se usa el carácter comodín ( \* ) para el nombre de instancia. Si especificó \\ "Process(svchost) % Processor Time" solo se supervisa la primera instancia encontrada de svchost, no todas las \\ instancias de svchost.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





