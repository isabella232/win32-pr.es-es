---
title: Controladores de notificaciones
description: Una llamada RasDial asincrónica debe especificar un controlador de notificación.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe735a17de4386bc48648cd20decd218ab102d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994542"
---
# <a name="notification-handlers"></a>Controladores de notificaciones

Una llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asincrónica debe especificar un controlador de notificación. Durante una operación de conexión asincrónica, el administrador de conexiones de acceso remoto utiliza el controlador de notificación para informar al cliente de RAS cada vez que cambia el estado de la [conexión](connection-states.md) o se produce un error.

Las acciones realizadas por un controlador de notificaciones se pueden dividir en las siguientes categorías:

-   [Control de errores](handling-ras-errors.md).
-   Proporcionar comentarios al usuario a medida que la operación de conexión se realiza a través de los distintos Estados de conexión. Vea [notificaciones informativas](informational-notifications.md).
-   Controlar [los Estados en pausa](paused-states.md).
-   Señalización de la aplicación cliente RAS cuando se ha completado la operación de conexión. Vea [notificaciones de finalización](completion-notifications.md).

Hay tres tipos de controladores de notificación, cada uno de los cuales recibe la misma información básica: el estado de conexión actual y un código de error que es distinto de cero solo si se ha producido un error.



| Value                                | Definición                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Prototipo de función de devolución de llamada que recibe solo la información del código de error y el estado de conexión actual.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Prototipo de función de devolución de llamada que recibe el identificador de conexión de **HRASCONN** y la información de error extendida, además de la información básica. El parámetro de identificador de conexión hace que [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) resulte útil para las aplicaciones cliente que admiten varias operaciones de conexión simultáneas. Esto permite al cliente especificar la misma función de devolución de llamada para todas las operaciones y permite a la función de devolución de llamada determinar qué conexión está cambiando los Estados. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Función de devolución de llamada similar a [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1). Sin embargo, [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) se ha mejorado para admitir conexiones Multilink.                                                                                                                                                                                                                                                                                                                             |
| Identificador de ventana                        | Identificador de ventana en el que RAS envía mensajes de [**WM \_ RASDIALEVENT**](wm-rasdialevent.md) que contienen el estado de conexión actual y la información del código de error. Use este método si el código fuente debe ser compatible con Windows de 16 bits, porque Windows de 16 bits no admite ninguna de las funciones de devolución de llamada.                                                                                                                                                                            |



 

El administrador de conexiones de acceso remoto suspende la operación de conexión hasta que el controlador de notificación vuelve. Por esta razón, el controlador debe volver lo antes posible, a menos que se haya producido un error.

No se debe llamar a la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) desde un controlador de notificación. Se puede llamar a las otras funciones de acceso remoto ( [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa), [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa), [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa), [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)y [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)) desde un controlador.

 

 




