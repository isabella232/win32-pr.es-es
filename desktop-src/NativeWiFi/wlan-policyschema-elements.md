---
description: Un perfil de directiva de LAN inalámbrica WIFI (WLAN) nativo se compone de los siguientes elementos de esquema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy elementos de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541043"
---
# <a name="wlan_policy-schema-elements"></a><span data-ttu-id="a73e9-103">Elementos de esquema de directiva de WLAN \_</span><span class="sxs-lookup"><span data-stu-id="a73e9-103">WLAN\_policy Schema Elements</span></span>

<span data-ttu-id="a73e9-104">Un perfil de directiva de LAN inalámbrica WIFI (WLAN) nativo se compone de los siguientes elementos de esquema.</span><span class="sxs-lookup"><span data-stu-id="a73e9-104">A Native Wifi wireless LAN (WLAN) policy profile is composed of the following schema elements.</span></span> <span data-ttu-id="a73e9-105">Todos los elementos con nombre se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="a73e9-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

<span data-ttu-id="a73e9-106">En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil.</span><span class="sxs-lookup"><span data-stu-id="a73e9-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="a73e9-107">Se aplica el orden de los elementos.</span><span class="sxs-lookup"><span data-stu-id="a73e9-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="a73e9-108">No todos los elementos están en cada perfil, ya que algunos elementos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="a73e9-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="a73e9-109">En esta lista no se muestran todos los elementos posibles que pueden aparecer en un perfil, ya que los elementos se pueden agregar en **xs: cualquier** punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="a73e9-109">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="a73e9-110">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="a73e9-110">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
    -   [<span data-ttu-id="a73e9-111">**nombre (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-111">**name (WLANPolicy)**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)
    -   [<span data-ttu-id="a73e9-112">**Descripción (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-112">**description (WLANPolicy)**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)
    -   [<span data-ttu-id="a73e9-113">**Indicadores_globales (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-113">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [<span data-ttu-id="a73e9-114">**enableAutoConfig (Indicadores_globales)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-114">**enableAutoConfig (globalFlags)**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [<span data-ttu-id="a73e9-115">**showDeniedNetwork (Indicadores_globales)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-115">**showDeniedNetwork (globalFlags)**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [<span data-ttu-id="a73e9-116">**allowEveryoneToCreateAllUserProfiles (Indicadores_globales)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [<span data-ttu-id="a73e9-117">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-117">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [<span data-ttu-id="a73e9-118">**Permitidos (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [<span data-ttu-id="a73e9-119">**red (permitidos)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-119">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
                -   [<span data-ttu-id="a73e9-120">**networkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-120">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="a73e9-121">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-121">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="a73e9-122">**listas de bloqueo (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-122">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [<span data-ttu-id="a73e9-123">**red (bloqueo de listas)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-123">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
                -   [<span data-ttu-id="a73e9-124">**networkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-124">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="a73e9-125">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-125">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="a73e9-126">**denyAllIBSS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-126">**denyAllIBSS (networkFilter)**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [<span data-ttu-id="a73e9-127">**denyAllESS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-127">**denyAllESS (networkFilter)**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [<span data-ttu-id="a73e9-128">**profileList (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="a73e9-128">**profileList (WLANPolicy)**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



