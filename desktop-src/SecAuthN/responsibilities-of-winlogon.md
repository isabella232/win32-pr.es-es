---
description: Enumera y explica las responsabilidades de Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Responsabilidades de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6561bea11c48eb474c0ff56c5c0aa5ebfa0c22d9d6689aa55a6a208bbbc683e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919033"
---
# <a name="responsibilities-of-winlogon"></a>Responsabilidades de Winlogon

[*Winlogon*](../secgloss/w-gly.md) tiene las siguientes responsabilidades:

-   Estación de ventana y protección de escritorio

    Winlogon establece la protección de la estación de ventana y los escritorios correspondientes para asegurarse de que cada uno sea accesible correctamente. En general, esto significa que el sistema local tendrá acceso total a estos objetos y que un usuario que inició sesión interactivamente tendrá acceso de lectura al objeto de estación de ventana y acceso completo al objeto de escritorio de la aplicación.

-   Reconocimiento de SAS estándar

    Winlogon tiene enlaces especiales en el servidor User32 que le [](../secgloss/s-gly.md) permiten supervisar eventos de secuencia de atención segura (SAS) CTRL+ALT+SUPR. Winlogon pone esta información de eventos de SAS a disposición de los EBAA para su uso como SAS o como parte de su SAS. En general, los ADA deben supervisar los SAS por sí solos; Sin embargo, cualquier [*GINA*](../secgloss/g-gly.md) que tenga la SAS estándar CTRL+ALT+SUPR como uno de los SAS que reconoce debe usar la compatibilidad con Winlogon proporcionada para este propósito.

-   Distribución rutinaria de SAS

    Cuando Winlogon encuentra un evento de SAS o cuando la GINA entrega una SAS a Winlogon, Winlogon establece el estado en consecuencia, cambia en el escritorio de Winlogon y llama a una de las funciones de procesamiento sas de la GINA.

-   Carga de perfiles de usuario

    Cuando los usuarios inician sesión, sus perfiles de usuario se cargan en el Registro. De esta manera, los procesos del usuario pueden usar la clave especial del Registro HKEY \_ CURRENT \_ USER. Winlogon hace esto automáticamente después de un inicio de sesión correcto, pero antes de la activación del shell para el usuario que acaba de iniciar sesión.

-   Asignación de seguridad al shell de usuario

    Cuando un usuario inicia sesión, la GINA es responsable de crear uno o varios procesos iniciales para ese usuario. Winlogon proporciona una función de soporte técnico para que la GINA aplique la seguridad del usuario que acaba de iniciar sesión a estos procesos. Sin embargo, la manera preferida de hacerlo es que la GINA llame a la función Windows [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)y permita que el sistema proporcione el servicio.

-   Control protector de pantalla

    Winlogon supervisa la actividad del teclado y del mouse para determinar cuándo activar los protectores de pantalla. Una vez activado el protector de pantalla, Winlogon continúa supervisando la actividad del teclado y del mouse para determinar cuándo finalizar el protector de pantalla. Si el protector de pantalla está marcado como seguro, Winlogon trata la estación de trabajo como bloqueada. Cuando hay actividad de mouse o teclado, Winlogon invoca la función [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) de la GINA y se reanuda el comportamiento de la estación de trabajo bloqueada. Si el protector de pantalla no es seguro, cualquier actividad de teclado o mouse finaliza el protector de pantalla sin notificación a la GINA.

-   Compatibilidad con varios proveedores de red

    Varias redes instaladas en un sistema Windows se pueden incluir en el proceso de autenticación y en las operaciones de actualización de contraseñas. Esta inclusión permite a las redes adicionales recopilar información de identificación y autenticación a la vez durante el inicio de sesión normal, mediante el escritorio seguro de Winlogon. Algunos de los parámetros necesarios en los servicios winlogon disponibles para las EBAA admiten explícitamente estos proveedores de red adicionales.

 

 
