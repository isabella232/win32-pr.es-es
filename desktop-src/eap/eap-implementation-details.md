---
title: Detalles de la implementación de EAP
description: Los puntos de acceso (APs), como el servicio de acceso remoto (RAS), interactúan con las implementaciones de EAP mediante el uso de llamadas a funciones que debe exportar el archivo DLL de EAP de terceros.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358890"
---
# <a name="eap-implementation-details"></a>Detalles de la implementación de EAP

Los puntos de acceso (APs), como el servicio de acceso remoto (RAS), interactúan con las implementaciones de EAP mediante el uso de llamadas a funciones que debe exportar el archivo DLL de EAP de terceros. En otras palabras, EAP es una API de proveedor, lo que significa que los complementos o los archivos dll implementan código para convertirse en proveedor EAP, pero no deben llamar a las propias API de EAP. Por ejemplo, un programador de una DLL de EAP crea código para una rutina de inicialización de EAP y coloca este código en la función predefinida de EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)). Después, en tiempo de ejecución, el administrador de conexiones de AP llama a la función **RasEapInitialize** , que contiene el código, para inicializar la implementación de EAP.

En los temas siguientes se detalla esta interacción:

-   [Inicialización de punto de acceso de EAP](ras-initialization-of-eap.md)
-   [Inicialización del Protocolo de autenticación](authentication-protocol-initialization.md)
-   [Interacción del Protocolo de autenticación y punto de acceso](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Finalización de la sesión de autenticación](completion-of-the-authentication-session.md)

 

 