---
description: La interfaz de programación ad hoc inalámbrica se compone de las siguientes interfaces.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfaces ad hoc inalámbricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677583"
---
# <a name="wireless-ad-hoc-interfaces"></a><span data-ttu-id="8daa0-103">Interfaces ad hoc inalámbricas</span><span class="sxs-lookup"><span data-stu-id="8daa0-103">Wireless Ad Hoc Interfaces</span></span>

<span data-ttu-id="8daa0-104">La interfaz de programación ad hoc inalámbrica se compone de las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="8daa0-104">The wireless ad hoc programming interface is composed of the following interfaces.</span></span>



| <span data-ttu-id="8daa0-105">Nombre de la interfaz</span><span class="sxs-lookup"><span data-stu-id="8daa0-105">Interface Name</span></span>                                                                       | <span data-ttu-id="8daa0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8daa0-106">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8daa0-107">**IDot11AdHocInterface**</span><span class="sxs-lookup"><span data-stu-id="8daa0-107">**IDot11AdHocInterface**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | <span data-ttu-id="8daa0-108">Representa una tarjeta de interfaz de red inalámbrica (NIC).</span><span class="sxs-lookup"><span data-stu-id="8daa0-108">Represents a wireless network interface card (NIC).</span></span>                                                    |
| [<span data-ttu-id="8daa0-109">**IDot11AdHocInterfaceNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="8daa0-109">**IDot11AdHocInterfaceNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | <span data-ttu-id="8daa0-110">Define las notificaciones admitidas por [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span><span class="sxs-lookup"><span data-stu-id="8daa0-110">Defines the notifications supported by [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span></span>           |
| [<span data-ttu-id="8daa0-111">**IDot11AdHocManager**</span><span class="sxs-lookup"><span data-stu-id="8daa0-111">**IDot11AdHocManager**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | <span data-ttu-id="8daa0-112">Crea y administra las redes ad hoc 802,11.</span><span class="sxs-lookup"><span data-stu-id="8daa0-112">Creates and manages 802.11 ad hoc networks.</span></span>                                                            |
| [<span data-ttu-id="8daa0-113">**IDot11AdHocManagerNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="8daa0-113">**IDot11AdHocManagerNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | <span data-ttu-id="8daa0-114">Define las notificaciones admitidas por la interfaz [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) .</span><span class="sxs-lookup"><span data-stu-id="8daa0-114">Defines the notifications supported by the [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) interface.</span></span> |
| [<span data-ttu-id="8daa0-115">**IDot11AdHocNetwork**</span><span class="sxs-lookup"><span data-stu-id="8daa0-115">**IDot11AdHocNetwork**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | <span data-ttu-id="8daa0-116">Representa un destino de red ad hoc disponible dentro del intervalo de conexión.</span><span class="sxs-lookup"><span data-stu-id="8daa0-116">Represents an available ad hoc network destination within connection range.</span></span>                            |
| [<span data-ttu-id="8daa0-117">**IDot11AdHocNetworkNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="8daa0-117">**IDot11AdHocNetworkNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | <span data-ttu-id="8daa0-118">Define las notificaciones admitidas por la interfaz [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) .</span><span class="sxs-lookup"><span data-stu-id="8daa0-118">Defines the notifications supported by the [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) interface.</span></span> |
| [<span data-ttu-id="8daa0-119">**IDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="8daa0-119">**IDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | <span data-ttu-id="8daa0-120">Especifica la configuración de seguridad para una red ad hoc inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="8daa0-120">Specifies the security settings for a wireless ad hoc network.</span></span>                                         |
| [<span data-ttu-id="8daa0-121">**IEnumDot11AdHocInterfaces**</span><span class="sxs-lookup"><span data-stu-id="8daa0-121">**IEnumDot11AdHocInterfaces**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | <span data-ttu-id="8daa0-122">Representa la colección de interfaces de red ad hoc 802,11 actualmente visibles.</span><span class="sxs-lookup"><span data-stu-id="8daa0-122">Represents the collection of currently visible 802.11 ad hoc network interfaces.</span></span>                       |
| [<span data-ttu-id="8daa0-123">**IEnumDot11AdHocNetworks**</span><span class="sxs-lookup"><span data-stu-id="8daa0-123">**IEnumDot11AdHocNetworks**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | <span data-ttu-id="8daa0-124">Representa la colección de redes ad hoc 802,11 actualmente visibles.</span><span class="sxs-lookup"><span data-stu-id="8daa0-124">Represents the collection of currently visible 802.11 ad hoc networks.</span></span>                                 |
| [<span data-ttu-id="8daa0-125">**IEnumDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="8daa0-125">**IEnumDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | <span data-ttu-id="8daa0-126">Representa la colección de opciones de configuración de seguridad asociada a cada red ad hoc inalámbrica visible.</span><span class="sxs-lookup"><span data-stu-id="8daa0-126">Represents the collection of security settings associated with each visible wireless ad hoc network.</span></span>   |



 

> [!Note]  
> <span data-ttu-id="8daa0-127">El modo ad hoc podría no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="8daa0-127">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="8daa0-128">A partir de Windows 8.1 y Windows Server 2012 R2, utilice en su lugar [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="8daa0-128">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

 

 



