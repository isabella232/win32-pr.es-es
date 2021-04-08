---
title: Eventos de control (COM)
description: Además de proporcionar propiedades y métodos, un control también proporciona interfaces de salida para notificar a su cliente los eventos.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1833e1396847e09366d1e06193196cfcf981d330
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078723"
---
# <a name="control-events-com"></a>Eventos de control (COM)

Además de proporcionar propiedades y métodos, un control también proporciona interfaces de salida para notificar a su cliente los eventos. El cliente debe admitir el control de estos eventos. Vea [eventos en com y objetos conectables](events-in-com-and-connectable-objects.md) para obtener más información sobre cómo funcionan los objetos conectables.

Un control puede admitir diferentes interfaces salientes para distintos fines. Todas las interfaces salientes se marcan como interfaces de origen en la información de tipo del control, pero solo una se marca como predeterminada para indicar que es la interfaz de salida principal.

Un contenedor puede admitir una o varias de las interfaces de salida definidas por un control. El control debe estar preparado para tratar los contenedores que solo proporcionan compatibilidad con algunas de las interfaces de salida.

Los controles admiten cuatro tipos de eventos:

-   Eventos de solicitud. Un control solicita permiso de su cliente para hacer algo llamando a un método en la interfaz de salida, lo que desencadena un evento de solicitud. El cliente señala el control a través de un parámetro out booleano en el método al que llamó el control. Por tanto, el cliente puede impedir que el control realice la acción.
-   Eventos Before. Un control notifica a su cliente Hat que va a hacer algo llamando a un método en la interfaz de salida, lo que desencadena un evento Before. El cliente no tiene la oportunidad de evitar la acción, pero puede llevar a cabo los pasos necesarios según la acción que está a punto de producirse.
-   Eventos after. Un control notifica a su cliente que acaba de hacer algo llamando a un método en la interfaz de salida, lo que desencadena un evento after. De nuevo, el cliente no puede cancelar esta acción, pero puede llevar a cabo los pasos necesarios según la acción que se ha producido.
-   Realice eventos. Un control desencadena un evento do para permitir que su cliente invalide la acción del control y proporcione algunas acciones alternativas o adicionales. Normalmente, el método al que un control llama para un evento do tiene una serie de parámetros para negociar con el cliente sobre las acciones que se producirán.

Los siguientes DISPID se definen para eventos estándar que los controles pueden admitir: click, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp y error. Todos estos eventos estándar tienen valores DISPID negativos, que indican su estado estándar.

El método [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) , cuando se llama con **true**, indica a un control si el contenedor molestará a controlar los eventos del control hasta que se llame a **FreezeEvents** con **false**. Durante este tiempo, el control no puede depender del contenedor que controla realmente los eventos. Si se debe controlar un evento, el control debe poner en cola el evento para que se desencadene cuando se llame a **FreezeEvents** con **false**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




