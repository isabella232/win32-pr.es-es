---
title: Creación de un proveedor de Protocolo de escritorio remoto
description: Información sobre cómo crear un proveedor de Protocolo de escritorio remoto. El administrador de protocolos se implementa como un servidor COM y se registra en una ubicación en la que se busca cuando se inicia el servicio Servicios de Escritorio remoto.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685470"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a><span data-ttu-id="332a9-104">Creación de un proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="332a9-104">Creating a Remote Desktop Protocol Provider</span></span>

<span data-ttu-id="332a9-105">Las secciones siguientes contienen información sobre cómo crear un proveedor de Protocolo de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="332a9-105">The following sections contain information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="332a9-106">El administrador de protocolos se implementa como un servidor COM y se registra en una ubicación en la que se busca cuando se inicia el servicio Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="332a9-106">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="332a9-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="332a9-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="332a9-108">Registro del administrador de protocolos</span><span class="sxs-lookup"><span data-stu-id="332a9-108">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
</dt> <dd>

<span data-ttu-id="332a9-109">Debe crear al menos una entrada de valor de registro para el administrador de protocolos para que el servicio de Servicios de Escritorio remoto pueda crear una instancia de ella.</span><span class="sxs-lookup"><span data-stu-id="332a9-109">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

</dd> <dt>

[<span data-ttu-id="332a9-110">Secuencia de llamada al método</span><span class="sxs-lookup"><span data-stu-id="332a9-110">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dd>

<span data-ttu-id="332a9-111">El servicio de Servicios de Escritorio remoto y el proveedor de protocolo se llaman entre sí en secuencias claramente definidas.</span><span class="sxs-lookup"><span data-stu-id="332a9-111">The Remote Desktop Services service and your protocol provider call each other in clearly defined sequences.</span></span>

</dd> </dl>

-   [<span data-ttu-id="332a9-112">Registro del administrador de protocolos</span><span class="sxs-lookup"><span data-stu-id="332a9-112">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
-   [<span data-ttu-id="332a9-113">Secuencia de llamada al método</span><span class="sxs-lookup"><span data-stu-id="332a9-113">Method Call Sequence</span></span>](method-call-sequence.md)

## <a name="related-topics"></a><span data-ttu-id="332a9-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="332a9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="332a9-115">API del proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="332a9-115">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dt>

[<span data-ttu-id="332a9-116">Usar Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="332a9-116">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> </dl>

 

 




