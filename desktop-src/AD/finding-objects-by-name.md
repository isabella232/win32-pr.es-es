---
title: Buscar objetos por nombre
description: La mayoría de los objetos de Active Directory Domain Services usar la propiedad CN como su atributo de nomenclatura.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, buscar por nombre
- objeto AD, buscar por nombre
- Buscar objetos por nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773153"
---
# <a name="finding-objects-by-name"></a><span data-ttu-id="fc671-106">Buscar objetos por nombre</span><span class="sxs-lookup"><span data-stu-id="fc671-106">Finding Objects by Name</span></span>

<span data-ttu-id="fc671-107">La mayoría de los objetos de Active Directory Domain Services usar la propiedad **CN** como su atributo de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="fc671-107">Most objects in Active Directory Domain Services use the **cn** property as their naming attribute.</span></span> <span data-ttu-id="fc671-108">Sin embargo, algunos objetos usan un atributo de nomenclatura distinto de **CN**.</span><span class="sxs-lookup"><span data-stu-id="fc671-108">Some objects, however, use a naming attribute other than **cn**.</span></span> <span data-ttu-id="fc671-109">Por ejemplo, un controlador de dominio usa la propiedad **domainDNS** para el atributo de asignación de nombres y una unidad organizativa usa la propiedad **organizationalUnit** para el atributo de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="fc671-109">For example, a domain controller uses the **domainDNS** property for the naming attribute and an organizational unit uses the **organizationalUnit** property for the naming attribute.</span></span> <span data-ttu-id="fc671-110">Para evitar tener que usar un atributo de asignación de nombres diferente para los distintos tipos de objeto, la propiedad **Name** , que contiene el nombre distintivo relativo del objeto, debe usarse para buscar objetos por su nombre.</span><span class="sxs-lookup"><span data-stu-id="fc671-110">To avoid having to use a different naming attribute for different object types, the **name** property, which contains the relative distinguished name of the object, should be used to search for objects by name.</span></span>

## <a name="examples"></a><span data-ttu-id="fc671-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fc671-111">Examples</span></span>

<span data-ttu-id="fc671-112">En los siguientes ejemplos de código se muestran cadenas de consulta diferentes que se pueden usar para buscar objetos por nombre.</span><span class="sxs-lookup"><span data-stu-id="fc671-112">The following code examples show different query strings that can be used to find objects by name.</span></span>

<span data-ttu-id="fc671-113">La siguiente cadena de consulta busca todos los objetos cuyo nombre comienza por "Jeff".</span><span class="sxs-lookup"><span data-stu-id="fc671-113">The following query string finds all objects with a name that begins with "Jeff".</span></span>


```C++
(name=Jeff*)
```



<span data-ttu-id="fc671-114">La siguiente cadena de consulta busca todos los objetos de equipo cuyo nombre comienza por "concedido" o "Corp".</span><span class="sxs-lookup"><span data-stu-id="fc671-114">The following query string finds all computer objects with a name that begins with "leased" or "corp".</span></span>


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



<span data-ttu-id="fc671-115">La siguiente cadena de consulta busca todos los usuarios y un nombre que comienza por "Karen" o "Jeff".</span><span class="sxs-lookup"><span data-stu-id="fc671-115">The following query string finds all users and with a name that begins with "Karen" or "Jeff".</span></span>


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




