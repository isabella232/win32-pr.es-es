---
title: Tareas de mantenimiento de la cuenta de inicio de sesión
description: En este tema se describen los problemas relacionados con las tareas de mantenimiento de la cuenta de inicio de sesión.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- Tareas de mantenimiento de la cuenta de inicio de sesión AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0f11f69d9a974fd666871833029eda0e059329
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104420519"
---
# <a name="logon-account-maintenance-tasks"></a>Tareas de mantenimiento de la cuenta de inicio de sesión

En este tema se describen los problemas relacionados con las tareas de mantenimiento de la cuenta de inicio de sesión.

Hay dos problemas principales que se refieren a las tareas de mantenimiento de la cuenta de inicio de sesión:

-   Actualización de la contraseña de la cuenta para una instancia de servicio que se ejecuta en una cuenta de usuario. Para obtener más información, consulte [cambiar la contraseña en la cuenta de usuario de un servicio](changing-the-password-on-a-serviceampaposs-user-account.md).
-   Control de los cambios en la cuenta de inicio de sesión de una instancia de servicio.

Este último es un caso poco frecuente, pero puede ocurrir. El sistema proporciona la herramienta administrativa administración de equipos que permite cambiar a una cuenta de inicio de sesión de servicio. Además, otras aplicaciones pueden usar la función [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) para especificar una nueva cuenta de inicio de sesión para un servicio instalado. De forma predeterminada, se requieren privilegios de administrador local para cambiar una cuenta de servicio. Si esto ocurriera, podría afectar al servicio de dos maneras:

-   Si ha registrado nombres de entidad de seguridad de servicio (SPN), se registrarán en la cuenta equivocada.
-   Si establece ACE para conceder acceso al servicio, ahora concederá acceso a la cuenta equivocada.

Un enfoque consiste en que el instalador del servicio almacene los SPN registrados para cada instancia de servicio en el registro del equipo host. Puede usar la misma clave del registro en HKEY \_ local \_ Machine que usó para almacenar la cadena de enlace para el SCP de servicio. Cuando se inicia el servicio, llama a la función [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para determinar su cuenta de inicio de sesión y, a continuación, consulta el servidor de Active Directory para determinar si los SPN están registrados en el objeto de directorio de dicha cuenta. Si los SPN no están registrados, o están registrados en la cuenta equivocada, el servicio rechaza el inicio y muestra un mensaje que indica que un administrador de dominio debe ejecutar el programa de configuración del servicio para actualizar la configuración de la cuenta de inicio de sesión. Tenga en cuenta que el administrador debe completar esta reconfiguración porque la cuenta de servicio no debe tener acceso para actualizar su propio SPN. Tenga en cuenta también que se deben quitar los SPN de la cuenta anterior; de lo contrario, los SPN serán inservibles para la autenticación porque no son únicos en el bosque.

 

 