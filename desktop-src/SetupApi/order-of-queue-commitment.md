---
description: 'Cuando la función SetupCommitFileQueue confirma la cola de archivos, procesa las operaciones de archivo en el orden siguiente: operaciones de eliminación de archivos, operaciones de cambio de nombre de archivo y, por último, operaciones de copia de archivos.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Orden de compromiso de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7ff3cc211b2a2d253dd307ca83113b536a3d9eaf21b7b2cec5bc977f585026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665545"
---
# <a name="order-of-queue-commitment"></a>Orden de compromiso de cola

Cuando la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) confirma la cola de archivos, procesa las operaciones de archivo en el orden siguiente: operaciones de eliminación de archivos, operaciones de cambio de nombre de archivo y, por último, operaciones de copia de archivos. En el esquema siguiente se muestra el ciclo de vida del proceso de compromiso de una cola.

 

-   iniciar la subcola de eliminación
    -   iniciar una operación de eliminación de <: repetir para cada uno
    -   finalizar una operación de eliminación de <: eliminación de archivos en cola
-   finalizar la subcola de eliminación

<!-- -->

-   iniciar la subcola de cambio de nombre
    -   iniciar una operación de cambio de nombre < archivo: repetir para cada uno
    -   finalizar una operación de eliminación de <: cambio de nombre de archivo en cola
-   finalizar la subcola de cambio de nombre

<!-- -->

-   iniciar la subqueta de copia
    -   iniciar una operación de copia de <: repetir para cada uno
    -   finalizar una operación de copia de <: copia de archivos en cola
    -   finalizar la subcola de copia
-   finalizar la cola

 

En cada paso, o si se produce un error, la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envía una notificación a la rutina de devolución de llamada. La rutina de devolución de llamada puede usar la información enviada por la cola para realizar un seguimiento del progreso de la instalación y, si es necesario, interactuar con el usuario.

Por ejemplo, si una operación de copia de archivos necesita un archivo de origen que no estaba disponible en la ruta de acceso actual, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enviaría una notificación SPFILENOTIFY NEEDMEDIA a la rutina de devolución de llamada, junto con información sobre el archivo y los medios \_ necesarios. La rutina de devolución de llamada podría usar esta información para generar un cuadro de diálogo que solicita al usuario que inserte el siguiente disco mediante una llamada a [ **SetupPromptForDisk.**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)

Se incluye una rutina de devolución de llamada de cola predeterminada, [**SetupDefaultQueueCallback,**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)con la API de instalación. Esta rutina controla las notificaciones de cola y genera cuadros de diálogo de error y barras de progreso para la instalación. Puede usar la rutina de devolución de llamada de cola predeterminada tal como está, o escribir una rutina de devolución de llamada de filtro para controlar un subconjunto de las notificaciones y pasar las demás a la rutina de devolución de llamada de cola predeterminada.

Si ninguna de las funciones de la rutina de devolución de llamada se adapta a sus necesidades, puede escribir una rutina de devolución de llamada personalizada independiente que no llame a la rutina de devolución de llamada de cola predeterminada.

Para obtener más información sobre las rutinas de devolución de llamada de cola, vea [Rutina](default-queue-callback-routine.md)de devolución de llamada de cola predeterminada y Crear una rutina de devolución de llamada [de cola personalizada.](creating-a-custom-queue-callback-routine.md)

 

 



