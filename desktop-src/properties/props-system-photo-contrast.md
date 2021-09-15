---
description: Indica la dirección del procesamiento de contraste aplicado por la cámara cuando se tomó la imagen. &\#0034;0&\# 0034; indica &\# 0034; Normal&\# 0034;; &\# 0034;1&\# 0034; indica &\# 0034;&\# 0034;; &\# 0034;2&\# 0034; indica &\# 0034;&\# 0034;.
ms.assetid: 32f89149-b90d-4fe9-9d1a-b8bb966d62fe
title: System.Photo.Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4117f13d35a352971a5f9b9f8685816f8ffbd1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468430"
---
# <a name="systemphotocontrast"></a>System.Photo.Contrast

Indica la dirección del procesamiento de contraste aplicado por la cámara cuando se tomó la imagen. "0" indica "Normal"; "1" indica "Soft"; "2" indica "Hard".

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
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
            defineToken = PHOTO_CONTRAST_NORMAL
         enum
            name = Soft
            value = 1
            text = Soft
            defineToken = PHOTO_CONTRAST_SOFT
         enum
            name = Hard
            value = 2
            text = Hard
            defineToken = PHOTO_CONTRAST_HARD
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
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
            defineName = PHOTO_CONTRAST_NORMAL
         enum
            value = 1
            text = Soft
            defineName = PHOTO_CONTRAST_SOFT
         enum
            value = 2
            text = Hard
            defineName = PHOTO_CONTRAST_HARD
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

 

 
