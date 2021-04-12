---
description: Nombre para mostrar descriptivo de la carpeta primaria de un elemento.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277802"
---
# <a name="systemitemfoldernamedisplay"></a>System. ItemFolderNameDisplay

Nombre para mostrar descriptivo de la carpeta primaria de un elemento.

Se deriva de [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md). Si esa propiedad está vacía en VT \_ , esta propiedad también debe ser.

Si la carpeta es una carpeta de archivos, el valor se traducirá si está disponible un nombre traducido.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Si [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) es VT \_ vacío, esta propiedad también debe estar vacía. De lo contrario, el origen de datos debe derivar de la forma adecuada de System. ItemFolderPathDisplay.

Ejemplos:



| Ruta de acceso dada                             | Nombre para mostrar de la carpeta |
|----------------------------------------|---------------------|
| c: \\ archivo de \\ texto \\hello.txt           | Texto                |
| \\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\ | myDir               |
| \\\\\\numbers.xls de recurso compartido de servidor \\         | Compartir               |
| c: \\ carpetas \\ carpeta                  | Carpetas             |
| Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '    | Bandeja de entrada               |



 

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

 

 
