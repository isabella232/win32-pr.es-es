---
title: Propiedad TaskSettings.DisallowStartIfOnBatteries
description: Para el scripting, obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se ejecuta con baterías.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Propiedad DisallowStartIfOnBatteries Programador de tareas
- Propiedad DisallowStartIfOnBatteries Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad DisallowStartIfOnBatteries
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891457"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>Propiedad TaskSettings.DisallowStartIfOnBatteries

Para el scripting, obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se ejecuta con baterías.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Valor booleano que indica que la tarea no se iniciará si el equipo se ejecuta con baterías. Si es True, la tarea no se inicia si el equipo se ejecuta con baterías. Si es False, la tarea se inicia si el equipo se ejecuta con baterías. El valor predeterminado es True.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) del esquema Programador de tareas datos.

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

 

 





