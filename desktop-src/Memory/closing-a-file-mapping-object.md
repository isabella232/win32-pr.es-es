---
description: Cuando un proceso ha finalizado con el objeto de asignación de archivos, debe destruir todas las vistas de archivo en su espacio de direcciones mediante la función UnmapViewOfFile para cada vista de archivo.
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: Cerrar un objeto de asignación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab35152bd90d401ca7f30a7497d1f0b06263539
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159893"
---
# <a name="closing-a-file-mapping-object"></a>Cerrar un objeto de asignación de archivos

Cuando un proceso ha finalizado con el objeto de asignación de archivos, debe destruir todas las vistas de archivo en su espacio de direcciones mediante la función [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) para cada vista de archivo.

La desasignación de una vista asignada de un archivo invalida el intervalo ocupado por la vista en el espacio de direcciones del proceso y hace que el intervalo esté disponible para otras asignaciones. Quita la entrada del espacio de trabajo para cada página virtual no seleccionada que formaba parte del espacio de trabajo del proceso y reduce el tamaño del espacio de trabajo del proceso. También disminuye el recuento de recurso compartido de la página física correspondiente.

Las páginas modificadas en la vista no mapa no se escriben en el disco hasta que el recuento de recurso compartido alcanza cero, o en otras palabras, hasta que se desasoden o se recortan de los conjuntos de trabajo de todos los procesos que comparten las páginas. Incluso entonces, las páginas modificadas se escriben "de forma temporal" en el disco. Es decir, las modificaciones se pueden almacenar en caché en la memoria y escribirse en el disco más adelante. Para minimizar el riesgo de pérdida de datos en caso de un error de alimentación o un bloqueo del sistema, las aplicaciones deben vaciar explícitamente las páginas modificadas mediante la función [**FlushViewOfFile.**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile)

Cuando cada proceso termina de usar el objeto de asignación de archivos y no asigna todas las vistas, debe cerrar el identificador del objeto de asignación de archivos y el archivo en disco llamando a [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle). Estas llamadas a **CloseHandle se** realiza correctamente incluso cuando hay vistas de archivo que todavía están abiertas. Sin embargo, dejar asignadas las vistas de archivo provoca pérdidas de memoria.

 

 
