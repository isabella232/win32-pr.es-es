---
description: Con el almacenamiento local para el subproceso (TLS), puede proporcionar datos únicos para cada subproceso al que el proceso puede tener acceso mediante un índice global. Un subproceso asigna el índice, que puede ser utilizado por otros subprocesos para recuperar los datos únicos asociados al índice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Almacenamiento local para el subproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104556041"
---
# <a name="thread-local-storage"></a>Almacenamiento local para el subproceso

Todos los subprocesos de un proceso comparten su espacio de direcciones virtuales. Las variables locales de una función son únicas para cada subproceso que ejecuta la función. Sin embargo, todos los subprocesos del proceso comparten las variables estáticas y globales. Con el *almacenamiento local para el subproceso* (TLS), puede proporcionar datos únicos para cada subproceso al que el proceso puede tener acceso mediante un índice global. Un subproceso asigna el índice, que puede ser utilizado por otros subprocesos para recuperar los datos únicos asociados al índice.

La constante TLS \_ mínima \_ disponible define el número mínimo de índices TLS disponibles en cada proceso. Se garantiza que este mínimo sea al menos 64 para todos los sistemas. El número máximo de índices por proceso es 1.088.

Cuando se crean los subprocesos, el sistema asigna una matriz de valores de **LPVOID** para TLS, que se inicializan en NULL. Antes de que se pueda usar un índice, debe asignarse mediante uno de los subprocesos. Cada subproceso almacena sus datos para un índice TLS en una *ranura TLS* de la matriz. Si los datos asociados a un índice caben en un valor de **LPVOID** , puede almacenar los datos directamente en la ranura de TLS. Sin embargo, si usa un gran número de índices de esta manera, es mejor asignar almacenamiento independiente, consolidar los datos y minimizar el número de ranuras TLS en uso.

En el diagrama siguiente se muestra cómo funciona TLS. Para obtener un ejemplo de código que ilustra el uso del almacenamiento local de subprocesos, vea [usar el almacenamiento local para el subproceso](using-thread-local-storage.md).

![Diagrama que muestra cómo funciona el proceso T L S.](images/tls.png)

El proceso tiene dos subprocesos, el subproceso 1 y el subproceso 2. Asigna dos índices para su uso con TLS, gdwTlsIndex1 y gdwTlsIndex2. Cada subproceso asigna dos bloques de memoria (uno para cada índice) en el que se almacenan los datos y almacena los punteros a estos bloques de memoria en las ranuras TLS correspondientes. Para tener acceso a los datos asociados a un índice, el subproceso recupera el puntero al bloque de memoria desde la ranura TLS y lo almacena en la variable local lpvData.

Es ideal usar TLS en una biblioteca de vínculos dinámicos (DLL). Para obtener un ejemplo, vea [usar el almacenamiento local para el subproceso en una biblioteca de vínculos dinámicos](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Almacenamiento local para el subproceso (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Uso del almacenamiento local de subprocesos](using-thread-local-storage.md)
</dt> <dt>

[Usar el almacenamiento local de subprocesos en una biblioteca de vínculos dinámicos](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
