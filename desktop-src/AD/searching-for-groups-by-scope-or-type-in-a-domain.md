---
title: Buscar grupos por ámbito o tipo en un dominio
description: En los dominios de Windows 2000, hay una sola clase denominada Group para todos los ámbitos de grupo (local de dominio, global, universal) y tipos (seguridad, distribución).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Buscar grupos por ámbito o tipo en un dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789471"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a><span data-ttu-id="8d84e-104">Buscar grupos por ámbito o tipo en un dominio</span><span class="sxs-lookup"><span data-stu-id="8d84e-104">Searching for Groups by Scope or Type in a Domain</span></span>

<span data-ttu-id="8d84e-105">En los dominios de Windows 2000, hay una sola clase denominada [**Group**](/windows/desktop/ADSchema/c-group) para todos los ámbitos de grupo (local de dominio, global, universal) y tipos (seguridad, distribución).</span><span class="sxs-lookup"><span data-stu-id="8d84e-105">In Windows 2000 domains, there is single class called [**group**](/windows/desktop/ADSchema/c-group) for all group scopes (Domain Local, Global, Universal) and types (security, distribution).</span></span> <span data-ttu-id="8d84e-106">El atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) del objeto Group especifica el tipo y el ámbito de grupo.</span><span class="sxs-lookup"><span data-stu-id="8d84e-106">The [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute of the group object specifies the group type and scope.</span></span>

<span data-ttu-id="8d84e-107">Para usar el tipo o ámbito para buscar grupos en los dominios de Windows 2000, use un filtro que contenga una regla de coincidencia para el atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="8d84e-107">To use type or scope to search for groups on Windows 2000 domains, use a filter that contains a matching rule for the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="8d84e-108">Para obtener más información sobre las reglas de coincidencia, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="8d84e-108">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="8d84e-109">Para obtener más información y un ejemplo de código que muestra cómo buscar grupos en un dominio, consulte el [código de ejemplo para buscar grupos en un dominio](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="8d84e-109">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

## <a name="example-ldap-query-strings"></a><span data-ttu-id="8d84e-110">Cadenas de consulta LDAP de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d84e-110">Example LDAP Query Strings</span></span>

<span data-ttu-id="8d84e-111">Los siguientes ejemplos de cadena de consulta muestran cómo construir una cadena de consulta LDAP que se usa para buscar o filtrar tipos de grupos específicos.</span><span class="sxs-lookup"><span data-stu-id="8d84e-111">The following query string examples show how to construct an LDAP query string used to search for or filter specific group types.</span></span>

<span data-ttu-id="8d84e-112">La cadena de consulta siguiente buscará grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8d84e-112">The following query string will search for security groups.</span></span> <span data-ttu-id="8d84e-113">En este ejemplo se usa "-2147483648" como el equivalente decimal de la marca de **\_ \_ \_ seguridad \_ habilitada de tipo de grupo de ADS** .</span><span class="sxs-lookup"><span data-stu-id="8d84e-113">This example uses "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



<span data-ttu-id="8d84e-114">La cadena de consulta siguiente buscará grupos de distribución universales; es decir, los grupos que contienen el tipo de grupo de ADS marca de **\_ \_ \_ \_ grupo universal** y no contienen la marca **seguridad de tipo de grupo de ADS \_ \_ \_ \_ habilitada** .</span><span class="sxs-lookup"><span data-stu-id="8d84e-114">The following query string will search for universal distribution groups; that is, groups that contain the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** flag and do not contain the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span> <span data-ttu-id="8d84e-115">En este ejemplo se usa "8" como el equivalente decimal del grupo universal de tipos de grupos de ADS y "-2147483648" como el equivalente decimal de la marca de **\_ \_ \_ seguridad \_ habilitada de tipo de grupo de ADS** . **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8d84e-115">This example uses "8" as the decimal equivalent of **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** and "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 