---
title: Funciones de escritorio y estación de ventana
description: Las aplicaciones pueden usar las siguientes funciones con objetos de estación de ventana.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccda67841508081444f7025e457c9a778195b99d0ab67ebb585362d7a3b22cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810405"
---
# <a name="window-station-and-desktop-functions"></a>Funciones de escritorio y estación de ventana

Las aplicaciones pueden usar las siguientes funciones con objetos [de estación de](window-stations.md) ventana.



| Función                                                     | Descripción                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Cierra un identificador de estación de ventana abierta.                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Crea un objeto de estación de ventana, lo asocia al proceso actual y lo asigna a la sesión actual. |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Enumera todas las estaciones de ventana de la sesión actual.                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Recupera un identificador de la estación de ventana actual para el proceso de llamada.                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Recupera información sobre la estación de ventana o el objeto de escritorio especificados.                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Recupera información de seguridad para la estación de ventana o el objeto de escritorio especificados.                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Abre la estación de ventana especificada.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Asigna la estación de ventana especificada al proceso de llamada.                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Establece información sobre la estación de ventana o el objeto de escritorio especificados.                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Establece la información de seguridad para la estación de ventana o el objeto de escritorio especificados.                                   |



 

Las aplicaciones pueden usar las siguientes funciones con objetos [de](desktops.md) escritorio.



| Función                                                     | Descripción                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Cierra un identificador abierto a un objeto de escritorio.                                                                                         |
| [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Crea un nuevo escritorio, lo asocia a la estación de ventana actual del proceso de llamada y lo asigna al subproceso que realiza la llamada. |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Crea un nuevo escritorio, lo asocia a la estación de ventana actual del proceso de llamada y lo asigna al subproceso que realiza la llamada. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Enumera todos los escritorios asociados a la estación de ventana actual del proceso de llamada.                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Enumera todas las ventanas de nivel superior asociadas al escritorio especificado.                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Recupera un identificador para el escritorio asignado al subproceso especificado.                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Obtiene información sobre una estación de ventana o un objeto de escritorio.                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Obtiene información de seguridad para una estación de ventana o un objeto de escritorio.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Abre el objeto de escritorio especificado.                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Abre el escritorio que recibe la entrada del usuario.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Asigna el escritorio especificado al subproceso que realiza la llamada.                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Establece información sobre una estación de ventana o un objeto de escritorio.                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Establece la información de seguridad de una estación de ventana o un objeto de escritorio.                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Hace que un escritorio sea visible y lo activa. Esto permite que el escritorio reciba la entrada del usuario.                                 |



 

 

 