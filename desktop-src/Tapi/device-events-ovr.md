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
# <a name="device-events-telephony-api"></a><span data-ttu-id="1fc55-103">Eventos de dispositivo (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="1fc55-103">Device Events (Telephony API)</span></span>

<span data-ttu-id="1fc55-104">TAPI responde a los cambios del dispositivo, como un teléfono que ha empezado a sonar o un módem que se ha quitado al activar eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc55-104">TAPI responds to device changes such as a phone that has started ringing or a modem that has been removed by firing device events.</span></span> <span data-ttu-id="1fc55-105">Una aplicación TAPI debe responder a un evento de dispositivo consultando el cambio específico que se ha producido y realizando la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="1fc55-105">A TAPI application should respond to a device event by querying for the specific change that has occurred and then taking appropriate action.</span></span> <span data-ttu-id="1fc55-106">Una aplicación puede mostrar los eventos que recibirá mediante la [notificación de eventos](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="1fc55-106">An application may screen for events it will receive using [event notification](event-notification.md).</span></span>

<span data-ttu-id="1fc55-107">**TAPI 2. x:** Las aplicaciones reciben la notificación de eventos de dispositivo mediante el mensaje [**line \_ LINEDEVSTATE**](./line-linedevstate.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc55-107">**TAPI 2.x:** Applications receive notification of device events using the [**LINE\_LINEDEVSTATE**](./line-linedevstate.md) message.</span></span> <span data-ttu-id="1fc55-108">El estado actual de una dirección se determina mediante una llamada a [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), que devuelve su información en una estructura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="1fc55-108">The current status of an address is determined by calling [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), which returns its information in a [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="1fc55-109">El estado de un dispositivo de línea de apertura especificado se obtiene mediante una llamada a [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), que devuelve su información en una estructura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="1fc55-109">The status of a specified open line device is obtained by calling [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), which returns its information in a [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure.</span></span>

<span data-ttu-id="1fc55-110">**TAPI 3. x:** Las aplicaciones reciben una notificación de [**\_ evento de dirección**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , que se procesa mediante la interfaz [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) .</span><span class="sxs-lookup"><span data-stu-id="1fc55-110">**TAPI 3.x:** Applications receive an [**ADDRESS\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) notification, which is processed using the [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) interface.</span></span> <span data-ttu-id="1fc55-111">A continuación, se puede usar [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="1fc55-111">The [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) can then be used to acquire more detail information.</span></span>

 

 
