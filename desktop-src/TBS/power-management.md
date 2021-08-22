---
title: Administración de energía (Servicios base de TPM)
description: El TBS recibe eventos de administración de energía.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece75e95065ca21d81ce7a3447cead33b6e3b8ae6693617fcb16bb27a30dd94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880699"
---
# <a name="power-management-tpm-base-services"></a>Administración de energía (Servicios base de TPM)

El TBS recibe eventos de administración de energía. Cuando se recibe una indicación de que el TPM u otras partes de la plataforma están a punto de entrar en un estado de energía en el que se interrumpirá la ejecución o se perderá el estado del TPM, el TBS comprueba si es probable que el comando que se está ejecutando actualmente finalice antes de que el sistema se apague. En general, el TBS permite que los comandos de duración corta y media finalicen, pero cancela los comandos de duración larga. Una vez devuelto el comando, el TBS deja de enviar nuevos comandos al TPM y se prepara para la hibernación. Cuando se restaura la energía, el TBS devuelve el resultado del comando al autor de la llamada y, a continuación, continúa con el procesamiento de los comandos TBS pendientes. El código de administración de energía de TBS se ejecuta de forma asincrónica, por lo que puede controlar las solicitudes de administración de energía incluso si el TPM está procesando un comando largo.

Cuando un equipo entra en estados de suspensión, incluidos S3 (suspensión) y S4 (hibernación), el TPM se apaga. Por lo tanto, se pierden todos los estados de TPM no persistentes. Antes de entrar en estos estados, se espera que el software de la aplicación se prepare para la pérdida de estados de TPM volátiles. Cuando el sistema vuelve de un estado de suspensión, el TBS se sincroniza con el TPM para que el estado de TBS sea coherente con el estado de TPM. Es posible que el software de la aplicación tenga que volver a emitir los comandos que se interrumpieron.

 

 




