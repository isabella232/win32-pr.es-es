---
title: Propiedad TaskSettings. RunOnlyIfNetworkAvailable
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Programador de tareas de la propiedad RunOnlyIfNetworkAvailable
- Programador de tareas de la propiedad RunOnlyIfNetworkAvailable, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905488"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>Propiedad TaskSettings. RunOnlyIfNetworkAvailable

En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, la propiedad indica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





