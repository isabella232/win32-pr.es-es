---
title: Novedades de la administración de redes
description: Novedades de la administración de redes
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421598"
---
# <a name="whats-new-in-network-management"></a><span data-ttu-id="19097-103">Novedades de la administración de redes</span><span class="sxs-lookup"><span data-stu-id="19097-103">What's New in Network Management</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="19097-104">Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19097-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="19097-105">Microsoft Windows 8 incorpora nuevas características de programación de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="19097-105">Microsoft Windows 8 introduces new Network Management programming features.</span></span> <span data-ttu-id="19097-106">Estos nuevos elementos amplían la funcionalidad de la administración de redes para crear paquetes de aprovisionamiento para operaciones de unión a un dominio sin conexión al aprovisionar equipos con Windows 8.</span><span class="sxs-lookup"><span data-stu-id="19097-106">These new elements extend the capability of Network Management to create provisioning packages for offline domain join operations when provisioning computers with Windows 8.</span></span>

<span data-ttu-id="19097-107">A continuación se indican las nuevas funciones de administración de red:</span><span class="sxs-lookup"><span data-stu-id="19097-107">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="19097-108">**NetCreateProvisioningPackage**</span><span class="sxs-lookup"><span data-stu-id="19097-108">**NetCreateProvisioningPackage**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="19097-109">**NetRequestProvisioningPackageInstall**</span><span class="sxs-lookup"><span data-stu-id="19097-109">**NetRequestProvisioningPackageInstall**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

<span data-ttu-id="19097-110">A continuación se indican las nuevas estructuras de administración de red:</span><span class="sxs-lookup"><span data-stu-id="19097-110">The following are new Network Management structures:</span></span>

-   [<span data-ttu-id="19097-111">**PARÁMETROS de aprovisionamiento de NETSETUP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="19097-111">**NETSETUP\_PROVISIONING\_PARAMS**</span></span>](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [<span data-ttu-id="19097-112">**Información de usuario \_ \_ 24**</span><span class="sxs-lookup"><span data-stu-id="19097-112">**USER\_INFO\_24**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

<span data-ttu-id="19097-113">La función [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) se ha mejorado en Windows 8 para admitir un nuevo nivel de información y devolver una estructura de información de [**usuario \_ \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) con información de la cuenta de usuario para una cuenta conectada a una identidad de Internet.</span><span class="sxs-lookup"><span data-stu-id="19097-113">The [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function has been enhanced on Windows 8 to support a new information level and return a [**USER\_INFO\_24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) structure with user account information for an account connected to an Internet identity.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="19097-114">Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19097-114">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="19097-115">Microsoft Windows 7 incorpora nuevas características de programación de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="19097-115">Microsoft Windows 7 introduces new Network Management programming features.</span></span> <span data-ttu-id="19097-116">Estos elementos amplían la funcionalidad de la administración de redes para permitir operaciones de unión al dominio sin conexión al aprovisionar equipos con Windows 7.</span><span class="sxs-lookup"><span data-stu-id="19097-116">These elements extend the capability of Network Management to allow offline domain join operations when provisioning computers with Windows 7.</span></span>

<span data-ttu-id="19097-117">A continuación se indican las nuevas funciones de administración de red:</span><span class="sxs-lookup"><span data-stu-id="19097-117">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="19097-118">**NetProvisionComputerAccount**</span><span class="sxs-lookup"><span data-stu-id="19097-118">**NetProvisionComputerAccount**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="19097-119">**NetRequestOfflineDomainJoin**</span><span class="sxs-lookup"><span data-stu-id="19097-119">**NetRequestOfflineDomainJoin**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

<span data-ttu-id="19097-120">Las siguientes funciones de administración de red existentes se han mejorado para admitir opciones adicionales:</span><span class="sxs-lookup"><span data-stu-id="19097-120">The following existing Network Management functions were enhanced to support additional options:</span></span>

-   [<span data-ttu-id="19097-121">**NetJoinDomain**</span><span class="sxs-lookup"><span data-stu-id="19097-121">**NetJoinDomain**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a><span data-ttu-id="19097-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19097-122">Windows Server 2003</span></span>

<span data-ttu-id="19097-123">Microsoft Windows Server 2003 presenta nuevas características de programación de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="19097-123">Microsoft Windows Server 2003 introduces new Network Management programming features.</span></span> <span data-ttu-id="19097-124">Estos elementos amplían la funcionalidad de las operaciones de administración de redes en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="19097-124">These elements extend the capability of Network Management operations on Windows Server 2003 and later.</span></span>

## <a name="windows-xp"></a><span data-ttu-id="19097-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="19097-125">Windows XP</span></span>

<span data-ttu-id="19097-126">Microsoft Windows XP presenta nuevas características de programación de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="19097-126">Microsoft Windows XP introduces new Network Management programming features.</span></span> <span data-ttu-id="19097-127">Estos elementos amplían la capacidad de las operaciones de administración de redes en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="19097-127">These elements extend the capability of Network Management operations on Windows XP and later.</span></span>

<span data-ttu-id="19097-128">A continuación se indican las nuevas funciones de administración de red:</span><span class="sxs-lookup"><span data-stu-id="19097-128">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="19097-129">**NetAddAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="19097-129">**NetAddAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [<span data-ttu-id="19097-130">**NetEnumerateComputerNames**</span><span class="sxs-lookup"><span data-stu-id="19097-130">**NetEnumerateComputerNames**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [<span data-ttu-id="19097-131">**NetRemoveAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="19097-131">**NetRemoveAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [<span data-ttu-id="19097-132">**NetSetPrimaryComputerName**</span><span class="sxs-lookup"><span data-stu-id="19097-132">**NetSetPrimaryComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [<span data-ttu-id="19097-133">**SetNetScheduleAccountInformation**</span><span class="sxs-lookup"><span data-stu-id="19097-133">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




