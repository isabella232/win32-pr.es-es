---
description: Un proveedor de red es un archivo DLL que permite al sistema operativo Windows interactuar con otros tipos de redes, como Novell. Es un cliente del controlador Windows WNet.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API de proveedor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648559"
---
# <a name="network-provider-api"></a><span data-ttu-id="a9700-104">API de proveedor de red</span><span class="sxs-lookup"><span data-stu-id="a9700-104">Network Provider API</span></span>

<span data-ttu-id="a9700-105">Un proveedor de red es un archivo DLL que permite al sistema operativo Windows interactuar con otros tipos de redes, como Novell.</span><span class="sxs-lookup"><span data-stu-id="a9700-105">A network provider is a DLL that enables the Windows operating system to interact with other kinds of networks, such as Novell.</span></span> <span data-ttu-id="a9700-106">Es un cliente del controlador Windows WNet.</span><span class="sxs-lookup"><span data-stu-id="a9700-106">It is a client of the Windows WNet driver.</span></span> <span data-ttu-id="a9700-107">Un proveedor de red implementa acciones específicas de la red, como establecer una conexión y expone una interfaz común a Windows.</span><span class="sxs-lookup"><span data-stu-id="a9700-107">A network provider implements network-specific actions, such as making a connection, and exposes a common interface to Windows.</span></span> <span data-ttu-id="a9700-108">Esta interfaz se denomina API de proveedor de red y consta de funciones implementadas por el proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="a9700-108">This interface is called the Network Provider API and consists of functions implemented by the network provider.</span></span> <span data-ttu-id="a9700-109">Puede crear un archivo DLL de proveedor de red para admitir nuevos protocolos de red.</span><span class="sxs-lookup"><span data-stu-id="a9700-109">You can create a network provider DLL to support new network protocols.</span></span>

<span data-ttu-id="a9700-110">Dado que cada red expone una interfaz común a través de su proveedor, Windows puede interactuar con varios tipos de redes sin conocer los detalles de la implementación específica de la red.</span><span class="sxs-lookup"><span data-stu-id="a9700-110">Because each network exposes a common interface through its provider, Windows can interact with several types of networks without knowing their network-specific implementation details.</span></span>

<span data-ttu-id="a9700-111">El [*enrutador de proveedor múltiple*](../secgloss/m-gly.md) (MPR) controla la comunicación con todos los diversos proveedores de red del sistema y presenta una red integrada al usuario.</span><span class="sxs-lookup"><span data-stu-id="a9700-111">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication with all of the various network providers on the system and presents an integrated network to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9700-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9700-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9700-113">Proveedores de red</span><span class="sxs-lookup"><span data-stu-id="a9700-113">Network Providers</span></span>](network-providers.md)
</dt> <dt>

[<span data-ttu-id="a9700-114">Administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="a9700-114">Credential Manager</span></span>](credential-manager.md)
</dt> <dt>

[<span data-ttu-id="a9700-115">Enrutador de varios proveedores</span><span class="sxs-lookup"><span data-stu-id="a9700-115">Multiple Provider Router</span></span>](multiple-provider-router.md)
</dt> <dt>

[<span data-ttu-id="a9700-116">Funciones implementadas por los proveedores de red</span><span class="sxs-lookup"><span data-stu-id="a9700-116">Functions Implemented by Network Providers</span></span>](functions-implemented-by-network-providers.md)
</dt> <dt>

[<span data-ttu-id="a9700-117">API de administración de credenciales</span><span class="sxs-lookup"><span data-stu-id="a9700-117">Credential Management API</span></span>](credential-management-api.md)
</dt> <dt>

[<span data-ttu-id="a9700-118">API de notificación de conexión</span><span class="sxs-lookup"><span data-stu-id="a9700-118">Connection Notification API</span></span>](connection-notification-api.md)
</dt> </dl>

 

 
