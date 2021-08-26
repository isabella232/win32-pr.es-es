---
title: Detalles de implementación de EAP
description: Los puntos de acceso (AP), como el Servicio de acceso remoto (RAS), interactúan con las implementaciones de EAP mediante el uso de llamadas de función que debe exportar el archivo DLL de EAP de terceros.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8772d839e6d6fb748f56de0329a958057400d37afeb92a2f3ec89b3ab462e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852415"
---
# <a name="eap-implementation-details"></a>Detalles de implementación de EAP

Los puntos de acceso (AP), como el Servicio de acceso remoto (RAS), interactúan con las implementaciones de EAP mediante el uso de llamadas de función que debe exportar el archivo DLL de EAP de terceros. En otras palabras, EAP es una API de proveedor, lo que significa que los complementos o archivos DLL implementan código para convertirse en un proveedor de EAP, pero no deben llamar a las PROPIAS API de EAP. Por ejemplo, un programador de un archivo DLL de EAP crea código para una rutina de inicialización de EAP y coloca este código en la función predefinida de EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)). A continuación, en tiempo de ejecución, el administrador de conexiones AP llama a la función **RasEapInitialize,** que contiene el código, para inicializar la implementación de EAP.

En los temas siguientes se detalla esta interacción:

-   [Inicialización de punto de acceso de EAP](ras-initialization-of-eap.md)
-   [Inicialización del protocolo de autenticación](authentication-protocol-initialization.md)
-   [Interacción del punto de acceso y del protocolo de autenticación](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Finalización de la sesión de autenticación](completion-of-the-authentication-session.md)

 

 