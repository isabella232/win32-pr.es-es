---
description: Ayuda a mostrar como un icono si una ubicación es la ubicación de almacenamiento predeterminada para el propietario o los usuarios que no son propietarios de una biblioteca.
ms.assetid: 42375796-bf95-4092-bce0-c77e7b5bfeea
title: System. DefaultSaveLocationDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1147a7c0fce8b4bc564b57bac2476b1826e4313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697118"
---
# <a name="systemdefaultsavelocationdisplay"></a>System. DefaultSaveLocationDisplay

Ayuda a mostrar como un icono si una ubicación es la ubicación de almacenamiento predeterminada para el propietario o los usuarios que no son propietarios de una biblioteca.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.DefaultSaveLocationDisplay
   shellPKey = PKEY_DefaultSaveLocationDisplay
   formatID = 5D76B67F-9B3D-44BB-B6AE-25DA4F638A67
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = DefaultSaveNone
            value = 0
            text
            defineToken = ISDEFAULTSAVE_NONE
         enum
            name = DefaultSaveOwner
            value = 1
            text = Default save location
            defineToken = ISDEFAULTSAVE_OWNER
         enum
            name = DefaultSavePublic
            value = 2
            text = Public save location
            defineToken = ISDEFAULTSAVE_NONOWNER
         enum
            name = DefaultSaveBoth
            value = 3
            text = Default and public save location
            defineToken = ISDEFAULTSAVE_BOTH
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

 

 
