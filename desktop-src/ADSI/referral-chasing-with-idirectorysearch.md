---
title: Referencia sobre el seguimiento con IDirectorySearch
description: Una referencia es el mecanismo que utiliza un servidor de directorio para dirigir un cliente a otro servidor cuando no contiene suficientes datos sobre el objeto solicitado por una consulta.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Referencia sobre el seguimiento con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, seguimiento de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995627"
---
# <a name="referral-chasing-with-idirectorysearch"></a><span data-ttu-id="b097e-105">Referencia sobre el seguimiento con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b097e-105">Referral Chasing with IDirectorySearch</span></span>

<span data-ttu-id="b097e-106">Una referencia es el mecanismo que utiliza un servidor de directorio para dirigir un cliente a otro servidor cuando no contiene suficientes datos sobre el objeto solicitado por una consulta.</span><span class="sxs-lookup"><span data-stu-id="b097e-106">A referral is the mechanism that a directory server uses to direct a client to another server when it does not contain sufficient data about the object requested by a query.</span></span>

<span data-ttu-id="b097e-107">En una búsqueda de un solo nivel o de subárbol, las referencias se devuelven para los contenedores de dominio, esquema o configuración de solo subordinados inmediatos. es decir, dominios secundarios que son descendientes directos.</span><span class="sxs-lookup"><span data-stu-id="b097e-107">In a one-level or subtree search, referrals are returned for known, immediately subordinate domain, schema, or configuration containers only; that is, child domains that are direct descendants.</span></span> <span data-ttu-id="b097e-108">Para obtener más información, vea [ámbito de búsqueda](/windows/desktop/AD/search-scope).</span><span class="sxs-lookup"><span data-stu-id="b097e-108">For more information, see [Search Scope](/windows/desktop/AD/search-scope).</span></span>

<span data-ttu-id="b097e-109">En un directorio, no todos los datos están disponibles en un solo servidor, sino que se distribuyen a través de varios servidores diferentes a través de la red.</span><span class="sxs-lookup"><span data-stu-id="b097e-109">In a directory, not all data is available on a single server, rather, it is distributed over several different servers across the network.</span></span> <span data-ttu-id="b097e-110">Si los servidores comparten los datos que otros servidores pueden proporcionar, pueden proporcionar referencias a un cliente cuando una consulta solicitada no se puede resolver en el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="b097e-110">If the servers share the data that other servers can provide, they can provide referrals to a client when a requested query cannot be resolved on the originating server.</span></span> <span data-ttu-id="b097e-111">Por ejemplo, cuando un cliente pide al servidor a que consulte un objeto de usuario (U), puede sugerir que el cliente continúe la búsqueda en el servidor B si U no reside en, pero se identifica como en B. El cliente tiene la opción de llevar a cabo la referencia o no.</span><span class="sxs-lookup"><span data-stu-id="b097e-111">For example, when a client asks Server A to query a user object (U), then A can suggest that the client continue the search on Server B if U does not reside on A, but is identified to be on B. The client has the choice to pursue the referral or not.</span></span> <span data-ttu-id="b097e-112">Las referencias liberan al cliente de tener que poseer el conocimiento anterior de la capacidad de cada servidor, pero el cliente debe especificar el tipo de referencias que debe realizar un servidor.</span><span class="sxs-lookup"><span data-stu-id="b097e-112">Referrals free the client from having to possess previous knowledge of the capability of each server, but the client must specify the type of referrals a server should perform.</span></span>

<span data-ttu-id="b097e-113">Para habilitar o deshabilitar el seguimiento de la referencia, establezca una opción de búsqueda de referencias **\_ SEARCHPREF de \_ \_ seguimiento de ADS** con un valor **\_ entero de ADSTYPE** que contenga uno de los valores de enumeración de las referencias de [**\_ seguimiento \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) de anuncios en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="b097e-113">To enable or disable referral chasing, set an **ADS\_SEARCHPREF\_CHASE\_REFERRALS** search option with an **ADSTYPE\_INTEGER** value that contains one of the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) enumeration values in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="b097e-114">En el ejemplo de código siguiente se muestra cómo habilitar las referencias de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b097e-114">The following code example shows how to enable chase referrals.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



<span data-ttu-id="b097e-115">Para obtener más información sobre las referencias en Active Directory, vea [Referrals](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="b097e-115">For more information about referrals in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

 

 