---
description: Indica la latitud.
ms.assetid: f36f81b3-4e3d-4e06-a039-c243fd69c937
title: System.GPS.Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4895e09a20c2a13aa1a6b003289d61d6802ef164b47c8cca63a5e45a5cacbcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091215"
---
# <a name="systemgpslatitude"></a>System.GPS.Latitude

Indica la latitud. Se trata de una matriz de tres valores, como se muestra a continuación: el índice 0 es el grado, el índice 1 son los minutos, el índice 2 son los segundos. Cada uno se calcula a partir de los valores de PKEY \_ GPS \_ LatitudeNumerator y PKEY \_ GPS \_ LatitudeDenominator.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.GPS.Latitude
   shellPKey = PKEY_GPS_Latitude
   formatID = 8727CFFF-4868-4EC6-AD5B-81B98521D1AB
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a>Windows 7, Windows Vista

```
propertyDescription
   name = System.GPS.Latitude
   shellPKey = PKEY_GPS_Latitude
   formatID = 8727CFFF-4868-4EC6-AD5B-81B98521D1AB
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

El requisito de una referencia de cadena indirecta específica para el atributo de labelInfo se agregó para Windows Vista con `label` Service Pack 1 (SP1). 

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

 

 
