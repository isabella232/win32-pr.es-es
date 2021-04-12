---
title: Entrada y salida de cinta
description: Hay varias funciones que las aplicaciones pueden usar para realizar operaciones de entrada y salida (e/s) en una unidad de cinta. La e/s de cinta es similar a la e/s realizada en un dispositivo de comunicaciones.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- Copia de seguridad de entrada y salida de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5946659f1ad0246e37981201e4e08611b45b70b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359228"
---
# <a name="tape-input-and-output"></a>Entrada y salida de cinta

Hay varias funciones que las aplicaciones pueden usar para realizar operaciones de entrada y salida (e/s) en una unidad de cinta. La e/s de cinta es similar a la e/s realizada en un dispositivo de comunicaciones.

Al realizar la e/s de cinta, algunas unidades de cinta almacenan información de firmware de cinta en los primeros bloques de una cinta, normalmente con una parte de los primeros 100 bloques. Las aplicaciones no deben usar estos bloques. La información más específica sobre este tema está disponible para los fabricantes de sistemas de cintas individuales. En general, una aplicación que omite los primeros 100 bloques de una cinta evitará la idiosincrasia de la unidad de cinta.

Las funciones [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) y [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) recuperan y mueven la posición de la cinta actual. La función [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) escribe un número especificado de setmarks, filemarks, Short filemarks y Long filemarks. La función [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape) borra todo o parte de una cinta.

Las funciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) leen y escriben datos de archivo desde y hacia la cinta. Los datos se leen y se escriben en bloques completos. Si el tamaño de bloque de la cinta es de 512 bytes, todas las operaciones de lectura y escritura deben usar búferes que sean múltiplos de entero sencillos de ese tamaño de bloque: 512, 1024, 1536, 2048, etc. La mayoría de las unidades, si no todas, solo permiten una operación de escritura después de rebobinar la cinta o después de que una operación de lectura genere un mensaje de error de final de datos.

Para leer o escribir datos de archivo en o desde una cinta en modo de bloque de longitud variable, realice los pasos siguientes:

1.  Determine si la unidad de cinta admite el modo de bloqueo de longitud variable mediante una llamada a la función [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) y compruebe el \_ \_ \_ bit de bloque de variable de la unidad de cinta del miembro **FeaturesLow** de la estructura de parámetros de [**unidad de cinta \_ Get \_ \_**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) devuelta.
2.  Especifique el modo de tamaño de bloque de variables mediante una llamada a la función [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) , estableciendo el miembro **blocksize** de la estructura de parámetros de medios del conjunto de cintas en cero. [**\_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) A continuación, use [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para leer o escribir los datos del archivo.

Si [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) encuentra una marca de acción, se leen los datos hasta la marca de registro y se produce un error en la función. (La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un código de error que indica el tipo de marca de código que se encontró). El sistema operativo mueve la cinta más allá de la marca de desplazamiento y una aplicación puede volver a llamar a **readfile** para seguir leyendo.

[**Readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) leen y escriben solo el flujo de datos. Las funciones [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) y [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) leen y escriben todas las secuencias asociadas a un archivo. Entre ellos se incluyen datos, atributos extendidos, seguridad y flujos de datos alternativos. La seguridad y los flujos de datos alternativos solo son relevantes en la partición del sistema de archivos NTFS.

La función [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek) busca hacia delante en un archivo al que tiene acceso inicialmente [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) o [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite). Esta función permite a una aplicación omitir la información que produce errores de acceso.

Si una aplicación necesita acceder únicamente a los datos del archivo, debe usar [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Estas funciones también pueden leer flujos de datos alternativos si las secuencias se crearon con la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

Una aplicación de copia de seguridad en cinta debe usar [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) y [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) para copiar toda la información relativa a un archivo. Sin embargo, estas funciones no leen ni escriben características de archivos como atributos, tiempo de creación de archivos, etc. Las aplicaciones deben usar las funciones de entrada y salida de archivo, como [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) y [**SetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa), para recuperar y establecer esos valores.

 

 