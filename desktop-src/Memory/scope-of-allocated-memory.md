---
description: Toda la memoria que un proceso asigna mediante las funciones de asignación de memoria (HeapAlloc, VirtualAlloc, GlobalAlloc o LocalAlloc) solo es accesible para el proceso.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Ámbito de la memoria asignada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d2db67a04c019683e737d0f9c581ce8d16b800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275566"
---
# <a name="scope-of-allocated-memory"></a>Ámbito de la memoria asignada

Toda la memoria que un proceso asigna mediante las funciones de asignación de memoria ( [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc), [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)) solo es accesible para el proceso. Sin embargo, la memoria asignada por un archivo DLL se asigna en el espacio de direcciones del proceso que llamó a la DLL y no es accesible para otros procesos que usan el mismo archivo DLL. Para crear memoria compartida, debe usar la asignación de archivos.

La asignación de archivos con nombre proporciona una manera sencilla de crear un bloque de memoria compartida. Un proceso puede especificar un nombre cuando usa la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) para crear un objeto de asignación de archivos. Otros procesos pueden especificar el mismo nombre para la función **CreateFileMapping** o [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) con el fin de obtener un identificador para el objeto de asignación.

Cada proceso especifica su identificador para el objeto de asignación de archivos en la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para asignar una vista del archivo en su propio espacio de direcciones. Las vistas de todos los procesos de un solo objeto de asignación de archivos se asignan a las mismas páginas que se pueden compartir de almacenamiento físico. Sin embargo, las direcciones virtuales de las vistas asignadas pueden variar de un proceso a otro, a menos que se use la función [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) para asignar la vista en una dirección especificada. Aunque se pueda compartir, las páginas de almacenamiento físico usadas para una vista de archivo asignada no son globales; no son accesibles para los procesos que no han asignado una vista del archivo.

Las páginas confirmadas mediante la asignación de una vista de un archivo se liberan cuando el último proceso con una vista del objeto de asignación finaliza o desasigna su vista mediante una llamada a la función [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) . En este momento, se actualiza el archivo especificado (si existe) asociado al objeto de asignación. También se puede forzar la actualización de un archivo especificado mediante una llamada a la función [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Para obtener más información, vea [asignación de archivos](file-mapping.md). Para obtener un ejemplo de memoria compartida en un archivo DLL, consulte [uso de memoria compartida en una biblioteca de Dynamic-Link](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Si hay varios procesos que tienen acceso de escritura a la memoria compartida, debe sincronizar el acceso a la memoria. Para obtener más información, consulte [Synchronization](../sync/synchronization.md).

 

 
