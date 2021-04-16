---
description: Un elemento contenedor emite como TRUE para indicar que no es necesario que un indexador Enumere sus elementos secundarios si el elemento contenedor no ha cambiado desde el último rastreo de comprobación de Índice incremental.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720684"
---
# <a name="systemsearchiscloseddirectory"></a>System. Search. IsClosedDirectory

Un elemento contenedor emite como **true** para indicar que no es necesario que un indexador Enumere sus elementos secundarios si el elemento contenedor no ha cambiado desde el último rastreo de comprobación de Índice incremental. Esto contribuye a la optimización del rendimiento del indexador. En estos casos de contenedor (los ejemplos son un correo electrónico con datos adjuntos o un archivo comprimido con la extensión. zip), los elementos secundarios son inseparables de su elemento primario. Por ejemplo, si la propiedad [System. DateModified](./props-system-datemodified.md) de un elemento contenido cambia, el valor System. DateModified del contenedor cambia para coincidir. Además, si se elimina un elemento primario, se eliminan también todos los elementos secundarios. Por lo tanto, si el contenedor no ha cambiado, el indizador sabe que no ha cambiado nada y no necesita abrir el contenedor para examinar el contenido de forma individual.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

> [!IMPORTANT]
> Si un elemento emite **true** para esta propiedad, cada uno de sus elementos secundarios debe emitir la propiedad [System. Search. IsFullyContained](./props-system-search-isfullycontained.md) como **true** para evitar que estos elementos se eliminen del índice.

 

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

 

 
