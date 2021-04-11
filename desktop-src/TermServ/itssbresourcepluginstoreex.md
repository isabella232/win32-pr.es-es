---
title: Interfaz ITsSbResourcePluginStoreEx
description: Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz ITsSbResourcePluginStoreEx
- Servicios de Escritorio remoto de la interfaz ITsSbResourcePluginStoreEx, descrito
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150491"
---
# <a name="itssbresourcepluginstoreex-interface"></a><span data-ttu-id="9024a-105">Interfaz ITsSbResourcePluginStoreEx</span><span class="sxs-lookup"><span data-stu-id="9024a-105">ITsSbResourcePluginStoreEx interface</span></span>

<span data-ttu-id="9024a-106">Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos.</span><span class="sxs-lookup"><span data-stu-id="9024a-106">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span> <span data-ttu-id="9024a-107">Estos métodos agregan, eliminan y consultan estos objetos.</span><span class="sxs-lookup"><span data-stu-id="9024a-107">These methods add, delete, and query these objects.</span></span>

<span data-ttu-id="9024a-108">Esta interfaz solo está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado.</span><span class="sxs-lookup"><span data-stu-id="9024a-108">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="9024a-109">Los métodos [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) y [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) de la interfaz [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) están disponibles a partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="9024a-109">The [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) and [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) methods of the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface are available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="9024a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9024a-110">Members</span></span>

