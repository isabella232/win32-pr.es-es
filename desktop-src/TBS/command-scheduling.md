---
title: Programación de comandos
description: Cada comando tiene una prioridad asociada.
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221702ee9dcebb8da454637f53cc29de1607d03088e24eb4a9a250d4e3ce2512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954443"
---
# <a name="command-scheduling"></a>Programación de comandos

## <a name="command-scheduling"></a>Programación de comandos

Los comandos se pueden enviar a los TBS desde varios contextos en cualquier momento. Sin embargo, un TPM físico solo puede procesar un comando a la vez y algunos comandos se pueden ejecutar durante un período de tiempo significativo. Cuando hay varios comandos pendientes, el TBS decide qué comando enviar al TPM. Cuando se envía un comando, cada comando tiene una prioridad asociada. El TBS usa estas prioridades para determinar qué comando pendiente enviar siempre que el TPM sea gratuito. Los cuatro niveles de prioridad son bajo, normal, alto y sistema. Las aplicaciones deben usar prioridad baja, normal o alta. Aunque los comandos de prioridad alta normalmente se ejecutan antes que los comandos de prioridad baja, el programador de comandos TBS tiene una directiva de edad que finalmente da prioridad muy alta a los comandos que se han bloqueado durante períodos de tiempo significativos.

## <a name="context-management"></a>Administración de contexto

Cuando se envía un comando SaveContext o TPM2 ContextSave de TPM con un identificador virtual a un recurso que el TBS administra, el TBS ejecuta el comando adecuado en el recurso físico y devuelve el resultado al autor de la llamada si el recurso está físicamente presente en \_ el TPM. Si el recurso no está físicamente presente en el TPM, el preprocesamiento del comando SaveContext o TPM2 ContextSave de TPM hace que el recurso se vuelva a cargar, momento en el que el contexto se guardará y se devolverá al autor de la \_ \_ llamada. Si el recurso que se guarda es de un tipo que normalmente se vacía automáticamente del TPM después de guardar, el TBS invalida el recurso virtual tras la finalización de este comando. Cuando se envía un comando LoadContext o TPM2 ContextLoad de TPM a \_ \_ TBS, el TBS ejecuta el comando inmediatamente. Si el comando se completa correctamente, el TBS virtualiza el identificador de recursos y pasa la secuencia de bytes de TPM resultante al autor de la llamada. Cuando se envía un comando FlushSpecific o TPM2 FlushContext de TPM con un identificador virtual a un recurso que el TBS administra, el TBS ejecuta un comando \_ \_ FlushSpecific o \_ TPM2 FlushContext de TPM para expulsar el recurso del TPM si está físicamente \_ presente. En este caso, TBS invalida el recurso virtual y devuelve el resultado del comando flush al autor de la llamada. Si el recurso no está físicamente presente en el TPM, el preprocesamiento del comando FlushSpecific o TPM2 FlushContext cargará el recurso correspondiente al identificador virtual, pero se vaciará cuando el comando se procese \_ \_ realmente. El TBS no admite el bit KeyControlOwner de TPM ni la funcionalidad keepHandle de la operación LoadContext de TPM, por lo que no dará a un recurso el mismo identificador que tenía antes de guardar el \_ \_ contexto.

## <a name="other-commands"></a>Otros comandos

Los comandos que no se mencionan en esta documentación se procesan reemplazando los identificadores de clave virtual por identificadores de clave física (si es necesario) y enviándolos al TPM. Esto se hace después de realizar las operaciones adecuadas para asegurarse de que los recursos que se usan están físicamente presentes en el TPM. No se realiza ningún procesamiento especial adicional. El TBS no intenta mejorar la fidelidad de la virtualización modificando los datos pasados desde el TPM como parte de una consulta \_ GetCapabilities o \_ GetCapability de TPM2. TBS también admite comandos de presencia física de TCG. El TBS actúa como paso a través para los comandos de presencia física; el propio TBS no realiza ningún procesamiento especial.

## <a name="cleanup"></a>Limpieza

Cuando se cierra un contexto, todos los recursos físicos y virtuales asociados a él se limpian para que ya no consuman recursos del sistema.

 

 




