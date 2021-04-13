---
description: La interfaz IUpdateSearcher define las siguientes propiedades.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propiedades de IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/11/2021
ms.locfileid: "104362402"
---
# <a name="iupdatesearcher-properties"></a><span data-ttu-id="299d1-103">Propiedades de IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="299d1-103">IUpdateSearcher Properties</span></span>

<span data-ttu-id="299d1-104">La interfaz [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="299d1-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following properties.</span></span>



| <span data-ttu-id="299d1-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="299d1-105">Property</span></span>                                                                                           | <span data-ttu-id="299d1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="299d1-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="299d1-107">**CanAutomaticallyUpgradeService**</span><span class="sxs-lookup"><span data-stu-id="299d1-107">**CanAutomaticallyUpgradeService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | <span data-ttu-id="299d1-108">Obtiene y establece un valor booleano que indica si las futuras llamadas a los métodos [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) y [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) dan como resultado una actualización automática a Windows Update Agent (WUA).</span><span class="sxs-lookup"><span data-stu-id="299d1-108">Gets and sets a Boolean value that indicates whether future calls to the [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) and [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) methods result in an automatic upgrade to Windows Update Agent (WUA).</span></span> |
| [<span data-ttu-id="299d1-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="299d1-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | <span data-ttu-id="299d1-110">Identifica la aplicación cliente actual.</span><span class="sxs-lookup"><span data-stu-id="299d1-110">Identifies the current client application.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="299d1-111">**IncludePotentiallySupersededUpdates**</span><span class="sxs-lookup"><span data-stu-id="299d1-111">**IncludePotentiallySupersededUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | <span data-ttu-id="299d1-112">Obtiene y establece un valor booleano que indica si los resultados de la búsqueda incluyen actualizaciones reemplazadas por otras actualizaciones en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="299d1-112">Gets and sets a Boolean value that indicates whether the search results include updates that are superseded by other updates in the search results.</span></span>                                                                                          |
| [<span data-ttu-id="299d1-113">**En línea**</span><span class="sxs-lookup"><span data-stu-id="299d1-113">**Online**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | <span data-ttu-id="299d1-114">Obtiene y establece un valor booleano que indica si [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) se conecta para buscar actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="299d1-114">Gets and sets a Boolean value that indicates whether the [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) goes online to search for updates.</span></span>                                                                                                        |
| [<span data-ttu-id="299d1-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="299d1-115">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | <span data-ttu-id="299d1-116">Obtiene y establece un sitio en el que buscar cuando el sitio que se va a buscar no es un sitio Windows Update.</span><span class="sxs-lookup"><span data-stu-id="299d1-116">Gets and sets a site to search when the site to search is not a Windows Update site.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="299d1-117">**ServerSelection**</span><span class="sxs-lookup"><span data-stu-id="299d1-117">**ServerSelection**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | <span data-ttu-id="299d1-118">Obtiene y establece un valor de [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica el servidor en el que se van a buscar actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="299d1-118">Gets and sets a [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) value that indicates the server to search for updates.</span></span>                                                                                                                            |




 

 

 