<span data-ttu-id="9024a-111">La interfaz **ITsSbResourcePluginStoreEx** hereda de [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span><span class="sxs-lookup"><span data-stu-id="9024a-111">The **ITsSbResourcePluginStoreEx** interface inherits from [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span></span> <span data-ttu-id="9024a-112">**ITsSbResourcePluginStoreEx** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9024a-112">**ITsSbResourcePluginStoreEx** also has these types of members:</span></span>

-   [<span data-ttu-id="9024a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9024a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9024a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9024a-114">Methods</span></span>

<span data-ttu-id="9024a-115">La interfaz **ITsSbResourcePluginStoreEx** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9024a-115">The **ITsSbResourcePluginStoreEx** interface has these methods.</span></span>



| <span data-ttu-id="9024a-116">Método</span><span class="sxs-lookup"><span data-stu-id="9024a-116">Method</span></span>                                                                                                            | <span data-ttu-id="9024a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9024a-117">Description</span></span>                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9024a-118">**AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="9024a-118">**AcquireTargetLock**</span></span>](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | <span data-ttu-id="9024a-119">Bloquea un destino.</span><span class="sxs-lookup"><span data-stu-id="9024a-119">Locks a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="9024a-120">**AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="9024a-120">**AddEnvironmentToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | <span data-ttu-id="9024a-121">Agrega un entorno al almacén del complemento de recursos.</span><span class="sxs-lookup"><span data-stu-id="9024a-121">Adds an environment to the resource plug-in store.</span></span><br/>                                                   |
| [<span data-ttu-id="9024a-122">**AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="9024a-122">**AddSessionToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | <span data-ttu-id="9024a-123">Agrega una nueva sesión al almacén del complemento de recursos.</span><span class="sxs-lookup"><span data-stu-id="9024a-123">Adds a new session to the resource plug-in store.</span></span><br/>                                                    |
| [<span data-ttu-id="9024a-124">**AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="9024a-124">**AddTargetToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | <span data-ttu-id="9024a-125">Agrega un destino al almacén del complemento de recursos.</span><span class="sxs-lookup"><span data-stu-id="9024a-125">Adds a target to the resource plug-in store.</span></span><br/>                                                         |
| [<span data-ttu-id="9024a-126">**DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="9024a-126">**DeleteTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | <span data-ttu-id="9024a-127">Elimina un destino.</span><span class="sxs-lookup"><span data-stu-id="9024a-127">Deletes a target.</span></span><br/>                                                                                    |
| [<span data-ttu-id="9024a-128">**EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="9024a-128">**EnumerateEnvironments**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | <span data-ttu-id="9024a-129">Devuelve una matriz que contiene los entornos presentes en el almacén del complemento de recursos.</span><span class="sxs-lookup"><span data-stu-id="9024a-129">Returns an array that contains the environments present in the resource plug-in store.</span></span><br/>               |
| [<span data-ttu-id="9024a-130">**EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="9024a-130">**EnumerateFarms**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | <span data-ttu-id="9024a-131">Enumera todas las granjas de servidores que se han agregado al almacén del complemento de recursos.</span><span class="sxs-lookup"><span data-stu-id="9024a-131">Enumerates all the farms that have been added to the resource plug-in store.</span></span><br/>                         |
| [<span data-ttu-id="9024a-132">**EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="9024a-132">**EnumerateSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | <span data-ttu-id="9024a-133">Enumera un conjunto especificado de sesiones.</span><span class="sxs-lookup"><span data-stu-id="9024a-133">Enumerates a specified set of sessions.</span></span><br/>                                                              |
| [<span data-ttu-id="9024a-134">**EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="9024a-134">**EnumerateTargets**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | <span data-ttu-id="9024a-135">Devuelve una matriz que contiene los destinos especificados presentes en el almacén del complemento de recursos.</span><span class="sxs-lookup"><span data-stu-id="9024a-135">Returns an array that contains the specified targets that are present in the resource plug-in store.</span></span><br/> |
| [<span data-ttu-id="9024a-136">**GetFarmProperty**</span><span class="sxs-lookup"><span data-stu-id="9024a-136">**GetFarmProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | <span data-ttu-id="9024a-137">Recupera una propiedad de una granja.</span><span class="sxs-lookup"><span data-stu-id="9024a-137">Retrieves a property of a farm.</span></span><br/>                                                                      |
| [<span data-ttu-id="9024a-138">**QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="9024a-138">**QueryEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | <span data-ttu-id="9024a-139">Devuelve el objeto de entorno especificado.</span><span class="sxs-lookup"><span data-stu-id="9024a-139">Returns the specified environment object.</span></span><br/>                                                            |
| [<span data-ttu-id="9024a-140">**QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="9024a-140">**QuerySessionBySessionId**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | <span data-ttu-id="9024a-141">Devuelve el objeto de sesión que tiene el identificador de sesión especificado.</span><span class="sxs-lookup"><span data-stu-id="9024a-141">Returns the session object that has the specified session ID.</span></span><br/>                                        |
| [<span data-ttu-id="9024a-142">**QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="9024a-142">**QueryTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | <span data-ttu-id="9024a-143">Devuelve el destino que tiene el nombre de destino y el nombre de granja especificados.</span><span class="sxs-lookup"><span data-stu-id="9024a-143">Returns the target that has the specified target name and farm name.</span></span><br/>                                 |
| [<span data-ttu-id="9024a-144">**ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="9024a-144">**ReleaseTargetLock**</span></span>](itssbresourcepluginstoreex-releasetargetlock.md)                                         | <span data-ttu-id="9024a-145">Libera un bloqueo en un destino.</span><span class="sxs-lookup"><span data-stu-id="9024a-145">Releases a lock on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="9024a-146">**RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="9024a-146">**RemoveEnvironmentFromStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | <span data-ttu-id="9024a-147">Quita el entorno especificado del almacén del complemento de recursos.</span><span class="sxs-lookup"><span data-stu-id="9024a-147">Removes the specified environment from the resource plug-in store.</span></span><br/>                                   |
| [<span data-ttu-id="9024a-148">**SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="9024a-148">**SaveEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | <span data-ttu-id="9024a-149">Guarda un entorno.</span><span class="sxs-lookup"><span data-stu-id="9024a-149">Saves an environment.</span></span><br/>                                                                                |
| [<span data-ttu-id="9024a-150">**SaveSession**</span><span class="sxs-lookup"><span data-stu-id="9024a-150">**SaveSession**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | <span data-ttu-id="9024a-151">Guarda una sesión.</span><span class="sxs-lookup"><span data-stu-id="9024a-151">Saves a session.</span></span><br/>                                                                                     |
| [<span data-ttu-id="9024a-152">**SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="9024a-152">**SaveTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | <span data-ttu-id="9024a-153">Guarda un destino.</span><span class="sxs-lookup"><span data-stu-id="9024a-153">Saves a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="9024a-154">**SetEnvironmentProperty**</span><span class="sxs-lookup"><span data-stu-id="9024a-154">**SetEnvironmentProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | <span data-ttu-id="9024a-155">Establece una propiedad en un entorno.</span><span class="sxs-lookup"><span data-stu-id="9024a-155">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="9024a-156">**SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="9024a-156">**SetEnvironmentPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | <span data-ttu-id="9024a-157">Establece una propiedad en un entorno.</span><span class="sxs-lookup"><span data-stu-id="9024a-157">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="9024a-158">**SetSessionState**</span><span class="sxs-lookup"><span data-stu-id="9024a-158">**SetSessionState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | <span data-ttu-id="9024a-159">Establece el estado de una sesión.</span><span class="sxs-lookup"><span data-stu-id="9024a-159">Sets the state of a session.</span></span><br/>                                                                         |
| [<span data-ttu-id="9024a-160">**SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="9024a-160">**SetTargetProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | <span data-ttu-id="9024a-161">Establece una propiedad en un destino.</span><span class="sxs-lookup"><span data-stu-id="9024a-161">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="9024a-162">**SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="9024a-162">**SetTargetPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | <span data-ttu-id="9024a-163">Establece una propiedad en un destino.</span><span class="sxs-lookup"><span data-stu-id="9024a-163">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="9024a-164">**SetTargetState**</span><span class="sxs-lookup"><span data-stu-id="9024a-164">**SetTargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | <span data-ttu-id="9024a-165">Establece el estado de un destino.</span><span class="sxs-lookup"><span data-stu-id="9024a-165">Sets the state of a target.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="9024a-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9024a-166">Requirements</span></span>



| <span data-ttu-id="9024a-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="9024a-167">Requirement</span></span> | <span data-ttu-id="9024a-168">Value</span><span class="sxs-lookup"><span data-stu-id="9024a-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9024a-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9024a-169">Minimum supported client</span></span><br/> | <span data-ttu-id="9024a-170">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9024a-170">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9024a-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9024a-171">Minimum supported server</span></span><br/> | <span data-ttu-id="9024a-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9024a-172">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="9024a-173">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9024a-173">End of server support</span></span><br/>    | <span data-ttu-id="9024a-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9024a-174">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="9024a-175">IID</span><span class="sxs-lookup"><span data-stu-id="9024a-175">IID</span></span><br/>                      | <span data-ttu-id="9024a-176">IID \_ ITsSbResourcePluginStoreEx se define como 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="9024a-176">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9024a-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="9024a-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9024a-178">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="9024a-178">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[<span data-ttu-id="9024a-179">Interfaces de virtualización Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9024a-179">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





