---
title: Escritura de un módulo DVC de cliente
description: Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685565"
---
# <a name="writing-a-client-dvc-module"></a><span data-ttu-id="e532d-103">Escritura de un módulo DVC de cliente</span><span class="sxs-lookup"><span data-stu-id="e532d-103">Writing a Client DVC Module</span></span>

<span data-ttu-id="e532d-104">Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="e532d-104">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span> <span data-ttu-id="e532d-105">El complemento DVC es una implementación de [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrada como un objeto de modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="e532d-105">The DVC plug-in is an implementation of [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registered as a Component Object Model (COM) object.</span></span>

> [!Note]  
> <span data-ttu-id="e532d-106">El complemento debe implementarse en un modelo de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="e532d-106">The plug-in must be implemented in a free-threading model.</span></span> <span data-ttu-id="e532d-107">No se admite la implementación de modelo de apartamento.</span><span class="sxs-lookup"><span data-stu-id="e532d-107">Apartment-model implementation is not supported.</span></span>

 

<span data-ttu-id="e532d-108">A continuación se muestra una lista de interfaces que se implementan mediante objetos a los que se crea una instancia del complemento.</span><span class="sxs-lookup"><span data-stu-id="e532d-108">The following is a list of interfaces that are implemented by objects that are instantiated by the plug-in.</span></span>



| <span data-ttu-id="e532d-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="e532d-109">Interface</span></span>                                                        | <span data-ttu-id="e532d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e532d-110">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e532d-111">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="e532d-111">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | <span data-ttu-id="e532d-112">Permite que el cliente de Conexión a Escritorio remoto (RDC) cargue el complemento de cliente de Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="e532d-112">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span><br/>                                                                 |
| [<span data-ttu-id="e532d-113">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="e532d-113">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | <span data-ttu-id="e532d-114">Notifica al complemento de cliente de Conexión a Escritorio remoto (RDC) sobre las solicitudes entrantes en un agente de escucha determinado.</span><span class="sxs-lookup"><span data-stu-id="e532d-114">Notifies the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span><br/>                                                                             |
| [<span data-ttu-id="e532d-115">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="e532d-115">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | <span data-ttu-id="e532d-116">Recibe notificaciones sobre los cambios de estado del canal o los datos recibidos.</span><span class="sxs-lookup"><span data-stu-id="e532d-116">Receives notifications about channel state changes or data received.</span></span> <span data-ttu-id="e532d-117">Cada instancia de esta interfaz está asociada a una instancia de [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span><span class="sxs-lookup"><span data-stu-id="e532d-117">Each instance of this interface is associated with one instance of [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span></span><br/> |



 

<span data-ttu-id="e532d-118">A continuación se muestra una lista de interfaces implementadas por objetos a los que se crean instancias mediante el cliente Conexión a Escritorio remoto (RDC) y que forman parte del marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e532d-118">The following is a list of interfaces that are implemented by objects that are instantiated by the Remote Desktop Connection (RDC) client, and are part of the framework.</span></span>



| <span data-ttu-id="e532d-119">Interfaz</span><span class="sxs-lookup"><span data-stu-id="e532d-119">Interface</span></span>                                                      | <span data-ttu-id="e532d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e532d-120">Description</span></span>                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e532d-121">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="e532d-121">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | <span data-ttu-id="e532d-122">Administra todos los complementos de cliente de Conexión a Escritorio remoto (RDC), agentes de escucha de DVC o canales virtuales estáticos.</span><span class="sxs-lookup"><span data-stu-id="e532d-122">Manages all Remote Desktop Connection (RDC) client plug-ins, DVC listeners, or static virtual channels.</span></span><br/> |
| [<span data-ttu-id="e532d-123">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="e532d-123">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | <span data-ttu-id="e532d-124">Administra los valores de configuración para cada agente de escucha para la conexión de DVC.</span><span class="sxs-lookup"><span data-stu-id="e532d-124">Manages configuration settings for each listener for the DVC connection.</span></span><br/>                                |
| [<span data-ttu-id="e532d-125">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="e532d-125">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | <span data-ttu-id="e532d-126">Controla el estado del canal, así como las operaciones de escritura en el canal.</span><span class="sxs-lookup"><span data-stu-id="e532d-126">Controls the channel state, as well as writes on the channel.</span></span><br/>                                           |



 

<span data-ttu-id="e532d-127">En la ilustración siguiente se muestra la relación entre el cliente de Conexión a Escritorio remoto (RDC) y el complemento de cliente de Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="e532d-127">The following illustration shows the relationship between the Remote Desktop Connection (RDC) client and the Remote Desktop Connection (RDC) client plug-in.</span></span>

![relación del cliente y el complemento](images/tsclient.png)

 

 





