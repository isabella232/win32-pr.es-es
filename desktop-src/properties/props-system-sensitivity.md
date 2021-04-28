---
description: System.Sensitivity
ms.assetid: ad20504c-4920-4d72-86ef-04c82d71be70
title: System.Sensitivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca07ace0be48de932dc7f9b4bbff8a91400fdd3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091563"
---
# <a name="systemsensitivity"></a>System.Sensitivity

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Sensitivity
   shellPKey = PKEY_Sensitivity
   formatID = F8D3F6AC-4874-42CB-BE59-AB454B30716A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = SENSITIVITY_PROP_NORMAL
         enum
            name = Personal
            value = 1
            text = Personal
            defineToken = SENSITIVITY_PROP_PERSONAL
         enum
            name = Private
            value = 2
            text = Private
            defineToken = SENSITIVITY_PROP_PRIVATE
         enum
            name = Confidential
            value = 3
            text = Confidential
            defineToken = SENSITIVITY_PROP_CONFIDENTIAL
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Sensitivity
   shellPKey = PKEY_Sensitivity
   formatID = F8D3F6AC-4874-42CB-BE59-AB454B30716A
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = SENSITIVITY_PROP_NORMAL
         enum
            value = 1
            text = Personal
            defineName = SENSITIVITY_PROP_PERSONAL
         enum
            value = 2
            text = Private
            defineName = SENSITIVITY_PROP_PRIVATE
         enum
            value = 3
            text = Confidential
            defineName = SENSITIVITY_PROP_CONFIDENTIAL
```

## <a name="remarks"></a>Comentarios

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

 

 
