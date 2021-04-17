---
title: Programación de comandos
description: Cada comando tiene una prioridad asociada.
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06512f0748aa88f6b32de3291e2ed1c262212ba2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665677"
---
# <a name="command-scheduling"></a>Programación de comandos

## <a name="command-scheduling"></a>Programación de comandos

Los comandos se pueden enviar a TBS desde varios contextos en cualquier momento. Sin embargo, un TPM físico solo puede procesar un comando cada vez y algunos comandos pueden ejecutarse durante un período de tiempo considerable. Cuando hay varios comandos pendientes, el TBS decide qué comando se va a enviar a TPM. Cuando se envía un comando, cada comando tiene una prioridad asociada. TBS usa estas prioridades para determinar qué comando pendiente debe enviar siempre que el TPM sea gratuito. Los cuatro niveles de prioridad son baja, normal, alta y sistema. Las aplicaciones deben usar prioridad baja, normal o alta. Aunque los comandos de prioridad alta normalmente se ejecutan antes que los comandos de prioridad baja, el programador de comandos de TBS tiene una directiva de caducidad que finalmente proporciona prioridad muy alta a los comandos que se han bloqueado durante períodos de tiempo importantes.

## <a name="context-management"></a>Administración de contexto

Cuando \_ se envía un comando SaveContext o TPM2 de TPM con un identificador virtual a un recurso que administra TBS, el TBS ejecuta el comando adecuado en el recurso físico y devuelve el resultado al llamador si el recurso está físicamente presente en el TPM. Si el recurso no está físicamente presente en el TPM, el preprocesamiento del \_ comando SaveContext o ContextSave de TPM2 de TPM \_ provoca que se vuelva a cargar el recurso, momento en el que el contexto se guardará y se devolverá al autor de la llamada. Si el recurso que se está guardando es de un tipo que normalmente se vacía automáticamente desde el TPM después de guardar, el TBS invalida el recurso virtual al completarse este comando. Cuando \_ se envía un comando LoadContext o TPM2 de TPM \_ a TBS, el TBS ejecuta el comando inmediatamente. Si el comando se completa correctamente, el TBS virtualiza el identificador de recursos y pasa la secuencia de bytes de TPM resultante al llamador. Cuando \_ se envía un comando FlushSpecific o TPM2 de TPM \_ con un identificador virtual a un recurso que administra TBS, el TBS ejecuta un \_ comando TPM FlushSpecific o TPM2 \_ FlushContext para expulsar el recurso del TPM, si está presente físicamente. En este caso, el TBS invalida el recurso virtual y devuelve el resultado del comando FLUSH al llamador. Si el recurso no está físicamente presente en el TPM, el preprocesamiento del \_ comando FlushSpecific de TPM o de TPM2 \_ FlushContext cargará el recurso correspondiente al identificador virtual, pero se vaciará cuando el comando se procese realmente. TBS no admite el \_ bit KeyControlOwner de TPM o la funcionalidad keepHandle de la \_ operación LOADCONTEXT de TPM, por lo que no asignará a un recurso el mismo identificador que tenía antes de que se guardara el contexto.

## <a name="other-commands"></a>Otros comandos

Los comandos que no se mencionan en esta documentación se procesan reemplazando los identificadores de clave virtual por los identificadores de clave física (si es necesario) y enviándolos al TPM. Esto se hace después de realizar las operaciones adecuadas para asegurarse de que los recursos que se están usando están físicamente presentes en el TPM. No se realiza ningún procesamiento especial adicional. TBS no intenta mejorar la fidelidad de la virtualización mediante la modificación de los datos que se devuelven desde el TPM como parte de una \_ consulta GetCapabilities de TPM o de TPM2 \_ GetCapability. TBS también admite comandos de presencia física de TCG. TBS actúa como un paso para los comandos de presencia física; el propio TBS no realiza ningún procesamiento especial.

## <a name="cleanup"></a>Limpieza

Cuando se cierra un contexto, se limpian todos los recursos físicos y virtuales asociados a él, por lo que ya no consumen recursos del sistema.

 

 




