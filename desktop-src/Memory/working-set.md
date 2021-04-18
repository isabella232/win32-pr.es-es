---
description: El conjunto de trabajo de un proceso es el conjunto de páginas del espacio de direcciones virtuales del proceso residente actualmente en la memoria física.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Espacio de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54ed26e9809ebffd01edb30f48f36d398689e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687766"
---
# <a name="working-set"></a>Espacio de trabajo

El conjunto de trabajo de un proceso es el conjunto de páginas del espacio de direcciones virtuales del proceso residente actualmente en la memoria física. El espacio de trabajo contiene solo asignaciones de memoria paginables; las asignaciones de memoria no paginables como [las extensiones de ventana de dirección](address-windowing-extensions.md) (AWE) o las asignaciones de [páginas grandes](large-page-support.md) no se incluyen en el espacio de trabajo.

Cuando un proceso hace referencia a una memoria paginable que no está actualmente en su espacio de trabajo, se produce un *error de página* . El controlador de errores de página del sistema intenta resolver el error de página y, si se realiza correctamente, la página se agrega al espacio de trabajo. (El acceso a asignaciones AWE o de páginas grandes nunca produce un error de página, ya que estas asignaciones no son paginables).

Un *error de página* debe resolverse mediante la lectura del contenido de la página desde la memoria *auxiliar* de la página, que es el archivo de paginación del sistema o un archivo asignado a la memoria creado por el proceso. Un *error de página de software* se puede resolver sin tener acceso a la memoria auxiliar. Se produce un error de página de software cuando:

-   La página está en el espacio de trabajo de algún otro proceso, por lo que ya está residente en memoria.
-   La página está en transición porque se ha quitado de los conjuntos de trabajo de todos los procesos que usaban la página y aún no se ha reasignado, o bien ya está residente como resultado de una operación de captura previa del administrador de memoria.
-   Un proceso hace referencia a una página virtual asignada por primera vez (a veces denominado *error de petición cero*).

Las páginas se pueden quitar de un espacio de trabajo del proceso como resultado de las siguientes acciones:

-   El proceso reduce o vacía el espacio de trabajo mediante una llamada a la función [**SetProcessWorkingSetSize**](/windows/win32/api/winbase/nf-winbase-setprocessworkingsetsize), [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) o [**EmptyWorkingSet**](/windows/win32/api/psapi/nf-psapi-emptyworkingset) .
-   El proceso llama a la función [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) en un intervalo de memoria que no está bloqueado.
-   El proceso desasigna una vista asignada de un archivo mediante la función [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) .
-   El administrador de memoria recorta las páginas del espacio de trabajo para crear más memoria disponible.
-   El administrador de memoria debe quitar una página del espacio de trabajo para dejar espacio para una nueva página (por ejemplo, porque el espacio de trabajo tiene el tamaño máximo).

Si varios procesos comparten una página, la eliminación de la página del espacio de trabajo de un proceso no afecta a otros procesos. Después de quitar una página de los conjuntos de trabajo de todos los procesos que la usaban, la página se convierte en una *Página de transición*. Las páginas de transición permanecen almacenadas en la memoria caché hasta que se hace referencia a la página mediante algún proceso o se reasignan (por ejemplo, se rellena con ceros y se asigna a otro proceso). Si se ha modificado una página de transición desde que se escribió por última vez en el disco (es decir, si la página está "sucio"), la página debe escribirse en su memoria auxiliar para que se pueda reasignar. El sistema puede empezar a escribir páginas de transición sucia en su memoria auxiliar en cuanto estén disponibles dichas páginas.

Cada proceso tiene un tamaño de espacio de trabajo mínimo y máximo que afecta al comportamiento de paginación de la memoria virtual del proceso. Para obtener el tamaño actual del espacio de trabajo de un proceso especificado, utilice la función [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) . Para obtener o cambiar los tamaños mínimo y máximo del espacio de trabajo, utilice las funciones [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) y [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) .

La interfaz de programación de aplicaciones (PSAPI) del estado del proceso proporciona una serie de funciones que devuelven información detallada sobre el espacio de trabajo de un proceso. Para obtener más información, vea [información de espacio de trabajo](../psapi/working-set-information.md).

 

 
