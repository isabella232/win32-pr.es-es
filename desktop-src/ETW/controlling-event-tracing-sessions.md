---
description: Las sesiones de seguimiento de eventos registran eventos de uno o varios proveedores.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controlar sesiones de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970eb160812991677aac775af60d08458c269152edca4aa2e30cdf30c111d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130665"
---
# <a name="controlling-event-tracing-sessions"></a>Controlar sesiones de seguimiento de eventos

Las sesiones de seguimiento de eventos registran eventos de uno o varios [proveedores.](providing-events.md) El controlador define la sesión y habilita los proveedores. La definición de la sesión normalmente incluye especificar el nombre de archivo de sesión y de registro, el tipo de archivo de registro que se usará y la resolución de la marca de tiempo utilizada para registrar los eventos. Los controladores también pueden actualizar y consultar sesiones de seguimiento de eventos.

En los temas siguientes se muestra cómo definir y actualizar una sesión, y cómo habilitar proveedores de seguimiento de eventos:

-   [Configuración e inicio de una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
-   [Configuración e inicio de una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configuración e inicio de una sesión de Registrador automático](configuring-and-starting-an-autologger-session.md)
-   [Configuración e inicio de una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
-   [Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
-   [Recuperación de datos adicionales de seguimiento de eventos](retrieving-additional-event-tracing-data.md)

Para obtener información sobre cómo vaciar y consultar sesiones, vea [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) y [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectivamente.

Solo los usuarios que se ejecutan con privilegios administrativos elevados, los usuarios del grupo Usuarios del registro de rendimiento y las aplicaciones que se ejecutan como LocalSystem, LocalService o NetworkService pueden controlar las sesiones de seguimiento de eventos. Para conceder a un usuario restringido la capacidad de controlar las sesiones de seguimiento, agrétrelas al grupo Usuarios del registro de rendimiento.

**Windows XP y Windows 2000:** Cualquiera puede controlar una sesión de seguimiento.

 

 
