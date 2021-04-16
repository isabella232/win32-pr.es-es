---
title: Sintaxis de Object (DN-String)
description: Cadena de octetos que contiene un valor de cadena y un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Sintaxis de objeto (DN-cadena) esquema de AD
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658463"
---
# <a name="objectdn-string-syntax"></a><span data-ttu-id="1e531-104">Sintaxis de Object (DN-String)</span><span class="sxs-lookup"><span data-stu-id="1e531-104">Object(DN-String) syntax</span></span>

<span data-ttu-id="1e531-105">Cadena de octetos que contiene un valor de cadena y un DN.</span><span class="sxs-lookup"><span data-stu-id="1e531-105">An octet string that contains a string value and a DN.</span></span>



| <span data-ttu-id="1e531-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e531-106">Entry</span></span> | <span data-ttu-id="1e531-107">Value</span><span class="sxs-lookup"><span data-stu-id="1e531-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e531-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e531-108">Name</span></span>         | <span data-ttu-id="1e531-109">Object(DN-String)</span><span class="sxs-lookup"><span data-stu-id="1e531-109">Object(DN-String)</span></span>                                                                  |
| <span data-ttu-id="1e531-110">IDENTIFICADOR de sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e531-110">Syntax ID</span></span>    | <span data-ttu-id="1e531-111">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="1e531-111">2.5.5.14</span></span>                                                                           |
| <span data-ttu-id="1e531-112">IDENTIFICADOR DE OM</span><span class="sxs-lookup"><span data-stu-id="1e531-112">OM ID</span></span>        | <span data-ttu-id="1e531-113">127</span><span class="sxs-lookup"><span data-stu-id="1e531-113">127</span></span>                                                                                |
| <span data-ttu-id="1e531-114">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="1e531-114">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="1e531-115">Tipo ADS</span><span class="sxs-lookup"><span data-stu-id="1e531-115">ADS Type</span></span>     | <span data-ttu-id="1e531-116">\_DN ADSTYPE \_ con \_ cadena</span><span class="sxs-lookup"><span data-stu-id="1e531-116">ADSTYPE\_DN\_WITH\_STRING</span></span>                                                          |
| <span data-ttu-id="1e531-117">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="1e531-117">Variant Type</span></span> | <span data-ttu-id="1e531-118">distribución de VT \_</span><span class="sxs-lookup"><span data-stu-id="1e531-118">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="1e531-119">Tipo de SDS</span><span class="sxs-lookup"><span data-stu-id="1e531-119">SDS Type</span></span>     | <span data-ttu-id="1e531-120">Objeto COM que se puede convertir en un [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span><span class="sxs-lookup"><span data-stu-id="1e531-120">A COM object that can be cast to an [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span></span> |



## <a name="remarks"></a><span data-ttu-id="1e531-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e531-121">Remarks</span></span>

<span data-ttu-id="1e531-122">Un valor con esta sintaxis tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="1e531-122">A value with this syntax has the following format:</span></span>

``` syntax
S:<char count>:<string value>:<object DN>
```

<span data-ttu-id="1e531-123">donde " &lt; Char Count &gt; " es el número de caracteres de la &lt; cadena "valor de cadena &gt; " y " &lt; DN del objeto &gt; " es un nombre distintivo de un objeto en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1e531-123">where "&lt;char count&gt;" is the number of characters in the "&lt;string value&gt;" string, and "&lt;object DN&gt;" is a distinguished name of an object in Active Directory.</span></span> <span data-ttu-id="1e531-124">Active Directory actualiza el DN si el objeto al que hace referencia se mueve o se cambia de nombre.</span><span class="sxs-lookup"><span data-stu-id="1e531-124">Active Directory updates the DN if the object that it refers to is moved or renamed.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e531-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e531-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e531-126">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="1e531-126">**IADsDNWithString**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
