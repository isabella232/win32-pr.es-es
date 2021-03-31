---
title: Estaciones de ventana y funciones de escritorio
description: Las aplicaciones pueden utilizar las siguientes funciones con objetos de la estación de ventana.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6665f52de1f7f57930105edb0063c4512e375ac3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791667"
---
# <a name="window-station-and-desktop-functions"></a>Estaciones de ventana y funciones de escritorio

Las aplicaciones pueden utilizar las siguientes funciones con objetos de la [estación de ventana](window-stations.md) .



| Función                                                     | Descripción                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Cierra un identificador de estación de ventana abierta.                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Crea un objeto de estación de ventana, lo asocia al proceso actual y lo asigna a la sesión actual. |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Enumera todas las estaciones de ventana de la sesión actual.                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Recupera un identificador de la estación de ventana actual para el proceso que realiza la llamada.                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Recupera información sobre la estación de ventana especificada o el objeto de escritorio.                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Recupera información de seguridad para la estación de ventana o el objeto de escritorio especificados.                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Abre la estación de ventana especificada.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Asigna la estación de ventana especificada al proceso que realiza la llamada.                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Establece información sobre la estación de ventana especificada o el objeto de escritorio.                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Establece la información de seguridad para la estación de ventana especificada o el objeto de escritorio.                                   |



 

Las aplicaciones pueden utilizar las siguientes funciones con objetos de [escritorio](desktops.md) .



| Función                                                     | Descripción                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Cierra un identificador abierto a un objeto de escritorio.                                                                                         |
| [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Crea un nuevo escritorio, lo asocia a la estación de ventana actual del proceso que realiza la llamada y lo asigna al subproceso que realiza la llamada. |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Crea un nuevo escritorio, lo asocia a la estación de ventana actual del proceso que realiza la llamada y lo asigna al subproceso que realiza la llamada. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Enumera todos los equipos de escritorio asociados a la estación de ventana actual del proceso de llamada.                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Enumera todas las ventanas de nivel superior asociadas al escritorio especificado.                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Recupera un identificador del escritorio asignado al subproceso especificado.                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Obtiene información sobre una estación de ventana o un objeto de escritorio.                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Obtiene información de seguridad para una estación de ventana o un objeto de escritorio.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Abre el objeto de escritorio especificado.                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Abre el escritorio que recibe los datos proporcionados por el usuario.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Asigna el escritorio especificado al subproceso que realiza la llamada.                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Establece información sobre una estación de ventana o un objeto de escritorio.                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Establece la información de seguridad para una estación de ventana o un objeto de escritorio.                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Hace que un escritorio esté visible y lo activa. Esto permite al escritorio recibir la entrada del usuario.                                 |



 

 

 