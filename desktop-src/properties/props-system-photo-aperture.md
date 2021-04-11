---
description: El valor de apertura de la imagen, en unidades de APEX.
ms.assetid: ec8c0271-1e1e-4d37-a09a-f430d0682213
title: System. Photo. abertura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2273425c1974617b7d76657f818c4f1c39cd3aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276568"
---
# <a name="systemphotoaperture"></a>System. Photo. abertura

El valor de apertura de la imagen, en unidades de APEX. Vea la especificación de archivo de imagen intercambiable (EXIF) 2,2, anexo C, para obtener una comparación de los números de [System. Photo. de apertura]() y los valores [System. Photo. FNumber](./props-system-photo-fnumber.md) . Esta propiedad se calcula a partir de [System. Photo. ApertureNumerator](./props-system-photo-aperturenumerator.md) y [System. Photo. ApertureDenominator](./props-system-photo-aperturedenominator.md).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Exchangeable Image File Format para las cámaras digitales fijas: versión Exif 2,2](https://www.exif.org/Exif2-2.PDF)
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

 

 
