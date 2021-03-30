---
description: 'Cuando la función SetupCommitFileQueue confirma la cola de archivos, procesa las operaciones de archivo en el siguiente orden: operaciones de eliminación de archivos, operaciones de cambio de nombre de archivos y, por último, operaciones de copia de archivos.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Orden de compromiso de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910334"
---
# <a name="order-of-queue-commitment"></a>Orden de compromiso de cola

Cuando la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) confirma la cola de archivos, procesa las operaciones de archivo en el siguiente orden: operaciones de eliminación de archivos, operaciones de cambio de nombre de archivos y, por último, operaciones de copia de archivos. En el siguiente esquema se muestra el ciclo de vida del proceso de compromiso de una cola.

 

-   Inicio de la subcola de eliminación
    -   iniciar una operación de eliminación de archivo <--REPEAT para cada
    -   finalizar una operación de eliminación de archivo <--eliminar archivo en cola
-   finalizar la subcola de eliminación

<!-- -->

-   iniciar la subcola Rename
    -   iniciar una operación de cambio de nombre de archivo <--REPEAT para cada
    -   finalizar una operación de eliminación de archivo <: cambio de nombre de archivo en cola
-   finalizar el cambio de nombre de la subcola

<!-- -->

-   Inicio de la copia subque
    -   iniciar una operación de copia de archivos <--REPEAT para cada
    -   finalizar una operación de copia de archivos <: copia de archivos en cola
    -   finalizar la subcola de copia
-   finalizar la cola

 

En cada paso, o si se produce un error, la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envía una notificación a la rutina de devolución de llamada. La rutina de devolución de llamada puede usar la información enviada por la cola para realizar el seguimiento del progreso de la instalación y, si es necesario, interactuar con el usuario.

Por ejemplo, si una operación de copia de archivos necesita un archivo de código fuente que no estaba disponible en la ruta de acceso actual, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enviaría una \_ notificación SPFILENOTIFY NEEDMEDIA a la rutina de devolución de llamada, junto con información sobre el archivo y los medios necesarios. La rutina de devolución de llamada podría usar esta información para generar un cuadro de diálogo que pide al usuario que inserte el siguiente disco mediante una llamada a [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)

Una rutina de devolución de llamada de cola predeterminada, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), se incluye con la API de instalación. Esta rutina controla las notificaciones de cola y genera cuadros de diálogo de error y barras de progreso para la instalación. Puede usar la rutina de devolución de llamada de cola predeterminada tal como está, o escribir una rutina de devolución de llamada de filtro para controlar un subconjunto de las notificaciones y pasar las demás a la rutina de devolución de llamada de cola predeterminada.

Si ninguna de las funciones de la rutina de devolución de llamada se adapta a sus necesidades, puede escribir una rutina de devolución de llamada personalizada independiente que no llame a la rutina de devolución de llamada de cola predeterminada.

Para obtener más información sobre las rutinas de devolución de llamada de cola, vea [rutina de devolución de llamada de cola predeterminada](default-queue-callback-routine.md)y [crear una rutina de devolución de llamada de cola personalizada](creating-a-custom-queue-callback-routine.md).

 

 



