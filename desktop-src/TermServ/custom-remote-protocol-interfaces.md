---
title: Interfaces de proveedor de Protocolo de escritorio remoto
description: Interfaces admitidas por la API del proveedor de Protocolo de escritorio remoto.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993816"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a><span data-ttu-id="771bc-103">Interfaces de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="771bc-103">Remote Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="771bc-104">La API del proveedor de Protocolo de escritorio remoto admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="771bc-104">The following interfaces are supported by the Remote Desktop Protocol Provider API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="771bc-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="771bc-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="771bc-106">**IWRdsProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="771bc-106">**IWRdsProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

<span data-ttu-id="771bc-107">Expone los métodos llamados por el servicio Servicios de Escritorio remoto para configurar una conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="771bc-107">Exposes methods called by the Remote Desktop Services service to configure a client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-108">**IWRdsProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="771bc-108">**IWRdsProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="771bc-109">Expone métodos que proporcionan información sobre el estado de una conexión de cliente y que realizan acciones para el cliente.</span><span class="sxs-lookup"><span data-stu-id="771bc-109">Exposes methods that provide information about the status of a client connection and that perform actions for the client.</span></span> <span data-ttu-id="771bc-110">El servicio Servicios de Escritorio remoto implementa esta interfaz y la llama el protocolo.</span><span class="sxs-lookup"><span data-stu-id="771bc-110">This interface is implemented by the Remote Desktop Services service and called by the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-111">**IWRdsProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="771bc-111">**IWRdsProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="771bc-112">Expone los métodos utilizados por el servicio de Servicios de Escritorio remoto para realizar el protocolo de enlace de licencias durante una secuencia de conexión.</span><span class="sxs-lookup"><span data-stu-id="771bc-112">Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-113">**IWRdsProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="771bc-113">**IWRdsProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

<span data-ttu-id="771bc-114">Expone métodos que solicitan que el protocolo inicie y deje de escuchar solicitudes de conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="771bc-114">Exposes methods that request that the protocol start and stop listening for client connection requests.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-115">**IWRdsProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="771bc-115">**IWRdsProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="771bc-116">Expone métodos que notifican al servicio Servicios de Escritorio remoto que un cliente se ha conectado.</span><span class="sxs-lookup"><span data-stu-id="771bc-116">Exposes methods that notify the Remote Desktop Services service that a client has connected.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-117">**IWRdsProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="771bc-117">**IWRdsProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="771bc-118">Expone los métodos llamados por el servicio Servicios de Escritorio remoto para actualizar el estado de inicio de sesión y determinar cómo dirigir los mensajes de error de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="771bc-118">Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-119">**IWRdsProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="771bc-119">**IWRdsProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

<span data-ttu-id="771bc-120">Expone los métodos que el servicio Servicios de Escritorio remoto utiliza para comunicarse con el proveedor de protocolo.</span><span class="sxs-lookup"><span data-stu-id="771bc-120">Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-121">**IWRdsProtocolSettings**</span><span class="sxs-lookup"><span data-stu-id="771bc-121">**IWRdsProtocolSettings**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

<span data-ttu-id="771bc-122">Expone métodos para recuperar y agregar la configuración relacionada con la Directiva.</span><span class="sxs-lookup"><span data-stu-id="771bc-122">Exposes methods for retrieving and adding policy-related settings.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-123">**IWRdsProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="771bc-123">**IWRdsProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="771bc-124">Expone los métodos llamados por el protocolo para notificar al servicio Servicios de Escritorio remoto que inicie o detenga el lado de destino de una sombra.</span><span class="sxs-lookup"><span data-stu-id="771bc-124">Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-125">**IWRdsProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="771bc-125">**IWRdsProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="771bc-126">Expone métodos que envían una notificación al proveedor del Protocolo sobre el estado de la sombra de la sesión.</span><span class="sxs-lookup"><span data-stu-id="771bc-126">Exposes methods that notify the protocol provider about the status of session shadowing.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-127">**IWRdsRemoteFXGraphicsConnection**</span><span class="sxs-lookup"><span data-stu-id="771bc-127">**IWRdsRemoteFXGraphicsConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

<span data-ttu-id="771bc-128">Expone métodos relacionados con la manipulación y el conocimiento de los gráficos en la conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="771bc-128">Exposes methods relating to the manipulation and understanding of graphics on the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="771bc-129">Interfaces de proveedor de protocolo de escritorio en desuso</span><span class="sxs-lookup"><span data-stu-id="771bc-129">Deprecated Desktop Protocol Provider Interfaces</span></span>](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

<span data-ttu-id="771bc-130">Las siguientes interfaces están desusadas y ya no deben usarse.</span><span class="sxs-lookup"><span data-stu-id="771bc-130">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="771bc-131">En el caso de los proyectos nuevos, use en su lugar las interfaces del proveedor de Protocolo de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="771bc-131">For new projects, use the Remote Desktop Protocol Provider Interfaces interfaces instead.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="771bc-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="771bc-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="771bc-133">Referencia del proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="771bc-133">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="771bc-134">Enumeraciones de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="771bc-134">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="771bc-135">Estructuras de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="771bc-135">Remote Desktop Protocol Provider Structures</span></span>](custom-remote-protocol-structures.md)
</dt> <dt>

[<span data-ttu-id="771bc-136">Uniones de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="771bc-136">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




