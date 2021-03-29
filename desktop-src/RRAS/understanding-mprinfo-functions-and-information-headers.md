---
title: Descripción de las funciones de MprInfo y los encabezados de información
description: Las siguientes funciones requieren que el llamador pase una estructura o un encabezado de información como uno de los parámetros.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994291"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a><span data-ttu-id="467bd-103">Descripción de las funciones de MprInfo y los encabezados de información</span><span class="sxs-lookup"><span data-stu-id="467bd-103">Understanding MprInfo Functions and Information Headers</span></span>

<span data-ttu-id="467bd-104">Las siguientes funciones requieren que el llamador pase una estructura o un *encabezado* de información como uno de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="467bd-104">The following functions require that the caller pass an information structure or *header* as one of the parameters.</span></span>



| <span data-ttu-id="467bd-105">Función de administración</span><span class="sxs-lookup"><span data-stu-id="467bd-105">Administration function</span></span>                                                        | <span data-ttu-id="467bd-106">Función de configuración</span><span class="sxs-lookup"><span data-stu-id="467bd-106">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="467bd-107">Sin función de administración</span><span class="sxs-lookup"><span data-stu-id="467bd-107">No administration function</span></span>                                                     | [<span data-ttu-id="467bd-108">**MprConfigTransportCreate**</span><span class="sxs-lookup"><span data-stu-id="467bd-108">**MprConfigTransportCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [<span data-ttu-id="467bd-109">**MprAdminTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-109">**MprAdminTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [<span data-ttu-id="467bd-110">**MprConfigTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-110">**MprConfigTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [<span data-ttu-id="467bd-111">**MprAdminInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-111">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="467bd-112">**MprConfigInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-112">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [<span data-ttu-id="467bd-113">**MprAdminInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="467bd-113">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="467bd-114">**MprConfigInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="467bd-114">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

<span data-ttu-id="467bd-115">Del mismo modo, las siguientes funciones devuelven encabezados de información.</span><span class="sxs-lookup"><span data-stu-id="467bd-115">Similarly, the following functions return information headers.</span></span>



| <span data-ttu-id="467bd-116">Función de administración</span><span class="sxs-lookup"><span data-stu-id="467bd-116">Administration function</span></span>                                                        | <span data-ttu-id="467bd-117">Función de configuración</span><span class="sxs-lookup"><span data-stu-id="467bd-117">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="467bd-118">**MprAdminTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-118">**MprAdminTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [<span data-ttu-id="467bd-119">**MprConfigTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-119">**MprConfigTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [<span data-ttu-id="467bd-120">**MprAdminInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-120">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="467bd-121">**MprConfigInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="467bd-121">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

<span data-ttu-id="467bd-122">En el caso de las funciones de transporte, el encabezado de información contiene información global para el transporte.</span><span class="sxs-lookup"><span data-stu-id="467bd-122">For the transport functions, the information header contains global information for the transport.</span></span> <span data-ttu-id="467bd-123">En el caso de las funciones de cliente (InterfaceTransport), el encabezado contiene información específica del cliente (por ejemplo, OSPF) que se administra.</span><span class="sxs-lookup"><span data-stu-id="467bd-123">For the client (InterfaceTransport) functions, the header contains information specific to the client (for example, OSPF) being administered.</span></span>

<span data-ttu-id="467bd-124">Los encabezados de información y su contenido deben manipularse solo mediante las funciones de [MprInfo](router-information-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="467bd-124">The information headers and their contents should be manipulated only by using the [MprInfo](router-information-functions.md) functions.</span></span> <span data-ttu-id="467bd-125">Los desarrolladores no deben intentar manipular el contenido de los encabezados de información directamente.</span><span class="sxs-lookup"><span data-stu-id="467bd-125">Developers should not attempt to manipulate the contents of the information headers directly.</span></span>

<span data-ttu-id="467bd-126">Las funciones de solo interfaz, como [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , no requieren el uso de las funciones de MprInfo.</span><span class="sxs-lookup"><span data-stu-id="467bd-126">The interface-only functions such as [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) do not require the use of MprInfo functions.</span></span> <span data-ttu-id="467bd-127">La información que se pasa y se devuelve con estas funciones siempre tiene el formato de una estructura de [**\_ interfaz de MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .</span><span class="sxs-lookup"><span data-stu-id="467bd-127">The information that is passed and returned with these functions is always in the form of an [**MPR\_INTERFACE**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) structure.</span></span>

 

 




