---
description: Obtenga información sobre la propiedad System.ItemFolderPathDisplay, que representa la ruta de acceso de presentación fácil de usar de la carpeta primaria de un elemento.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System.ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12909b29790ea2c016154cea9fccf7c53e45630
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570461"
---
# <a name="systemitemfolderpathdisplay"></a>System.ItemFolderPathDisplay

Ruta de acceso para mostrar fácil de usar de la carpeta primaria de un elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey.h.

Si [System.ItemPathDisplay es](./props-system-itempathdisplay.md) VT \_ EMPTY, esta propiedad también debe estar vacía. De lo contrario, el origen de datos debe derivarlo correctamente de System.ItemPathDisplay.

Valores de ejemplo:



| Path                                   | ItemFolderPathDisplay    |
|----------------------------------------|--------------------------|
| c: \\ archivos personales \\ \\hello.txt         | c: \\ archivos \\ personales      |
| \\\\servidor \\ compartido \\ mydir \\goodnews.doc | \\\\server \\ share \\ mydir |
| \\\\servidor \\ compartidonumbers.xls \\         | \\\\recurso \\ compartido de servidor        |
| c: \\ food \\ MyFolder                     | c: \\ comida                 |
| /Mailbox Account/Inbox/'Re: Hello!'    | /Cuenta de buzón/Bandeja de entrada   |



 

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

 

 
