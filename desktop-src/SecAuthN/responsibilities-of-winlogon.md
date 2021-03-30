---
description: Enumera y explica las responsabilidades de Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Responsabilidades de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7842df1d4194dc7086f658a13f6725af8fa0d88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001854"
---
# <a name="responsibilities-of-winlogon"></a>Responsabilidades de Winlogon

[*Winlogon*](../secgloss/w-gly.md) tiene las siguientes responsabilidades:

-   Estación de ventana y protección de escritorio

    Winlogon establece la protección de la estación de ventana y los escritorios correspondientes para asegurarse de que cada una sea accesible correctamente. En general, esto significa que el sistema local tendrá acceso completo a estos objetos y que un usuario que haya iniciado sesión de forma interactiva tendrá acceso de lectura al objeto de la estación de ventana y acceso completo al objeto de escritorio de la aplicación.

-   Reconocimiento de SAS estándar

    Winlogon tiene enlaces especiales en el servidor user32 que le permiten supervisar los eventos de la secuencia de [*atención segura*](../secgloss/s-gly.md) (SAS) de Ctrl + Alt + Supr. Winlogon hace que esta información de eventos de SAS esté disponible para que GINA la use como SAS o como parte de su SAS. En general, GINAs debe supervisar SASs por sí mismo; sin embargo, cualquier [*Gina*](../secgloss/g-gly.md) que tenga la SAS estándar Ctrl + Alt + Supr como uno de los Sass que reconoce debe usar la compatibilidad con Winlogon proporcionada para este fin.

-   Envío de rutinas SAS

    Cuando Winlogon encuentra un evento de SAS o cuando se entrega una SAS a Winlogon mediante GINA, Winlogon establece el estado en consecuencia, cambia en el escritorio de Winlogon y llama a una de las funciones de procesamiento de SAS de GINA.

-   Carga de perfiles de usuario

    Cuando los usuarios inician sesión, sus perfiles de usuario se cargan en el registro. De esta manera, los procesos del usuario pueden usar la clave especial del registro HKEY \_ Current \_ User. Winlogon realiza esta operación automáticamente después de un inicio de sesión correcto, pero antes de la activación del shell para el usuario que acaba de iniciar sesión.

-   Asignación de seguridad al shell de usuario

    Cuando un usuario inicia sesión, GINA es responsable de crear uno o más procesos iniciales para ese usuario. Winlogon proporciona una función de soporte técnico para que GINA aplique la seguridad del usuario que ha iniciado sesión recientemente a estos procesos. Sin embargo, la mejor manera de hacerlo es que GINA llame a la función de Windows [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)y permita que el sistema proporcione el servicio.

-   Control de protector de pantalla

    Winlogon supervisa la actividad del teclado y del mouse para determinar cuándo se deben activar los protectores de pantalla. Una vez activado el protector de pantalla, Winlogon continúa supervisando la actividad del teclado y del mouse para determinar cuándo terminar el protector de pantalla. Si el protector de pantalla está marcado como seguro, Winlogon trata la estación de trabajo como bloqueada. Cuando hay actividad del mouse o del teclado, Winlogon invoca la función [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) de los currículos de Gina y el comportamiento de la estación de trabajo bloqueado. Si el protector de pantalla no es seguro, cualquier actividad del teclado o del mouse finaliza el protector de pantalla sin notificación a GINA.

-   Compatibilidad con varios proveedores de redes

    En el proceso de autenticación y en las operaciones de actualización de contraseñas se pueden incluir varias redes instaladas en un sistema Windows. Esta inclusión permite que las redes adicionales recopilen la información de identificación y autenticación todos a la vez durante el inicio de sesión normal, mediante el escritorio seguro de Winlogon. Algunos de los parámetros necesarios en los servicios de Winlogon disponibles para GINAs admiten explícitamente estos proveedores de red adicionales.

 

 
