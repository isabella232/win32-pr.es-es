---
title: Finalización y cancelación de un trabajo
description: Para completar un trabajo de transferencia, llame al método IBackgroundCopyJob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- transfer job BITS , canceling
- cancelar bits de un trabajo
- transfer job BITS , completing
- finalización de un trabajo BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 348ee7c4ad4b9a38350e6a1f25d8d05d206b299518cf25197b643dbcb15cb4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835060"
---
# <a name="completing-and-canceling-a-job"></a>Finalización y cancelación de un trabajo

Para completar un trabajo de transferencia, llame al [**método IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Para los trabajos de descarga, puede llamar al método **Complete** antes de que se hayan transferido todos los archivos del trabajo (antes de que el estado del trabajo sea BG \_ JOB STATE \_ \_ TRANSFERRED). Solo los archivos que BITS transfirieron correctamente al cliente antes de llamar al **método Complete** están disponibles para el usuario.

Para los trabajos de carga, llame al [**método Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) solo si el estado del trabajo es BG JOB \_ STATE \_ \_ TRANSFERRED. Para determinar cuándo el estado del trabajo es BG \_ JOB \_ STATE \_ TRANSFERRED, [](polling-for-the-status-of-the-job.md) sondee \_ \_ \_ [](registering-a-com-callback.md)la propiedad de estado del trabajo o regístrese para recibir la notificación de eventos BG NOTIFY JOB TRANSFERRED .

Para cancelar un trabajo de transferencia, llame al [**método IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) El **método Cancel** quita el trabajo de la cola de transferencia y quita los archivos temporales del cliente. Normalmente, se llama a este método si no se puede resolver un error asociado al trabajo.

El [**método Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) cancela una carga si la carga no se ha completado. Si la carga se ha completado y el trabajo es de tipo BG JOB TYPE UPLOAD REPLY, el \_ método cancela la \_ \_ \_ respuesta.

Si no llama al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o al método [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) en un plazo de 90 días (valor predeterminado [de JobInactivityTimeout](group-policies.md) directiva de grupo), el servicio cancela el trabajo. Si el servicio cancela el trabajo, los archivos descargados y el archivo de respuesta no están disponibles para el cliente; la cancelación de trabajos no afecta a los archivos que se han cargado correctamente. Siempre debe llamar al método **Complete** o **Cancel** y no confiar en la directiva JobInactivityTimeout para limpiar los trabajos. Los trabajos que quedan en la cola pueden impedir que los usuarios creen otros trabajos si se alcanza el límite de directivas MaxJobsPerUser o MaxJobsPerMachine.

 

 




