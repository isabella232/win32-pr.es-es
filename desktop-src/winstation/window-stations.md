---
title: Estaciones de ventana
description: Una estación de ventana contiene un Portapapeles, una tabla atom y uno o varios objetos de escritorio. Cada objeto de estación de ventana es un objeto protegible. Cuando se crea una estación de ventana, se asocia al proceso de llamada y se asigna a la sesión actual.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- objetos de estación de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251613"
---
# <a name="window-stations"></a>Estaciones de ventana

Una *estación de ventana* contiene un Portapapeles, una tabla atom y uno o varios objetos [de](desktops.md) escritorio. Cada objeto de estación de ventana es un objeto protegible. Cuando se crea una estación de ventana, se asocia al proceso de llamada y se asigna a la sesión actual.

La *estación de ventana interactiva* es la única estación de ventana que puede mostrar una interfaz de usuario o recibir la entrada del usuario. Se asigna a la sesión de inicio de sesión del usuario interactivo y contiene el teclado, el mouse y el dispositivo para mostrar. Siempre se denomina "WinSta0". Todas las demás estaciones de ventana no son inactivas, lo que significa que no pueden mostrar una interfaz de usuario ni recibir la entrada del usuario.

Cuando un usuario inicia sesión en un equipo Servicios de Escritorio remoto, se inicia una sesión para el usuario. Cada sesión está asociada a su propia estación de ventana interactiva denominada "WinSta0". Para obtener más información, [vea Escritorio remoto Sessions](/windows/desktop/TermServ/terminal-services-sessions).

Para obtener más información sobre las estaciones de ventana, vea los temas siguientes:

-   [Estación de ventana y creación de escritorio](window-station-and-desktop-creation.md)
-   [Procesar conexión a una estación de ventana](process-connection-to-a-window-station.md)
-   [Derechos de acceso y seguridad de la estación de windows](window-station-security-and-access-rights.md)

 

 