---
description: El espacio de trabajo de un proceso es el conjunto de páginas del espacio de direcciones virtuales del proceso que residen actualmente en la memoria física.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Espacio de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4985e7eb526d5dda8469ccc2f46bfe6fd050c745
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549897"
---
# <a name="working-set"></a>Espacio de trabajo

El espacio de trabajo de un proceso es el conjunto de páginas del espacio de direcciones virtuales del proceso que residen actualmente en la memoria física. El espacio de trabajo solo contiene asignaciones de memoria paginables; Las asignaciones de memoria no paginables, como las [](large-page-support.md) extensiones de ventana de direcciones [](address-windowing-extensions.md) (AWE) o las asignaciones de páginas grandes, no se incluyen en el espacio de trabajo.

Cuando un proceso hace referencia a memoria paginable que no está actualmente en su espacio de trabajo, se *produce un error de* página. El controlador de errores de la página del sistema intenta resolver el error de la página y, si se realiza correctamente, la página se agrega al conjunto de trabajo. (El acceso a AWE o asignaciones de páginas grandes nunca produce un error de página, porque estas asignaciones no se pueden paginar).

Un *error de página* duro debe resolverse mediante la lectura del contenido de la página desde el almacén de respaldo de la página, que es el archivo de paginación del sistema o un archivo asignado a memoria creado por el proceso.  Un *error de página de software* se puede resolver sin tener acceso a la tienda de respaldo. Se produce un error de página flexible cuando:

-   La página está en el espacio de trabajo de algún otro proceso, por lo que ya está en la memoria.
-   La página está en transición, porque se ha quitado de los conjuntos de trabajo de todos los procesos que usaban la página y aún no se ha reasignado, o ya está residentes como resultado de una operación de captura previa del administrador de memoria.
-   Un proceso hace referencia a una página virtual asignada por primera vez (a veces denominada error *de petición cero).*

Las páginas se pueden quitar de un conjunto de trabajo de proceso como resultado de las siguientes acciones:

-   El proceso reduce o vacía el espacio de trabajo mediante una llamada a la función [**SetProcessWorkingSetSize**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize), [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) [**o EmptyWorkingSet.**](/windows/win32/api/psapi/nf-psapi-emptyworkingset)
-   El proceso llama a [**la función VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) en un intervalo de memoria que no está bloqueado.
-   El proceso desasigna una vista asignada de un archivo mediante la [**función UnmapViewOfFile.**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile)
-   El administrador de memoria recorta las páginas del espacio de trabajo para crear más memoria disponible.
-   El administrador de memoria debe quitar una página del espacio de trabajo para dejar espacio para una nueva página (por ejemplo, porque el espacio de trabajo tiene su tamaño máximo).

Si varios procesos comparten una página, quitar la página del conjunto de trabajo de un proceso no afecta a otros procesos. Después de quitar una página de los conjuntos de trabajo de todos los procesos que la estaban usando, la página se convierte en una *página de transición*. Las páginas de transición permanecen almacenadas en caché en la MEMORIA RAM hasta que algún proceso hace referencia a la página de nuevo o se reasigna (por ejemplo, se rellena con ceros y se da a otro proceso). Si se ha modificado una página de transición desde que se escribió por última vez en el disco (es decir, si la página está "desusada"), la página debe escribirse en su memoria de respaldo para poder reasignarse. El sistema puede empezar a escribir páginas de transición desa partir de su almacén de respaldo en cuanto dichas páginas estén disponibles.

Cada proceso tiene un tamaño mínimo y máximo del espacio de trabajo que afecta al comportamiento de paginación de memoria virtual del proceso. Para obtener el tamaño actual del conjunto de trabajo de un proceso especificado, use la [**función GetProcessMemoryInfo.**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) Para obtener o cambiar los tamaños mínimo y máximo del espacio de trabajo, use las funciones [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) y [**SetProcessWorkingSetSizeEx.**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)

La interfaz de programación de aplicaciones de estado de proceso (PSAPI) proporciona una serie de funciones que devuelven información detallada sobre el conjunto de trabajo de un proceso. Para obtener más información, vea [Información del conjunto de trabajo.](../psapi/working-set-information.md)

 

 
