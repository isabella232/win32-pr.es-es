---
description: La ruta de acceso de visualización fácil de ver al elemento.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278326"
---
# <a name="systemitempathdisplaynarrow"></a>System. ItemPathDisplayNarrow

La ruta de acceso de visualización fácil de ver al elemento.

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

Los valores PKEY se definen en Propkey. h.

Para optimizar en una columna de visualización estrecha, el formato de la cadena debe estar adaptado para que el nombre aparezca primero.

Si el elemento es un archivo, el valor de la propiedad excluye la extensión de archivo, pero incluye nombres localizados si están presentes. Si el elemento es un mensaje, el valor incluye [System. ItemNamePrefix](./props-system-itemnameprefix.md). Para analizar una ruta de acceso de elemento, use [System. ItemUrl](./props-system-itemurl.md) o [System. ParsingPath](./props-system-parsingpath.md).

Valores de ejemplo:



| Ruta                                   | ItemPathDisplayName                 |
|----------------------------------------|-------------------------------------|
| c: \\hello.txt de la \\ barra myDir \\              | Hola (c: \\ myDir \\ bar)              |
| \\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\ | Goodnews ( \\ \\ \\ recurso compartido de servidor \\ myDir) |
| \\\\\\carpeta de recurso compartido de servidor \\              | carpeta ( \\ \\ \\ recurso compartido de servidor)          |
| c: \\ MyDir \\ carpeta                    | Carpeta (c: \\ myDir)                |
| Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '    | Re: ¡ Hola! (Cuenta o bandeja de entrada de/Mailbox) |



 

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

 

 
