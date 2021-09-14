---
description: La asignación de archivos se puede usar para compartir un archivo o memoria entre dos o más procesos. Para compartir un archivo o memoria, todos los procesos deben usar el nombre o el identificador del mismo objeto de asignación de archivos.
ms.assetid: 942cb50d-df07-444f-bba5-58194556ae66
title: Uso compartido de archivos y memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d402eba3f87f1f799593ae0d6b23fba06124a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159812"
---
# <a name="sharing-files-and-memory"></a>Uso compartido de archivos y memoria

La asignación de archivos se puede usar para compartir un archivo o memoria entre dos o más procesos. Para compartir un archivo o memoria, todos los procesos deben usar el nombre o el identificador del mismo objeto de asignación de archivos.

Para compartir un archivo, el primer proceso crea o abre un archivo mediante la [**función CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea) A continuación, crea un objeto de asignación de archivos mediante la función [**CreateFileMapping,**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) especificando el identificador de archivo y un nombre para el objeto de asignación de archivos. Los nombres de los objetos event, semaphore, mutex, waitable timer, job y file mapping comparten el mismo espacio de nombres. Por lo tanto, **las funciones CreateFileMapping** y [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) producirán un error si especifican un nombre que está en uso por un objeto de otro tipo.

Para compartir memoria que no está asociada a un archivo, un proceso debe usar la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) y especificar INVALID HANDLE VALUE como parámetro hFile en lugar de un identificador \_ de archivo \_ existente.  El objeto de asignación de archivos correspondiente tiene acceso a la memoria con el respaldo del archivo de paginación del sistema. Debe especificar un tamaño mayor que cero cuando especifique un *hFile* de INVALID HANDLE VALUE en una llamada \_ a \_ **CreateFileMapping**.

La manera más fácil de que otros procesos obtengan un identificador del objeto de asignación de archivos creado por el primer proceso es usar la función [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) y especificar el nombre del objeto. Esto se conoce como memoria *compartida con nombre.* Si el objeto de asignación de archivos no tiene un nombre, el proceso debe obtener un identificador para él a través de herencia o duplicación. Para obtener más información sobre la herencia y la duplicación, vea [Herencia](../procthread/inheritance.md).

Los procesos que comparten archivos o memoria deben crear vistas de archivo mediante la [**función MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) [**o MapViewOfFileEx.**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) Deben coordinar su acceso mediante semáforos, exclusiones mutuas, eventos o alguna otra técnica de exclusión mutua. Para obtener más información, vea [Synchronization](../sync/synchronization.md).

Un objeto de asignación de archivos compartidos no se destruirá hasta que todos los procesos que lo usan cierren sus identificadores a él mediante la [**función CloseHandle.**](/windows/win32/api/handleapi/nf-handleapi-closehandle)

Para obtener información sobre la seguridad de objetos de asignación de archivos, vea [File Mapping Security and Access Rights](file-mapping-security-and-access-rights.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de memoria compartida con nombre](creating-named-shared-memory.md)
</dt> </dl>

 

 
