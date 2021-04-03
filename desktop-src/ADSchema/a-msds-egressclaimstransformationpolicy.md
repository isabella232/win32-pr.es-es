---
title: atributo MS-DS-out-Claims-Transformation-Policy
description: Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de salida (las notificaciones que abandonan este bosque) al dominio de confianza.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- MS-DS-out-Claims-Transformation-esquema de AD de atributo de Directiva
- Esquema de AD de atributo msDS-EgressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997440"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a><span data-ttu-id="3f090-105">atributo MS-DS-out-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="3f090-105">ms-DS-Egress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="3f090-106">Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de salida (las notificaciones que abandonan este bosque) al dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="3f090-106">This is a link to a Claims Transformation Policy Object for the egress claims (claims leaving this forest) to the Trusted Domain.</span></span> <span data-ttu-id="3f090-107">Esto solo es aplicable a una confianza entre bosques entrantes o bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="3f090-107">This is applicable only for an incoming or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="3f090-108">Cuando este vínculo no está presente, todas las notificaciones pueden salir tal cual.</span><span class="sxs-lookup"><span data-stu-id="3f090-108">When this link is not present, all claims are allowed to egress as-is.</span></span>



| <span data-ttu-id="3f090-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f090-109">Entry</span></span> | <span data-ttu-id="3f090-110">Value</span><span class="sxs-lookup"><span data-stu-id="3f090-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="3f090-111">CN</span><span class="sxs-lookup"><span data-stu-id="3f090-111">CN</span></span>                | <span data-ttu-id="3f090-112">MS-DS-out-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="3f090-112">ms-DS-Egress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="3f090-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="3f090-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3f090-114">msDS-EgressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="3f090-114">msDS-EgressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="3f090-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="3f090-115">Size</span></span>              | \-                                        |
| <span data-ttu-id="3f090-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="3f090-116">Update Privilege</span></span>  | \-                                        |
| <span data-ttu-id="3f090-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="3f090-117">Update Frequency</span></span>  | \-                                        |
| <span data-ttu-id="3f090-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3f090-118">Attribute-Id</span></span>      | <span data-ttu-id="3f090-119">1.2.840.113556.1.4.2192</span><span class="sxs-lookup"><span data-stu-id="3f090-119">1.2.840.113556.1.4.2192</span></span>                   |
| <span data-ttu-id="3f090-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3f090-120">System-Id-Guid</span></span>    | <span data-ttu-id="3f090-121">c137427e-9a73-b040-9190-1b095bb43288</span><span class="sxs-lookup"><span data-stu-id="3f090-121">c137427e-9a73-b040-9190-1b095bb43288</span></span>      |
| <span data-ttu-id="3f090-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f090-122">Syntax</span></span>            | [<span data-ttu-id="3f090-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3f090-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)   |



## <a name="implementations"></a><span data-ttu-id="3f090-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="3f090-124">Implementations</span></span>

-   [<span data-ttu-id="3f090-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f090-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="3f090-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f090-126">Windows Server 2012</span></span>



| <span data-ttu-id="3f090-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f090-127">Entry</span></span> | <span data-ttu-id="3f090-128">Value</span><span class="sxs-lookup"><span data-stu-id="3f090-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="3f090-129">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3f090-129">Link-Id</span></span>                | <span data-ttu-id="3f090-130">2192</span><span class="sxs-lookup"><span data-stu-id="3f090-130">2192</span></span>                                                 |
| <span data-ttu-id="3f090-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f090-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="3f090-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f090-132">System-Only</span></span>            | <span data-ttu-id="3f090-133">False</span><span class="sxs-lookup"><span data-stu-id="3f090-133">False</span></span>                                                |
| <span data-ttu-id="3f090-134">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3f090-134">Is-Single-Valued</span></span>       | <span data-ttu-id="3f090-135">True</span><span class="sxs-lookup"><span data-stu-id="3f090-135">True</span></span>                                                 |
| <span data-ttu-id="3f090-136">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3f090-136">Is Indexed</span></span>             | <span data-ttu-id="3f090-137">False</span><span class="sxs-lookup"><span data-stu-id="3f090-137">False</span></span>                                                |
| <span data-ttu-id="3f090-138">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f090-138">In Global Catalog</span></span>      | <span data-ttu-id="3f090-139">False</span><span class="sxs-lookup"><span data-stu-id="3f090-139">False</span></span>                                                |
| <span data-ttu-id="3f090-140">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3f090-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f090-141">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f090-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="3f090-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f090-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="3f090-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f090-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="3f090-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f090-144">Search-Flags</span></span>           | <span data-ttu-id="3f090-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f090-145">0x00000000</span></span>                                           |
| <span data-ttu-id="3f090-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f090-146">System-Flags</span></span>           | <span data-ttu-id="3f090-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f090-147">0x00000010</span></span>                                           |
| <span data-ttu-id="3f090-148">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3f090-148">Classes used in</span></span>        | [<span data-ttu-id="3f090-149">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="3f090-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





