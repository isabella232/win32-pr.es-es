---
description: La operación de recogida permite a una aplicación responder a una sesión que está alertando en otra dirección. La aplicación identifica el destino de la recogida y se devuelve un identificador de sesión para la llamada de recogida.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Recogida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168870"
---
# <a name="pickup"></a>Recogida

La operación de recogida permite a una aplicación responder a una sesión que está alertando en otra dirección. La aplicación identifica el destino de la recogida y se devuelve un identificador de sesión para la llamada de recogida.

Hay varias maneras de identificar el destino de la solicitud de recogida. En primer lugar, la aplicación puede especificar la dirección de la entidad de alerta. En segundo lugar, si no se especifica ninguna dirección y el conmutador lo permite, la aplicación puede recoger cualquier sesión de alertas en su grupo de recogida. En tercer lugar, algunos modificadores permiten la recogida de alertas de sesión en un grupo de recogida diferente si se especifica el identificador de grupo.

Algunos sistemas telefónicos clave admiten una funcionalidad de transferencia a *través de* retención en apariencias de llamadas exclusivas de puente. En este esquema, un teléfono determinado posee una llamada exclusivamente cuando la llamada está activa, pero cuando la llamada está en espera, cualquier teléfono que tenga una apariencia de la línea puede recoger la llamada.

**TAPI 2.x:** Una aplicación puede usar una operación de recogida con una dirección de destino **NULL** para este propósito, de forma similar a cómo se usa la función para recoger una llamada en espera de llamada en una línea análoga. LINEADDRFEATURE \_ PICKUP REENVÍO indica la existencia de la funcionalidad.

Si LINEADDRCAPFLAGS PICKUPCALLWAIT es TRUE, se puede seleccionar una sesión para la que el usuario haya detectado de forma telefónica la señal de llamada en espera, pero para la que el proveedor de servicios no puede realizar la \_ detección.  Esto proporciona al usuario un mecanismo para "responder" a una llamada en espera aunque el proveedor de servicios no pueda detectar la señal de llamada en espera. Tanto la dirección de destino como el identificador de grupo deben ser **NULL** para elegir una llamada en espera de llamada.

Cuando una sesión se ha seleccionado correctamente, la aplicación [](reason-ovr.md) recibe una notificación de cambio de estado con el motivo establecido en LINECALLREASON \_ PICKUP.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Vea [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).

**TAPI 3.x:** Vea [**ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).

 

 
