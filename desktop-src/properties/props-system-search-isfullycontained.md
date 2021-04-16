---
description: Lo emiten todos los elementos secundarios de un contenedor (por ejemplo, un correo electrónico o un archivo comprimido con la extensión de nombre. zip) que emite System. Search. IsClosedDirectory como TRUE. Esto garantiza que los elementos secundarios se incluyen en el índice de búsqueda.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546758"
---
# <a name="systemsearchisfullycontained"></a>System. Search. IsFullyContained

**Lo** emiten todos los elementos secundarios de un contenedor (por ejemplo, un correo electrónico o un archivo comprimido con la extensión de nombre. zip) que emite [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) como **true**. Esto garantiza que los elementos secundarios se incluyen en el índice de búsqueda.

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

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

La propiedad [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) ayuda a optimizar el rendimiento del indexador permitiendo al indizador omitir la enumeración de los elementos secundarios de un contenedor. Sin embargo, los elementos secundarios están marcados por el indexador como no visitados y, como tal, se eliminarán del índice. Al emitir [System. Search. IsFullyContained]() como **true**, no se elimina un elemento del índice a pesar de que no se ha visitado.

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

 

 
