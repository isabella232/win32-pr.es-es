---
description: El primer paso para asignar un archivo es abrir el archivo llamando a la función CreateFile.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Crear un objeto de asignación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65badc2af8aed5211c2f5c590fc0998019dae264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360672"
---
# <a name="creating-a-file-mapping-object"></a>Crear un objeto de asignación de archivos

El primer paso para asignar un archivo es abrir el archivo llamando a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) . Para asegurarse de que otros procesos no pueden escribir en la parte del archivo que está asignada, debe abrir el archivo con acceso exclusivo. Además, el identificador de archivo debe permanecer abierto hasta que el proceso ya no necesite el objeto de asignación de archivos. Una manera sencilla de obtener acceso exclusivo es especificar cero en el parámetro *fdwShareMode* de **CreateFile**. La función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) usa el identificador devuelto por **CreateFile** para crear un objeto de asignación de archivos.

La función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) devuelve un identificador al objeto de asignación de archivos. Este identificador se usará al [crear una vista de archivo](creating-a-file-view.md) para que pueda tener acceso a la memoria compartida. Cuando se llama a **CreateFileMapping**, se especifica un nombre de objeto, el número de bytes que se van a asignar desde el archivo y el permiso de lectura y escritura para la memoria asignada. El primer proceso que llama a **CreateFileMapping** crea el objeto de asignación de archivos. Los procesos que llaman a **CreateFileMapping** para un objeto existente reciben un identificador del objeto existente. Puede saber si una llamada correcta a **CreateFileMapping** ha creado o abierto el objeto de asignación de archivos mediante una llamada a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) . **GetLastError** **no devuelve ningún \_ error** en el proceso de creación y el **error \_ ya \_ existe** en los procesos posteriores.

Se produce un error en la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) si las marcas de acceso entran en conflicto con las especificadas cuando la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) abrió el archivo. Por ejemplo, para leer y escribir en el archivo:

-   Especifique los valores **genéricos de \_ lectura** y **\_ escritura** genéricos en el parámetro *fdwAccess* de [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea).
-   Especifique el **valor \_ ReadWrite** de la página en el parámetro *fdwProtect* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga).

La creación de un objeto de asignación de archivos no confirma la memoria física, solo lo reserva.

## <a name="file-mapping-size"></a>Tamaño de asignación de archivos

El tamaño del objeto de asignación de archivos es independiente del tamaño del archivo que se está asignando. Sin embargo, si el objeto de asignación de archivos es mayor que el archivo, el sistema expande el archivo antes de que se devuelva [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) . Si el objeto de asignación de archivos es menor que el archivo, el sistema asigna solo el número especificado de bytes del archivo.

Los parámetros *dwMaximumSizeHigh* y *dwMaximumSizeLow* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) permiten especificar el número de bytes que se van a asignar desde el archivo:

-   Si no desea que cambie el tamaño del archivo (por ejemplo, al asignar archivos de solo lectura), llame a [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) y especifique cero para *dwMaximumSizeHigh* y *dwMaximumSizeLow*. Al hacerlo, se crea un objeto de asignación de archivos que tiene exactamente el mismo tamaño que el archivo. De lo contrario, debe calcular o calcular el tamaño del archivo terminado, ya que los objetos de asignación de archivos tienen un tamaño estático. una vez creado, su tamaño no se puede aumentar ni disminuir. Un intento de asignar un archivo con una longitud de cero de esta manera produce un error con un código de error de **\_ archivo \_ no válido**. Los programas deben probar los archivos con una longitud de cero y rechazarlos.

-   El tamaño de un objeto de asignación de archivos respaldado por un archivo con nombre está limitado por el espacio en disco. El tamaño de una vista de archivo se limita al bloque contiguo más grande disponible de la memoria virtual sin reservar. Esto es como máximo 2 GB menos la memoria virtual ya reservada por el proceso.

El tamaño del objeto de asignación de archivos que seleccione controla la distancia que se puede ver con la asignación de memoria en el archivo. Si crea un objeto de asignación de archivos de 500 KB de tamaño, solo tendrá acceso a los primeros 500 KB del archivo, independientemente del tamaño del archivo. Dado que no le cuesta ningún recurso del sistema para crear un objeto de asignación de archivos más grande, cree un objeto de asignación de archivos que sea el tamaño del archivo (establezca los parámetros *dwMaximumSizeHigh* y *dwMaximumSizeLow* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) ambos en cero) incluso si no espera ver todo el archivo. El costo de los recursos del sistema se obtiene al crear las vistas y acceder a ellas.

Si desea ver una parte del archivo que no comienza al principio del archivo, debe crear un objeto de asignación de archivos. Este objeto es el tamaño de la parte del archivo que desea ver y el desplazamiento en el archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una vista dentro de un archivo](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
