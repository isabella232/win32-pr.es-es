---
title: Propiedad TaskSettings.RunOnlyIfNetworkAvailable
description: Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Propiedad RunOnlyIfNetworkAvailable Programador de tareas
- Propiedad RunOnlyIfNetworkAvailable Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad RunOnlyIfNetworkAvailable
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160605"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>Propiedad TaskSettings.RunOnlyIfNetworkAvailable

Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la propiedad indica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





