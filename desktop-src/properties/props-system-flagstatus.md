---
description: 'Estado de una marca. Valores: (0 = ninguno 1 = blanco 2 = rojo).'
ms.assetid: 0485deab-2408-4147-acaa-cb09e9e0032a
title: System. FlagStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dde42493f2d450854c3f53de5ecab26394f0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276608"
---
# <a name="systemflagstatus"></a>System. FlagStatus

Estado de una marca. Valores: (0 = ninguno 1 = blanco 2 = rojo).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotFlagged
            value = 0
            text = Not flagged
            defineToken = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            name = Completed
            value = 1
            text = Completed
            defineToken = FLAGSTATUS_COMPLETED
         enum
            name = FollowUp
            value = 2
            text = Follow Up
            defineToken = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not flagged
            defineName = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            value = 1
            text = Completed
            defineName = FLAGSTATUS_COMPLETED
         enum
            value = 2
            text = Follow Up
            defineName = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Requerida](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numérico](./propdesc-schema-numberformat.md)
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

[Consulta](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
