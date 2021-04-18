---
description: Representa una dirección URL con formato correcto que señala al elemento.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. ItemUrl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707165"
---
# <a name="systemitemurl"></a>System. ItemUrl

Representa una dirección URL con formato correcto que señala al elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Para hacer referencia a los elementos del espacio de nombres del shell a través de las API de Shell, use [System. ParsingPath](./props-system-parsingpath.md).

Valores de ejemplo:



| Tipo de elemento | Ejemplo                        |
|-----------|--------------------------------|
| Archivo      | hello.txt file:///c:/mydir/bar/ |
| Archivo      | CSC://{GUID}/...               |
| Message   | mapi://...                     |



 

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

 

 
