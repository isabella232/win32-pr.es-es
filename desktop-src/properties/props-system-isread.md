---
description: Identifica si se ha leído el elemento.
ms.assetid: 2efa6dd9-8521-48c9-9aff-e2e8f0e2296d
title: System.IsRead
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045dda6e840ff9d800b44573c4ba8537cdd2ebfd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363434"
---
# <a name="systemisread"></a>System.IsRead

Identifica si se ha leído el elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.IsRead
   shellPKey = PKEY_IsRead
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Read
            value = #TRUE#
            text = Read
            defineToken = ISREAD_READ
         enum
            name = NotRead
            value = #FALSE#
            text = Unread
            defineToken = ISREAD_NOTREAD
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.IsRead
   shellPKey = PKEY_IsRead
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 10
   SearchInfo
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            value = #TRUE#
            text = Read
            mnemonics = read
         enum
            value = #FALSE#
            text = Unread
            mnemonics = unread
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

 

 
