---
title: Administración de energía (servicios base de TPM)
description: El TBS recibe los eventos de administración de energía.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "105665771"
---
# <a name="power-management-tpm-base-services"></a>Administración de energía (servicios base de TPM)

El TBS recibe los eventos de administración de energía. Cuando se recibe una indicación de que el TPM u otras partes de la plataforma están a punto de entrar en un estado de energía en el que se interrumpirá la ejecución o se perderá el estado de TPM, el TBS realiza comprobaciones para determinar si es probable que finalice el comando que se está ejecutando antes de que el sistema se apague. En general, el TBS permite finalizar los comandos de duración corta y media, pero cancela los comandos de larga duración. Una vez que se ha devuelto el comando, el TBS detiene el envío de nuevos comandos al TPM y se prepara para la hibernación. Cuando se restaura la alimentación, el TBS devuelve el resultado del comando al autor de la llamada y, a continuación, continúa con el procesamiento de los comandos TBS pendientes. El código de administración de energía de TBS se ejecuta de forma asincrónica, por lo que puede controlar las solicitudes de administración de energía, incluso si el TPM está procesando un comando largo.

Cuando un equipo entra en Estados de suspensión, incluido S3 (suspensión) y S4 (hibernación), el TPM se apaga. Por lo tanto, se pierden todos los Estados de TPM no persistentes. Antes de entrar en estos Estados, se espera que el software de aplicación se prepare para la pérdida de Estados de TPM volátiles. Cuando el sistema vuelve de un estado de suspensión, el TBS se sincroniza con el TPM para que el estado de TBS sea coherente con el estado de TPM. Es posible que el software de la aplicación tenga que volver a emitir los comandos que se han interrumpido.

 

 




