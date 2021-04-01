---
description: Una hora de archivo es un valor de 64 bits que representa el número de intervalos de 100 segundos que han transcurrido desde la 12:00 A.M. 1 de enero de 1601 hora universal coordinada (UTC). El sistema registra los tiempos de archivo cuando las aplicaciones crean, acceden y escriben en los archivos.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Horas de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5919a2378e08798e4cd64d8f8357cb55692bd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913838"
---
# <a name="file-times"></a>Horas de archivo

Una *hora de archivo* es un valor de 64 bits que representa el número de intervalos de 100 segundos que han transcurrido desde la 12:00 A.M. 1 de enero de 1601 hora universal coordinada (UTC). El sistema registra los tiempos de archivo cuando las aplicaciones crean, acceden y escriben en los archivos.

El sistema de archivos NTFS almacena los valores de hora en formato UTC, por lo que no se ven afectados por los cambios en la zona horaria o el horario de verano. El sistema de archivos FAT almacena valores de hora basados en la hora local del equipo. Por ejemplo, un archivo que se guarda en 3: p.m. PST en Washington se considera 6: p.m. EST en Nueva York en un volumen NTFS, pero se considera 3: p.m. EST en Nueva York en un volumen FAT.

Las marcas de tiempo se actualizan en varias ocasiones y por varias razones. La única garantía de una marca de tiempo de archivo es que la hora del archivo se refleja correctamente cuando se cierra el identificador que hace el cambio.

No todos los sistemas de archivos pueden registrar los tiempos de creación y último acceso, y no todos los sistemas de archivos los registran de la misma manera. Por ejemplo, la resolución de la hora de creación en FAT es de 10 milisegundos, mientras que el tiempo de escritura tiene una resolución de 2 segundos y el tiempo de acceso tiene una resolución de 1 día, por lo que es realmente la fecha de acceso. El sistema de archivos NTFS retrasa las actualizaciones de la última hora de acceso de un archivo hasta 1 hora después del último acceso.

Para recuperar los tiempos de archivo de un archivo especificado, utilice la función [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) . **GetFileTime** copia las horas de creación, último acceso y última escritura en estructuras [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) individuales. También puede recuperar los tiempos de archivo mediante las funciones [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) . Estas funciones copian las horas de archivo en estructuras **FILETIME** en una estructura de [**datos de \_ búsqueda \_ de Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Al escribir en un archivo, la hora de la última escritura no se actualiza completamente hasta que se cierran todos los identificadores que se usan para escribir.

Para establecer las horas de archivo de un archivo, use la función [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) . Esta función le permite modificar la creación, el último acceso y las horas de última escritura sin cambiar el contenido del archivo. Puede comparar las horas de archivos diferentes mediante la función [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) . La función compara dos horas de archivo y devuelve un valor que indica qué hora es posterior o devuelve 0 (cero) si las horas son iguales.

Si tiene previsto modificar las horas de archivo de los archivos especificados, puede convertir una fecha y hora del día a una hora de archivo mediante la función [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) . También puede obtener la hora del sistema en una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) llamando a la función [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) .

Para facilitar la visualización a un usuario de un archivo, use la función [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) . **FileTimeToSystemTime** convierte la hora de archivo y copia el mes, el día, el año y la hora del día desde la hora del archivo a una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

## <a name="file-times-and-daylight-saving-time"></a>Horas de archivo y horario de verano

Debe tener cuidado al usar los tiempos de archivo si el usuario ha configurado el sistema para que se ajuste automáticamente al horario de verano.

Para convertir una hora de archivo en hora local, utilice la función [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) . Sin embargo, **FileTimeToLocalFileTime** usa la configuración actual para la zona horaria y el horario de verano. Por lo tanto, si es el horario de verano, se tarda en cuenta el horario de verano, incluso si la hora de archivo que está convirtiendo está en el horario estándar.

El sistema de archivos FAT registra las horas en el disco en la hora local. [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) recupera las horas UTC almacenadas en caché del sistema de archivos FAT. Cuando se convierte en el horario de verano, el tiempo recuperado por **GetFileTime** está fuera de una hora, ya que la memoria caché no se actualiza. Al reiniciar el equipo, el tiempo almacenado en caché que **GetFileTime** recupera es correcto. [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) recupera la hora local del sistema de archivos FAT y la convierte a UTC mediante la configuración actual de la zona horaria y el horario de verano. Por lo tanto, si es el horario de verano, **FindFirstFile** tarda en cuenta el horario de verano, incluso si la hora de archivo que está convirtiendo está en el horario estándar.

El sistema de archivos NTFS registra las horas en el disco en UTC. Para tener en cuenta el horario de verano al convertir una hora de archivo en una hora local, use la siguiente secuencia de funciones en lugar de usar [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime):

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Tiempos de archivo y CDFS

Las marcas de fecha y hora de los archivos que se encuentran en el archivo o que se originan desde el medio mediante el sistema de archivos de disco compacto (CDFS) se ajustan a la zona horaria local. ISO 9660 indica que CDFS debe mostrar la información de fecha correctamente para la zona horaria local. Esto se hace para que las fechas de los archivos en CDFS se muestren igual que en el formato de disco universal (UDF). UDF es el estándar más reciente para medios de distribución. Si el código depende de la información de fecha sin modificar de un archivo que reside o se origina desde un medio mediante CDFS, puede que no funcione correctamente.

 

 
