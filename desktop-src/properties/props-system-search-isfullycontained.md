---
description: Emitido como TRUE por todos los elementos secundarios de un contenedor (por ejemplo, un correo electrónico o un archivo comprimido con una extensión de nombre .zip) que emite System.Search.IsClosedDirectory como TRUE. Esto garantiza que los elementos secundarios se incluyen en el índice de búsqueda.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System.Search.IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce7f325be26abdb81dcb51da7018f6da786e6ec5f3a31111e4ae3823acf8c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864994"
---
# <a name="systemsearchisfullycontained"></a>System.Search.IsFullyContained

Emitido como **TRUE por** todos los elementos secundarios de un contenedor (por ejemplo, un correo electrónico o un archivo comprimido con una extensión de nombre .zip) que emite [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) como **TRUE.** Esto garantiza que los elementos secundarios se incluyen en el índice de búsqueda.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

La [propiedad System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) ayuda a optimizar el rendimiento del indexador al permitir que el indexador omita la enumeración de los elementos secundarios de un contenedor. Sin embargo, esos elementos secundarios están marcados por el indexador como no visitados y, como tal, se eliminarán del índice. Al emitir [System.Search.IsFullyContained]() como **TRUE,** un elemento no se elimina del índice a pesar de no haber sido visitado.

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

 

 
