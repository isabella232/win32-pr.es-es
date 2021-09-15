---
description: Tipo canónico del elemento.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System.ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784a72c46e92ac5956532994df4f36758d42f440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570452"
---
# <a name="systemitemtype"></a>System.ItemType

Tipo canónico del elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey.h.

El valor de System.ItemType está pensado para analizarse mediante programación y puede ser:

-   Extensión de archivo que apunta a un valor ProgID (HKEY \_ CLASSES \_ ROOT \\ &lt; ProgID) &gt; que mantiene el nombre para mostrar del tipo.
-   Valor progID (HKEY \_ CLASSES \_ RROOT \\ &lt; &gt; ProgID), que contiene el nombre para mostrar del tipo.

El elemento FriendlyTypeName de un ProgID debe ser una versión localizada del nombre de la aplicación ( ,-42), mientras que el valor predeterminado de la clave ProgID es un nombre no localizado @winword.dll (Word.Document.12).

Si no hay ningún tipo canónico, el valor es VT \_ EMPTY. Si el elemento es un archivo ([System.FileName](./props-system-filename.md) no es VT EMPTY), el valor es el mismo \_ que [System.FileExtension.](./props-system-fileextension.md) Use [System.ItemTypeText](./props-system-itemtypetext.md) cuando desee mostrar el tipo a los usuarios finales en una vista.

> [!Note]  
> Si el elemento es un archivo, pasar el valor [System.ItemType]() a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) da como resultado el mismo valor que [System.ItemTypeText](./props-system-itemtypetext.md).

 

Valores de ejemplo:



| Path                                   | ItemType         |
|----------------------------------------|------------------|
| c: \\ barra de mydir \\ \\hello.txt              | .txt             |
| \\\\servidor \\ compartido \\ mydir \\goodnews.doc | .doc             |
| \\\\carpeta de \\ recurso compartido de \\ servidor              | Directorio        |
| c: \\ MyDir \\ MyFolder                    | Directorio        |
| \[desktop\]                            | Carpeta           |
| /Mailbox Account/Inbox/'Re: Hello!'    | MAPI/IPM. Mensaje |



 

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
</dt> <dt>

[Identificadores mediante programación](../shell/fa-progids.md)
</dt> </dl>

 

 
