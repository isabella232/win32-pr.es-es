---
description: Identifica la extensión de archivo del elemento basado en archivo, incluido el punto inicial.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659881"
---
# <a name="systemfileextension"></a>System. FileExtension

Identifica la extensión de archivo del elemento basado en archivo, incluido el punto inicial. Esta propiedad se deriva de System. FileName. Si System. FileName no tiene una extensión de archivo o es VT \_ vacío, el valor de esta propiedad debe ser VT \_ vacío.

Para obtener el tipo de cualquier elemento (incluido un elemento que no es un archivo), use System. ItemType.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Si [System. FileName](./props-system-filename.md) es VT \_ vacío, esta propiedad también debe estar vacía. De lo contrario, esta propiedad debe derivarse apropiadamente por el origen de datos de System. FileName. Si System. FileName no incluye una extensión de archivo, [System. FileExtension]() debe ser VT \_ vacío. Para obtener el tipo de cualquier elemento (incluido un elemento que no es un archivo), use [System. ItemType](./props-system-itemtype.md).

Ejemplos de propiedades de extensión de archivo y ruta de acceso. 

| Ruta                               | Extensión de archivo |
|------------------------------------|----------------|
| c: \\ archivos \\ personales \\hello.txt     | .txt           |
| \\\\\\news.doc del recurso compartido del servidor \\ myDir \\ | .doc           |
| \\\\\\numbers.xls de recurso compartido de servidor \\     | .xls           |
| \\\\\\carpeta de recurso compartido de servidor \\          | VT \_ vacío      |
| c: \\ mis \\ carpetas                | VT \_ vacío      |
| \[desktop\]                        | VT \_ vacío      |



 

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

 

 
