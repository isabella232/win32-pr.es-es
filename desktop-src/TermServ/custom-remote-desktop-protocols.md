---
title: API del proveedor de Protocolo de escritorio remoto
description: La API de proveedor de Protocolo de escritorio remoto se usa para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993817"
---
# <a name="remote-desktop-protocol-provider-api"></a><span data-ttu-id="ad533-103">API del proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="ad533-103">Remote Desktop Protocol Provider API</span></span>

<span data-ttu-id="ad533-104">La API de proveedor de Protocolo de escritorio remoto se usa para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.</span><span class="sxs-lookup"><span data-stu-id="ad533-104">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

<span data-ttu-id="ad533-105">Cuando se carga Windows Server, se inicia el servicio Servicios de Escritorio remoto (también conocido como administrador de conexiones remotas (RCM)).</span><span class="sxs-lookup"><span data-stu-id="ad533-105">When Windows Server loads, the Remote Desktop Services service (also known as Remote Connection Manager (RCM)) starts.</span></span> <span data-ttu-id="ad533-106">El servicio también inicia objetos de escucha para los proveedores de Protocolo de escritorio remoto que, a su vez, escuchan las conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="ad533-106">The service also starts listener objects for the Remote Desktop Protocol Providers that in turn listen for client connections.</span></span> <span data-ttu-id="ad533-107">El servicio y los proveedores de protocolo son objetos de modo usuario que se comunican mediante las API descritas en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="ad533-107">The service and the protocol providers are user-mode objects that communicate by using the APIs discussed in this documentation.</span></span> <span data-ttu-id="ad533-108">Los proveedores de protocolos pueden comunicarse con los controladores de modo kernel mediante controles de entrada y salida (ioctl).</span><span class="sxs-lookup"><span data-stu-id="ad533-108">The protocol providers can communicate with kernel-mode drivers by using input/output controls (IOCTLs).</span></span> <span data-ttu-id="ad533-109">Esto se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ad533-109">This is shown in the following illustration.</span></span>

![arquitectura de API de protocolo personalizado](images/protocol-architecture.png)

<span data-ttu-id="ad533-111">Microsoft implementó el Protocolo de escritorio remoto (RDP) para proporcionar comunicación entre el servicio Servicios de Escritorio remoto y las conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="ad533-111">Microsoft has implemented the Remote Desktop Protocol (RDP) to provide communication between the Remote Desktop Services service and client connections.</span></span> <span data-ttu-id="ad533-112">Puede crear su propio protocolo con las interfaces, estructuras, uniones y tipos de enumeración que componen la API de proveedor de Protocolo de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ad533-112">You can create your own protocol by using the interfaces, structures, unions, and enumeration types that make up the Remote Desktop Protocol Provider API.</span></span> <span data-ttu-id="ad533-113">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="ad533-113">For more information, see the following topics.</span></span>

<dl> <dt>

[<span data-ttu-id="ad533-114">Creación de un proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="ad533-114">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dd>

<span data-ttu-id="ad533-115">Información sobre cómo crear un proveedor de Protocolo de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ad533-115">Information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="ad533-116">El administrador de protocolos se implementa como un servidor COM y se registra en una ubicación en la que se busca cuando se inicia el servicio Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ad533-116">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

</dd> <dt>

[<span data-ttu-id="ad533-117">Referencia del proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="ad533-117">Remote Desktop Protocol Provider reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dd>

<span data-ttu-id="ad533-118">Contiene interfaces, estructuras, uniones y tipos de enumeración que permiten crear un Protocolo de escritorio remoto personalizado (RDP).</span><span class="sxs-lookup"><span data-stu-id="ad533-118">Contains interfaces, structures, unions, and enumeration types that enable you to create a custom Remote Desktop Protocol (RDP).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ad533-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad533-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad533-120">Acerca de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="ad533-120">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> </dl>

 

 




