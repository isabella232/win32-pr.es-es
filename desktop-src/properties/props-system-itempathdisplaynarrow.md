---
description: Obtenga información sobre la propiedad System.ItemPathDisplayNarrow, que representa la ruta de acceso de presentación fácil de usar al elemento.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System.ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84455a8b69ebf42cb91c191d1c275b70eeeb5ac
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403898"
---
# <a name="systemitempathdisplaynarrow"></a>System.ItemPathDisplayNarrow

Ruta de acceso de presentación fácil de usar al elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey.h.

Para optimizar una columna de visualización estrecha, el formato de la cadena debe adaptarse para que el nombre sea el primero.

Si el elemento es un archivo, el valor de propiedad excluye la extensión de archivo, pero incluye nombres localizados si están presentes. Si el elemento es un mensaje, el valor incluye [System.ItemNamePrefix](./props-system-itemnameprefix.md). Para analizar una ruta de acceso de elemento, use [System.ItemUrl](./props-system-itemurl.md) o [System.ParsingPath](./props-system-parsingpath.md).

Valores de ejemplo:



| Ruta de acceso                                   | ItemPathDisplayName                 |
|----------------------------------------|-------------------------------------|
| c: \\ barra de mydir \\ \\hello.txt              | hello (c: \\ barra \\ mydir)              |
| \\\\servidor \\ compartido \\ mydir \\goodnews.doc | goodnews ( \\ \\ server share \\ \\ mydir) |
| \\\\carpeta de \\ recurso compartido \\ de servidor              | carpeta \\ \\ (recurso compartido \\ de servidor)          |
| c: \\ MyDir \\ MyFolder                    | MyFolder (c: \\ mydir)                |
| /Mailbox Account/Inbox/'Re: Hello!'    | Re: Hello! (/Cuenta de buzón/Bandeja de entrada) |



 

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

 

 
