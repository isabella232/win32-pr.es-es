---
title: Permiso extendido permitido para autenticarse
description: Los controles derechos de control de acceso que se pueden autenticar en un equipo o servicio determinado.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Esquema de AD derecho extendido permitido para autenticar
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494086"
---
# <a name="allowed-to-authenticate-extended-right"></a><span data-ttu-id="a4fb6-104">Permiso extendido permitido para autenticarse</span><span class="sxs-lookup"><span data-stu-id="a4fb6-104">Allowed-To-Authenticate extended right</span></span>

<span data-ttu-id="a4fb6-105">Los controles derechos de control de acceso que se pueden autenticar en un equipo o servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="a4fb6-105">The control access right controls who can authenticate to a particular computer or service.</span></span> <span data-ttu-id="a4fb6-106">Básicamente vive en objetos de equipo, usuario y InetOrgPerson.</span><span class="sxs-lookup"><span data-stu-id="a4fb6-106">It basically lives on computer, user, and InetOrgPerson objects.</span></span> <span data-ttu-id="a4fb6-107">También es aplicable en el objeto de dominio si se permite el acceso a todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="a4fb6-107">It is also applicable on the domain object if access is allowed for the entire domain.</span></span> <span data-ttu-id="a4fb6-108">Se puede aplicar a las unidades organizativas para permitir que los usuarios puedan establecer entradas de acceso heredables en unidades organizativas que contengan un conjunto de objetos de usuario o de equipo.</span><span class="sxs-lookup"><span data-stu-id="a4fb6-108">It can be applied to OUs to permit users to be able to set inheritable ACEs on OUs that contain a set of user or computer objects.</span></span>



| <span data-ttu-id="a4fb6-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4fb6-109">Entry</span></span> | <span data-ttu-id="a4fb6-110">Value</span><span class="sxs-lookup"><span data-stu-id="a4fb6-110">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="a4fb6-111">CN</span><span class="sxs-lookup"><span data-stu-id="a4fb6-111">CN</span></span>           | <span data-ttu-id="a4fb6-112">Permitido a autenticar</span><span class="sxs-lookup"><span data-stu-id="a4fb6-112">Allowed-To-Authenticate</span></span>              |
| <span data-ttu-id="a4fb6-113">Display-Name</span><span class="sxs-lookup"><span data-stu-id="a4fb6-113">Display-Name</span></span> | <span data-ttu-id="a4fb6-114">Permiso para autenticar</span><span class="sxs-lookup"><span data-stu-id="a4fb6-114">Allowed to Authenticate</span></span>              |
| <span data-ttu-id="a4fb6-115">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="a4fb6-115">Rights-GUID</span></span>  | <span data-ttu-id="a4fb6-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span><span class="sxs-lookup"><span data-stu-id="a4fb6-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span></span> |



## <a name="implementations"></a><span data-ttu-id="a4fb6-117">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a4fb6-117">Implementations</span></span>

-   [<span data-ttu-id="a4fb6-118">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-118">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a4fb6-119">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-119">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a4fb6-120">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-120">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a4fb6-121">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-121">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a4fb6-122">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-122">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a4fb6-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4fb6-123">Windows Server 2003</span></span>



| <span data-ttu-id="a4fb6-124">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4fb6-124">Entry</span></span> | <span data-ttu-id="a4fb6-125">Value</span><span class="sxs-lookup"><span data-stu-id="a4fb6-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fb6-126">Applies-To</span><span class="sxs-lookup"><span data-stu-id="a4fb6-126">Applies-To</span></span>              | [<span data-ttu-id="a4fb6-127">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-127">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a4fb6-128">**User**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-128">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a4fb6-129">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-129">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="a4fb6-130">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="a4fb6-130">Localization-Display-ID</span></span> | <span data-ttu-id="a4fb6-131">65</span><span class="sxs-lookup"><span data-stu-id="a4fb6-131">65</span></span>                                                                                                                              |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a4fb6-132">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a4fb6-132">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a4fb6-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4fb6-133">Entry</span></span> | <span data-ttu-id="a4fb6-134">Value</span><span class="sxs-lookup"><span data-stu-id="a4fb6-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fb6-135">Applies-To</span><span class="sxs-lookup"><span data-stu-id="a4fb6-135">Applies-To</span></span>              | [<span data-ttu-id="a4fb6-136">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-136">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a4fb6-137">**User**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-137">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a4fb6-138">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-138">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="a4fb6-139">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="a4fb6-139">Localization-Display-ID</span></span> | <span data-ttu-id="a4fb6-140">65</span><span class="sxs-lookup"><span data-stu-id="a4fb6-140">65</span></span>                                                                                                                              |



## <a name="windows-server-2008"></a><span data-ttu-id="a4fb6-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4fb6-141">Windows Server 2008</span></span>



| <span data-ttu-id="a4fb6-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4fb6-142">Entry</span></span> | <span data-ttu-id="a4fb6-143">Value</span><span class="sxs-lookup"><span data-stu-id="a4fb6-143">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fb6-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="a4fb6-144">Applies-To</span></span>              | [<span data-ttu-id="a4fb6-145">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-145">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a4fb6-146">**User**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-146">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a4fb6-147">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-147">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="a4fb6-148">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="a4fb6-148">Localization-Display-ID</span></span> | <span data-ttu-id="a4fb6-149">65</span><span class="sxs-lookup"><span data-stu-id="a4fb6-149">65</span></span>                                                                                                                              |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a4fb6-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4fb6-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a4fb6-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4fb6-151">Entry</span></span> | <span data-ttu-id="a4fb6-152">Value</span><span class="sxs-lookup"><span data-stu-id="a4fb6-152">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fb6-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="a4fb6-153">Applies-To</span></span>              | [<span data-ttu-id="a4fb6-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a4fb6-155">**Cuenta de servicio de MS-DS-Managed**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-155">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="a4fb6-156">**User**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-156">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a4fb6-157">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-157">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="a4fb6-158">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="a4fb6-158">Localization-Display-ID</span></span> | <span data-ttu-id="a4fb6-159">65</span><span class="sxs-lookup"><span data-stu-id="a4fb6-159">65</span></span>                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a><span data-ttu-id="a4fb6-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4fb6-160">Windows Server 2012</span></span>



| <span data-ttu-id="a4fb6-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4fb6-161">Entry</span></span> | <span data-ttu-id="a4fb6-162">Value</span><span class="sxs-lookup"><span data-stu-id="a4fb6-162">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fb6-163">Applies-To</span><span class="sxs-lookup"><span data-stu-id="a4fb6-163">Applies-To</span></span>              | [<span data-ttu-id="a4fb6-164">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-164">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a4fb6-165">**Cuenta de servicio de MS-DS-Managed**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-165">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="a4fb6-166">**User**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-166">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="a4fb6-167">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a4fb6-167">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="a4fb6-168">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="a4fb6-168">Localization-Display-ID</span></span> | <span data-ttu-id="a4fb6-169">65</span><span class="sxs-lookup"><span data-stu-id="a4fb6-169">65</span></span>                                                                                                                                                                                                               |



 

 





