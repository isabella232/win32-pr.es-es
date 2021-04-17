---
title: Comunicación entre cliente y servidor
description: El mecanismo WinEvents proporciona una manera para que los servidores se comuniquen fácilmente con los clientes de Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "105704885"
---
# <a name="clientserver-communication"></a>Comunicación entre cliente y servidor

El mecanismo [WinEvents](winevents-overview.md) proporciona una manera para que los servidores se comuniquen fácilmente con los clientes de Microsoft Active Accessibility. A menudo, los clientes recopilan información al reaccionar a WinEvents (por ejemplo, el siguiente enfoque), pero pueden solicitar información de un servidor en cualquier momento.

Para solicitar información para un objeto accesible que genera un WinEvent, un cliente debe procesar el evento y establecer una conexión con el objeto accesible pertinente. Para ello, el cliente realiza los seis pasos siguientes:

-   Un servidor llama a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para generar una notificación WinEvent para cada cambio en sus elementos de la interfaz de usuario.
-   El código de administración de WinEvent en el usuario determina si alguna aplicación cliente ha registrado una [*función de enlace*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent mediante [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) y llama a la función de devolución de llamada registrada.
-   En su función de devolución de llamada, el cliente solicita acceso al objeto que generó el evento llamando a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) u otras funciones de recuperación de objetos accesibles. Para obtener más información, vea [recuperar un objeto IAccessible](retrieving-an-iaccessible-object.md).
-   Esta API de Microsoft Active Accessibility envía la aplicación de servidor a un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) para recuperar el objeto accesible.
-   En respuesta a [**WM \_ GETOBJECT**](wm-getobject.md), la aplicación de servidor devuelve cero o devuelve un valor que actúa como una referencia de una sola vez al objeto que generó el evento.
-   Si el servidor devuelve cero, Microsoft Active Accessibility crea un objeto proxy y proporciona su dirección al cliente. De lo contrario, Microsoft Active Accessibility usa esta referencia para recuperar la dirección de una interfaz de objeto como [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o [**IDispatch**](idispatch-interface.md)y proporciona esa dirección al cliente.

Una vez que el cliente tiene una dirección de interfaz, puede llamar a las propiedades y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto accesible para recuperar la información.

## <a name="in-this-section"></a>En esta sección

-   [WinEvents y Active Accessibility](winevents-overview.md)
-   [Cómo \_ funciona WM GETOBJECT](how-wm-getobject-works.md)
-   [Recuperar un objeto IAccessible](retrieving-an-iaccessible-object.md)

 

 




