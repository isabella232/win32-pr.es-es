---
title: Consultar los grupos de un dominio
description: Los grupos se pueden colocar en cualquier contenedor o unidad organizativa de un dominio, así como en la raíz del dominio.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Consulta de grupos en un dominio de Active Directory
- Agrupa AD, consultar los grupos de un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904476"
---
# <a name="querying-for-groups-in-a-domain"></a><span data-ttu-id="9f060-105">Consultar los grupos de un dominio</span><span class="sxs-lookup"><span data-stu-id="9f060-105">Querying for Groups in a Domain</span></span>

<span data-ttu-id="9f060-106">Los grupos se pueden colocar en cualquier contenedor o unidad organizativa de un dominio, así como en la raíz del dominio.</span><span class="sxs-lookup"><span data-stu-id="9f060-106">Groups can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="9f060-107">Es posible que los grupos no siempre estén en un contenedor.</span><span class="sxs-lookup"><span data-stu-id="9f060-107">Groups may not always be in one container.</span></span> <span data-ttu-id="9f060-108">Por lo tanto, es necesario buscar en todo el dominio para buscar todos los grupos del dominio.</span><span class="sxs-lookup"><span data-stu-id="9f060-108">Therefore, it is necessary to search the entire domain to find all groups in the domain.</span></span>

<span data-ttu-id="9f060-109">Para buscar todos los grupos de un dominio, establezca el punto de inicio de la búsqueda en la raíz del dominio, establezca el ámbito de búsqueda en subárbol y busque todos los objetos que tengan un valor de [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de "grupo".</span><span class="sxs-lookup"><span data-stu-id="9f060-109">To search for all groups in a domain, set the search start point to the root of the domain, set the search scope to subtree and search for all objects that have an [**objectClass**](/windows/desktop/ADSchema/a-objectclass) value of "group".</span></span>

<span data-ttu-id="9f060-110">Si se deben encontrar grupos que contienen valores de [**\_ \_ \_ enumeración de tipo de grupo de anuncios**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) concretos, se pueden usar el bit de regla de coincidencia de **LDAP \_ \_ \_ \_ y** el operador de regla de coincidencia para buscar grupos que tengan determinados bits establecidos en el atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="9f060-110">If groups that contain particular [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) values must be found, the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator can be used to search for groups that have particular bits set in the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="9f060-111">Para obtener más información sobre el uso de reglas de coincidencia, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="9f060-111">For more information about using matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="9f060-112">Para obtener más información y un ejemplo de código que muestra cómo buscar grupos en un dominio, consulte el [código de ejemplo para buscar grupos en un dominio](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="9f060-112">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

 

 