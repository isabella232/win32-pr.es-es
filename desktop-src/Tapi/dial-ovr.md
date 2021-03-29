---
description: Las operaciones de marcado permiten a una aplicación enviar dígitos adicionales en una sesión creada anteriormente. Un ejemplo del uso de la marcación parcial es marcar una extensión. El marcado parcial a veces se denomina marcado incremental o marcado retardado.
ms.assetid: 1dfaefd7-f8dd-451e-af18-249c89bdb517
title: Dial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c603d8e846694b4728d1b5ad4c887be34fbac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809235"
---
# <a name="dial"></a>Dial

Las operaciones de marcado permiten a una aplicación enviar dígitos adicionales en una sesión creada anteriormente. Un ejemplo del uso de la marcación parcial es marcar una extensión. El marcado parcial a veces se denomina marcado incremental o marcado retardado.

Cuando la dirección proporcionada está incompleta, el marcado de algunos dígitos se puede retrasar colocando un punto y coma (;) al final del número. Después, una operación de marcado se utiliza para enviar datos de direcciones adicionales en la sesión existente, como marcar la dirección de una entidad a la que se transferirá la llamada.

Cada proveedor de servicios debe rechazar una cadena de marcado que contenga el **?** y permita que la aplicación se ocupe de ello según corresponda. Por ejemplo, la aplicación podría utilizar el marcado parcial para marcar la cadena, hasta, pero sin incluir el **?** y, a continuación, muestre un cuadro de diálogo para que el usuario señale Cuándo se debe marcar el resto de la cadena de marcado.

Una razón adicional para que una aplicación use el marcado parcial es si el proveedor de servicios no admite uno o varios de los caracteres de control de detección del progreso de la llamada. Estos caracteres, que pueden aparecer en una dirección que se puede marcar, son W (esperar al tono de marcado); @ (esperar respuesta silenciosa); y $ (esperar el tono de petición de la tarjeta de llamada). Estos y todos los demás caracteres que se usan en las cadenas de direcciones se describen con más detalle en direcciones que se pueden [marcar](address-ovr.md).

El proveedor indica qué modificadores de cadena de marcado (wait for) admite. Una aplicación TAPI 2 encuentra estos datos en el miembro **dwDevCapFlags** de la estructura [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) devuelta por [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps). Una aplicación TAPI 3 llama [**a ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) con *AddressCap* establecido en el miembro **AC \_ DEVCAPFLAGS** de la [**\_ capacidad Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).

La aplicación puede optar por realizar un examen de las cadenas marcables para los caracteres no admitidos o puede pasar la cadena "sin formato" como parte del inicio de una sesión. Si la cadena contiene un modificador no admitido o "?", el proveedor devolverá un error que indica que el modificador infractor se produjo primero dentro de la cadena:

-   LINEERR \_ DIALBILLING
-   LINEERR \_ DIALQUIET
-   LINEERR \_ DIALDIALTONE
-   LINEERR \_ DIALPROMPT

A continuación, la aplicación puede encontrar el modificador infractor en la cadena, tomar los dígitos a la izquierda del modificador, anexar un punto y coma e iniciar una sesión con la dirección parcial. El resto de la cadena se puede enviar mediante la operación de marcado.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**lineales**](/windows/win32/api/tapi/nf-tapi-linedial).

**TAPI 3. x:** Vea [**ITBasicCallControl::D cial**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial).

 

 
