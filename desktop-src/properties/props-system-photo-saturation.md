---
description: Indica la dirección del procesamiento de saturación aplicado por la cámara cuando se tomó la foto.
ms.assetid: 209edf55-fd6c-416b-b175-346f5158fc2a
title: System. Photo. saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50655b1d9344bb3c25576de9ece3ac6ef2bba95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697058"
---
# <a name="systemphotosaturation"></a>System. Photo. saturación

Indica la dirección del procesamiento de saturación aplicado por la cámara cuando se tomó la foto.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_SATURATION_NORMAL
         enum
            name = Low
            value = 1
            text = Low saturation
            defineToken = PHOTO_SATURATION_LOW
         enum
            name = High
            value = 2
            text = High saturation
            defineToken = PHOTO_SATURATION_HIGH
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_SATURATION_NORMAL
         enum
            value = 1
            text = Low saturation
            defineName = PHOTO_SATURATION_LOW
         enum
            value = 2
            text = High saturation
            defineName = PHOTO_SATURATION_HIGH
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

 

 
