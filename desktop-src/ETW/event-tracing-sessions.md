---
description: Las sesiones de seguimiento de eventos registran eventos de uno o varios proveedores habilitados por un controlador.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Sesiones de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce49453881d9106119dab15b64ac0698e9a493f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911046"
---
# <a name="event-tracing-sessions"></a>Sesiones de seguimiento de eventos

Las sesiones de seguimiento de eventos registran eventos de uno o varios [proveedores](providing-events.md) habilitados por un [controlador](controlling-event-tracing-sessions.md) . La sesión también es responsable de administrar y vaciar los búferes. El controlador define la sesión, que normalmente incluye la especificación de la sesión y el nombre del archivo de registro, el tipo de archivo de registro que se va a usar y la resolución de la marca de tiempo utilizada para registrar los eventos.

El seguimiento de eventos admite un máximo de 64 sesiones de seguimiento de eventos que se ejecutan simultáneamente. De estas sesiones, hay dos sesiones de propósito especial. Las sesiones restantes están disponibles para su uso general. Las dos sesiones de uso especial son:

-   Sesión del registrador global
-   Sesión del registrador del kernel de NT

La sesión de seguimiento de eventos de registrador global registra los eventos que se producen al principio del proceso de arranque del sistema operativo, como los generados por los controladores de dispositivos. Para obtener información sobre la configuración de la sesión de seguimiento de eventos de registrador global, vea [configurar e iniciar la sesión del registrador global](configuring-and-starting-the-global-logger-session.md).

La sesión de seguimiento de eventos del registrador del kernel de NT registra eventos del sistema predefinidos generados por el sistema operativo, por ejemplo, e/s de disco o eventos de error de página. Para obtener información sobre la configuración de la sesión de seguimiento de eventos del registrador del kernel de NT, [Configure e inicie la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obtener información sobre cómo definir una sesión de seguimiento de eventos normal, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000:** Solo admite sesiones de seguimiento de eventos de 32.

 

 



