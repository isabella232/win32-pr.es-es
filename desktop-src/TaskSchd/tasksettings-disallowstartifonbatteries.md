---
title: Propiedad TaskSettings. DisallowStartIfOnBatteries
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se está ejecutando con baterías.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Programador de tareas de la propiedad DisallowStartIfOnBatteries
- Programador de tareas de la propiedad DisallowStartIfOnBatteries, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150841"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>Propiedad TaskSettings. DisallowStartIfOnBatteries

En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se está ejecutando con baterías.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Un valor booleano que indica que la tarea no se iniciará si el equipo se está ejecutando con baterías. Si es true, la tarea no se iniciará si el equipo se está ejecutando con baterías. Si es false, la tarea se iniciará si el equipo se ejecuta con baterías. El valor predeterminado es True.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) del esquema de programador de tareas.

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

 

 





