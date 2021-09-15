---
description: Indica el estado actual de la tarea.
ms.assetid: 76bb9bb7-3383-4e5a-ae75-a11c40f318e2
title: System.Communication.TaskStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd74f25400093d9719607a718b4d1fc727ff36de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574653"
---
# <a name="systemcommunicationtaskstatus"></a>System.Communication.TaskStatus

Indica el estado actual de la tarea.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotStarted
            value = 0
            text = Not Started
            defineToken = TASKSTATUS_NOTSTARTED
         enum
            name = InProgress
            value = 1
            text = In Progress
            defineToken = TASKSTATUS_INPROGRESS
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = TASKSTATUS_COMPLETE
         enum
            name = Waiting
            value = 3
            text = Waiting
            defineToken = TASKSTATUS_WAITING
         enum
            name = Deferred
            value = 4
            text = Deferred
            defineToken = TASKSTATUS_DEFERRED
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not Started
            defineName = TASKSTATUS_NOTSTARTED
         enum
            value = 1
            text = In Progress
            defineName = TASKSTATUS_INPROGRESS
         enum
            value = 2
            text = Complete
            defineName = TASKSTATUS_COMPLETE
         enum
            value = 3
            text = Waiting
            defineName = TASKSTATUS_WAITING
         enum
            value = 4
            text = Deferred
            defineName = TASKSTATUS_DEFERRED
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
