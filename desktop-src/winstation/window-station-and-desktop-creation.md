---
title: Creación de estación de ventana y escritorio
description: El sistema crea automáticamente la estación de ventana interactiva.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358976"
---
# <a name="window-station-and-desktop-creation"></a>Creación de estación de ventana y escritorio

El sistema crea automáticamente la estación de ventana interactiva. Cuando un usuario interactivo inicia sesión, el sistema asocia la estación de ventana interactiva con la sesión de inicio de sesión del usuario. El sistema también crea el escritorio de entrada predeterminado para la estación de ventana interactiva ( \\ valor predeterminado de Winsta0). Los procesos iniciados por el usuario que ha iniciado sesión están asociados al \\ escritorio predeterminado de Winsta0.

Un proceso puede usar la función [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) para crear una nueva estación de ventana y la función **CreateDesktop** o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) para crear un nuevo escritorio. El número de escritorios que se pueden crear está limitado por el tamaño del montón de escritorio del sistema. Para obtener más información, vea [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).

Cuando un proceso no interactivo, como una aplicación de servicio intenta conectarse a una estación de ventana y no existe ninguna estación de ventana para la sesión de inicio de sesión de proceso, el sistema intenta crear una estación de ventana y un escritorio para la sesión. El nombre de la estación de ventana creada se basa en el identificador de la sesión de inicio de sesión y el nombre del escritorio es default, tal como se describe aquí:

-   Si un servicio se ejecuta en el contexto de seguridad de la cuenta LocalSystem pero no incluye el \_ atributo de proceso interactivo de servicio \_ , usa la estación de ventana y el escritorio siguientes: Service-0X0-3e7 $ \\ default. Esta estación de ventana no es interactiva, por lo que el servicio no puede mostrar una interfaz de usuario. Además, los procesos creados por el servicio no pueden mostrar una interfaz de usuario.
-   Si el servicio se ejecuta en el contexto de seguridad de una cuenta de usuario, el nombre de la estación de ventana se basa en el SID de usuario Service-0x *Z1* - *Z2*$, donde *Z1* es la parte alta del SID de inicio de sesión y *Z2* es la parte baja del SID de inicio de sesión. Dado que un SID es único para la sesión de inicio de sesión, dos servicios que se ejecutan en el mismo contexto de seguridad reciben estaciones de ventana únicas. Estas estaciones de ventana no son interactivas.

La lista de control de acceso discrecional (DACL) de la estación de ventana y el escritorio incluyen los siguientes derechos de acceso para la cuenta de usuario del servicio:

Estación de ventana:

<dl> WINSTA \_ ACCESSCLIPBOARD  
WINSTA \_ ACCESSGLOBALATOMS  
WINSTA \_ CREATEDESKTOP  
WINSTA \_ EXITWINDOWS  
WINSTA \_ READATTRIBUTES  
\_derechos estándar \_ requeridos  
</dl>

Escritorio:

<dl> ESCRITORIO \_ CREATEMENU  
CREATEWINDOW de escritorio \_  
\_enumerar escritorio  
ESCRITORIO \_ HOOKCONTROL  
ESCRITORIO \_ READOBJECTS  
ESCRITORIO \_ WRITEOBJECTS  
\_derechos estándar \_ requeridos  
</dl>

 

 