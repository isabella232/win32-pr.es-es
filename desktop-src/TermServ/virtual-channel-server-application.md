---
title: Aplicación de servidor de canal virtual
description: El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación de modo de usuario que se ejecute en una sesión de cliente en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776950"
---
# <a name="virtual-channel-server-application"></a><span data-ttu-id="1406a-104">Aplicación de servidor de canal virtual</span><span class="sxs-lookup"><span data-stu-id="1406a-104">Virtual Channel Server Application</span></span>

<span data-ttu-id="1406a-105">El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación de modo de usuario que se ejecute en una sesión de cliente en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="1406a-105">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="1406a-106">Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="1406a-106">Note that you must provide a method to start the server application.</span></span> <span data-ttu-id="1406a-107">Puede hacerlo de varias maneras: por ejemplo, puede usar un script de inicio de sesión o un programa o script en la carpeta de inicio.</span><span class="sxs-lookup"><span data-stu-id="1406a-107">You can accomplish this in multiple ways; for example, you can use a logon script, or a program or script in the Startup folder.</span></span> <span data-ttu-id="1406a-108">Los usuarios también pueden iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1406a-108">Users could also launch the application.</span></span>

<span data-ttu-id="1406a-109">Debe almacenar el nombre de la aplicación de servidor de canal virtual en el registro agregando una subclave en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="1406a-109">You must store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="1406a-110">**HKEY \_ \_** \\  \\  \\ AddIns de **control** \\  \\  del sistema de equipo local Terminal Server</span><span class="sxs-lookup"><span data-stu-id="1406a-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Terminal Server**\\**Addins**</span></span>

<span data-ttu-id="1406a-111">Para obtener más información acerca de la subclave, vea [supervisar conexiones y desconexiones de sesión](monitoring-session-connections-and-disconnections.md).</span><span class="sxs-lookup"><span data-stu-id="1406a-111">For more information about the subkey, see [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).</span></span>

<span data-ttu-id="1406a-112">La aplicación de servidor puede llamar a la función [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) para abrir un identificador de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="1406a-112">The server application can call the [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) function to open a handle to a virtual channel.</span></span> <span data-ttu-id="1406a-113">A continuación, la aplicación puede utilizar el identificador en cualquiera de las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="1406a-113">The application can then use the handle in any of the following functions.</span></span>

<dl> <dt>

[<span data-ttu-id="1406a-114">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="1406a-114">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="1406a-115">Cierra un identificador de canal virtual abierto.</span><span class="sxs-lookup"><span data-stu-id="1406a-115">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="1406a-116">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="1406a-116">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="1406a-117">Elimina todos los datos de entrada en cola enviados del cliente al servidor en un canal virtual específico.</span><span class="sxs-lookup"><span data-stu-id="1406a-117">Deletes all queued input data sent from the client to the server on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="1406a-118">Servicios de Escritorio remoto no usa esta función actualmente.</span><span class="sxs-lookup"><span data-stu-id="1406a-118">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="1406a-119">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="1406a-119">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="1406a-120">Elimina todos los datos de salida en cola enviados desde el servidor al cliente en un canal virtual específico.</span><span class="sxs-lookup"><span data-stu-id="1406a-120">Deletes all queued output data sent from the server to the client on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="1406a-121">Servicios de Escritorio remoto no usa esta función actualmente.</span><span class="sxs-lookup"><span data-stu-id="1406a-121">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="1406a-122">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="1406a-122">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="1406a-123">Devuelve información sobre un canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="1406a-123">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="1406a-124">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="1406a-124">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="1406a-125">Lee los datos del extremo del servidor de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="1406a-125">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="1406a-126">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="1406a-126">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="1406a-127">Escribe datos en el extremo del servidor de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="1406a-127">Writes data to the server end of a virtual channel.</span></span>

</dd> </dl>

 

 




