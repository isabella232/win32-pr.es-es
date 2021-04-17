---
description: Indica la dirección del procesamiento de nitidez aplicado por la cámara cuando se tomó la foto.
ms.assetid: ee3dca97-a094-4de8-aacd-729abcef4965
title: System. Photo. nitidez
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b6b1b3dc90df576b90b8de6d912a176872bfee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697054"
---
# <a name="systemphotosharpness"></a>System. Photo. nitidez

Indica la dirección del procesamiento de nitidez aplicado por la cámara cuando se tomó la foto.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Sharpness
   shellPKey = PKEY_Photo_Sharpness
   formatID = FC6976DB-8349-4970-AE97-B3C5316A08F0
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
            defineToken = PHOTO_SHARPNESS_NORMAL
         enum
            name = Soft
            value = 1
            text = Soft
            defineToken = PHOTO_SHARPNESS_SOFT
         enum
            name = Hard
            value = 2
            text = Hard
            defineToken = PHOTO_SHARPNESS_HARD
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Sharpness
   shellPKey = PKEY_Photo_Sharpness
   formatID = FC6976DB-8349-4970-AE97-B3C5316A08F0
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
            defineName = PHOTO_SHARPNESS_NORMAL
         enum
            value = 1
            text = Soft
            defineName = PHOTO_SHARPNESS_SOFT
         enum
            value = 2
            text = Hard
            defineName = PHOTO_SHARPNESS_HARD
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

 

 
