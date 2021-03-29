---
description: La red del modo de transferencia asincrónico (ATM) está en funcionamiento en el estándar de la informática y se ha agregado compatibilidad con ATM a muchas partes del sistema operativo.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Calidad de servicio (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911986"
---
# <a name="quality-of-service-telephony-api"></a><span data-ttu-id="201a8-103">Calidad de servicio (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="201a8-103">Quality of Service (Telephony API)</span></span>

<span data-ttu-id="201a8-104">La red del modo de transferencia asincrónico (ATM) está en funcionamiento en el estándar de la informática y se ha agregado compatibilidad con ATM a muchas partes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="201a8-104">Asynchronous Transfer Mode (ATM) networking is emerging into the mainstream of computing, and support for ATM has been added to many parts of the operating system.</span></span> <span data-ttu-id="201a8-105">TAPI también admite atributos clave para establecer llamadas en las instalaciones de ATM.</span><span class="sxs-lookup"><span data-stu-id="201a8-105">TAPI also supports key attributes of establishing calls on ATM facilities.</span></span> <span data-ttu-id="201a8-106">Lo más importante de la perspectiva de la aplicación es la posibilidad de solicitar, negociar, renegociar y recibir indicaciones de los parámetros de calidad de servicio (QOS) en las llamadas entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="201a8-106">The most important of these from an application perspective is the ability to request, negotiate, renegotiate, and receive indications of Quality of Service (QOS) parameters on incoming and outgoing calls.</span></span>

<span data-ttu-id="201a8-107">La información de QOS en TAPI se intercambia entre aplicaciones y proveedores de servicios en estructuras [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) definidas en Windows sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="201a8-107">QOS information in TAPI is exchanged between applications and service providers in [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) structures that are defined in Windows Sockets 2.0.</span></span>

<span data-ttu-id="201a8-108">Las aplicaciones solicitan QOS en las llamadas salientes estableciendo los valores de información de sesión antes de iniciar una sesión de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="201a8-108">Applications request QOS on outgoing calls by setting session information values prior to starting a communications session.</span></span> <span data-ttu-id="201a8-109">El proveedor de servicios intentará proporcionar la QOS especificada y se producirá un error en la llamada si no es posible.</span><span class="sxs-lookup"><span data-stu-id="201a8-109">The service provider will try to provide the specified QOS, and fail the call if it cannot.</span></span> <span data-ttu-id="201a8-110">A continuación, la aplicación puede ajustar sus parámetros y volver a intentar la llamada.</span><span class="sxs-lookup"><span data-stu-id="201a8-110">The application can then adjust its parameters and try the call again.</span></span> <span data-ttu-id="201a8-111">Una vez establecida una llamada, una aplicación puede solicitar un cambio en la QOS.</span><span class="sxs-lookup"><span data-stu-id="201a8-111">After a call is established, an application can request a change in the QOS.</span></span>

<span data-ttu-id="201a8-112">TAPI proporciona notificaciones de eventos para el propietario o la supervisión de aplicaciones si se produce algún cambio en los niveles de QOS.</span><span class="sxs-lookup"><span data-stu-id="201a8-112">TAPI provides event notifications to owner or monitor applications if there is any change in QOS levels.</span></span>

<span data-ttu-id="201a8-113">La compatibilidad con QOS no está restringida a los transportes ATM; cualquier proveedor de servicios puede implementar características de QOS.</span><span class="sxs-lookup"><span data-stu-id="201a8-113">Support for QOS is not restricted to ATM transports; any service provider can implement QOS features.</span></span>

<span data-ttu-id="201a8-114">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="201a8-114">Not all service providers support use of this information.</span></span>

<span data-ttu-id="201a8-115">\* \* TAPI 2. x: \* \*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** y **dwReceivingFlowspecOffset** miembros de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span><span class="sxs-lookup"><span data-stu-id="201a8-115">\*\*TAPI 2.x:  \*\*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize**, and **dwReceivingFlowspecOffset** members of [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span></span>

<span data-ttu-id="201a8-116">\* \* TAPI 3. x: \* \*[**ITBasicCallControl:: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span><span class="sxs-lookup"><span data-stu-id="201a8-116">\*\*TAPI 3.x:  \*\*[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span></span>

 

 
