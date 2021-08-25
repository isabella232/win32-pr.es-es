---
description: Las funciones globales y locales se admiten para la porción desde código de 16 bits o para mantener la compatibilidad del código fuente con archivos de 16 Windows.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Funciones globales y locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d7832f90a420e6be87fe6599cc8c9e4722ddf45b789663ed9b39eab4e5449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869705"
---
# <a name="global-and-local-functions"></a>Funciones globales y locales

Las funciones globales y locales se admiten para la porción desde código de 16 bits o para mantener la compatibilidad del código fuente con archivos de 16 Windows. A partir de los Windows de 32 bits, las funciones globales y [](heap-functions.md) locales se implementan como funciones contenedoras que llaman a las funciones de montón correspondientes mediante un identificador para el montón predeterminado del proceso. Por lo tanto, las funciones globales y locales tienen una mayor sobrecarga que otras funciones de administración de memoria.

Las [funciones del montón](heap-functions.md) proporcionan más características y control que las funciones globales y locales. Las nuevas aplicaciones deben usar las funciones del montón a menos que la documentación indique específicamente que se debe usar una función global o local. Por ejemplo, algunas funciones Windows asignan memoria que se debe liberar con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree)y las funciones globales se siguen utilizando con datos dinámicos Exchange (DDE), las funciones del Portapapeles y los objetos de datos OLE. Para obtener una lista completa de las funciones globales y locales, vea la tabla de [Funciones de administración de memoria](memory-management-functions.md).

Windows administración de memoria no proporciona un montón local y un montón global independientes, como lo hace la administración Windows 16 bits. Como resultado, las familias globales y locales de funciones son equivalentes y elegir entre ellas es una cuestión de preferencia personal. Tenga en cuenta que el cambio de un modelo de memoria segmentada de 16 bits a un modelo de memoria virtual de 32 bits ha hecho que algunas de las funciones globales y locales relacionadas y sus opciones sean innecesarias o sin sentido. Por ejemplo, ya no hay punteros cercanos y lejanos, ya que las asignaciones locales y globales devuelven direcciones virtuales de 32 bits.

Los objetos de memoria asignados por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) se encuentran en páginas privadas y asignadas con acceso de lectura y escritura a los que otros procesos no pueden acceder. La memoria asignada mediante **GlobalAlloc** con **GMEM \_ DDESHARE** no se comparte globalmente, ya que se encuentra en un entorno de 16 Windows. Este valor no tiene ningún efecto y solo está disponible por compatibilidad. Las aplicaciones que requieren memoria compartida para otros fines deben usar objetos de asignación de archivos. Varios procesos pueden asignar una vista del mismo objeto de asignación de archivos para proporcionar memoria compartida con nombre. Para obtener más información, vea [Asignación de archivos.](file-mapping.md)

Las asignaciones de memoria solo están limitadas por la memoria física disponible, incluido el almacenamiento en el archivo de paginación en disco. Al asignar memoria fija, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) devuelven un puntero que el proceso de llamada puede usar inmediatamente para acceder a la memoria. Al asignar memoria desplazable, el valor devuelto es un identificador. Para obtener un puntero a un objeto de memoria móvil, use las funciones [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) y [**LocalLock.**](/windows/desktop/api/WinBase/nf-winbase-locallock)

El tamaño real de la memoria asignada puede ser mayor que el tamaño solicitado. Para determinar el número real de bytes asignados, use la [**función GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) [**o LocalSize.**](/windows/desktop/api/WinBase/nf-winbase-localsize) Si la cantidad asignada es mayor que la cantidad solicitada, el proceso puede usar la cantidad completa.

Las [**funciones GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) y [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) cambian el tamaño o los atributos de un objeto de memoria asignado por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc). El tamaño puede aumentar o disminuir.

Las [**funciones GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) y [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) liberan memoria asignada por [**GlobalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**LocalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-localalloc) [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)o [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc). Para descartar el objeto de memoria especificado sin invalidar el identificador, use la [**función GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) [**o LocalDiscard.**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) **GlobalReAlloc** o **LocalReAlloc** pueden usar el identificador más adelante para asignar un nuevo bloque de memoria asociado al mismo identificador.

Para devolver información sobre un objeto de memoria especificado, use la [**función GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) o [**LocalFlags.**](/windows/desktop/api/WinBase/nf-winbase-localflags) La información incluye el recuento de bloqueos del objeto e indica si el objeto se puede descartar o si ya se ha descartado. Para devolver un identificador al objeto de memoria asociado a un puntero especificado, use la [**función GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) [**o LocalHandle.**](/windows/desktop/api/WinBase/nf-winbase-localhandle)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comparar métodos de asignación de memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
