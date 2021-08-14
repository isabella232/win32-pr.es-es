---
title: Notificaciones de finalización
description: El acceso remoto Connection Manager las notificaciones de progreso hasta que se haya completado la operación de conexión.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6dcfad1ae0dfd4eefb3df00dceefce0df77d93239a6e7c2c4fa6517cac25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791611"
---
# <a name="completion-notifications"></a>Notificaciones de finalización

El acceso remoto Connection Manager las notificaciones de progreso hasta que se haya completado la operación de conexión. Esto se produce en las situaciones siguientes:

-   El controlador recibe una notificación RASCS \_ Connected o RASCS \_ Disconnected. La aplicación cliente RAS puede salir sin que se rompa ninguna conexión establecida.
-   Se produce un error. El controlador recibe una notificación que indica el error y el estado de conexión cuando se produjo el error. La aplicación cliente RAS puede salir.

La aplicación cliente RAS no debe asumir que la operación de conexión se ha completado después de llamar a [**RasHangUp.**](/windows/desktop/api/Ras/nf-ras-rashangupa) Debe esperar una de las condiciones anteriores antes de salir.

 

 




