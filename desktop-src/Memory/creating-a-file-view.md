---
description: Para asignar los datos de un archivo a la memoria virtual de un proceso, debe crear una vista del archivo.
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: Crear una vista de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f7ba132efd9ecf82f9ec087492c9622824b51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159884"
---
# <a name="creating-a-file-view"></a>Crear una vista de archivo

Para asignar los datos de un archivo a la memoria virtual de un proceso, debe crear una vista del archivo. Las [**funciones MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) y [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) usan el identificador de objeto de asignación de archivos devuelto por [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) para crear una vista del archivo o una parte del archivo en el espacio de direcciones virtuales del proceso. Estas funciones producirán un error si las marcas de acceso están en conflicto con las especificadas cuando **CreateFileMapping** creó el objeto de asignación de archivos.

La [**función MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) devuelve un puntero a la vista de archivo. Al desreferenciar un puntero en el intervalo de direcciones especificado en **MapViewOfFile**, una aplicación puede leer datos del archivo y escribir datos en el archivo. La escritura en la vista de archivos produce cambios en el objeto de asignación de archivos. El sistema controla la escritura real en el archivo en el disco. Los datos no se transfieren realmente en el momento en que se escribe el objeto de asignación de archivos. En su lugar, gran parte de la entrada y salida de archivo (E/S) se almacena en caché para mejorar el rendimiento general del sistema. Las aplicaciones pueden invalidar este comportamiento llamando a [**la función FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) para forzar al sistema a realizar transacciones de disco inmediatamente.

La [**función MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) funciona exactamente igual que la función [**MapViewOfFile,**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) salvo que permite que un proceso especifique la dirección base de la vista del archivo en el espacio de direcciones virtuales del proceso en el parámetro *lpvBase.* Si no hay suficiente espacio en la dirección especificada, se produce un error en la llamada. Por lo tanto, si debe asignar un archivo a la misma dirección en varios procesos, los procesos deben negociar una dirección adecuada: el parámetro *lpvBase* debe ser un múltiplo entero de la granularidad de asignación de memoria del sistema o se produce un error en la llamada. Para obtener la granularidad de asignación de memoria del sistema, use la función [**GetSystemInfo,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) que rellena los miembros de una [**estructura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)

Una aplicación puede crear varias vistas de archivo a partir del mismo objeto de asignación de archivos. Una vista de archivo puede tener un tamaño diferente al objeto de asignación de archivos del que se deriva, pero debe ser menor que el objeto de asignación de archivos. El desplazamiento especificado por los parámetros *dwOffsetHigh* y *dwOffsetLow* de [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) debe ser un múltiplo de la granularidad de asignación del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una vista dentro de un archivo](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
