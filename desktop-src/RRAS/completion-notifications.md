---
title: Notificaciones de finalización
description: El administrador de conexiones de acceso remoto continúa con las notificaciones de progreso hasta que se completa la operación de conexión.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075763"
---
# <a name="completion-notifications"></a>Notificaciones de finalización

El administrador de conexiones de acceso remoto continúa con las notificaciones de progreso hasta que se completa la operación de conexión. Esto sucede en las siguientes situaciones:

-   El controlador recibe una \_ notificación RASCS conectada o RASCS \_ desconectada. La aplicación cliente RAS puede salir sin interrumpir ninguna conexión establecida.
-   Se produce un error. El controlador recibe una notificación que indica el error y el estado de conexión cuando se produjo el error. La aplicación cliente RAS puede salir.

La aplicación cliente RAS no debe suponer que la operación de conexión se ha completado después de llamar a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa). Antes de salir, debe esperar a una de las condiciones anteriores.

 

 




