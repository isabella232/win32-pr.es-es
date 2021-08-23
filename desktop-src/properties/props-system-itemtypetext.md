---
description: Nombre de tipo descriptivo del elemento.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System.ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f145aa2491f3352c4691be95c0e8ae16a75e8e0880732904e983fbf02c167dbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553755"
---
# <a name="systemitemtypetext"></a>System.ItemTypeText

Nombre de tipo descriptivo del elemento. Este valor no está pensado para analizarse mediante programación.

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

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

Si [System.ItemType](./props-system-itemtype.md) es VT \_ EMPTY, el valor de esta propiedad también es VT \_ EMPTY. Si el elemento es un archivo, el valor de esta propiedad es el mismo que si pasara el valor System.ItemType del archivo a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).

Esta propiedad no debe confundirse con [System.Kind,](./props-system-kind.md)que es un nombre de tipo descriptivo de alto nivel. Por ejemplo, para un .doc de documento, las distintas propiedades son las que se muestran aquí:



| Propiedad                                               | Valor                   |
|--------------------------------------------------------|-------------------------|
| [System.Kind](./props-system-kind.md)                 | Documento                |
| [System.ItemType](./props-system-itemtype.md)         | .doc                    |
| [System.ItemTypeText]() | Microsoft Word Documento |



 

Valores de ejemplo:



| Ruta de acceso                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c: \\ mydir \\ bar \\hello.txt              | Archivo de texto               |
| \\\\servidor \\ compartido \\ mydir \\goodnews.doc | Microsoft Word Documento |
| \\\\carpeta de \\ recurso compartido de \\ servidor              | Carpeta de archivos             |
| c: \\ MyDir \\ MyFolder                    | Carpeta de archivos             |
| /Mailbox Account/Inbox/'Re: Hello!'    | Outlook Mensaje de correo electrónico  |



 

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

 

 
