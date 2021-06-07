---
description: El primer paso para asignar un archivo es abrir el archivo mediante una llamada a la función CreateFile.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Crear un objeto de asignación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502c484dd0466b47a87f4db205d1da5499bf5ef
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432507"
---
# <a name="creating-a-file-mapping-object"></a>Crear un objeto de asignación de archivos

El primer paso para asignar un archivo es abrir el archivo mediante una llamada a la [**función CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea) Para asegurarse de que otros procesos no puedan escribir en la parte del archivo asignado, debe abrir el archivo con acceso exclusivo. Además, el identificador de archivo debe permanecer abierto hasta que el proceso ya no necesite el objeto de asignación de archivos. Una manera fácil de obtener acceso exclusivo es especificar cero en el *parámetro fdwShareMode* de **CreateFile**. La función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) usa el identificador devuelto por **CreateFile** para crear un objeto de asignación de archivos.

La [**función CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) devuelve un identificador al objeto de asignación de archivos. Este identificador se usará al [crear una vista de archivo](creating-a-file-view.md) para que pueda acceder a la memoria compartida. Cuando se llama a **CreateFileMapping,** se especifica un nombre de objeto, el número de bytes que se asignarán desde el archivo y el permiso de lectura y escritura para la memoria asignada. El primer proceso que llama a **CreateFileMapping** crea el objeto de asignación de archivos. Los procesos que llaman a **CreateFileMapping** para un objeto existente reciben un identificador para el objeto existente. Puede saber si una llamada correcta a **CreateFileMapping** creó o abrió el objeto de asignación de archivos llamando a la [**función GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) **GetLastError devuelve** **NO ERROR \_ al** proceso de creación y **ERROR ALREADY \_ \_ EXISTS** a los procesos posteriores.

Se produce un error en la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) si las marcas de acceso están en conflicto con las especificadas cuando la [**función CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) abrió el archivo. Por ejemplo, para leer y escribir en el archivo:

-   Especifique los **valores GENERIC \_ READ** **y GENERIC \_ WRITE** en el *parámetro fdwAccess* [**de CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea).
-   Especifique el **valor PAGE \_ READWRITE** en el *parámetro fdwProtect* [**de CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)

La creación de un objeto de asignación de archivos no confirma la memoria física, solo la reserva.

## <a name="file-mapping-size"></a>Tamaño de asignación de archivos

El tamaño del objeto de asignación de archivos es independiente del tamaño del archivo que se está asignando. Sin embargo, si el objeto de asignación de archivos es mayor que el archivo, el sistema expande el archivo antes de que [**vuelva CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) Si el objeto de asignación de archivos es menor que el archivo, el sistema asigna solo el número especificado de bytes del archivo.

Los *parámetros dwMaximumSizeHigh* y *dwMaximumSizeLow* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) permiten especificar el número de bytes que se asignarán desde el archivo:

-   Si no desea que cambie el tamaño del archivo (por ejemplo, al asignar archivos de solo lectura), llame a [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) y especifique cero para *dwMaximumSizeHigh* y *dwMaximumSizeLow*. Al hacerlo, se crea un objeto de asignación de archivos que tiene exactamente el mismo tamaño que el archivo. De lo contrario, debe calcular o calcular el tamaño del archivo terminado porque los objetos de asignación de archivos tienen un tamaño estático; una vez creado, su tamaño no se puede aumentar ni disminuir. Se produce un error al intentar asignar un archivo con una longitud de cero de esta manera con un código de error **de ARCHIVO DE ERROR NO \_ \_ VÁLIDO.** Los programas deben probar archivos con una longitud de cero y rechazar dichos archivos.

-   El tamaño de un objeto de asignación de archivos con el respaldo de un archivo con nombre está limitado por el espacio en disco. El tamaño de una vista de archivo se limita al bloque contiguo más grande disponible de memoria virtual no conservada. Esto es como máximo 2 GB menos la memoria virtual ya reservada por el proceso.

El tamaño del objeto de asignación de archivos que seleccione controla hasta qué punto puede "ver" el archivo con la asignación de memoria. Si crea un objeto de asignación de archivos con un tamaño de 500 Kb, solo tendrá acceso a los primeros 500 Kb del archivo, independientemente del tamaño del archivo. Dado que no le cuesta ningún recurso del sistema crear un objeto de asignación de archivos mayor, cree un objeto de asignación de archivos que tenga el tamaño del archivo (establezca los parámetros *dwMaximumSizeHigh* y *dwMaximumSizeLow* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) ambos en cero) incluso si no espera ver todo el archivo. El costo de los recursos del sistema se produce al crear las vistas y acceder a ellas.

Puede ver una parte del archivo que no se inicia al principio del archivo. Para obtener más información, [vea Crear una vista dentro de un archivo](creating-a-view-within-a-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>
[Crear una vista de archivo](creating-a-file-view.md)
</dt> creando una vista dentro de un <dt> 
[archivo](creating-a-view-within-a-file.md)
</dt> </dl>


 
