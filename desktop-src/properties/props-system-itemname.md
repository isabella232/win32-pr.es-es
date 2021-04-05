---
description: Nombre base de la propiedad System. ItemNameDisplay.
ms.assetid: 8add2d72-efd3-4971-89d9-428190115ba0
title: System. ItemName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5ba987d8bdcd966724c15f0632edbfc8eb3d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001804"
---
# <a name="systemitemname"></a>System. ItemName

Nombre base de la propiedad [System. ItemNameDisplay](./props-system-itemnamedisplay.md) .

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemName
   shellPKey = PKEY_ItemName
   formatID = 6B8DA074-3B5C-43BC-886F-0A2CDCE00B6F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Si el elemento es un archivo, esta propiedad incluye la extensión en todos los casos y se localiza si un nombre traducido está disponible. Si el elemento es un mensaje, el valor de esta propiedad no incluye los prefijos de reenvío o de respuesta. Vea [System. ItemNamePrefix](./props-system-itemnameprefix.md) para obtener más información.

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

 

 
