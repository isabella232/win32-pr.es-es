---
description: El agente DDE de red inicia DDE de red si detecta la actividad DDE de red local.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agente DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686524"
---
# <a name="network-dde-agent"></a><span data-ttu-id="3eadb-103">Agente DDE de red</span><span class="sxs-lookup"><span data-stu-id="3eadb-103">Network DDE Agent</span></span>

<span data-ttu-id="3eadb-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="3eadb-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="3eadb-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="3eadb-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="3eadb-106">El agente DDE de red inicia DDE de red si detecta la actividad DDE de red local.</span><span class="sxs-lookup"><span data-stu-id="3eadb-106">The network DDE agent starts network DDE if it detects local network DDE activity.</span></span> <span data-ttu-id="3eadb-107">No detecta un cliente remoto que intente conectarse.</span><span class="sxs-lookup"><span data-stu-id="3eadb-107">It does not detect a remote client trying to connect.</span></span> <span data-ttu-id="3eadb-108">Por lo tanto, antes de que un cliente pueda conectarse correctamente, se debe iniciar DDE de red en el equipo servidor.</span><span class="sxs-lookup"><span data-stu-id="3eadb-108">Therefore, before any client can successfully connect, network DDE must be started on the server computer.</span></span> <span data-ttu-id="3eadb-109">Tenga en cuenta que DDE de red no se inicia de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3eadb-109">Note that network DDE is not started by default.</span></span> <span data-ttu-id="3eadb-110">Para iniciar DDE de red, ejecute NETDDE.EXE.</span><span class="sxs-lookup"><span data-stu-id="3eadb-110">To start network DDE, run NETDDE.EXE.</span></span> <span data-ttu-id="3eadb-111">Este archivo se encuentra en el directorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="3eadb-111">This file is located in your Windows directory.</span></span>

<span data-ttu-id="3eadb-112">El agente DDE de red también inicia las aplicaciones necesarias para DDE de red.</span><span class="sxs-lookup"><span data-stu-id="3eadb-112">The network DDE agent also starts the applications necessary for network DDE.</span></span> <span data-ttu-id="3eadb-113">Una vez iniciado DDE de red, las conversaciones DDE se controlan a través de una ventana DDE de red asociada a una de las aplicaciones DDE de red.</span><span class="sxs-lookup"><span data-stu-id="3eadb-113">After network DDE is started, DDE conversations are controlled through a network DDE window associated with one of the network DDE applications.</span></span> <span data-ttu-id="3eadb-114">Esta aplicación actúa como proxy.</span><span class="sxs-lookup"><span data-stu-id="3eadb-114">This application acts as a proxy.</span></span> <span data-ttu-id="3eadb-115">Se comunica con todas las aplicaciones DDE locales y remotas.</span><span class="sxs-lookup"><span data-stu-id="3eadb-115">It communicates with all local and remote DDE applications.</span></span>

 

 



