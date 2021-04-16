---
title: Secuencia de inicio
description: Pasos para iniciar el protocolo personalizado.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268365"
---
# <a name="start-sequence"></a><span data-ttu-id="e18ed-103">Secuencia de inicio</span><span class="sxs-lookup"><span data-stu-id="e18ed-103">Start Sequence</span></span>

<span data-ttu-id="e18ed-104">Para iniciar el proveedor de protocolo, el servicio de Servicios de Escritorio remoto:</span><span class="sxs-lookup"><span data-stu-id="e18ed-104">To start your protocol provider, the Remote Desktop Services service:</span></span>

-   <span data-ttu-id="e18ed-105">Recupera el nombre del agente de escucha y el CLSID del objeto de administrador de protocolos ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) del registro.</span><span class="sxs-lookup"><span data-stu-id="e18ed-105">Retrieves the name of the listener and the CLSID of your protocol manager object ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) from the registry.</span></span> <span data-ttu-id="e18ed-106">Para obtener más información, consulte [registrar el administrador de protocolos](registering-the-custom-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="e18ed-106">For more information, see [Registering the Protocol Manager](registering-the-custom-protocol.md).</span></span>
-   <span data-ttu-id="e18ed-107">Llama a [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) para inicializar el administrador de protocolos.</span><span class="sxs-lookup"><span data-stu-id="e18ed-107">Calls [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) to initialize the protocol manager.</span></span>
-   <span data-ttu-id="e18ed-108">Crea un objeto de administrador de protocolos mediante el CLSID.</span><span class="sxs-lookup"><span data-stu-id="e18ed-108">Creates a protocol manager object using the CLSID.</span></span> <span data-ttu-id="e18ed-109">Aunque haya varios agentes de escucha registrados para el mismo proveedor de protocolo, el servicio solo crea un objeto de administrador de protocolos.</span><span class="sxs-lookup"><span data-stu-id="e18ed-109">Even if there are multiple listeners registered for the same protocol provider, the service only creates one protocol manager object.</span></span>
-   <span data-ttu-id="e18ed-110">Llama a [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) para indicar al objeto de administrador de protocolos que debe crear un objeto de escucha de [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) y devolverlo al servicio.</span><span class="sxs-lookup"><span data-stu-id="e18ed-110">Calls [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) to instruct the protocol manager object to create an [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) listener object and return it to the service.</span></span> <span data-ttu-id="e18ed-111">El objeto de administrador de protocolos debe agregar una referencia al objeto de agente de escucha antes de devolverlo al servicio.</span><span class="sxs-lookup"><span data-stu-id="e18ed-111">The protocol manager object must add a reference to the listener object before returning it to the service.</span></span> <span data-ttu-id="e18ed-112">El servicio liberará el objeto cuando el servicio se detenga o se elimine el agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="e18ed-112">The service will release the object when the service stops or the listener is deleted.</span></span>
-   <span data-ttu-id="e18ed-113">Llama a [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) en el objeto de agente de escucha para que el agente de escucha pueda empezar a escuchar las conexiones entrantes.</span><span class="sxs-lookup"><span data-stu-id="e18ed-113">Calls [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) on the listener object so that the listener can start listening for incoming connections.</span></span>
-   <span data-ttu-id="e18ed-114">Llama a [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) para detener la escucha del objeto de escucha.</span><span class="sxs-lookup"><span data-stu-id="e18ed-114">Calls [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) to stop the listener object from listening.</span></span>
-   <span data-ttu-id="e18ed-115">Llama a [**UnInitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) para anular la inicialización del administrador de protocolos.</span><span class="sxs-lookup"><span data-stu-id="e18ed-115">Calls [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) to uninitialize the protocol manager.</span></span>

<span data-ttu-id="e18ed-116">El agente de escucha crea un objeto [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) cuando un cliente intenta conectarse.</span><span class="sxs-lookup"><span data-stu-id="e18ed-116">The listener creates an [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) object when a client tries to connect.</span></span> <span data-ttu-id="e18ed-117">El objeto de agente de escucha llama a [**Alconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) para notificar al servicio servicios de escritorio remoto que un nuevo cliente está intentando conectarse o volver a conectarse, y pasa el objeto **IWRdsProtocolConnection** en esa llamada.</span><span class="sxs-lookup"><span data-stu-id="e18ed-117">The listener object calls [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) to notify the Remote Desktop Services service that a new client is trying to connect or reconnect, and passes the **IWRdsProtocolConnection** object in that call.</span></span> <span data-ttu-id="e18ed-118">A su vez, el servicio Servicios de Escritorio remoto devolverá un objeto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) en esa llamada para que el protocolo pueda comunicarse con el servicio servicios de escritorio remoto según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e18ed-118">The Remote Desktop Services service will in turn return an [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) object in that call so that the protocol can communicate with the Remote Desktop Services service as needed.</span></span> <span data-ttu-id="e18ed-119">El servicio agrega una referencia al objeto de devolución de llamada antes de devolver y el protocolo debe liberar esa referencia cuando se cierre la conexión.</span><span class="sxs-lookup"><span data-stu-id="e18ed-119">The service adds a reference to the callback object before returning, and the protocol must release that reference when the connection closes.</span></span>

<span data-ttu-id="e18ed-120">En la ilustración siguiente se muestra la interacción entre los distintos objetos durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="e18ed-120">The following illustration shows the interaction between the various objects during startup.</span></span>

![secuencia de inicio de RCM](images/protocol-startsequence.png)

## <a name="related-topics"></a><span data-ttu-id="e18ed-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e18ed-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e18ed-123">Secuencia de llamada al método</span><span class="sxs-lookup"><span data-stu-id="e18ed-123">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="e18ed-124">Secuencia de conexión</span><span class="sxs-lookup"><span data-stu-id="e18ed-124">Connection Sequence</span></span>](connection-sequence.md)
</dt> </dl>

 

 




