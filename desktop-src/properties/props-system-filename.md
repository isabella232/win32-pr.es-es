---
description: Nombre de archivo, incluida su extensión.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System.FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8a92febe0a4f2dfe8cc9d5741118fdb76bcb56c7bcd1ef5c3d881e8c0f9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119096924"
---
# <a name="systemfilename"></a>System.FileName

Nombre de archivo, incluida su extensión. System.FileExtension se deriva de esta propiedad.

Es posible que el elemento no exista en un sistema de archivos (es decir, es posible que no se abra mediante CreateFile). No obstante, si el elemento se representa como un archivo y su nombre sigue la sintaxis estándar de nomenclatura de archivos Win32, el origen de datos debe emitir esta propiedad. Si el elemento no es un archivo, el origen de datos debe emitir esta propiedad como VT \_ EMPTY.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

Es posible que el elemento no exista en un sistema de archivos (es decir, es posible que no se abra mediante CreateFile), pero si el elemento se representa como un archivo desde el sentido lógico y su nombre sigue la sintaxis estándar de nomenclatura de archivos Win32, el origen de datos debe emitir esta propiedad. Si un elemento no es un archivo, el valor de esta propiedad es VT \_ EMPTY. Vea System.ItemNameDisplay. Tiene el mismo valor que System.ParsingName para los elementos proporcionados por la carpeta de archivos del shell.

En la tabla siguiente se enumeran ejemplos de valores de propiedad path y filename:



| Ruta de acceso                               | Valor de propiedad |
|------------------------------------|----------------|
| c: \\ archivos \\ personales \\hello.txt     | hello.txt      |
| \\\\servidor \\ compartido \\ mydir \\news.doc | news.doc       |
| \\\\servidor \\ compartidonumbers.xls \\     | numbers.xls    |
| c: \\ Stuff \\ MyFolder                | MyFolder       |
| \[mensaje de correo electrónico\]                  | VT \_ EMPTY      |
| \[song.wma en un dispositivo portátil\]    | song.wma       |



 

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

 

 
