---
description: Emitido por un IFilter de contenedor para cada dirección URL secundaria dentro del contenedor. Finalmente, el indexador rastrea los elementos secundarios si están dentro del ámbito.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. Search. UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716230"
---
# <a name="systemsearchurltoindex"></a>System. Search. UrlToIndex

Emitido por un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de contenedor para cada dirección URL secundaria dentro del contenedor. Finalmente, el indexador rastrea los elementos secundarios si están dentro del ámbito.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a>Observaciones

Esta propiedad contiene una dirección URL y se emite mediante un controlador de protocolo para cada dirección URL secundaria o directo en la dirección URL actual. El indexador vuelve a llamar al controlador de protocolo y pide que se indexe el documento. [System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) se llamó PID \_ GTHR \_ DIRLINK en versiones anteriores del sistema operativo Windows.

Los valores PKEY se definen en Propkey. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Search. UrlToIndexWithModificationTime](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

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

 

 
