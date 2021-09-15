---
description: Tipo de archivo percibido en función de su tipo canónico.
ms.assetid: dc5122a1-43b3-4c91-a44f-315fec5b4862
title: System.PerceivedType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc0be5e2ba481d113981efc264c4da66428e675
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468445"
---
# <a name="systemperceivedtype"></a>System.PerceivedType

Tipo de archivo percibido en función de su tipo canónico.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Custom
            value = -3
            text = Custom
         enum
            name = Unspecified
            value = -2
            text = Unspecified
         enum
            name = Folder
            value = -1
            text = Folder
            mnemonics = folders
         enum
            name = Unknown
            value = 0
            text = Unknown
         enum
            name = Text
            value = 1
            text = Text
         enum
            name = Image
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            name = Audio
            value = 3
            text = Audio
         enum
            name = Video
            value = 4
            text = Video
            mnemonics = videos
         enum
            name = Compressed
            value = 5
            text = Compressed
         enum
            name = Document
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            name = System
            value = 7
            text = System
         enum
            name = Application
            value = 8
            text = Application
         enum
            name = GameMedia
            value = 9
            text = Game Media
         enum
            name = Contacts
            value = 10
            text = Contacts
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = -3
            text = Custom
         enum
            value = -2
            text = Unspecified
         enum
            value = -1
            text = Folder
            mnemonics = folders
         enum
            value = 0
            text = Unknown
         enum
            value = 1
            text = Text
         enum
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            value = 3
            text = Audio
         enum
            value = 4
            text = Video
            mnemonics = videos
         enum
            value = 5
            text = Compressed
         enum
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            value = 7
            text = System
         enum
            value = 8
            text = Application
         enum
            value = 9
            text = Game Media
         enum
            value = 10
            text = Contacts
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey.h. El shell asigna automáticamente este valor.

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

 

 
