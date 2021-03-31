---
description: El MSP de conferencias IP implementa varias interfaces específicas del proveedor para el control del participante. Estas interfaces se exponen en el objeto de llamada si este MSP está asociado a la llamada.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Interfaces de IPConf MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155889"
---
# <a name="ipconf-msp-interfaces"></a><span data-ttu-id="41693-104">Interfaces de IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="41693-104">IPConf MSP Interfaces</span></span>

<span data-ttu-id="41693-105">\[ Las interfaces IPConf MSP no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="41693-105">\[ The IPConf MSP Interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="41693-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="41693-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="41693-107">El MSP de conferencias IP implementa varias interfaces específicas del proveedor para el control del participante.</span><span class="sxs-lookup"><span data-stu-id="41693-107">The IP conferencing MSP implements several provider-specific interfaces for participant control.</span></span> <span data-ttu-id="41693-108">Estas interfaces se exponen en el objeto de llamada si este MSP está asociado a la llamada.</span><span class="sxs-lookup"><span data-stu-id="41693-108">These interfaces are exposed on the call object, if this MSP is associated with the call.</span></span>

<span data-ttu-id="41693-109">Las interfaces [**ITParticipantEvent**](itparticipantevent.md) y [**IEnumParticipant**](ienumparticipant.md) son objetos independientes y se enumeran aquí para mayor comodidad de referencia.</span><span class="sxs-lookup"><span data-stu-id="41693-109">The [**ITParticipantEvent**](itparticipantevent.md) and [**IEnumParticipant**](ienumparticipant.md) interfaces are stand-alone objects, and are listed here for reference convenience.</span></span>



| <span data-ttu-id="41693-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="41693-110">Interface</span></span>                                            | <span data-ttu-id="41693-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="41693-111">Description</span></span>                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41693-112">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="41693-112">**IMulticastControl**</span></span>](imulticastcontrol.md)       | <span data-ttu-id="41693-113">Permite a una aplicación establecer y obtener el modo de bucle invertido ( [**\_ \_ modo de bucle invertido de multidifusión**](multicast-loopback-mode.md)) para un objeto de conferencia de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="41693-113">Allows an application to set and get the loopback mode ( [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md)) for a multicast conference object.</span></span> |
| [<span data-ttu-id="41693-114">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="41693-114">**ITParticipant**</span></span>](itparticipant.md)               | <span data-ttu-id="41693-115">Permite a una aplicación recuperar información sobre los participantes de la Conferencia y obtener punteros a las secuencias asociadas a esos participantes.</span><span class="sxs-lookup"><span data-stu-id="41693-115">Allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>             |
| [<span data-ttu-id="41693-116">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="41693-116">**ITParticipantControl**</span></span>](itparticipantcontrol.md) | <span data-ttu-id="41693-117">Permite que una aplicación recupere punteros a los participantes de una conferencia.</span><span class="sxs-lookup"><span data-stu-id="41693-117">Allows an application to retrieve pointers to the participants in a conference.</span></span>                                                                           |
| [<span data-ttu-id="41693-118">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="41693-118">**ITParticipantEvent**</span></span>](itparticipantevent.md)     | <span data-ttu-id="41693-119">Permite que una aplicación recupere información de eventos relativa a un participante de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="41693-119">Allows an application to retrieve event information concerning a conference participant.</span></span>                                                                  |
| [<span data-ttu-id="41693-120">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="41693-120">**IEnumParticipant**</span></span>](ienumparticipant.md)         | <span data-ttu-id="41693-121">Enumera [**ITParticipant**](itparticipant.md).</span><span class="sxs-lookup"><span data-stu-id="41693-121">Enumerates [**ITParticipant**](itparticipant.md).</span></span>                                                                                                        |



 

 

 



