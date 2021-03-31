---
description: Las funciones globales y locales se admiten para la migración desde código de 16 bits o para mantener la compatibilidad con el código fuente con Windows de 16 bits.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Funciones globales y locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf356647f92f0e7d82e914a91020c438363ff082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907878"
---
# <a name="global-and-local-functions"></a>Funciones globales y locales

Las funciones globales y locales se admiten para la migración desde código de 16 bits o para mantener la compatibilidad con el código fuente con Windows de 16 bits. A partir de Windows de 32 bits, las funciones globales y locales se implementan como funciones contenedoras que llaman a las [funciones del montón](heap-functions.md) correspondientes mediante un identificador del montón predeterminado del proceso. Por lo tanto, las funciones globales y locales tienen una mayor sobrecarga que otras funciones de administración de memoria.

Las [funciones del montón](heap-functions.md) proporcionan más características y control que las funciones globales y locales. Las nuevas aplicaciones deben usar las funciones del montón, a menos que la documentación indique específicamente que se debe usar una función global o local. Por ejemplo, algunas funciones de Windows asignan memoria que se debe liberar con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree)y las funciones globales todavía se utilizan con intercambio dinámico de datos (DDE), las funciones del portapapeles y los objetos de datos OLE. Para obtener una lista completa de las funciones globales y locales, consulte la tabla en [funciones de administración de memoria](memory-management-functions.md).

La administración de memoria de Windows no proporciona un montón local independiente y un montón global, como Windows de 16 bits. Como resultado, las familias de funciones globales y locales son equivalentes y elegir entre ellas es una cuestión de preferencia personal. Tenga en cuenta que el cambio de un modelo de memoria segmentada de 16 bits a un modelo de memoria virtual de 32 bits ha realizado algunas de las funciones globales y locales relacionadas, y sus opciones no son necesarias o no tienen sentido. Por ejemplo, ya no hay punteros Near y Far, porque las asignaciones locales y globales devuelven direcciones virtuales de 32 bits.

Los objetos de memoria asignados por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) están en páginas privadas y confirmadas con acceso de lectura y escritura al que no pueden tener acceso otros procesos. En realidad, la memoria asignada mediante **GlobalAlloc** con **GMEM \_ DDESHARE** no se comparte de forma global, ya que se encuentra en Windows de 16 bits. Este valor no tiene ningún efecto y solo está disponible por compatibilidad. Las aplicaciones que requieren memoria compartida para otros propósitos deben usar objetos de asignación de archivos. Varios procesos pueden asignar una vista del mismo objeto de asignación de archivos para proporcionar la memoria compartida con nombre. Para obtener más información, vea [asignación de archivos](file-mapping.md).

Las asignaciones de memoria están limitadas solo por la memoria física disponible, incluido el almacenamiento en el archivo de paginación en el disco. Al asignar memoria fija, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) devuelven un puntero que el proceso de llamada puede usar inmediatamente para tener acceso a la memoria. Al asignar memoria móvil, el valor devuelto es un identificador. Para obtener un puntero a un objeto de memoria movible, utilice las funciones [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) y [**LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) .

El tamaño real de la memoria asignada puede ser mayor que el tamaño solicitado. Para determinar el número real de bytes asignados, utilice la función [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) o [**variables locales**](/windows/desktop/api/WinBase/nf-winbase-localsize) . Si la cantidad asignada es mayor que la cantidad solicitada, el proceso puede utilizar la cantidad completa.

Las funciones [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) y [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) cambian el tamaño o los atributos de un objeto de memoria asignado por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc). El tamaño puede aumentar o disminuir.

Las funciones [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) y [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) liberan memoria asignada por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)o [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc). Para descartar el objeto de memoria especificado sin invalidar el identificador, utilice la función [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) o [**LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) . El identificador se puede usar más adelante por **GlobalReAlloc** o **LocalReAlloc** para asignar un nuevo bloque de memoria asociado al mismo identificador.

Para devolver información sobre un objeto de memoria especificado, utilice la función [**indicadores_globales**](/windows/desktop/api/WinBase/nf-winbase-globalflags) o [**LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) . La información incluye el recuento de bloqueos del objeto e indica si el objeto es descartable o ya se ha descartado. Para devolver un identificador al objeto de memoria asociado a un puntero especificado, utilice la función [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) o [**LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comparar métodos de asignación de memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
