---
description: Proporción de zoom digital cuando se rodó la imagen.
ms.assetid: 1164e2c9-0864-4520-a3be-0c29a5b70ba4
title: System.Photo.DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47f98b4ff65f541160804c41f0b6bcd0218d04514a079f39374b222e15013cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598321"
---
# <a name="systemphotodigitalzoom"></a>System.Photo.DigitalZoom

Proporción de zoom digital cuando se rodó la imagen. Lee de la cámara en la información de Archivo de imagen intercambiable (EXIF) del archivo. Esta propiedad se calcula a [partir de System.Photo.DigitalZoomNumerator](./props-system-photo-digitalzoomnumerator.md) y [System.Photo.DigitalZoomDenominator.](./props-system-photo-digitalzoomdenominator.md) Si el numerador del valor registrado es 0, no se usó un zoom digital.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Photo.DigitalZoom
   shellPKey = PKEY_Photo_DigitalZoom
   formatID = F85BF840-A925-4BC2-B0C4-8E36B598679E
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Exchangeable Image File Format para cámaras Digital Still: Exif versión 2.2](https://www.exif.org/Exif2-2.PDF)
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

 

 
