---
title: Controladores de notificaciones
description: Una llamada RasDial asincrónica debe especificar un controlador de notificaciones.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7210072e0542eeb63e3de6116d61995ef2363ca7b43e7a9e2c309165c0e862
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074035"
---
# <a name="notification-handlers"></a>Controladores de notificaciones

Una llamada [**RasDial asincrónica**](/windows/desktop/api/Ras/nf-ras-rasdiala) debe especificar un controlador de notificaciones. Durante una operación de conexión asincrónica, el Connection Manager acceso remoto usa el [](connection-states.md) controlador de notificaciones para informar al cliente RAS cada vez que cambia el estado de conexión o se produce un error.

Las acciones realizadas por un controlador de notificaciones se pueden dividir en las siguientes categorías:

-   [Control de errores](handling-ras-errors.md).
-   Proporcionar comentarios al usuario a medida que la operación de conexión continúa a través de los distintos estados de conexión. Vea [Informational Notifications](informational-notifications.md).
-   Control de [estados en pausa.](paused-states.md)
-   Señalización de la aplicación cliente RAS cuando se ha completado la operación de conexión. Vea [Notificaciones de finalización](completion-notifications.md).

Hay tres tipos de controladores de notificación, cada uno de los cuales recibe la misma información básica: el estado de conexión actual y un código de error distinto de cero solo si se ha producido un error.



| Value                                | Definición                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Prototipo de función de devolución de llamada que recibe solo el estado de conexión actual y la información del código de error.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Prototipo de función de devolución de llamada que recibe el identificador de conexión **HRASCONN** y la información de error extendida, además de la información básica. El parámetro de identificador de conexión hace que [**RasDialFunc1 sea**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) útil para las aplicaciones cliente que admiten varias operaciones de conexión simultáneas. Esto permite al cliente especificar la misma función de devolución de llamada para todas las operaciones y permite que la función de devolución de llamada determine qué conexión cambia de estado. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Una función de devolución de llamada similar a [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Sin embargo, [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) se ha mejorado para admitir conexiones de varios vínculos.                                                                                                                                                                                                                                                                                                                             |
| Identificador de ventana                        | Identificador de ventana al que RAS envía [**mensajes \_ WM RASDIALEVENT**](wm-rasdialevent.md) que contienen el estado de conexión actual y la información del código de error. Use este método si el código fuente debe ser compatible con el Windows de 16 bits, ya que el Windows de 16 bits no admite ninguna de las funciones de devolución de llamada.                                                                                                                                                                            |



 

El controlador de acceso Connection Manager suspende la operación de conexión hasta que se devuelve el controlador de notificaciones. Por este motivo, el controlador debe devolver lo antes posible a menos que se haya producido un error.

No se debe llamar a la función [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) desde dentro de un controlador de notificaciones. Las demás funciones de acceso remoto [**(RasGetConnectStatus,**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) [**RasEnumEntries,**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) [**RasEnumConnections,**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)y [**RasStatusUp)**](/windows/desktop/api/Ras/nf-ras-rashangupa)se pueden llamar desde dentro de un controlador.

 

 




