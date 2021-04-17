---
description: Hay tres funciones principales de estado de la estación que requieren el control de las luces de espera del mensaje de control, el reenvío y no molestar.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Control de estado de la estación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f6ddd1b1ce6df1ad2f3dc61e891ed6952a7f05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677797"
---
# <a name="station-status-control"></a>Control de estado de la estación

Hay tres funciones de estado de estación principales que necesitan control: semáforos en espera, reenvío y no molestar. El reenvío y no molestar se pueden controlar a través de la función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) existente (que es específica de la dirección) y se consultan mediante [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). El \_ bit LINEDEVSTATUSFLAGS MSGWAIT en el miembro **DwDevStatusFlags** de [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) indica el estado de la luz de espera del mensaje en el dispositivo y se envía un mensaje LINEDEVSTATE MSGWAITON o LINEDEVSTATE MSGWAITOFF \_ \_ para indicar cuándo cambia el estado. La función [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) permite controlar la luz de espera del mensaje sin tener que implementar un dispositivo de teléfono TAPI solo para ese fin. El \_ bit LINEFEATURE SETDEVSTATUS (en el miembro **DwLineFeatures** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) y **LINEDEVSTATUS**) indica cuándo se puede llamar, y el miembro **dwSettableDevStatus** de **LINEDEVCAPS** permite que la aplicación detecte qué configuración del estado del dispositivo se puede controlar desde la aplicación. Además de permitir que la característica de espera de mensajes se controle, también permite establecer el estado conectado, inservicio y bloqueado del dispositivo, en la medida en que se admitan en el conmutador u otro hardware. Las llamadas a esta función dan lugar a que se envíen mensajes [**\_ LINEDEVSTATE de línea**](line-linedevstate.md) adecuados para reflejar el nuevo estado.

 

 



