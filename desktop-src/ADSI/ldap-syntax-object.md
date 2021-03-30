---
title: Objeto de sintaxis LDAP
description: El proveedor LDAP utiliza la siguiente asignación entre la sintaxis LDAP y la sintaxis ADSI.
ms.assetid: a82cf8ab-9591-4489-87a6-ccfab0e01d61
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, proveedores de servicios, sintaxis de asignación de sintaxis LDAP
- asignación de la sintaxis ADSI a ADSI de sintaxis LDAP
- sintaxis y asignación de ADSI a ADSI LDAP
- ADSI del proveedor de servicios LDAP, asignar sintaxis ADSI a sintaxis LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2272a0805ec32fd7ade9c4584feefb64fb1467f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148737"
---
# <a name="ldap-syntax-object"></a><span data-ttu-id="73a63-107">Objeto de sintaxis LDAP</span><span class="sxs-lookup"><span data-stu-id="73a63-107">LDAP Syntax Object</span></span>

<span data-ttu-id="73a63-108">El proveedor LDAP utiliza la siguiente asignación entre la sintaxis LDAP y la sintaxis ADSI.</span><span class="sxs-lookup"><span data-stu-id="73a63-108">The LDAP provider uses the following mapping between the LDAP syntax and ADSI syntax.</span></span>



| <span data-ttu-id="73a63-109">Sintaxis LDAP</span><span class="sxs-lookup"><span data-stu-id="73a63-109">LDAP Syntax</span></span>   | <span data-ttu-id="73a63-110">Sintaxis ADSI (Automation)</span><span class="sxs-lookup"><span data-stu-id="73a63-110">ADSI Syntax (Automation)</span></span>            |
|---------------|-------------------------------------|
| <span data-ttu-id="73a63-111">ADsPath</span><span class="sxs-lookup"><span data-stu-id="73a63-111">ADsPath</span></span>       | <span data-ttu-id="73a63-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-112">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="73a63-113">Boolean</span></span>       | <span data-ttu-id="73a63-114">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="73a63-114">VT\_BOOL</span></span>                            |
| <span data-ttu-id="73a63-115">Contador</span><span class="sxs-lookup"><span data-stu-id="73a63-115">Counter</span></span>       | <span data-ttu-id="73a63-116">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="73a63-116">VT\_I4</span></span>                              |
| <span data-ttu-id="73a63-117">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="73a63-117">EmailAddress</span></span>  | <span data-ttu-id="73a63-118">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-118">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-119">FaxNumber</span><span class="sxs-lookup"><span data-stu-id="73a63-119">FaxNumber</span></span>     | <span data-ttu-id="73a63-120">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-120">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-121">Entero</span><span class="sxs-lookup"><span data-stu-id="73a63-121">Integer</span></span>       | <span data-ttu-id="73a63-122">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="73a63-122">VT\_I4</span></span>                              |
| <span data-ttu-id="73a63-123">Intervalo</span><span class="sxs-lookup"><span data-stu-id="73a63-123">Interval</span></span>      | <span data-ttu-id="73a63-124">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="73a63-124">VT\_I4</span></span>                              |
| <span data-ttu-id="73a63-125">List</span><span class="sxs-lookup"><span data-stu-id="73a63-125">List</span></span>          | <span data-ttu-id="73a63-126">VT \_ (variante) (matriz de VT \_ BSTR \| \_ )</span><span class="sxs-lookup"><span data-stu-id="73a63-126">VT\_VARIANT (VT\_BSTR \| VT\_ARRAY)</span></span> |
| <span data-ttu-id="73a63-127">NetAddress</span><span class="sxs-lookup"><span data-stu-id="73a63-127">NetAddress</span></span>    | <span data-ttu-id="73a63-128">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-128">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-129">OctetString</span><span class="sxs-lookup"><span data-stu-id="73a63-129">OctetString</span></span>   | <span data-ttu-id="73a63-130">VT ( \_ variante)</span><span class="sxs-lookup"><span data-stu-id="73a63-130">VT\_VARIANT</span></span>                         |
| <span data-ttu-id="73a63-131">Ruta</span><span class="sxs-lookup"><span data-stu-id="73a63-131">Path</span></span>          | <span data-ttu-id="73a63-132">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-132">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-133">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="73a63-133">PhoneNumber</span></span>   | <span data-ttu-id="73a63-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-134">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-135">PostalAddress</span><span class="sxs-lookup"><span data-stu-id="73a63-135">PostalAddress</span></span> | <span data-ttu-id="73a63-136">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-136">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-137">SmallInterval</span><span class="sxs-lookup"><span data-stu-id="73a63-137">SmallInterval</span></span> | <span data-ttu-id="73a63-138">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="73a63-138">VT\_I4</span></span>                              |
| <span data-ttu-id="73a63-139">String</span><span class="sxs-lookup"><span data-stu-id="73a63-139">String</span></span>        | <span data-ttu-id="73a63-140">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="73a63-140">VT\_BSTR</span></span>                            |
| <span data-ttu-id="73a63-141">Hora</span><span class="sxs-lookup"><span data-stu-id="73a63-141">Time</span></span>          | <span data-ttu-id="73a63-142">fecha de VT \_</span><span class="sxs-lookup"><span data-stu-id="73a63-142">VT\_DATE</span></span>                            |



 

 

 




