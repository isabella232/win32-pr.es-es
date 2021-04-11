---
description: Nombre de tipo descriptivo del elemento.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276585"
---
# <a name="systemitemtypetext"></a>System. ItemTypeText

Nombre de tipo descriptivo del elemento. Este valor no se ha diseñado para analizarse mediante programación.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Si [System. ItemType](./props-system-itemtype.md) es VT \_ vacío, el valor de esta propiedad también es VT \_ vacío. Si el elemento es un archivo, el valor de esta propiedad es el mismo que si se pasa el valor System. ItemType del archivo a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).

Esta propiedad no se debe confundir con [System. Kind](./props-system-kind.md), que es un nombre de clase de alto nivel fácil de usar. Por ejemplo, para un archivo de documento. doc, las distintas propiedades se muestran a continuación:



| Propiedad                                               | Value                   |
|--------------------------------------------------------|-------------------------|
| [System. Kind](./props-system-kind.md)                 | Documento                |
| [System. ItemType](./props-system-itemtype.md)         | .doc                    |
| [System. ItemTypeText]() | Documento de Microsoft Word |



 

Valores de ejemplo:



| Ruta                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c: \\hello.txt de la \\ barra myDir \\              | Archivo de texto               |
| \\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\ | Documento de Microsoft Word |
| \\\\\\carpeta de recurso compartido de servidor \\              | Carpeta de archivos             |
| c: \\ MyDir \\ carpeta                    | Carpeta de archivos             |
| Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '    | Mensaje de correo electrónico de Outlook  |



 

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

 

 
