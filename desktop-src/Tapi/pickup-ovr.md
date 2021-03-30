---
description: La operación de recogida permite a una aplicación responder a una sesión que se alerta en otra dirección. La aplicación identifica el destino de la recogida y se devuelve un identificador de sesión para la llamada de recogida.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Diodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816139"
---
# <a name="pickup"></a>Diodo

La operación de recogida permite a una aplicación responder a una sesión que se alerta en otra dirección. La aplicación identifica el destino de la recogida y se devuelve un identificador de sesión para la llamada de recogida.

Hay varias maneras de identificar el destino de la solicitud de recogida. En primer lugar, la aplicación puede especificar la dirección de la entidad de alerta. En segundo lugar, si no se especifica ninguna dirección y el modificador lo permite, la aplicación puede seleccionar cualquier sesión de alertas en su grupo de recogida. En tercer lugar, algunos modificadores permiten la recogida de una alerta de sesión en un grupo de recogida diferente si se especifica el identificador de grupo.

Algunos sistemas de teléfono clave admiten una *transferencia a través* de la capacidad de retención en las orientaciones de llamadas exclusivas de puente. En este esquema, un teléfono determinado posee una llamada exclusivamente cuando la llamada está activa, pero cuando la llamada está en espera, cualquier teléfono que tenga una apariencia de la línea puede recoger la llamada.

**TAPI 2. x:** Una aplicación puede usar una operación de recogida con una dirección de destino **null** para este propósito, de forma similar a cómo se utiliza la función para recoger una llamada en espera en una línea analógica. LINEADDRFEATURE \_ PICKUPHELD indica la existencia de la funcionalidad.

Si LINEADDRCAPFLAGS \_ PICKUPCALLWAIT es **true**, se puede seleccionar una sesión para la que el usuario ha detectado de forma audible la señal de llamada en espera, pero para la que el proveedor de servicios no puede realizar la detección. Esto proporciona al usuario un mecanismo para "responder" a una llamada en espera aunque el proveedor de servicios no pudiera detectar la señal de llamada en espera. Tanto la dirección de destino como el ID. de grupo deben ser **null** para recoger una llamada de llamada en espera.

Cuando una sesión se ha recopilado correctamente, la aplicación recibe una notificación de cambio de estado con la [razón](reason-ovr.md) establecida en LINECALLREASON \_ pickup.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).

**TAPI 3. x:** Vea [**ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).

 

 
