---
description: Fecha de adquisición del archivo o medio.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System.DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a78ae9ccfe938551ab6c4a265972e48c3aad1c1791f02cfa933c583c6d4b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599185"
---
# <a name="systemdateacquired"></a>System.DateAcquired

Fecha de adquisición del archivo o medio. Esta propiedad está relacionada con un determinado usuario o grupo de usuarios. Por ejemplo, estos datos se usan como eje de ordenación principal para la carpeta virtual **New Música**, que permite a los usuarios examinar las adiciones más recientes a su colección.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

[DateAcquired]() se almacena como un valor en la secuencia principal del archivo, pero puede que no siempre esté presente. En esos casos, la fecha de adquisición se puede aproximar en función de otras fechas conocidas del contenido. El controlador de metadatos debe usar un conjunto de reglas para determinar la fecha que se devolverá. En el ejemplo siguiente se muestra esto para los archivos de música.

-   En el caso de la música comprada, se debe usar la hora de creación del archivo si no hay ninguna fecha adquirida. Sin embargo, el proveedor de descarga debe establecer la [propiedad DateAcquired]() en el archivo .
-   En el caso de los archivos de música que el usuario o grupo "arrasó" (copiando música o vídeo de un CD o DVD a un disco duro), la fecha de adquisición debe ser la fecha en que se produjo la acción. Por ejemplo, el [atributo WM/EncodingTime.](../wmp/wm-encodingtime-attribute.md)
-   En el caso de la música copiada desde otra ubicación, la hora de creación del archivo debe usarse como fecha de adquisición.

Algunos ejemplos [de System.DateAcquired]() son la fecha y hora en que se adquieren imágenes de una cámara o cuándo se compra música en línea. Esto no es lo mismo que [System.DateImported.](./props-system-dateimported.md)

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

 

 
