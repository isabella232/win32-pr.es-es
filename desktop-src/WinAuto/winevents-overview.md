---
title: Información general sobre WinEvents y Active Accessibility
description: Los servidores de Microsoft Active Accessibility generan WinEvents para notificar a los clientes cuando cambia un objeto accesible.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b351b1ce7b6337c4ca0ac0827daff2978c6611af
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103994897"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents y Active Accessibility

Los servidores de Microsoft Active Accessibility generan *WinEvents* para notificar a los clientes cuando cambia un objeto accesible. Hay numerosas condiciones en las que un servidor notifica un cambio a un cliente. Cada [constante de evento](event-constants.md) definida por Microsoft Active Accessibility describe una condición sobre la que se notifica a un cliente. Por ejemplo, WinEvents puede indicar:

- Cuando se crea o se destruye un objeto.
- Cuando un objeto recibe o pierde el foco.
- Cuando cambia el estado o la ubicación de un objeto.
- Cuando cambia alguna propiedad de un objeto.

Las aplicaciones cliente no reciben notificaciones de eventos de forma automática. deben especificar qué eventos desean recibir llamando a la función [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) . Con **SetWinEventHook**, un cliente se registra para recibir uno o más eventos y establece una función de enlace para controlar los eventos especificados. Los clientes pueden utilizar la misma función de enlace para controlar varios tipos de eventos o pueden usar las funciones de enlace varios. Los clientes llaman una vez a **SetWinEventHook** para cada función de enlace que debe registrar.

Las funciones de enlace se encuentran dentro del cuerpo del código del cliente, en un archivo DLL asignado al proceso del cliente, o en un archivo DLL asignado al proceso del servidor. Cada uno de estos métodos tiene ventajas y desventajas. Para obtener más información, vea [funciones de enlace en contexto y fuera de contexto](in-context-and-out-of-context-hook-functions.md).

Para notificar a los clientes la aparición de un evento, los servidores llaman a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent). El sistema comprueba si alguna aplicación cliente tiene definidas funciones de enlace para el evento y llama a las funciones de enlace apropiadas según sea necesario.

Cuando se llama a la función de enlace del cliente, recibe una serie de parámetros que describen el evento y el objeto que generó el evento. Para obtener acceso al objeto que generó el evento, la función de enlace de cliente llama a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

> [!NOTE]
> Si no hay clientes registrados para recibir WinEvents, el impacto en el rendimiento de un servidor para llamar a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) es insignificante.
>
> Los servidores llaman a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para los cambios únicamente en sus propios objetos accesibles; no llaman a **NotifyWinEvent** para los cambios en los elementos de la interfaz de usuario proporcionados por el sistema.

## <a name="event-driven-communication"></a>Comunicación Event-Driven

Los clientes deben registrar un enlace de WinEvent para poder recibir notificaciones de WinEvent. Para evitar devoluciones de llamada innecesarias y mejorar el rendimiento, se recomienda que los clientes se registren solo para los eventos que necesitan recibir.

Dentro del procedimiento de enlace, el cliente puede llamar a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) para recuperar un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento al que se aplica el evento. Con este objeto, el cliente puede empezar a llamar a métodos **IAccessible** para recuperar información o interactuar con el elemento de la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

[WinEvents](winevents-infrastructure.md)
