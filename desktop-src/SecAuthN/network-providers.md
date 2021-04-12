---
description: Un proveedor de red es un archivo DLL que admite un protocolo de red específico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278124"
---
# <a name="network-providers"></a><span data-ttu-id="d449a-103">Proveedores de red</span><span class="sxs-lookup"><span data-stu-id="d449a-103">Network Providers</span></span>

<span data-ttu-id="d449a-104">Un proveedor de red es un archivo DLL que admite un protocolo de red específico.</span><span class="sxs-lookup"><span data-stu-id="d449a-104">A network provider is a DLL that supports a specific network protocol.</span></span> <span data-ttu-id="d449a-105">También implementa la API del [proveedor de red](network-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="d449a-105">It also implements the [Network Provider API](network-provider-api.md).</span></span> <span data-ttu-id="d449a-106">Esto le permite interactuar con el sistema operativo Windows para recibir solicitudes de red estándar, como solicitudes de conexión o desconexión.</span><span class="sxs-lookup"><span data-stu-id="d449a-106">This enables it to interact with the Windows operating system to receive standard network requests, such as connection or disconnection requests.</span></span> <span data-ttu-id="d449a-107">Para controlar estas solicitudes, el proveedor de red llama entonces a la API específica de la red que sea adecuada para el protocolo de red que admite el proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="d449a-107">To handle these requests, the network provider then calls the network-specific API that is appropriate to the network protocol the network provider supports.</span></span> <span data-ttu-id="d449a-108">En otras palabras, el proveedor de red ajusta la funcionalidad específica de la red en un archivo DLL, que expone una interfaz estándar a Windows.</span><span class="sxs-lookup"><span data-stu-id="d449a-108">In other words, the network provider wraps the network-specific functionality in a DLL, which exposes a standard interface to Windows.</span></span>

<span data-ttu-id="d449a-109">Mediante el uso de proveedores de red, Windows puede admitir muchos tipos diferentes de protocolos de red sin tener que conocer los detalles específicos de la red de cada red.</span><span class="sxs-lookup"><span data-stu-id="d449a-109">Using network providers, Windows can support many different types of network protocols without having to know the network-specific details of each network.</span></span> <span data-ttu-id="d449a-110">Esto es esencial porque los nuevos protocolos de red se están desarrollando todo el tiempo.</span><span class="sxs-lookup"><span data-stu-id="d449a-110">This is essential because new network protocols are being developed all the time.</span></span> <span data-ttu-id="d449a-111">Con los proveedores de red, la compatibilidad con un nuevo protocolo requiere la creación e instalación de un nuevo proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="d449a-111">With network providers, supporting a new protocol simply requires creating and installing a new network provider.</span></span>

<span data-ttu-id="d449a-112">Para obtener información sobre las funciones y estructuras de proveedor de red, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d449a-112">For information about network provider functions and structures, see the following topics:</span></span>

-   [<span data-ttu-id="d449a-113">Funciones de proveedor de red</span><span class="sxs-lookup"><span data-stu-id="d449a-113">Network Provider Functions</span></span>](authentication-functions.md)
-   [<span data-ttu-id="d449a-114">Estructuras de proveedor de red</span><span class="sxs-lookup"><span data-stu-id="d449a-114">Network Provider Structures</span></span>](authentication-structures.md)

 

 



