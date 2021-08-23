---
title: Entrada y salida de cinta
description: Hay varias funciones que las aplicaciones pueden usar para realizar entradas y salidas (E/S) en una unidad de cinta. La E/S de cinta es similar a la E/S realizada en un dispositivo de comunicaciones.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- copia de seguridad de entrada y salida de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281eb6104cb71fbd5e7f0b3d9072cefe562ac7b9cc54e05ede53bece8755178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021282"
---
# <a name="tape-input-and-output"></a>Entrada y salida de cinta

Hay varias funciones que las aplicaciones pueden usar para realizar entradas y salidas (E/S) en una unidad de cinta. La E/S de cinta es similar a la E/S realizada en un dispositivo de comunicaciones.

Al realizar E/S de cinta, algunas unidades de cinta almacenan información de firmware de cinta en los primeros bloques de una cinta, normalmente con alguna parte de los primeros 100 bloques. Las aplicaciones no deben usar esos bloques. Hay información más específica sobre este tema disponible de fabricantes de sistemas de cinta individuales. En general, una aplicación que omite los primeros 100 bloques de una cinta evitará la idiosincrasia de la unidad de cinta.

Las [**funciones GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) [**y SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) recuperan y mueven la posición de cinta actual. La [**función WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) escribe un número especificado de marcas de conjunto, marcas de archivo, marcas de archivo cortas y marcas de archivo largas. La [**función EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape) borra todo o parte de una cinta.

Las [**funciones ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) leen y escriben datos de archivo desde y en la cinta. Los datos se leen y escriben en bloques completos. Si el tamaño de bloque de la cinta es de 512 bytes, todas las operaciones de lectura y escritura deben usar búferes que sean múltiplo entero simple de ese tamaño de bloque: 512, 1024, 1536, 2048, y así sucesivamente. La mayoría, si no todas, las unidades solo permiten una operación de escritura después de que se vuelva a generar la cinta o después de que una operación de lectura produzca un mensaje de error de fin de datos.

Para leer o escribir datos de archivo en o desde una cinta en modo de bloque de longitud variable, realice los pasos siguientes:

1.  Determine si la unidad de cinta admite el modo de bloque de longitud variable llamando a la función [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) y comprobando el bit TAPE DRIVE VARIABLE BLOCK del miembro FeaturesLow de la estructura \_ TAPE GET DRIVE \_ \_ [**\_ \_ \_ PARAMETERS**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) devuelta. 
2.  Especifique el modo de tamaño de bloque variable llamando a la función [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) y estableciendo el miembro **BlockSize** de la estructura [**TAPE SET MEDIA \_ \_ \_ PARAMETERS**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) en cero. A continuación, [**use ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para leer o escribir los datos del archivo.

Si [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) encuentra una marca de archivo, se leen los datos hasta la marca de archivo y se produce un error en la función. (La [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un código de error que indica el tipo de marca de archivo que se encontró). El sistema operativo mueve la cinta más allá de la marca de archivo y una aplicación puede llamar a **ReadFile** de nuevo para continuar con la lectura.

[**ReadFile y**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile solo**](/windows/desktop/api/fileapi/nf-fileapi-writefile) leen y escriben el flujo de datos. Las [**funciones BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) [**y BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) leen y escriben todas las secuencias asociadas a un archivo. Estos incluyen datos, atributos extendidos, seguridad y flujos de datos alternativos. La seguridad y los flujos de datos alternativos solo son relevantes en la partición del sistema de archivos NTFS.

La [**función BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek) busca hacia delante en un archivo al que Accede inicialmente [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) o [**BackupWrite.**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) Esta función permite a una aplicación omitir la información que provoca errores de acceso.

Si una aplicación solo necesita acceder a los datos de archivo, debe usar [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Estas funciones también pueden leer secuencias de datos alternativas si las secuencias se crearon mediante la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

Una aplicación de copia de seguridad en cinta debe [**usar BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) y [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) para copiar toda la información relativa a un archivo. Sin embargo, estas funciones no leen ni escriben características de archivo como atributos, tiempo de creación de archivos, entre otras. Las aplicaciones deben usar las funciones de entrada y salida de archivo, como [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) y [**SetFileAttributes,**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa)para recuperar y establecer esos valores.

 

 