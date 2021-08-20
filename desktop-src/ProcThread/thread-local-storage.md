---
description: Con el almacenamiento local de subprocesos (TLS), puede proporcionar datos únicos para cada subproceso al que el proceso pueda acceder mediante un índice global. Un subproceso asigna el índice, que pueden usar los otros subprocesos para recuperar los datos únicos asociados al índice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Almacenamiento local para el subproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32c1630fb5690fc3ade4d319e7787c5287b27c270a9b43e3825e547e68bd4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793009"
---
# <a name="thread-local-storage"></a>Almacenamiento local para el subproceso

Todos los subprocesos de un proceso comparten su espacio de direcciones virtuales. Las variables locales de una función son únicas para cada subproceso que ejecuta la función. Sin embargo, todos los subprocesos del proceso comparten las variables estáticas y globales. Con *el almacenamiento local de* subprocesos (TLS), puede proporcionar datos únicos para cada subproceso al que el proceso pueda acceder mediante un índice global. Un subproceso asigna el índice, que pueden usar los otros subprocesos para recuperar los datos únicos asociados al índice.

La constante TLS \_ MINIMUM AVAILABLE define el número mínimo de índices TLS disponibles en cada \_ proceso. Se garantiza que este mínimo sea al menos 64 para todos los sistemas. El número máximo de índices por proceso es 1088.

Cuando se crean los subprocesos, el sistema asigna una matriz de valores **LPVOID** para TLS, que se inicializan en NULL. Para poder usar un índice, uno de los subprocesos debe asignarlo. Cada subproceso almacena sus datos para un índice TLS en una *ranura TLS* de la matriz. Si los datos asociados a un índice caben en un valor **LPVOID,** puede almacenar los datos directamente en la ranura TLS. Sin embargo, si usa un gran número de índices de esta manera, es mejor asignar almacenamiento independiente, consolidar los datos y minimizar el número de ranuras TLS en uso.

En el diagrama siguiente se muestra cómo funciona TLS. Para obtener un ejemplo de código que ilustra el uso del almacenamiento local de subprocesos, vea [Using Thread Local Storage](using-thread-local-storage.md).

![Diagrama que muestra cómo funciona el proceso de T LS.](images/tls.png)

El proceso tiene dos subprocesos, Subproceso 1 y Subproceso 2. Asigna dos índices para su uso con TLS, gdwTlsIndex1 y gdwTlsIndex2. Cada subproceso asigna dos bloques de memoria (uno para cada índice) en los que almacenar los datos y almacena los punteros a estos bloques de memoria en las ranuras TLS correspondientes. Para acceder a los datos asociados a un índice, el subproceso recupera el puntero al bloque de memoria de la ranura TLS y lo almacena en la variable local lpvData.

Es ideal usar TLS en una biblioteca de vínculos dinámicos (DLL). Para obtener un ejemplo, vea [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subproceso local Storage (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Uso del almacenamiento local de subprocesos](using-thread-local-storage.md)
</dt> <dt>

[Uso de subprocesos Storage en una biblioteca de vínculos dinámicos](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
