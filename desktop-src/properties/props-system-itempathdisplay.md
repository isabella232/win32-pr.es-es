---
description: La ruta de acceso de visualización fácil de ver al elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156420"
---
# <a name="systemitempathdisplay"></a>System. ItemPathDisplay

La ruta de acceso de visualización fácil de ver al elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Si el elemento es un archivo o una carpeta, esta propiedad incluye la extensión en todos los casos y se localiza si hay disponible un nombre traducido. En el caso de otros elementos, este es el equivalente descriptivo, siempre que el elemento exista en el almacenamiento jerárquico.

A diferencia de [System. ItemUrl](./props-system-itemurl.md), este valor de propiedad no incluye el esquema de la dirección URL. Para analizar una ruta de acceso de elemento, use System. ItemUrl o [System. ParsingPath](./props-system-parsingpath.md). Para hacer referencia a elementos de espacio de nombres del shell mediante las API de Shell, use System. ParsingPath.

Valores de ejemplo:



| Ruta                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\hello.txt de la \\ barra myDir \\              | c: \\hello.txt de la \\ barra myDir \\              |
| \\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\ | \\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\ |
| \\\\\\numbers.xls de recurso compartido de servidor \\         | \\\\\\numbers.xls de recurso compartido de servidor \\         |
| c: \\ myDir \\ carpeta                    | c: \\ myDir \\ carpeta                    |
| Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '    | Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '    |



 

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

 

 
