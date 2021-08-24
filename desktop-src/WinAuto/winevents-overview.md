---
title: Información general sobre winevents Active Accessibility datos
description: Microsoft Active Accessibility genera WinEvents para notificar a los clientes cuando cambia un objeto accesible.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95507ff1b6cd56451dd7f9acc04014c6013a7179d536565b3518bccb9137e689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052183"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents y Active Accessibility

Microsoft Active Accessibility genera *WinEvents para* notificar a los clientes cuando cambia un objeto accesible. Hay numerosas condiciones en las que un servidor notifica un cambio a un cliente. Cada [constante de](event-constants.md) evento definida por Microsoft Active Accessibility describe una condición sobre la que se notifica a un cliente. Por ejemplo, WinEvents puede indicar:

- Cuando se crea o destruye un objeto.
- Cuando un objeto recibe o pierde el foco.
- Cuando cambia el estado o la ubicación de un objeto.
- Cuando cambia cualquier propiedad de un objeto.

Las aplicaciones cliente no reciben notificaciones de eventos automáticamente; deben especificar qué eventos quieren recibir llamando a la [**función SetWinEventHook.**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) Con **SetWinEventHook,** un cliente se registra para recibir uno o varios eventos y establece una función de enlace para controlar los eventos especificados. Los clientes pueden usar la misma función de enlace para controlar varios tipos de eventos o pueden usar funciones de enlace multipe. Los clientes llaman **a SetWinEventHook una** vez por cada función de enlace que necesita registrar.

Las funciones de enlace se encuentran en el cuerpo del código del cliente, en un archivo DLL asignado al proceso del cliente o en un archivo DLL asignado al proceso del servidor. Cada uno de estos métodos tiene ventajas y desventajas. Para obtener más información, vea Funciones de enlace en contexto y [fuera de contexto](in-context-and-out-of-context-hook-functions.md).

Para notificar a los clientes la aparición de un evento, los servidores [**llaman a NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent). El sistema comprueba si alguna aplicación cliente ha establecido funciones de enlace para el evento y llama a las funciones de enlace adecuadas según sea necesario.

Cuando se llama a la función de enlace del cliente, recibe una serie de parámetros que describen el evento y el objeto que generó el evento. Para obtener acceso al objeto que generó el evento, la función de enlace de cliente llama [**a AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

> [!NOTE]
> Si ningún cliente se ha registrado para recibir WinEvents, el impacto en el rendimiento en un servidor para llamar a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) es insignificante.
>
> Los servidores llaman [**a NotifyWinEvent solo**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para los cambios en sus propios objetos accesibles; no llaman a **NotifyWinEvent para los** cambios en los elementos de la interfaz de usuario proporcionados por el sistema.

## <a name="event-driven-communication"></a>Event-Driven comunicación

Los clientes deben registrar un enlace de WinEvent para poder recibir notificaciones de WinEvent. Para evitar devoluciones de llamada innecesarias y mejorar el rendimiento, se recomienda a los clientes registrarse solo para los eventos que necesitan recibir.

Dentro del procedimiento de enlace, el cliente puede llamar a [**AccessibleObjectFromEvent para**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) recuperar un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento al que se aplica el evento. Con este objeto, el cliente puede empezar a llamar a **métodos IAccessible** para recuperar información o interactuar con el elemento de interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

[WinEvents](winevents-infrastructure.md)
