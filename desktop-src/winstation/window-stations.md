---
title: Estaciones de ventana
description: Una estación de ventana contiene un portapapeles, una tabla Atom y uno o más objetos de escritorio. Cada objeto de estación de ventana es un objeto protegible. Cuando se crea una estación de ventana, se asocia al proceso de llamada y se asigna a la sesión actual.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- objetos de la estación de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077924"
---
# <a name="window-stations"></a>Estaciones de ventana

Una *estación de ventana* contiene un portapapeles, una tabla Atom y uno o más objetos de [escritorio](desktops.md) . Cada objeto de estación de ventana es un objeto protegible. Cuando se crea una estación de ventana, se asocia al proceso de llamada y se asigna a la sesión actual.

La *estación de ventana interactiva* es la única estación de ventana que puede mostrar una interfaz de usuario o recibir datos proporcionados por el usuario. Se asigna a la sesión de inicio de sesión del usuario interactivo y contiene el teclado, el mouse y el dispositivo de pantalla. Siempre se denomina "WinSta0". El resto de las estaciones de ventana no son interactivas, lo que significa que no pueden mostrar una interfaz de usuario ni recibir datos proporcionados por el usuario.

Cuando un usuario inicia sesión en un equipo mediante Servicios de Escritorio remoto, se inicia una sesión para el usuario. Cada sesión está asociada a su propia estación de ventana interactiva denominada "WinSta0". Para obtener más información, vea [sesiones de escritorio remoto](/windows/desktop/TermServ/terminal-services-sessions).

Para obtener más información sobre las estaciones de ventana, vea los temas siguientes:

-   [Creación de estación de ventana y escritorio](window-station-and-desktop-creation.md)
-   [Proceso de conexión a una estación de ventana](process-connection-to-a-window-station.md)
-   [Seguridad y derechos de acceso de la estación de ventana](window-station-security-and-access-rights.md)

 

 