---
description: Hay tres funciones principales de estado de estación que necesitan controlar las luces de espera de mensajes, el reenvío y no alterar.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Control de estado de la estación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e136450dbda8cec260a460f49ce8d45b65d1b58ec588ccbcc435c5e3a2b1cd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861938"
---
# <a name="station-status-control"></a>Control de estado de la estación

Hay tres funciones principales de estado de estación que necesitan control: Luces de espera de mensajes, Reenvío y No alterar. El reenvío y No interrumpir se pueden controlar a través de la función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) existente (que es específica de la dirección) y se consultan mediante [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). El bit LINEDEVSTATUSFLAGS MSGWAIT del miembro \_ **dwDevStatusFlags** de [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) indica el estado del mensaje que espera luz en el dispositivo y se envía un mensaje LINEDEVSTATE \_ MSGWAITON o LINEDEVSTATE MSGWAITOFF para indicar cuándo cambia \_ el estado. La [**función lineSetLineDevStatus permite**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) controlar la luz de espera del mensaje sin tener que implementar un dispositivo de teléfono TAPI solo para ese propósito. El bit LINEFEATURE SETDEVSTATUS (en el miembro \_ **dwLineFeatures** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) y **LINEDEVSTATUS)** indica cuándo se puede llamar y el miembro **dwSettableDevStatus** de **LINEDEVCAPS** permite a la aplicación detectar qué configuración de estado del dispositivo se puede controlar desde la aplicación. Además de permitir el control de la característica de espera de mensajes, también permite establecer los estados Conectado, Inservicio y Bloqueado del dispositivo, en la medida en que sean compatibles con el conmutador u otro hardware. Las llamadas a esta función darán lugar a que se envíen los mensajes [**\_ LINEDEVSTATE**](line-linedevstate.md) adecuados para reflejar el nuevo estado.

 

 



