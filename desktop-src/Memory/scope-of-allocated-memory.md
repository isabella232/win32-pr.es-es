---
description: Toda la memoria que un proceso asigna mediante las funciones de asignación de memoria (HeapAlloc, VirtualAlloc, GlobalAlloc o LocalAlloc) solo es accesible para el proceso.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Ámbito de la memoria asignada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d2db67a04c019683e737d0f9c581ce8d16b800
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159814"
---
# <a name="scope-of-allocated-memory"></a>Ámbito de la memoria asignada

Toda la memoria que un proceso asigna mediante las funciones de asignación de memoria [**(HeapAlloc,**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)o [**LocalAlloc)**](/windows/desktop/api/WinBase/nf-winbase-localalloc)solo es accesible para el proceso. Sin embargo, la memoria asignada por un archivo DLL se asigna en el espacio de direcciones del proceso que llamó al archivo DLL y no es accesible para otros procesos que usan el mismo archivo DLL. Para crear memoria compartida, debe usar la asignación de archivos.

La asignación de archivos con nombre proporciona una manera sencilla de crear un bloque de memoria compartida. Un proceso puede especificar un nombre cuando usa la [**función CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) para crear un objeto de asignación de archivos. Otros procesos pueden especificar el mismo nombre para la **función CreateFileMapping** o [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) para obtener un identificador para el objeto de asignación.

Cada proceso especifica su identificador para el objeto de asignación de archivos en la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para asignar una vista del archivo a su propio espacio de direcciones. Las vistas de todos los procesos de un único objeto de asignación de archivos se asignan a las mismas páginas compartibles de almacenamiento físico. Sin embargo, las direcciones virtuales de las vistas asignadas pueden variar de un proceso a otro, a menos que se utilice la función [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) para asignar la vista en una dirección especificada. Aunque se pueden compartir, las páginas de almacenamiento físico que se usan para una vista de archivo asignada no son globales; no son accesibles para los procesos que no han asignado una vista del archivo.

Las páginas que se confirman mediante la asignación de una vista de un archivo se liberan cuando el último proceso con una vista del objeto de asignación finaliza o anula la asignación de su vista mediante una llamada a la función [**UnmapViewOfFile.**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) En este momento, se actualiza el archivo especificado (si existe) asociado al objeto de asignación. También se puede forzar la actualización de un archivo especificado llamando a la [**función FlushViewOfFile.**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile)

Para obtener más información, vea [Asignación de archivos.](file-mapping.md) Para obtener un ejemplo de memoria compartida en un archivo DLL, vea [Using Shared Memory in a Dynamic-Link Library](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Si varios procesos tienen acceso de escritura a la memoria compartida, debe sincronizar el acceso a la memoria. Para obtener más información, vea [Synchronization](../sync/synchronization.md).

 

 
