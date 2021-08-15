---
title: Tareas de mantenimiento de cuentas de inicio de sesión
description: En este tema se describen los problemas relacionados con las tareas de mantenimiento de la cuenta de inicio de sesión.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- Tareas de mantenimiento de cuentas de inicio de sesión ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d026f37ad81d71691ac418ea49b1b0fda5e1d09fb3e4b6e2259083eb80ada9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186637"
---
# <a name="logon-account-maintenance-tasks"></a>Tareas de mantenimiento de cuentas de inicio de sesión

En este tema se describen los problemas relacionados con las tareas de mantenimiento de la cuenta de inicio de sesión.

Hay dos problemas principales que se refieren a las tareas de mantenimiento de la cuenta de inicio de sesión:

-   Actualización de la contraseña de cuenta para una instancia de servicio que se ejecuta en una cuenta de usuario. Para obtener más información, [consulte Cambio de la contraseña en la cuenta de usuario de un servicio.](changing-the-password-on-a-serviceampaposs-user-account.md)
-   Controlar los cambios en la cuenta de inicio de sesión de una instancia de servicio.

Este último es un caso poco frecuente, pero puede ocurrir. El sistema proporciona la herramienta administrativa Administración de equipos que permite cambiar a una cuenta de inicio de sesión de servicio. Además, otras aplicaciones pueden usar la [**función ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) para especificar una nueva cuenta de inicio de sesión para un servicio instalado. De forma predeterminada, se requieren privilegios de administrador local para cambiar una cuenta de servicio. Si esto ocurriera, podría afectar al servicio de dos maneras:

-   Si ha registrado nombres de entidad de seguridad de servicio (SPN), se registrarán en la cuenta incorrecta.
-   Si establece las ACE para conceder acceso al servicio, ahora concederían acceso a la cuenta incorrecta.

Un enfoque es hacer que el instalador de servicio almacene los SPN registrados para cada instancia de servicio en el registro en el equipo host. Puede usar la misma clave del Registro en HKEY LOCAL MACHINE que usó para almacenar la \_ cadena de enlace para el SCP del \_ servicio. Cuando se inicia el servicio, llama a la función [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para determinar su cuenta de inicio de sesión y, a continuación, consulta al servidor Active Directory para determinar si los SPN están registrados en el objeto de directorio de esa cuenta. Si los SPN no están registrados o están registrados en una cuenta incorrecta, el servicio se niega a iniciarse y muestra un mensaje que indica que un administrador de dominio debe ejecutar el programa de configuración del servicio para actualizar la configuración de la cuenta de inicio de sesión. Tenga en cuenta que un administrador debe completar esta reconfiguración porque la cuenta de servicio no debe tener acceso para actualizar su propio SPN. Tenga en cuenta también que los SPN deben quitarse de la cuenta anterior; de lo contrario, los SPN no serán útiles para la autenticación porque no son únicos en el bosque.

 

 