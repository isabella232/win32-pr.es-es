---
title: API de cliente de DVC
description: Las API de cliente de canal virtual dinámico (DVC) se implementan específicamente para el cliente de Conexión a Escritorio remoto (RDC) de la conexión.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356974"
---
# <a name="dvc-client-apis"></a><span data-ttu-id="167cd-103">API de cliente de DVC</span><span class="sxs-lookup"><span data-stu-id="167cd-103">DVC Client APIs</span></span>

<span data-ttu-id="167cd-104">Las API de cliente de canal virtual dinámico (DVC) se implementan específicamente para el cliente de Conexión a Escritorio remoto (RDC) de la conexión.</span><span class="sxs-lookup"><span data-stu-id="167cd-104">The dynamic virtual channel (DVC) client APIs are implemented specifically for the Remote Desktop Connection (RDC) client of the connection.</span></span> <span data-ttu-id="167cd-105">Algunas de las API se implementan mediante el marco de DVC y otras las implementa el desarrollador del complemento.</span><span class="sxs-lookup"><span data-stu-id="167cd-105">Some of the APIs are implemented by the DVC framework, and some are implemented by the plug-in developer.</span></span> <span data-ttu-id="167cd-106">Algunas de las API se utilizan para admitir el complemento de cliente de Conexión a Escritorio remoto (RDC) y no están directamente relacionadas con el transporte de datos.</span><span class="sxs-lookup"><span data-stu-id="167cd-106">Some of the APIs are used to support the Remote Desktop Connection (RDC) client plug-in, and are not directly related to data transport.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="167cd-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="167cd-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="167cd-108">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="167cd-108">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

<span data-ttu-id="167cd-109">Permite que el cliente de Conexión a Escritorio remoto (RDC) cargue el complemento de cliente de Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="167cd-109">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="167cd-110">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="167cd-110">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

<span data-ttu-id="167cd-111">Administra los valores de configuración para cada agente de escucha para la conexión de canal virtual dinámico (DVC).</span><span class="sxs-lookup"><span data-stu-id="167cd-111">Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.</span></span>

</dd> <dt>

[<span data-ttu-id="167cd-112">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="167cd-112">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

<span data-ttu-id="167cd-113">Se usa para notificar al complemento de cliente de Conexión a Escritorio remoto (RDC) acerca de las solicitudes entrantes en un agente de escucha determinado.</span><span class="sxs-lookup"><span data-stu-id="167cd-113">Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span>

</dd> <dt>

[<span data-ttu-id="167cd-114">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="167cd-114">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

<span data-ttu-id="167cd-115">Administra todos los complementos de cliente de Conexión a Escritorio remoto (RDC) y los agentes de escucha del canal virtual dinámico (DVC).</span><span class="sxs-lookup"><span data-stu-id="167cd-115">Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.</span></span>

</dd> <dt>

[<span data-ttu-id="167cd-116">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="167cd-116">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

<span data-ttu-id="167cd-117">Se usa para controlar el estado del canal y escribe en el canal.</span><span class="sxs-lookup"><span data-stu-id="167cd-117">Used to control the channel state, and writes on the channel.</span></span>

</dd> <dt>

[<span data-ttu-id="167cd-118">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="167cd-118">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

<span data-ttu-id="167cd-119">Recibe notificaciones sobre los cambios de estado del canal o los datos recibidos.</span><span class="sxs-lookup"><span data-stu-id="167cd-119">Receives notifications about channel state changes or data received.</span></span>

</dd> <dt>

[<span data-ttu-id="167cd-120">**IWTSVirtualChannelCallback2**</span><span class="sxs-lookup"><span data-stu-id="167cd-120">**IWTSVirtualChannelCallback2**</span></span>](iwtsvirtualchannelcallback2.md)
</dt> <dd>

<span data-ttu-id="167cd-121">No se admite esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="167cd-121">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="167cd-122">**VirtualChannelGetInstance**</span><span class="sxs-lookup"><span data-stu-id="167cd-122">**VirtualChannelGetInstance**</span></span>](virtualchannelgetinstance.md)
</dt> <dd>

<span data-ttu-id="167cd-123">Se llama para que el complemento cree una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="167cd-123">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

</dd> </dl>

 

 




