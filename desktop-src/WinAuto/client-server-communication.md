---
title: Comunicación entre cliente y servidor
description: El mecanismo WinEvents proporciona una manera de que los servidores se comuniquen fácilmente con Microsoft Active Accessibility clientes.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896b6f6688e0e2929ebb351fe9d7cc210803768a8031faa44a8aca8127b12002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133938"
---
# <a name="clientserver-communication"></a>Comunicación entre cliente y servidor

El [mecanismo WinEvents](winevents-overview.md) proporciona una manera de que los servidores se comuniquen fácilmente con Microsoft Active Accessibility clientes. A menudo, los clientes recopilan información reaccionando a WinEvents (por ejemplo, siguiendo el foco), pero pueden solicitar información de un servidor en cualquier momento.

Para solicitar información para un objeto accesible que genera un WinEvent, un cliente debe procesar el evento y establecer una conexión con el objeto accesible pertinente. Para ello, el cliente realiza los seis pasos siguientes:

-   Un servidor llama [**a NotifyWinEvent para**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) generar una notificación de WinEvent para cada cambio en sus elementos de la interfaz de usuario.
-   El código de administración de WinEvent en USER determina si alguna aplicación cliente ha registrado una función de enlace de [*WinEvent*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) mediante [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) y llama a la función de devolución de llamada registrada.
-   En su función de devolución de llamada, el cliente solicita acceso al objeto que generó el evento mediante una llamada a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) u otras funciones de recuperación de objetos accesibles. Para obtener más información, [vea Recuperar un objeto IAccessible](retrieving-an-iaccessible-object.md).
-   Esta Microsoft Active Accessibility API envía a la aplicación de servidor un [**mensaje \_ WM GETOBJECT**](wm-getobject.md) para recuperar el objeto accesible.
-   En respuesta a [**WM \_ GETOBJECT,**](wm-getobject.md)la aplicación de servidor devuelve cero o devuelve un valor que actúa como referencia única al objeto que generó el evento.
-   Si el servidor devuelve cero, Microsoft Active Accessibility crea un objeto proxy y proporciona su dirección al cliente. De lo contrario, Microsoft Active Accessibility esta referencia para recuperar la dirección de una interfaz de objeto como [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o [**IDispatch**](idispatch-interface.md)y proporciona esa dirección al cliente.

Una vez que el cliente tiene una dirección de interfaz, puede llamar a las propiedades y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto accesible para recuperar información.

## <a name="in-this-section"></a>En esta sección

-   [WinEvents y Active Accessibility](winevents-overview.md)
-   [Funcionamiento de WM \_ GETOBJECT](how-wm-getobject-works.md)
-   [Recuperar un objeto IAccessible](retrieving-an-iaccessible-object.md)

 

 




