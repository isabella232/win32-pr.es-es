---
description: Las sesiones de seguimiento de eventos registran eventos de uno o más proveedores.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controlar sesiones de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984519"
---
# <a name="controlling-event-tracing-sessions"></a>Controlar sesiones de seguimiento de eventos

Las sesiones de seguimiento de eventos registran eventos de uno o más [proveedores](providing-events.md). El controlador define la sesión y habilita los proveedores. La definición de la sesión suele incluir la especificación de la sesión y el nombre del archivo de registro, el tipo de archivo de registro que se va a usar y la resolución de la marca de tiempo utilizada para registrar los eventos. Los controladores también pueden actualizar y consultar sesiones de seguimiento de eventos.

En los temas siguientes se muestra cómo definir y actualizar una sesión y habilitar los proveedores de seguimiento de eventos:

-   [Configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
-   [Configurar e iniciar una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md)
-   [Configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
-   [Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
-   [Recuperación de datos de seguimiento de eventos adicionales](retrieving-additional-event-tracing-data.md)

Para obtener información sobre cómo vaciar y consultar sesiones, vea [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) y [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectivamente.

Solo los usuarios que ejecutan con privilegios administrativos elevados, los usuarios del grupo usuarios del registro de rendimiento y las aplicaciones que se ejecutan como LocalSystem, LocalService o NetworkService pueden controlar las sesiones de seguimiento de eventos. Para conceder a un usuario restringido la capacidad de controlar las sesiones de seguimiento, agréguelas al grupo usuarios del registro de rendimiento.

**Windows XP y windows 2000:** Cualquier persona puede controlar una sesión de seguimiento.

 

 
