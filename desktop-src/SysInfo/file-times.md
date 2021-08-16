---
description: Un tiempo de archivo es un valor de 64 bits que representa el número de intervalos de 100 nanosegundos que han transcurrido desde las 12:00 a.m. 1 de enero de 1601 Hora universal coordinada (UTC). El sistema registra las horas de archivo cuando las aplicaciones crean, acceden y escriben en archivos.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Horas de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1492597b4e71775974ed8b19f6109c5900a8a28720b769c1c10dcf2f70166b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764499"
---
# <a name="file-times"></a>Horas de archivo

Un *tiempo de archivo* es un valor de 64 bits que representa el número de intervalos de 100 nanosegundos que han transcurrido desde las 12:00 a.m. 1 de enero de 1601 Hora universal coordinada (UTC). El sistema registra las horas de archivo cuando las aplicaciones crean, acceden y escriben en archivos.

El sistema de archivos NTFS almacena los valores de hora en formato UTC, por lo que no se ven afectados por cambios en la zona horaria ni en el horario de verano. El sistema de archivos FAT almacena valores de hora en función de la hora local del equipo. Por ejemplo, un archivo que se guarda a las 3:00 p. m. PST en Washington se ve como 6:00 p. m. EST en Nueva York en un volumen NTFS, pero se ve como 3:00 p.m. EST en Nueva York en un volumen FAT.

Las marcas de tiempo se actualizan en varias ocasiones y por diversos motivos. La única garantía sobre una marca de tiempo de archivo es que la hora del archivo se refleja correctamente cuando se cierra el identificador que realiza el cambio.

No todos los sistemas de archivos pueden registrar los tiempos de creación y de último acceso, y no todos los sistemas de archivos los registran de la misma manera. Por ejemplo, la resolución del tiempo de creación en FAT es de 10 milisegundos, mientras que el tiempo de escritura tiene una resolución de 2 segundos y el tiempo de acceso tiene una resolución de 1 día, por lo que es realmente la fecha de acceso. El sistema de archivos NTFS retrasa las actualizaciones a la hora de último acceso de un archivo hasta una hora después del último acceso.

Para recuperar las horas de archivo de un archivo especificado, use la [**función GetFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) **GetFileTime copia** los tiempos de creación, último acceso y última escritura en estructuras [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) individuales. También puede recuperar tiempos de archivo mediante las [**funciones FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) [**y FindNextFile.**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) Estas funciones copian las horas de archivo **en estructuras FILETIME** en una [**estructura FIND DATA \_ \_ de WIN32.**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Al escribir en un archivo, la hora de la última escritura no se actualiza por completo hasta que se cierran todos los identificadores que se usan para escribir.

Para establecer las horas de archivo de un archivo, use la [**función SetFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) Esta función permite modificar la creación, el último acceso y las últimas horas de escritura sin cambiar el contenido del archivo. Puede comparar las horas de distintos archivos mediante la [**función CompareFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) La función compara dos veces el archivo y devuelve un valor que indica qué hora es posterior o devuelve 0 (cero) si las horas son iguales.

Si tiene previsto modificar las horas de archivo de los archivos especificados, puede convertir una fecha y hora del día en una hora de archivo mediante la [**función SystemTimeToFileTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) También puede obtener la hora del sistema en una [**estructura FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) llamando a la [**función GetSystemTimeAsFileTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime)

Para facilitar la presentación de un archivo a un usuario, use la [**función FileTimeToSystemTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) **FileTimeToSystemTime convierte** la hora del archivo y copia el mes, el día, el año y la hora del día de la hora del archivo a una [**estructura SYSTEMTIME.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

## <a name="file-times-and-daylight-saving-time"></a>Horas de archivo y horario de verano

Debe tener cuidado al usar horas de archivo si el usuario ha establecido el sistema para ajustarse automáticamente al horario de verano.

Para convertir una hora de archivo a la hora local, use la [**función FileTimeToLocalFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) Sin embargo, **FileTimeToLocalFileTime usa** la configuración actual para la zona horaria y el horario de verano. Por lo tanto, si es el horario de verano, se tiene en cuenta el horario de verano, incluso si el tiempo de archivo que se va a convertir está en hora estándar.

El sistema de archivos FAT registra las horas en disco en la hora local. [**GetFileTime recupera**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) las horas UTC almacenadas en caché del sistema de archivos FAT. Cuando se convierte en horario de verano, el tiempo recuperado por **GetFileTime** es de una hora, porque la memoria caché no se actualiza. Al reiniciar el equipo, la hora almacenada en caché que **GetFileTime** recupera es correcta. [**FindFirstFile recupera**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) la hora local del sistema de archivos FAT y la convierte a UTC mediante la configuración actual de la zona horaria y el horario de verano. Por lo tanto, si se trata del horario de verano, **FindFirstFile** tiene en cuenta el horario de verano, incluso si el tiempo de archivo que va a convertir está en hora estándar.

El sistema de archivos NTFS registra las horas en disco en formato UTC. Para tener en cuenta el horario de verano al convertir una hora de archivo a una hora local, use la siguiente secuencia de funciones en lugar de [**usar FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime):

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Tiempos de archivo y CDFS

Las marcas de fecha y hora de los archivos que se encuentran en los medios o se originan en ellos mediante el Sistema de archivos de disco compacto (CDFS) se ajustan para la zona horaria local. ISO 9660 indica que CDFS debe mostrar la información de fecha correctamente para la zona horaria local. Esto se hace para que las fechas de los archivos en CDFS se muestren igual que las de formato de disco universal (UDF). UDF es el estándar más reciente para los medios de distribución. Si el código depende de la información de fecha sin modificar de un archivo que reside o se origina en medios mediante CDFS, es posible que no funcione correctamente.

 

 
