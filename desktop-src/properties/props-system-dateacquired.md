---
description: Fecha de adquisición del archivo o medio.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278893"
---
# <a name="systemdateacquired"></a>System. DateAcquired

Fecha de adquisición del archivo o medio. Esta propiedad está relacionada con un usuario o grupo de usuarios determinado. Por ejemplo, estos datos se usan como el eje principal de ordenación de la carpeta virtual **New Music**, que permite a los usuarios examinar las adiciones más recientes a su colección.

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

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

[DateAcquired]() se almacena como un valor en la secuencia principal del archivo, pero es posible que no siempre esté presente. En esos casos, la fecha de adquisición se puede aproximar en función de otras fechas conocidas para el contenido. El controlador de metadatos debe utilizar un conjunto de reglas para determinar la fecha que se va a devolver. En el ejemplo siguiente se muestra esto para los archivos de música.

-   En el caso de la música comprada, se debe usar la hora de creación del archivo si no hay ninguna fecha adquirida. Sin embargo, el proveedor de descargas debe establecer la propiedad [DateAcquired]() en el archivo.
-   En el caso de los archivos de música que el usuario o el grupo "copió" (copiando música o vídeo desde un CD o DVD a un disco duro), la fecha de adquisición debe ser la fecha en que tuvo lugar la acción. Por ejemplo, el atributo [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) .
-   En el caso de la música copiada desde otra ubicación, la hora de creación del archivo debe usarse como la fecha de adquisición.

Algunos ejemplos de [System. DateAcquired]() son la fecha y la hora en que se adquieren imágenes de una cámara o cuando la música se adquiere en línea. No es lo mismo que [System. DateImported](./props-system-dateimported.md).

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

 

 
