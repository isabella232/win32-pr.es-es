---
description: Normalmente, los servicios son aplicaciones de consola diseñadas para ejecutarse en modo desatendido sin una interfaz gráfica de usuario (GUI).
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Servicios interactivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dda3018b4b37e8c5ee56d67cd1db2c56da9b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912229"
---
# <a name="interactive-services"></a>Servicios interactivos

Normalmente, los servicios son aplicaciones de consola diseñadas para ejecutarse en modo desatendido sin una interfaz gráfica de usuario (GUI). Sin embargo, algunos servicios pueden requerir una interacción ocasional con un usuario. En esta página se describen las mejores formas de interactuar con el usuario desde un servicio.

> [!IMPORTANT]
> Los servicios no pueden interactuar directamente con un usuario a partir de Windows Vista. Por lo tanto, las técnicas mencionadas en la sección titulada uso de un servicio interactivo no deben usarse en el código nuevo.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Interactuar indirectamente con un usuario de un servicio

Puede usar las técnicas siguientes para interactuar con el usuario desde un servicio en todas las versiones compatibles de Windows:

-   Muestra un cuadro de diálogo en la sesión del usuario mediante la función [**WTSSendMessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) .
-   Cree una aplicación independiente de GUI oculta y use la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para ejecutar la aplicación en el contexto del usuario interactivo. Diseñe la aplicación de GUI para comunicarse con el servicio a través de algún método de comunicación entre procesos (IPC), por ejemplo, canalizaciones con nombre. El servicio se comunica con la aplicación GUI para indicarle Cuándo se debe mostrar la GUI. La aplicación comunica los resultados de la interacción del usuario de nuevo con el servicio para que el servicio pueda realizar la acción adecuada. Tenga en cuenta que IPC puede exponer las interfaces de servicio a través de la red a menos que utilice una lista de control de acceso (ACL) adecuada.

    Si este servicio se ejecuta en un sistema multiusuario, agregue la aplicación a la siguiente clave para que se ejecute en cada sesión: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**. Si la aplicación usa canalizaciones con nombre para IPC, el servidor puede distinguir entre varios procesos de usuario al asignar a cada canalización un nombre único basado en el ID. de sesión.

La técnica siguiente también está disponible para Windows Server 2003 y Windows XP:

-   Para mostrar un cuadro de mensaje, llame a la función [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) con la **\_ \_ notificación de servicio MB**. Esto se recomienda para mostrar mensajes de estado sencillos. No llame a **MessageBox** durante la inicialización del servicio o desde la rutina [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) , a menos que lo llame desde un subproceso independiente, de modo que vuelva al SCM de manera oportuna.

## <a name="using-an-interactive-service"></a>Uso de un servicio interactivo

De forma predeterminada, los servicios usan una [estación de ventana](/windows/desktop/winstation/window-stations) no interactiva y no pueden interactuar con el usuario. Sin embargo, un *servicio interactivo* puede mostrar una interfaz de usuario y recibir datos proporcionados por el usuario.

> [!Caution]  
> Los servicios que se ejecutan en un contexto de seguridad elevado, como la cuenta LocalSystem, no deben crear una ventana en el escritorio interactivo porque cualquier otra aplicación que se ejecute en el escritorio interactivo puede interactuar con esta ventana. Esto expone el servicio a cualquier aplicación que ejecute un usuario que haya iniciado sesión. Además, los servicios que se ejecutan como LocalSystem no deben tener acceso al escritorio interactivo mediante una llamada a la función [**OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) o [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) .

 

Para crear un servicio interactivo, haga lo siguiente al llamar a la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) :

1.  Especifique NULL para el parámetro *lpServiceStartName* para ejecutar el servicio en el contexto de la [cuenta LocalSystem](localsystem-account.md).
2.  Especifique el marcador de **\_ \_ proceso interactivo de servicio** .

Para determinar si un servicio se ejecuta como un servicio interactivo, llame a la función [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) para recuperar un identificador de la estación de ventana y la función [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) para comprobar si la estación de ventana tiene el atributo **\_ visible de WSF** .

Sin embargo, tenga en cuenta que la siguiente clave del registro contiene un valor, **NoInteractiveServices**, que controla el efecto del \_ proceso interactivo de servicio \_ :

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Windows**

El valor predeterminado de **NoInteractiveServices** es 1, lo que significa que no se permite que ningún servicio se ejecute de forma interactiva, independientemente de si tiene un **\_ \_ proceso interactivo de servicio**. Cuando **NoInteractiveServices** se establece en 0, se permite que los servicios con el **\_ \_ proceso interactivo de servicio** se ejecuten de forma interactiva.

**Windows 7, Windows server 2008 R2, Windows XP y Windows server 2003:** El valor predeterminado de **NoInteractiveServices** es 0, lo que significa que los servicios con el **\_ \_ proceso interactivo de servicio** pueden ejecutarse de forma interactiva. Cuando **NoInteractiveServices** se establece en un valor distinto de cero, no se permite que ningún servicio iniciado después se ejecute de forma interactiva, independientemente de si tiene un **\_ \_ proceso interactivo de servicio**.

> [!IMPORTANT]
> Todos los servicios se ejecutan en Terminal Services sesión 0. Por lo tanto, si un servicio interactivo muestra una interfaz de usuario, solo es visible para el usuario que se conectó a la sesión 0. Dado que no hay ninguna manera de garantizar que el usuario interactivo esté conectado a la sesión 0, no configure un servicio para que se ejecute como un servicio interactivo en Terminal Services o en un sistema que admita el cambio rápido de usuario (el cambio rápido de usuario se implementa mediante Terminal Services).

 

 

 
