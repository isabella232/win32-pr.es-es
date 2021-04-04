---
description: TAPI responde a los cambios del dispositivo, como un teléfono que ha empezado a sonar o un módem que se ha quitado al activar eventos de dispositivo.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Eventos de dispositivo (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809871"
---
# <a name="device-events-telephony-api"></a>Eventos de dispositivo (API de telefonía)

TAPI responde a los cambios del dispositivo, como un teléfono que ha empezado a sonar o un módem que se ha quitado al activar eventos de dispositivo. Una aplicación TAPI debe responder a un evento de dispositivo consultando el cambio específico que se ha producido y realizando la acción adecuada. Una aplicación puede mostrar los eventos que recibirá mediante la [notificación de eventos](event-notification.md).

**TAPI 2. x:** Las aplicaciones reciben la notificación de eventos de dispositivo mediante el mensaje [**line \_ LINEDEVSTATE**](./line-linedevstate.md) . El estado actual de una dirección se determina mediante una llamada a [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), que devuelve su información en una estructura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) . El estado de un dispositivo de línea de apertura especificado se obtiene mediante una llamada a [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), que devuelve su información en una estructura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .

**TAPI 3. x:** Las aplicaciones reciben una notificación de [**\_ evento de dirección**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , que se procesa mediante la interfaz [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) . A continuación, se puede usar [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) para obtener información más detallada.

 

 
