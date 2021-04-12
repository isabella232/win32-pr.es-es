---
description: Las funciones de redireccionamiento de dispositivos redirigen los dispositivos de MS-DOS estándar, las letras de unidad y los puertos LPT. Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y tengan acceso a la red de forma totalmente transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Funciones de Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275216"
---
# <a name="device-redirecting-functions"></a><span data-ttu-id="62588-104">Funciones de Device-Redirecting</span><span class="sxs-lookup"><span data-stu-id="62588-104">Device-Redirecting Functions</span></span>

<span data-ttu-id="62588-105">Las funciones de redireccionamiento de dispositivos redirigen los dispositivos de MS-DOS estándar, las letras de unidad y los puertos LPT.</span><span class="sxs-lookup"><span data-stu-id="62588-105">The device-redirecting functions redirect standard MS-DOS devices, drive letters and LPT ports.</span></span> <span data-ttu-id="62588-106">Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y tengan acceso a la red de forma totalmente transparente.</span><span class="sxs-lookup"><span data-stu-id="62588-106">This enables applications running on the system to use the devices and access the network in a totally transparent manner.</span></span>



| <span data-ttu-id="62588-107">Función</span><span class="sxs-lookup"><span data-stu-id="62588-107">Function</span></span>                                                         | <span data-ttu-id="62588-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="62588-108">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62588-109">**NPAddConnection**</span><span class="sxs-lookup"><span data-stu-id="62588-109">**NPAddConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | <span data-ttu-id="62588-110">Redirige o conecta un dispositivo local a un recurso de red.</span><span class="sxs-lookup"><span data-stu-id="62588-110">Redirects or connects a local device to a network resource.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="62588-111">**NPAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="62588-111">**NPAddConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | <span data-ttu-id="62588-112">Realiza la misma acción que [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), pero permite al usuario especificar qué ventana debe ser propietaria de los cuadros de diálogo y cómo debe establecerse la conexión.</span><span class="sxs-lookup"><span data-stu-id="62588-112">Performs the same action as [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), but lets the user specify which window should own any dialog boxes and how the connection should be established.</span></span><br/> |
| [<span data-ttu-id="62588-113">**NPCancelConnection**</span><span class="sxs-lookup"><span data-stu-id="62588-113">**NPCancelConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | <span data-ttu-id="62588-114">Interrumpe una conexión de red.</span><span class="sxs-lookup"><span data-stu-id="62588-114">Breaks a network connection.</span></span> <span data-ttu-id="62588-115">Los cambios se recuerdan si un dispositivo se desconecta a menos que la conexión sea una conexión sin dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62588-115">The changes are remembered if a device is disconnected unless the connection is a deviceless connection.</span></span><br/>                                                    |
| [<span data-ttu-id="62588-116">**NPGetConnection**</span><span class="sxs-lookup"><span data-stu-id="62588-116">**NPGetConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | <span data-ttu-id="62588-117">Devuelve información sobre una conexión.</span><span class="sxs-lookup"><span data-stu-id="62588-117">Returns information about a connection.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="62588-118">**NPGetConnection3**</span><span class="sxs-lookup"><span data-stu-id="62588-118">**NPGetConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | <span data-ttu-id="62588-119">Devuelve información sobre una conexión, incluso si la conexión está actualmente desconectada.</span><span class="sxs-lookup"><span data-stu-id="62588-119">Returns information about a connection, even if the connection is currently disconnected.</span></span><br/>                                                                                                |
| [<span data-ttu-id="62588-120">**NPGetConnectionPerformance**</span><span class="sxs-lookup"><span data-stu-id="62588-120">**NPGetConnectionPerformance**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | <span data-ttu-id="62588-121">Devuelve información de rendimiento sobre una conexión.</span><span class="sxs-lookup"><span data-stu-id="62588-121">Returns performance information about a connection.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="62588-122">**NPGetUniversalName**</span><span class="sxs-lookup"><span data-stu-id="62588-122">**NPGetUniversalName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | <span data-ttu-id="62588-123">Devuelve el nombre universal local o remoto, en el formato especificado durante la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="62588-123">Returns the remote or local universal name, in the format specified during the function call.</span></span><br/>                                                                                            |



 

 

 




