---
description: Una cola de archivos es una lista de operaciones de archivo que se procesan al mismo tiempo. Las operaciones de archivo en la cola pueden ser operaciones de copiar, cambiar nombre o eliminar. La cola de archivos organiza las operaciones de archivo por tipo, creando subcolas de copia, cambio de nombre y eliminación.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Acerca de las colas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666434"
---
# <a name="about-file-queues"></a>Acerca de las colas de archivos

Una cola de archivos es una lista de operaciones de archivo que se procesan al mismo tiempo. Las operaciones de archivo en la cola pueden ser operaciones de copiar, cambiar nombre o eliminar. La cola de archivos organiza las operaciones de archivo por tipo, creando subcolas de copia, cambio de nombre y eliminación.

Estas operaciones se pueden enviar a la cola en cualquier orden y el proceso de puesta en cola no debe ser contiguo. Cuando se confirma la cola, la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) realiza operaciones de archivo en orden del tipo de operación.

Normalmente, todas las operaciones de archivo necesarias para una instalación completa se ponen en cola en la cola de archivos y, a continuación, se procesan en un lote único cuando se confirma la cola.

Una ventaja de poner en cola las operaciones de archivo sobre la instalación de archivos sección por sección desde un archivo INF es que puede simplificar el proceso de instalación. En lugar de tener que obtener información del usuario para que se instale cada sección, puede obtener información de instalación del usuario para todos los archivos que se van a instalar al compilar la cola. Esto permite al usuario realizar otras actividades mientras se procesan las operaciones de copia con un uso intensivo de tiempo mediante la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .

Otra ventaja de las colas de archivos es que puede realizar un seguimiento del progreso de la instalación en su conjunto. Al instalar la sección por sección desde un archivo INF, los indicadores de progreso, como las barras de progreso, solo pueden realizar el seguimiento de la sección INF actual. Cuando se instala la sección siguiente, la barra de progreso comienza de nuevo. Con una cola, el número total de archivos que se procesan durante toda la instalación se conoce antes de que se confirme la cola y, por lo tanto, se puede generar una barra de progreso para realizar el seguimiento de toda la instalación.

Para obtener más información, vea los temas siguientes:

-   [Orden de compromiso de cola](order-of-queue-commitment.md)
-   [Notificaciones de cola](queue-notifications.md)

 

 



