---
title: Completar y cancelar un trabajo
description: Para completar un trabajo de transferencia, llame al método IBackgroundCopyJob complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- transferir BITS de trabajo, cancelar
- cancelar los BITS de un trabajo
- transferir BITS de trabajo, completar
- completar BITS de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486651"
---
# <a name="completing-and-canceling-a-job"></a>Completar y cancelar un trabajo

Para completar un trabajo de transferencia, llame al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . En el caso de los trabajos de descarga, puede llamar al método **Complete** antes de que se transfieran todos los archivos del trabajo (antes de que el estado del trabajo sea transferencia de estado del trabajo de BG \_ \_ \_ ). Solo los archivos que BITS se transfirieron correctamente al cliente antes de llamar al método **Complete** están disponibles para el usuario.

En el caso de los trabajos de carga, llame al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) solo si el estado del trabajo es el estado del trabajo de BG \_ \_ \_ transferido. Para determinar cuándo se transfiere el estado del trabajo \_ \_ \_ , transfiera el estado del trabajo, [sondee](polling-for-the-status-of-the-job.md) la propiedad de estado del trabajo o regístrese para recibir la notificación de eventos del trabajo de notificación de BG \_ \_ \_ transferida. [](registering-a-com-callback.md)

Para cancelar un trabajo de transferencia, llame al método [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . El método **Cancel** quita el trabajo de la cola de transferencia y quita los archivos temporales del cliente. Normalmente, se llama a este método si no se puede resolver un error asociado al trabajo.

El método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) cancela una carga si la carga no se ha completado. Si la carga se ha completado y el trabajo es de tipo BG \_ Job \_ Type \_ upload \_ , el método cancela la respuesta.

Si no llama al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o al método [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) en 90 días (el valor predeterminado de [valor jobinactivitytimeout](group-policies.md) Directiva de grupo), el servicio cancela el trabajo. Si el servicio cancela el trabajo, los archivos descargados y el archivo de respuesta no están disponibles para el cliente; la cancelación del trabajo no afecta a los archivos que se han cargado correctamente. Siempre debe llamar al método **Complete** o **Cancel** y no confiar en la Directiva valor jobinactivitytimeout para limpiar los trabajos. Los trabajos que quedan en la cola pueden impedir que los usuarios creen otros trabajos si se alcanza el límite de la Directiva MaxJobsPerUser o MaxJobsPerMachine.

 

 




