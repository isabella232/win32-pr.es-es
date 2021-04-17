---
title: Sintaxis de Object (DS-DN)
description: Cadena que contiene un nombre distintivo (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de objeto (DS-DN)
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535662"
---
# <a name="objectds-dn-syntax"></a><span data-ttu-id="a510a-104">Sintaxis de Object (DS-DN)</span><span class="sxs-lookup"><span data-stu-id="a510a-104">Object(DS-DN) syntax</span></span>

<span data-ttu-id="a510a-105">Cadena que contiene un nombre distintivo (DN).</span><span class="sxs-lookup"><span data-stu-id="a510a-105">String that contains a distinguished name (DN).</span></span> <span data-ttu-id="a510a-106">En el caso de los atributos con esta sintaxis, Active Directory controla los valores de atributo como referencias al objeto identificado por el DN y actualiza automáticamente el valor si el objeto se mueve o se cambia de nombre.</span><span class="sxs-lookup"><span data-stu-id="a510a-106">For attributes with this syntax, Active Directory handles attribute values as references to the object identified by the DN and automatically updates the value if the object is moved or renamed.</span></span> <span data-ttu-id="a510a-107">En el caso de las consultas que incluyen atributos de sintaxis DN en un filtro, especifique nombres distintivos completos.</span><span class="sxs-lookup"><span data-stu-id="a510a-107">For queries that include attributes of DN syntax in a filter, specify full distinguished names.</span></span> <span data-ttu-id="a510a-108">No se admiten los caracteres comodín (por ejemplo, CN = John \* ).</span><span class="sxs-lookup"><span data-stu-id="a510a-108">Wildcards (for example, cn=John\*) are not supported.</span></span>



| <span data-ttu-id="a510a-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a510a-109">Entry</span></span> | <span data-ttu-id="a510a-110">Value</span><span class="sxs-lookup"><span data-stu-id="a510a-110">Value</span></span> |
|--------------|------------------------------------------------------------------------|
| <span data-ttu-id="a510a-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="a510a-111">Name</span></span>         | <span data-ttu-id="a510a-112">Object(DS-DN) </span><span class="sxs-lookup"><span data-stu-id="a510a-112">Object(DS-DN)</span></span>                                                          |
| <span data-ttu-id="a510a-113">IDENTIFICADOR de sintaxis</span><span class="sxs-lookup"><span data-stu-id="a510a-113">Syntax ID</span></span>    | <span data-ttu-id="a510a-114">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="a510a-114">2.5.5.1</span></span>                                                                |
| <span data-ttu-id="a510a-115">IDENTIFICADOR DE OM</span><span class="sxs-lookup"><span data-stu-id="a510a-115">OM ID</span></span>        | <span data-ttu-id="a510a-116">127</span><span class="sxs-lookup"><span data-stu-id="a510a-116">127</span></span>                                                                    |
| <span data-ttu-id="a510a-117">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="a510a-117">MAPI Type</span></span>    | <span data-ttu-id="a510a-118">OBJECT</span><span class="sxs-lookup"><span data-stu-id="a510a-118">OBJECT</span></span>                                                                 |
| <span data-ttu-id="a510a-119">Tipo ADS</span><span class="sxs-lookup"><span data-stu-id="a510a-119">ADS Type</span></span>     | <span data-ttu-id="a510a-120">ADSTYPE \_ \_ cadena DN</span><span class="sxs-lookup"><span data-stu-id="a510a-120">ADSTYPE\_DN\_STRING</span></span>                                                    |
| <span data-ttu-id="a510a-121">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="a510a-121">Variant Type</span></span> | <span data-ttu-id="a510a-122">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a510a-122">VT\_BSTR</span></span>                                                               |
| <span data-ttu-id="a510a-123">Tipo de SDS</span><span class="sxs-lookup"><span data-stu-id="a510a-123">SDS Type</span></span>     | [<span data-ttu-id="a510a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="a510a-124">System.String</span></span>](/dotnet/api/system.string) |



## <a name="see-also"></a><span data-ttu-id="a510a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a510a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a510a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a510a-126">System.String</span></span>](/dotnet/api/system.string)
</dt> </dl>

 

 
