---
title: Eventos de control (COM)
description: Además de proporcionar propiedades y métodos, un control también proporciona interfaces salientes para notificar a su cliente de eventos.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b987202cb4e4e635a947ed60e9f947cc428f0aaaacb3d27c27d60ad536b636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243635"
---
# <a name="control-events-com"></a>Eventos de control (COM)

Además de proporcionar propiedades y métodos, un control también proporciona interfaces salientes para notificar a su cliente de eventos. El cliente debe admitir el control de estos eventos. Consulte [Eventos en COM y Objetos conectables para](events-in-com-and-connectable-objects.md) obtener más información sobre cómo funcionan los objetos conectables.

Un control puede admitir interfaces salientes diferentes para distintos propósitos. Todas las interfaces salientes se marcan como interfaces de origen en la información de tipo del control, pero solo una está marcada como predeterminada para indicar que es la interfaz saliente principal.

Un contenedor puede admitir una o varias de las interfaces salientes definidas por un control . El control debe estar preparado para tratar con contenedores que solo proporcionan compatibilidad con algunas de sus interfaces salientes.

Los controles admiten cuatro tipos de eventos:

-   Solicitar eventos. Un control solicita permiso a su cliente para hacer algo mediante una llamada a un método en la interfaz saliente, lo que desencadena un evento de solicitud. El cliente señala el control a través de un parámetro booleano out en el método al que llamó el control. Por lo tanto, el cliente puede impedir que el control realice la acción.
-   Antes de los eventos. Un control notifica a su cliente que va a hacer algo llamando a un método en la interfaz saliente, lo que desencadena un evento before. El cliente no tiene la oportunidad de impedir la acción, pero puede realizar los pasos necesarios dada la acción que está a punto de producirse.
-   Después de los eventos. Un control notifica a su cliente que acaba de hacer algo llamando a un método en la interfaz saliente, lo que desencadena un evento after. De nuevo, el cliente no puede cancelar esta acción, pero puede realizar los pasos necesarios dada la acción que se ha producido.
-   Realizar eventos. Un control desencadena un evento do para permitir que su cliente invalide la acción del control y proporcione algunas acciones alternativas o adicionales. Normalmente, el método al que llama un control para un evento do tiene una serie de parámetros para negociar con el cliente sobre las acciones que se producirán.

Los siguientes errores se definen para los eventos estándar que los controles pueden admitir: Click, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp y Error. Todos estos eventos estándar tienen valores DISPID negativos, lo que indica su estado estándar.

El [**método IOleControl::FreezeEvents,**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) cuando se llama con **TRUE**, indica a un control si el contenedor se preocupará de controlar los eventos del control hasta que se vuelva a llamar a **FreezeEvents** **con FALSE.** Durante este tiempo, el control no puede depender de que el contenedor controle realmente los eventos. Si se debe controlar un evento, el control debe poner en cola el evento para que se desen marcha cuando se llama a **FreezeEvents** con **FALSE.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




