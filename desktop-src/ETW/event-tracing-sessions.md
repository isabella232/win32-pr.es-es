---
description: Las sesiones de seguimiento de eventos registran eventos de uno o varios proveedores que un controlador habilita.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Sesiones de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2edfe4bdfaf621575d8f2f8ab7d81a09aae8bfbddcb3f63890c4083378bb905b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083245"
---
# <a name="event-tracing-sessions"></a>Sesiones de seguimiento de eventos

Las sesiones de seguimiento de eventos registran eventos de uno o varios [proveedores](providing-events.md) que un [controlador](controlling-event-tracing-sessions.md) habilita. La sesión también es responsable de administrar y vaciar los búferes. El controlador define la sesión, que normalmente incluye especificar el nombre de archivo de sesión y de registro, el tipo de archivo de registro que se va a usar y la resolución de la marca de tiempo utilizada para registrar los eventos.

Seguimiento de eventos admite un máximo de 64 sesiones de seguimiento de eventos que se ejecutan simultáneamente. De estas sesiones, hay dos sesiones de propósito especial. Las sesiones restantes están disponibles para uso general. Las dos sesiones de propósito especial son:

-   Sesión de registrador global
-   Sesión del registrador de kernel nt

La sesión de seguimiento de eventos del registrador global registra los eventos que se producen al principio del proceso de arranque del sistema operativo, como los generados por los controladores de dispositivos. Para obtener información sobre cómo configurar la sesión de seguimiento de eventos del registrador global, vea [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).

La sesión de seguimiento de eventos del registrador de kernel nt registra eventos del sistema predefinidos generados por el sistema operativo, por ejemplo, eventos de error de E/S de disco o de página. Para obtener información sobre cómo configurar la sesión de seguimiento de eventos del registrador de kernel nt, configure [e inicie la sesión del registrador de kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obtener información sobre cómo definir una sesión de seguimiento de eventos normal, vea [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000:** Solo admite 32 sesiones de seguimiento de eventos.

 

 



