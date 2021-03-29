---
description: Un perfil de 802.1 X contiene los siguientes elementos de esquema.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Elementos del esquema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813635"
---
# <a name="onex-schema-elements"></a><span data-ttu-id="46aa3-103">Elementos del esquema OneX</span><span class="sxs-lookup"><span data-stu-id="46aa3-103">OneX Schema Elements</span></span>

<span data-ttu-id="46aa3-104">Un perfil de 802.1 X contiene los siguientes elementos de esquema.</span><span class="sxs-lookup"><span data-stu-id="46aa3-104">An 802.1X profile contains the following schema elements.</span></span> <span data-ttu-id="46aa3-105">Todos los elementos de esquema OneX se aplican tanto a los perfiles con cable como a los inalámbricos.</span><span class="sxs-lookup"><span data-stu-id="46aa3-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="46aa3-106">La mayoría de los elementos con nombre se encuentran en el espacio de nombres `https://www.microsoft.com/networking/OneX/v1` , excepto en el caso de [**EAPConfig (Onex)**](onexschema-eapconfig-onex-element.md) que se encuentra en el espacio de nombres `https://www.microsoft.com/provisioning/EapHostConfig` .</span><span class="sxs-lookup"><span data-stu-id="46aa3-106">Most of the named elements are in the namespace `https://www.microsoft.com/networking/OneX/v1`, except for [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) which is in the namespace `https://www.microsoft.com/provisioning/EapHostConfig`.</span></span>

<span data-ttu-id="46aa3-107">En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil.</span><span class="sxs-lookup"><span data-stu-id="46aa3-107">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="46aa3-108">Se aplica el orden de los elementos.</span><span class="sxs-lookup"><span data-stu-id="46aa3-108">The ordering of elements is enforced.</span></span> <span data-ttu-id="46aa3-109">No todos los elementos están en cada perfil, ya que algunos elementos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="46aa3-109">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="46aa3-110">En esta lista no se muestran todos los elementos posibles que pueden aparecer en un perfil, ya que los elementos se pueden agregar en **xs: cualquier** punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="46aa3-110">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="46aa3-111">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="46aa3-111">**OneX**</span></span>](onexschema-onex-element.md)
    -   [<span data-ttu-id="46aa3-112">**cacheUserData (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-112">**cacheUserData (OneX)**</span></span>](onexschema-cacheuserdata-onex-element.md)
    -   [<span data-ttu-id="46aa3-113">**heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-113">**heldPeriod (OneX)**</span></span>](onexschema-heldperiod-onex-element.md)
    -   [<span data-ttu-id="46aa3-114">**authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-114">**authPeriod (OneX)**</span></span>](onexschema-authperiod-onex-element.md)
    -   [<span data-ttu-id="46aa3-115">**startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-115">**startPeriod (OneX)**</span></span>](onexschema-startperiod-onex-element.md)
    -   [<span data-ttu-id="46aa3-116">**maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-116">**maxStart (OneX)**</span></span>](onexschema-maxstart-onex-element.md)
    -   [<span data-ttu-id="46aa3-117">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-117">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
    -   [<span data-ttu-id="46aa3-118">**supplicantMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-118">**supplicantMode (OneX)**</span></span>](onexschema-supplicantmode-onex-element.md)
    -   [<span data-ttu-id="46aa3-119">**authMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-119">**authMode (OneX)**</span></span>](onexschema-authmode-onex-element.md)
    -   [<span data-ttu-id="46aa3-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
        -   [<span data-ttu-id="46aa3-121">**tipo (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-121">**type (singleSignOn)**</span></span>](onexschema-type-singlesignon-element.md)
        -   [<span data-ttu-id="46aa3-122">**maxDelay (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-122">**maxDelay (singleSignOn)**</span></span>](onexschema-maxdelay-singlesignon-element.md)
        -   [<span data-ttu-id="46aa3-123">**userBasedVirtualLan (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-123">**userBasedVirtualLan (singleSignOn)**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [<span data-ttu-id="46aa3-124">**EAPConfig (OneX)**</span><span class="sxs-lookup"><span data-stu-id="46aa3-124">**EAPConfig (OneX)**</span></span>](onexschema-eapconfig-onex-element.md)

 

 



