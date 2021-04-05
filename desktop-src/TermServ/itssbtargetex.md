---
title: Interfaz ITsSbTargetEx
description: Expone propiedades que almacenan información de configuración y estado sobre un destino.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, descrito
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997053"
---
# <a name="itssbtargetex-interface"></a><span data-ttu-id="6c3b1-105">Interfaz ITsSbTargetEx</span><span class="sxs-lookup"><span data-stu-id="6c3b1-105">ITsSbTargetEx interface</span></span>

<span data-ttu-id="6c3b1-106">Expone propiedades que almacenan información de configuración y estado sobre un destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-106">Exposes properties that store configuration and state information about a target.</span></span>

<span data-ttu-id="6c3b1-107">Esta interfaz solo está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-107">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="6c3b1-108">La propiedad [**TargetLoad**](itssbtarget-targetload.md) de la interfaz [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) está disponible a partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-108">The [**TargetLoad**](itssbtarget-targetload.md) property of the [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) interface is available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="6c3b1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c3b1-109">Members</span></span>

<span data-ttu-id="6c3b1-110">La interfaz **ITsSbTargetEx** hereda de [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span><span class="sxs-lookup"><span data-stu-id="6c3b1-110">The **ITsSbTargetEx** interface inherits from [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span></span> <span data-ttu-id="6c3b1-111">**ITsSbTargetEx** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6c3b1-111">**ITsSbTargetEx** also has these types of members:</span></span>

-   [<span data-ttu-id="6c3b1-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c3b1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c3b1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c3b1-113">Properties</span></span>

<span data-ttu-id="6c3b1-114">La interfaz **ITsSbTargetEx** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-114">The **ITsSbTargetEx** interface has these properties.</span></span>



| <span data-ttu-id="6c3b1-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c3b1-115">Property</span></span>                                                                      | <span data-ttu-id="6c3b1-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6c3b1-116">Access type</span></span>           | <span data-ttu-id="6c3b1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c3b1-117">Description</span></span>                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c3b1-118">**EnvironmentName**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-118">**EnvironmentName**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | <span data-ttu-id="6c3b1-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-119">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-120">Recupera o especifica el nombre del entorno asociado al destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-120">Retrieves or specifies the name of the environment associated with the target.</span></span><br/> |
| [<span data-ttu-id="6c3b1-121">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-121">**FarmName**</span></span>](itssbtarget-farmname.md)<br/>                           | <span data-ttu-id="6c3b1-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-122">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-123">Especifica o recupera el nombre de la granja a la que está unido este destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-123">Specifies or retrieves the name of the farm to which this target is joined.</span></span><br/>    |
| [<span data-ttu-id="6c3b1-124">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-124">**IpAddresses**</span></span>](itssbtarget-ipaddresses.md)<br/>                     | <span data-ttu-id="6c3b1-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-125">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-126">Recupera o especifica las direcciones IP externas del destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-126">Retrieves or specifies the external IP addresses of the target.</span></span><br/>                |
| [<span data-ttu-id="6c3b1-127">**NumPendingConnections**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-127">**NumPendingConnections**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | <span data-ttu-id="6c3b1-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-128">Read-only</span></span><br/>  | <span data-ttu-id="6c3b1-129">Recupera el número de conexiones de usuario pendientes para el destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-129">Retrieves the number of pending user connections for the target.</span></span><br/>               |
| [<span data-ttu-id="6c3b1-130">**NumSessions**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-130">**NumSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | <span data-ttu-id="6c3b1-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-131">Read-only</span></span><br/>  | <span data-ttu-id="6c3b1-132">Recupera el número de sesiones que mantiene el agente para el destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-132">Retrieves the number of sessions maintained by broker for the target.</span></span><br/>          |
| [<span data-ttu-id="6c3b1-133">**TargetFQDN**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-133">**TargetFQDN**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | <span data-ttu-id="6c3b1-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-134">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-135">Especifica o recupera el nombre de dominio completo del destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-135">Specifies or retrieves the fully qualified domain name of the target.</span></span><br/>          |
| <span data-ttu-id="6c3b1-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6c3b1-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span></span><br/>                     | <span data-ttu-id="6c3b1-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-137">Read-only</span></span><br/>  | <span data-ttu-id="6c3b1-138">Recupera la carga relativa de un destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-138">Retrieves the relative load on a target.</span></span><br/>                                       |
| [<span data-ttu-id="6c3b1-139">**NombreDeDestino**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-139">**TargetName**</span></span>](itssbtarget-targetname.md)<br/>                       | <span data-ttu-id="6c3b1-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-140">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-141">Especifica o recupera el nombre del destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-141">Specifies or retrieves the name of the target.</span></span><br/>                                 |
| [<span data-ttu-id="6c3b1-142">**TargetNetbios**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-142">**TargetNetbios**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | <span data-ttu-id="6c3b1-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-143">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-144">Especifica o recupera el nombre NetBIOS del destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-144">Specifies or retrieves the NetBIOS name of the target.</span></span><br/>                         |
| [<span data-ttu-id="6c3b1-145">**TargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-145">**TargetPropertySet**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | <span data-ttu-id="6c3b1-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-146">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-147">Especifica o recupera el conjunto de propiedades para el destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-147">Specifies or retrieves the property set for the target.</span></span><br/>                        |
| [<span data-ttu-id="6c3b1-148">**TargetState**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-148">**TargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | <span data-ttu-id="6c3b1-149">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6c3b1-149">Read/write</span></span><br/> | <span data-ttu-id="6c3b1-150">Especifica o recupera el estado de destino.</span><span class="sxs-lookup"><span data-stu-id="6c3b1-150">Specifies or retrieves the target state.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="6c3b1-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c3b1-151">Requirements</span></span>



| <span data-ttu-id="6c3b1-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c3b1-152">Requirement</span></span> | <span data-ttu-id="6c3b1-153">Value</span><span class="sxs-lookup"><span data-stu-id="6c3b1-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c3b1-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c3b1-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3b1-155">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6c3b1-155">None supported</span></span><br/>                                                        |
| <span data-ttu-id="6c3b1-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c3b1-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3b1-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6c3b1-157">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="6c3b1-158">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6c3b1-158">End of server support</span></span><br/>    | <span data-ttu-id="6c3b1-159">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6c3b1-159">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="6c3b1-160">IID</span><span class="sxs-lookup"><span data-stu-id="6c3b1-160">IID</span></span><br/>                      | <span data-ttu-id="6c3b1-161">IID \_ ITsSbTargetEx se define como 74f99987-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="6c3b1-161">IID\_ITsSbTargetEx is defined as 74f99987-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c3b1-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c3b1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3b1-163">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="6c3b1-163">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="6c3b1-164">Interfaces de virtualización Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="6c3b1-164">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

