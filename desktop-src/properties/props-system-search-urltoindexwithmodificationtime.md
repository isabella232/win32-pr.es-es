---
description: Esta propiedad es la misma que System.Search.UrlToIndex, salvo que incluye la hora en que la dirección URL se modificó por última vez.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System.Search.UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7869005084379db1bdf288c6237a420666634c349eee47ca7942af2bb271a39d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118464775"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System.Search.UrlToIndexWithModificationTime

Esta propiedad es la misma que [**System.Search.UrlToIndex,**](props-system-search-urltoindex.md) salvo que incluye la hora en que la dirección URL se modificó por última vez. Se trata de una optimización para el indexador, por lo que no tiene que volver a llamar al controlador de protocolos para solicitar esta información para determinar si es necesario volver a indexar el contenido.

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

## <a name="remarks"></a>Comentarios

Esta [propiedad System.Search.UrlToIndexWithModificationTime]() es la misma que la propiedad [System.Search.UrlToIndex,](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) excepto que también se pasa la hora de la última modificación del documento. Si la hora de la última modificación coincide, el indexador asume que el documento ya está indexado y genera la notificación. Esta propiedad es un vector con dos elementos, un valor **\_ LPWSTR de VT** que contiene la dirección URL y un valor **\_ FILETIME** de VT que contiene la hora de la última modificación.

[System.Search.UrlToIndexWithModificationTime]() se denominaba PID GTHR DIRLINK WITH TIME en versiones anteriores del \_ \_ Windows \_ \_ operativo.

Los valores PKEY se definen en Propkey.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
</dt> <dt>

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

 

 
