---
title: atributo MS-DS-Ingress-Claims-Transformation-Policy
description: Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de entrada (notificaciones que entran en este bosque) desde el dominio de confianza.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- MS-DS-Ingress-Claims-Transformation-esquema de AD de atributo de Directiva
- Esquema de AD de atributo msDS-IngressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536039"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a><span data-ttu-id="92394-105">atributo MS-DS-Ingress-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="92394-105">ms-DS-Ingress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="92394-106">Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de entrada (notificaciones que entran en este bosque) desde el dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="92394-106">This is a link to a Claims Transformation Policy Object for the ingress claims (claims entering this forest) from the Trusted Domain.</span></span> <span data-ttu-id="92394-107">Esto solo es aplicable a una confianza entre bosques de salida o bidireccional.</span><span class="sxs-lookup"><span data-stu-id="92394-107">This is applicable only for an outgoing or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="92394-108">Si este vínculo está ausente, se quitan todas las notificaciones de entrada.</span><span class="sxs-lookup"><span data-stu-id="92394-108">If this link is absent, all the ingress claims are dropped.</span></span>



| <span data-ttu-id="92394-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="92394-109">Entry</span></span> | <span data-ttu-id="92394-110">Value</span><span class="sxs-lookup"><span data-stu-id="92394-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="92394-111">CN</span><span class="sxs-lookup"><span data-stu-id="92394-111">CN</span></span>                | <span data-ttu-id="92394-112">MS-DS-Ingress-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="92394-112">ms-DS-Ingress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="92394-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="92394-113">Ldap-Display-Name</span></span> | <span data-ttu-id="92394-114">msDS-IngressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="92394-114">msDS-IngressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="92394-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="92394-115">Size</span></span>              | \-                                         |
| <span data-ttu-id="92394-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="92394-116">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="92394-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="92394-117">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="92394-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92394-118">Attribute-Id</span></span>      | <span data-ttu-id="92394-119">1.2.840.113556.1.4.2191</span><span class="sxs-lookup"><span data-stu-id="92394-119">1.2.840.113556.1.4.2191</span></span>                    |
| <span data-ttu-id="92394-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="92394-120">System-Id-Guid</span></span>    | <span data-ttu-id="92394-121">86284c08-0c6e-1540-8b15-75147d23d20d</span><span class="sxs-lookup"><span data-stu-id="92394-121">86284c08-0c6e-1540-8b15-75147d23d20d</span></span>       |
| <span data-ttu-id="92394-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92394-122">Syntax</span></span>            | [<span data-ttu-id="92394-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="92394-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)    |



## <a name="implementations"></a><span data-ttu-id="92394-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="92394-124">Implementations</span></span>

-   [<span data-ttu-id="92394-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92394-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="92394-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92394-126">Windows Server 2012</span></span>



| <span data-ttu-id="92394-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="92394-127">Entry</span></span> | <span data-ttu-id="92394-128">Value</span><span class="sxs-lookup"><span data-stu-id="92394-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="92394-129">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92394-129">Link-Id</span></span>                | <span data-ttu-id="92394-130">2190</span><span class="sxs-lookup"><span data-stu-id="92394-130">2190</span></span>                                                 |
| <span data-ttu-id="92394-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92394-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92394-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="92394-132">System-Only</span></span>            | <span data-ttu-id="92394-133">False</span><span class="sxs-lookup"><span data-stu-id="92394-133">False</span></span>                                                |
| <span data-ttu-id="92394-134">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92394-134">Is-Single-Valued</span></span>       | <span data-ttu-id="92394-135">True</span><span class="sxs-lookup"><span data-stu-id="92394-135">True</span></span>                                                 |
| <span data-ttu-id="92394-136">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92394-136">Is Indexed</span></span>             | <span data-ttu-id="92394-137">False</span><span class="sxs-lookup"><span data-stu-id="92394-137">False</span></span>                                                |
| <span data-ttu-id="92394-138">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92394-138">In Global Catalog</span></span>      | <span data-ttu-id="92394-139">False</span><span class="sxs-lookup"><span data-stu-id="92394-139">False</span></span>                                                |
| <span data-ttu-id="92394-140">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92394-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="92394-141">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92394-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="92394-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92394-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="92394-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92394-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="92394-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92394-144">Search-Flags</span></span>           | <span data-ttu-id="92394-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92394-145">0x00000000</span></span>                                           |
| <span data-ttu-id="92394-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92394-146">System-Flags</span></span>           | <span data-ttu-id="92394-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92394-147">0x00000010</span></span>                                           |
| <span data-ttu-id="92394-148">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92394-148">Classes used in</span></span>        | [<span data-ttu-id="92394-149">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="92394-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





