---
description: El nombre de archivo, incluida su extensión.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687408"
---
# <a name="systemfilename"></a>System. FileName

El nombre de archivo, incluida su extensión. System. FileExtension se deriva de esta propiedad.

Es posible que el elemento no exista en un sistema de archivos (es decir, que no se pueda abrir con CreateFile). No obstante, si el elemento se representa como un archivo y su nombre sigue la sintaxis estándar de nombres de archivo de Win32, el origen de datos debe emitir esta propiedad. Si el elemento no es un archivo, el origen de datos debe emitir esta propiedad como VT \_ vacío.

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

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Es posible que el elemento no exista en un sistema de archivos (es decir, que no se pueda abrir con CreateFile), pero si el elemento se representa como un archivo desde el sentido lógico y su nombre sigue la sintaxis estándar de nombres de archivo de Win32, el origen de datos debe emitir esta propiedad. Si un elemento no es un archivo, el valor de esta propiedad es VT \_ vacío. Vea System. ItemNameDisplay. Tiene el mismo valor que System. ParsingName para los elementos que proporciona la carpeta de archivos del shell.

En la tabla siguiente se muestran ejemplos de valores de propiedad path y FILENAME:



| Ruta                               | Valor de propiedad |
|------------------------------------|----------------|
| c: \\ archivos \\ personales \\hello.txt     | hello.txt      |
| \\\\\\news.doc del recurso compartido del servidor \\ myDir \\ | news.doc       |
| \\\\\\numbers.xls de recurso compartido de servidor \\     | numbers.xls    |
| c: \\ mis \\ carpetas                | MyFolder       |
| \[mensaje de correo electrónico\]                  | VT \_ vacío      |
| \[Song. WMA en dispositivo portátil\]    | Song. WMA       |



 

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

 

 
