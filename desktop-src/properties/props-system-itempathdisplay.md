---
description: Obtenga información sobre la propiedad System.ItemPathDisplay, que representa la ruta de acceso de presentación fácil de usar al elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System.ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddad0edbc1a77a3de1fab7956d8ce6e6f906f06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403908"
---
# <a name="systemitempathdisplay"></a>System.ItemPathDisplay

Ruta de acceso de presentación fácil de usar al elemento.

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

Los valores PKEY se definen en Propkey.h.

Si el elemento es un archivo o una carpeta, esta propiedad incluye la extensión en todos los casos y se localiza si hay un nombre localizado disponible. Para otros elementos, este es el equivalente fácil de usar, suponiendo que el elemento existe en el almacenamiento jerárquico.

A [diferencia de System.ItemUrl](./props-system-itemurl.md), este valor de propiedad no incluye el esquema de dirección URL. Para analizar una ruta de acceso de elemento, use System.ItemUrl o [System.ParsingPath](./props-system-parsingpath.md). Para hacer referencia a elementos de espacio de nombres de Shell mediante las API de Shell, use System.ParsingPath.

Valores de ejemplo:



| Ruta de acceso                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\ barra de mydir \\ \\hello.txt              | c: \\ barra de mydir \\ \\hello.txt              |
| \\\\servidor \\ compartido \\ mydir \\goodnews.doc | \\\\servidor \\ compartido \\ mydir \\goodnews.doc |
| \\\\servidor \\ compartidonumbers.xls \\         | \\\\servidor \\ compartidonumbers.xls \\         |
| c: \\ mydir \\ MyFolder                    | c: \\ mydir \\ MyFolder                    |
| /Mailbox Account/Inbox/'Re: Hello!'    | /Mailbox Account/Inbox/'Re: Hello!'    |



 

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

 

 
