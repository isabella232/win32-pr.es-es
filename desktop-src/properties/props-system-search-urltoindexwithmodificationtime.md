---
description: Esta propiedad es igual que System. Search. UrlToIndex, salvo que incluye la hora en que se modificó por última vez la dirección URL.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716730"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System. Search. UrlToIndexWithModificationTime

Esta propiedad es igual que [**System. Search. UrlToIndex**](props-system-search-urltoindex.md) , salvo que incluye la hora en que se modificó por última vez la dirección URL. Se trata de una optimización para el indizador, de modo que no tenga que volver a llamar al controlador de protocolo para solicitar esta información para determinar si es necesario indizar el contenido de nuevo.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a>Observaciones

Esta propiedad [System. Search. UrlToIndexWithModificationTime]() es la misma que la propiedad [System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , salvo que también se pasa la hora de la última modificación del documento. Si la hora de la última modificación coincide, el indexador supone que el documento ya está indexado y que sale de la notificación. Esta propiedad es un vector con dos elementos, un valor de **VT \_ LPWStr** que contiene la dirección URL y un valor **\_ FILETIME de VT** que contiene la hora de la última modificación.

[System. Search. UrlToIndexWithModificationTime]() se llamaba PID \_ GTHR \_ DIRLINK \_ con \_ hora en versiones anteriores del sistema operativo Windows.

Los valores PKEY se definen en Propkey. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
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

 

 
