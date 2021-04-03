---
title: Actualizar grupo-almacenar en caché derecho extendido
description: Se trata de un inicio de sesión sin GC. Ningún inicio de sesión de GC se basa en el almacenamiento en caché de las pertenencias a grupos y este derecho de acceso de control se usa para conceder derechos de permisos a los administradores y operadores para producir una actualización inmediata de la memoria caché, poniéndose en contacto con un GC disponible.
ms.assetid: 1db49a92-ccf8-4087-ac79-f4c1bcea6aa4
ms.tgt_platform: multiple
keywords:
- Actualizar grupo-almacenar en caché el esquema de AD derecho extendido
topic_type:
- apiref
api_name:
- Refresh-Group-Cache
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb576b5ef2310bceedb632a3b1ab8453b4d435e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905768"
---
# <a name="refresh-group-cache-extended-right"></a><span data-ttu-id="20650-105">Actualizar grupo-almacenar en caché derecho extendido</span><span class="sxs-lookup"><span data-stu-id="20650-105">Refresh-Group-Cache extended right</span></span>

<span data-ttu-id="20650-106">Se trata de un inicio de sesión sin GC.</span><span class="sxs-lookup"><span data-stu-id="20650-106">This is for no GC logon.</span></span> <span data-ttu-id="20650-107">Ningún inicio de sesión de GC se basa en el almacenamiento en caché de las pertenencias a grupos y este derecho de acceso de control se usa para conceder derechos de permisos a los administradores y operadores para producir una actualización inmediata de la memoria caché, poniéndose en contacto con un GC disponible.</span><span class="sxs-lookup"><span data-stu-id="20650-107">No GC logon relies on caching group memberships, and this control access right is used to grant administrators and operators permission rights to cause an immediate refresh of the cache, contacting an available GC.</span></span>



| <span data-ttu-id="20650-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="20650-108">Entry</span></span> | <span data-ttu-id="20650-109">Value</span><span class="sxs-lookup"><span data-stu-id="20650-109">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="20650-110">CN</span><span class="sxs-lookup"><span data-stu-id="20650-110">CN</span></span>           | <span data-ttu-id="20650-111">Actualizar grupo-caché</span><span class="sxs-lookup"><span data-stu-id="20650-111">Refresh-Group-Cache</span></span>                  |
| <span data-ttu-id="20650-112">Display-Name</span><span class="sxs-lookup"><span data-stu-id="20650-112">Display-Name</span></span> | <span data-ttu-id="20650-113">Actualizar caché de grupo para inicios de sesión</span><span class="sxs-lookup"><span data-stu-id="20650-113">Refresh Group Cache for Logons</span></span>       |
| <span data-ttu-id="20650-114">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="20650-114">Rights-GUID</span></span>  | <span data-ttu-id="20650-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span><span class="sxs-lookup"><span data-stu-id="20650-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span></span> |



## <a name="implementations"></a><span data-ttu-id="20650-116">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="20650-116">Implementations</span></span>

-   [<span data-ttu-id="20650-117">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="20650-117">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="20650-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="20650-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="20650-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="20650-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="20650-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="20650-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="20650-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="20650-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="20650-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="20650-122">Windows Server 2003</span></span>



| <span data-ttu-id="20650-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="20650-123">Entry</span></span> | <span data-ttu-id="20650-124">Value</span><span class="sxs-lookup"><span data-stu-id="20650-124">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="20650-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="20650-125">Applies-To</span></span>              | [<span data-ttu-id="20650-126">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="20650-126">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="20650-127">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="20650-127">Localization-Display-ID</span></span> | <span data-ttu-id="20650-128">56</span><span class="sxs-lookup"><span data-stu-id="20650-128">56</span></span>                                       |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="20650-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="20650-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="20650-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="20650-130">Entry</span></span> | <span data-ttu-id="20650-131">Value</span><span class="sxs-lookup"><span data-stu-id="20650-131">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="20650-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="20650-132">Applies-To</span></span>              | [<span data-ttu-id="20650-133">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="20650-133">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="20650-134">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="20650-134">Localization-Display-ID</span></span> | <span data-ttu-id="20650-135">56</span><span class="sxs-lookup"><span data-stu-id="20650-135">56</span></span>                                       |



## <a name="windows-server-2008"></a><span data-ttu-id="20650-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20650-136">Windows Server 2008</span></span>



| <span data-ttu-id="20650-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="20650-137">Entry</span></span> | <span data-ttu-id="20650-138">Value</span><span class="sxs-lookup"><span data-stu-id="20650-138">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="20650-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="20650-139">Applies-To</span></span>              | [<span data-ttu-id="20650-140">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="20650-140">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="20650-141">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="20650-141">Localization-Display-ID</span></span> | <span data-ttu-id="20650-142">56</span><span class="sxs-lookup"><span data-stu-id="20650-142">56</span></span>                                       |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="20650-143">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="20650-143">Windows Server 2008 R2</span></span>



| <span data-ttu-id="20650-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="20650-144">Entry</span></span> | <span data-ttu-id="20650-145">Value</span><span class="sxs-lookup"><span data-stu-id="20650-145">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="20650-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="20650-146">Applies-To</span></span>              | [<span data-ttu-id="20650-147">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="20650-147">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="20650-148">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="20650-148">Localization-Display-ID</span></span> | <span data-ttu-id="20650-149">56</span><span class="sxs-lookup"><span data-stu-id="20650-149">56</span></span>                                       |



## <a name="windows-server-2012"></a><span data-ttu-id="20650-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20650-150">Windows Server 2012</span></span>



| <span data-ttu-id="20650-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="20650-151">Entry</span></span> | <span data-ttu-id="20650-152">Value</span><span class="sxs-lookup"><span data-stu-id="20650-152">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="20650-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="20650-153">Applies-To</span></span>              | [<span data-ttu-id="20650-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="20650-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="20650-155">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="20650-155">Localization-Display-ID</span></span> | <span data-ttu-id="20650-156">56</span><span class="sxs-lookup"><span data-stu-id="20650-156">56</span></span>                                       |



 

 





