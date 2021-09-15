---
title: Estación de ventana y creación de escritorio
description: El sistema crea automáticamente la estación de ventana interactiva.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359943"
---
# <a name="window-station-and-desktop-creation"></a>Estación de ventana y creación de escritorio

El sistema crea automáticamente la estación de ventana interactiva. Cuando un usuario interactivo inicia sesión, el sistema asocia la estación de ventana interactiva con la sesión de inicio de sesión del usuario. El sistema también crea el escritorio de entrada predeterminado para la estación de ventana interactiva (valor predeterminado de \\ Winsta0). Los procesos iniciados por el usuario que inició sesión están asociados al escritorio predeterminado de \\ Winsta0.

Un proceso puede usar la [**función CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) para crear una nueva estación de ventana y la **función CreateDesktop** o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) para crear un nuevo escritorio. El número de escritorios que se pueden crear está limitado por el tamaño del montón de escritorio del sistema. Para obtener más información, vea [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).

Cuando un proceso no interactivo, como una aplicación de servicio, intenta conectarse a una estación de ventana y no existe ninguna estación de ventana para la sesión de inicio de sesión del proceso, el sistema intenta crear una estación de ventana y un escritorio para la sesión. El nombre de la estación de ventana creada se basa en el identificador de sesión de inicio de sesión y el escritorio se denomina predeterminado, como se describe aquí:

-   Si un servicio se ejecuta en el contexto de seguridad de la cuenta LocalSystem pero no incluye el atributo SERVICE INTERACTIVE PROCESS, usa la siguiente estación de ventana y \_ \_ escritorio: Service-0x0-3e7$ \\ predeterminado. Esta estación de ventana no es interactiva, por lo que el servicio no puede mostrar una interfaz de usuario. Además, los procesos creados por el servicio no pueden mostrar una interfaz de usuario.
-   Si el servicio se ejecuta en el contexto de seguridad de una cuenta de usuario, el nombre de la estación de ventana se basa en el sid de usuario Service-0x *Z1* - *Z2*$, donde *Z1* es la parte alta del SID de inicio de sesión y *Z2* es la parte baja del SID de inicio de sesión. Dado que un SID es único para la sesión de inicio de sesión, dos servicios que se ejecutan en el mismo contexto de seguridad reciben estaciones de ventana únicas. Estas estaciones de ventana no son interactivas.

La lista de control de acceso discrecional (DACL) para la estación de ventana y el escritorio incluye los siguientes derechos de acceso para la cuenta de usuario del servicio:

Estación de ventana:

<dl> WINSTA \_ ACCESSCLIPBOARD  
ACCESO \_ WINSTAGLOBALATOMS  
WINSTA \_ CREATEDESKTOP  
WINSTA \_ EXITWINDOWS  
WINSTA \_ READATTRIBUTES  
DERECHOS \_ ESTÁNDAR \_ REQUERIDOS  
</dl>

Escritorio:

<dl> DESKTOP \_ CREATEMENU  
DESKTOP \_ CREATEWINDOW  
ENUMERACIÓN \_ DE ESCRITORIO  
DESKTOP \_ HOOKCONTROL  
\_READOBJECTS DE ESCRITORIO  
OBJETOS \_ WRITEOBJECT DE ESCRITORIO  
DERECHOS \_ ESTÁNDAR \_ REQUERIDOS  
</dl>

 

 