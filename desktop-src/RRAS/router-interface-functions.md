---
title: Funciones de interfaz de enrutador
description: Utilice las siguientes funciones para administrar interfaces en el enrutador.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356661"
---
# <a name="router-interface-functions"></a><span data-ttu-id="f779f-103">Funciones de interfaz de enrutador</span><span class="sxs-lookup"><span data-stu-id="f779f-103">Router Interface Functions</span></span>

<span data-ttu-id="f779f-104">Utilice las siguientes funciones para administrar interfaces en el enrutador.</span><span class="sxs-lookup"><span data-stu-id="f779f-104">Use the following functions to administer interfaces on the router.</span></span>



| <span data-ttu-id="f779f-105">Función de administración</span><span class="sxs-lookup"><span data-stu-id="f779f-105">Administration Function</span></span>                                          | <span data-ttu-id="f779f-106">Función de configuración</span><span class="sxs-lookup"><span data-stu-id="f779f-106">Configuration Function</span></span>                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="f779f-107">**MprAdminInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="f779f-107">**MprAdminInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [<span data-ttu-id="f779f-108">**MprConfigInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="f779f-108">**MprConfigInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [<span data-ttu-id="f779f-109">**MprAdminInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="f779f-109">**MprAdminInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [<span data-ttu-id="f779f-110">**MprConfigInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="f779f-110">**MprConfigInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [<span data-ttu-id="f779f-111">**MprAdminInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="f779f-111">**MprAdminInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [<span data-ttu-id="f779f-112">**MprConfigInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="f779f-112">**MprConfigInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [<span data-ttu-id="f779f-113">**MprAdminInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="f779f-113">**MprAdminInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [<span data-ttu-id="f779f-114">**MprConfigInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="f779f-114">**MprConfigInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [<span data-ttu-id="f779f-115">**MprAdminInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="f779f-115">**MprAdminInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [<span data-ttu-id="f779f-116">**MprConfigInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="f779f-116">**MprConfigInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [<span data-ttu-id="f779f-117">**MprAdminInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="f779f-117">**MprAdminInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [<span data-ttu-id="f779f-118">**MprConfigInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="f779f-118">**MprConfigInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

<span data-ttu-id="f779f-119">Estas funciones afectan a las interfaces, no a los clientes que se ejecutan en las interfaces.</span><span class="sxs-lookup"><span data-stu-id="f779f-119">These functions affect the interfaces themselves, not clients running on the interfaces.</span></span> <span data-ttu-id="f779f-120">Por esta razón, ninguna de las funciones requiere que el llamador especifique un transporte determinado (IP o IPX); Aunque los clientes (como los protocolos de enrutamiento) están asociados a transportes particulares, las propias interfaces no lo son.</span><span class="sxs-lookup"><span data-stu-id="f779f-120">For this reason, none of the functions require the caller to specify a particular transport (IP or IPX); although clients (such as routing protocols) are associated with particular transports, the interfaces themselves are not.</span></span>

<span data-ttu-id="f779f-121">Estas funciones se controlan directamente mediante DIM.</span><span class="sxs-lookup"><span data-stu-id="f779f-121">These functions are handled directly by DIM.</span></span> <span data-ttu-id="f779f-122">No usan los administradores de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="f779f-122">They do not utilize the router managers.</span></span>

<span data-ttu-id="f779f-123">Las funciones [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) y [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) no pueden crear ni eliminar interfaces LAN.</span><span class="sxs-lookup"><span data-stu-id="f779f-123">The [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) and [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) functions cannot create or delete LAN interfaces.</span></span> <span data-ttu-id="f779f-124">Solo pueden crear o eliminar interfaces de marcado a petición.</span><span class="sxs-lookup"><span data-stu-id="f779f-124">They can only create or delete demand-dial interfaces.</span></span> <span data-ttu-id="f779f-125">Consulte [**\_ \_ tipo de interfaz de enrutador**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) para obtener una lista de tipos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="f779f-125">See [**ROUTER\_INTERFACE\_TYPE**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) for a list of interface types.</span></span>

 

 




