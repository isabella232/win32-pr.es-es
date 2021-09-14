---
description: Enumera y explica las responsabilidades de Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Responsabilidades de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7842df1d4194dc7086f658a13f6725af8fa0d88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259620"
---
# <a name="responsibilities-of-winlogon"></a>Responsabilidades de Winlogon

[*Winlogon*](../secgloss/w-gly.md) tiene las siguientes responsabilidades:

-   Estación de ventana y protección de escritorio

    Winlogon establece la protección de la estación de ventana y los escritorios correspondientes para asegurarse de que cada uno sea accesible correctamente. En general, esto significa que el sistema local tendrá acceso total a estos objetos y que un usuario que ha iniciado sesión de forma interactiva tendrá acceso de lectura al objeto de estación de ventana y acceso completo al objeto de escritorio de la aplicación.

-   Reconocimiento de SAS estándar

    Winlogon tiene enlaces especiales en el servidor User32 que le [](../secgloss/s-gly.md) permiten supervisar eventos de secuencia de atención segura (SAS) CTRL+ALT+SUPR. Winlogon pone esta información de eventos de SAS a disposición de los ÚSA para su uso como SAS o como parte de su SAS. En general, los ADA deben supervisar los SAS por su cuenta; sin embargo, cualquier [*GINA*](../secgloss/g-gly.md) que tenga la SAS estándar CTRL+ALT+SUPR como uno de los SAS que reconoce debe usar la compatibilidad con Winlogon proporcionada para este propósito.

-   Envío de rutinas de SAS

    Cuando Winlogon encuentra un evento de SAS o cuando la GINA entrega una SAS a Winlogon, Winlogon establece el estado en consecuencia, cambia en el escritorio de Winlogon y llama a una de las funciones de procesamiento sas de la GINA.

-   Carga de perfiles de usuario

    Cuando los usuarios inician sesión, sus perfiles de usuario se cargan en el registro. De esta manera, los procesos del usuario pueden usar la clave del Registro especial HKEY \_ CURRENT \_ USER. Winlogon hace esto automáticamente después de un inicio de sesión correcto, pero antes de la activación del shell para el usuario que acaba de iniciar sesión.

-   Asignación de seguridad al shell de usuario

    Cuando un usuario inicia sesión, la GINA es responsable de crear uno o varios procesos iniciales para ese usuario. Winlogon proporciona una función de soporte técnico para que GINA aplique la seguridad del usuario que acaba de iniciar sesión a estos procesos. Sin embargo, la manera preferida de hacerlo es que GINA llame a la función Windows [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)y permita que el sistema proporcione el servicio.

-   Control de protector de pantalla

    Winlogon supervisa la actividad del teclado y del mouse para determinar cuándo activar los protectores de pantalla. Una vez activado el protector de pantalla, Winlogon continúa supervisando la actividad del teclado y del mouse para determinar cuándo finalizar el protector de pantalla. Si el protector de pantalla está marcado como seguro, Winlogon trata la estación de trabajo como bloqueada. Cuando hay actividad de mouse o teclado, Winlogon invoca la función [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) de la GINA y se reanuda el comportamiento de la estación de trabajo bloqueada. Si el protector de pantalla no es seguro, cualquier actividad de teclado o mouse finaliza el protector de pantalla sin notificación al GINA.

-   Compatibilidad con varios proveedores de red

    En el proceso de autenticación y en las operaciones de actualización de contraseñas se pueden incluir varias redes instaladas en un Windows sistema de autenticación. Esta inclusión permite que redes adicionales recopile información de identificación y autenticación a la vez durante el inicio de sesión normal, mediante el escritorio seguro de Winlogon. Algunos de los parámetros necesarios en los servicios winlogon disponibles para las EDA admiten explícitamente estos proveedores de red adicionales.

 

 
