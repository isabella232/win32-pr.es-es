---
description: Cuando un proceso ha terminado con el objeto de asignación de archivos, debe destruir todas las vistas de archivo en su espacio de direcciones mediante la función UnmapViewOfFile para cada vista de archivo.
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: Cerrar un objeto de asignación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab35152bd90d401ca7f30a7497d1f0b06263539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909482"
---
# <a name="closing-a-file-mapping-object"></a>Cerrar un objeto de asignación de archivos

Cuando un proceso ha terminado con el objeto de asignación de archivos, debe destruir todas las vistas de archivo en su espacio de direcciones mediante la función [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) para cada vista de archivo.

Al desasignar una vista asignada de un archivo, se invalida el intervalo ocupado por la vista en el espacio de direcciones del proceso y hace que el intervalo esté disponible para otras asignaciones. Quita la entrada del espacio de trabajo de cada página virtual sin asignar que formaba parte del espacio de trabajo del proceso y reduce el tamaño del espacio de trabajo del proceso. También disminuye el recuento de recursos compartidos de la página física correspondiente.

Las páginas modificadas en la vista sin asignar no se escriben en el disco hasta que su recuento de recursos compartidos llega a cero, o en otras palabras, hasta que no se asignan o se recortan de los conjuntos de trabajo de todos los procesos que comparten las páginas. Incluso después, las páginas modificadas se escriben "de forma diferida" en el disco; es decir, es posible que las modificaciones se almacenen en la memoria caché y se escriban en el disco más adelante. Para minimizar el riesgo de pérdida de datos en caso de que se produzca un error de alimentación o un bloqueo del sistema, las aplicaciones deben vaciar explícitamente las páginas modificadas mediante la función [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Cuando cada proceso termina de usar el objeto de asignación de archivos y ha desasignado todas las vistas, debe cerrar el identificador del objeto de asignación de archivos y el archivo en el disco llamando a [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle). Estas llamadas a **CloseHandle** se realizan correctamente aunque haya vistas de archivo que todavía estén abiertas. Sin embargo, si se dejan las vistas de archivo asignadas, se producen fugas de memoria.

 

 
