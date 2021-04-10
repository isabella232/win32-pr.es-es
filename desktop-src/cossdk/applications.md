---
description: Contiene un objeto para cada aplicación COM+ instalada en el equipo local. Las propiedades expuestas por estos objetos contienen todas las configuraciones realizadas en el nivel de la aplicación.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Colección de aplicaciones
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153273"
---
# <a name="applications-collection"></a><span data-ttu-id="b1488-104">Colección de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b1488-104">Applications collection</span></span>

<span data-ttu-id="b1488-105">Contiene un objeto para cada aplicación COM+ instalada en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="b1488-105">Contains an object for each COM+ application installed on the local computer.</span></span> <span data-ttu-id="b1488-106">Las propiedades expuestas por estos objetos contienen todas las configuraciones realizadas en el nivel de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-106">The properties exposed by these objects hold all settings made at the application level.</span></span>

<span data-ttu-id="b1488-107">Las propiedades de los componentes de una aplicación se establecen mediante la colección de [**componentes**](components.md) relacionados.</span><span class="sxs-lookup"><span data-stu-id="b1488-107">You set properties for components within an application by using the related [**Components**](components.md) collection.</span></span> <span data-ttu-id="b1488-108">Los roles se asignan a una aplicación mediante la colección de [**roles**](roles.md) relacionados.</span><span class="sxs-lookup"><span data-stu-id="b1488-108">You assign roles to an application by using the related [**Roles**](roles.md) collection.</span></span>

<span data-ttu-id="b1488-109">Para instalar los componentes en una aplicación, use los métodos del objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="b1488-109">To install components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="b1488-110">Para instalar una aplicación desde un archivo o para apagar o exportar una aplicación, use también métodos en el objeto **COMAdminCatalog** .</span><span class="sxs-lookup"><span data-stu-id="b1488-110">To install an application from a file or to shut down or export an application, also use methods on the **COMAdminCatalog** object.</span></span> <span data-ttu-id="b1488-111">De lo contrario, para crear una nueva aplicación, puede Agregar un objeto a la colección de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="b1488-111">Otherwise, to create a new application, you can add an object to the **Applications** collection.</span></span>

<span data-ttu-id="b1488-112">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b1488-112">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b1488-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1488-113">Members</span></span>

<span data-ttu-id="b1488-114">La colección de **aplicaciones** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="b1488-114">The **Applications** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b1488-115">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="b1488-115">Related Collections</span></span>

<span data-ttu-id="b1488-116">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="b1488-116">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b1488-117">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="b1488-117">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="b1488-118">**Componentes**</span><span class="sxs-lookup"><span data-stu-id="b1488-118">**Components**</span></span>](components.md)
-   [<span data-ttu-id="b1488-119">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b1488-119">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b1488-120">**LegacyComponents**</span><span class="sxs-lookup"><span data-stu-id="b1488-120">**LegacyComponents**</span></span>](legacycomponents.md)
-   [<span data-ttu-id="b1488-121">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b1488-121">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b1488-122">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b1488-122">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="b1488-123">**Roles**</span><span class="sxs-lookup"><span data-stu-id="b1488-123">**Roles**</span></span>](roles.md)

<span data-ttu-id="b1488-124">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b1488-124">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b1488-125">**Particiones**</span><span class="sxs-lookup"><span data-stu-id="b1488-125">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="b1488-126">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="b1488-126">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b1488-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1488-127">Properties</span></span>

<span data-ttu-id="b1488-128">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="b1488-128">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b1488-129">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-129">3GigSupportEnabled</span></span>](#3gigsupportenabled)
-   [<span data-ttu-id="b1488-130">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="b1488-130">AccessChecksLevel</span></span>](#accesscheckslevel)
-   [<span data-ttu-id="b1488-131">Activación</span><span class="sxs-lookup"><span data-stu-id="b1488-131">Activation</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="b1488-132">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-132">ApplicationAccessChecksEnabled</span></span>](#applicationaccesschecksenabled)
-   [<span data-ttu-id="b1488-133">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="b1488-133">ApplicationDirectory</span></span>](#applicationdirectory)
-   [<span data-ttu-id="b1488-134">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="b1488-134">ApplicationProxy</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="b1488-135">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="b1488-135">ApplicationProxyServerName</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="b1488-136">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="b1488-136">AppPartitionID</span></span>](#apppartitionid)
-   [<span data-ttu-id="b1488-137">Autenticación</span><span class="sxs-lookup"><span data-stu-id="b1488-137">Authentication</span></span>](#authenticationcapability)
-   [<span data-ttu-id="b1488-138">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="b1488-138">AuthenticationCapability</span></span>](#authenticationcapability)
-   [<span data-ttu-id="b1488-139">Sustituir</span><span class="sxs-lookup"><span data-stu-id="b1488-139">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="b1488-140">CommandLine</span><span class="sxs-lookup"><span data-stu-id="b1488-140">CommandLine</span></span>](#commandline)
-   [<span data-ttu-id="b1488-141">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="b1488-141">ConcurrentApps</span></span>](#concurrentapps)
-   [<span data-ttu-id="b1488-142">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="b1488-142">CreatedBy</span></span>](#createdby)
-   [<span data-ttu-id="b1488-143">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-143">CRMEnabled</span></span>](#crmenabled)
-   [<span data-ttu-id="b1488-144">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="b1488-144">CRMLogFile</span></span>](#crmlogfile)
-   [<span data-ttu-id="b1488-145">Eliminable</span><span class="sxs-lookup"><span data-stu-id="b1488-145">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="b1488-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-146">Description</span></span>](#description)
-   [<span data-ttu-id="b1488-147">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-147">DumpEnabled</span></span>](#dumpenabled)
-   [<span data-ttu-id="b1488-148">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="b1488-148">DumpOnException</span></span>](#dumponexception)
-   [<span data-ttu-id="b1488-149">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="b1488-149">DumpOnFailfast</span></span>](#dumponfailfast)
-   [<span data-ttu-id="b1488-150">DumpPath</span><span class="sxs-lookup"><span data-stu-id="b1488-150">DumpPath</span></span>](#dumppath)
-   [<span data-ttu-id="b1488-151">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-151">EventsEnabled</span></span>](#eventsenabled)
-   [<span data-ttu-id="b1488-152">Id</span><span class="sxs-lookup"><span data-stu-id="b1488-152">ID</span></span>](#applications-collection)
-   [<span data-ttu-id="b1488-153">Identidad</span><span class="sxs-lookup"><span data-stu-id="b1488-153">Identity</span></span>](#identity)
-   [<span data-ttu-id="b1488-154">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="b1488-154">ImpersonationLevel</span></span>](#impersonationlevel)
-   [<span data-ttu-id="b1488-155">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-155">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="b1488-156">IsSystem</span><span class="sxs-lookup"><span data-stu-id="b1488-156">IsSystem</span></span>](#issystem)
-   [<span data-ttu-id="b1488-157">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="b1488-157">MaxDumpCount</span></span>](#maxdumpcount)
-   [<span data-ttu-id="b1488-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1488-158">Name</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="b1488-159">Contraseña</span><span class="sxs-lookup"><span data-stu-id="b1488-159">Password</span></span>](#password)
-   [<span data-ttu-id="b1488-160">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="b1488-160">QCAuthenticateMsgs</span></span>](#qcauthenticatemsgs)
-   [<span data-ttu-id="b1488-161">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="b1488-161">QCListenerMaxThreads</span></span>](#qclistenermaxthreads)
-   [<span data-ttu-id="b1488-162">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-162">QueueListenerEnabled</span></span>](#queuelistenerenabled)
-   [<span data-ttu-id="b1488-163">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-163">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="b1488-164">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-164">RecycleActivationLimit</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="b1488-165">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-165">RecycleCallLimit</span></span>](#recyclecalllimit)
-   [<span data-ttu-id="b1488-166">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="b1488-166">RecycleExpirationTimeout</span></span>](#recycleexpirationtimeout)
-   [<span data-ttu-id="b1488-167">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-167">RecycleLifetimeLimit</span></span>](#recyclelifetimelimit)
-   [<span data-ttu-id="b1488-168">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-168">RecycleMemoryLimit</span></span>](#recyclememorylimit)
-   [<span data-ttu-id="b1488-169">Replicable</span><span class="sxs-lookup"><span data-stu-id="b1488-169">Replicable</span></span>](#replicable)
-   [<span data-ttu-id="b1488-170">RunForever</span><span class="sxs-lookup"><span data-stu-id="b1488-170">RunForever</span></span>](#runforever)
-   [<span data-ttu-id="b1488-171">ServiceName</span><span class="sxs-lookup"><span data-stu-id="b1488-171">ServiceName</span></span>](#servicename)
-   [<span data-ttu-id="b1488-172">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="b1488-172">ShutdownAfter</span></span>](#shutdownafter)
-   [<span data-ttu-id="b1488-173">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="b1488-173">SoapActivated</span></span>](#soapactivated)
-   [<span data-ttu-id="b1488-174">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="b1488-174">SoapBaseUrl</span></span>](#soapbaseurl)
-   [<span data-ttu-id="b1488-175">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="b1488-175">SoapMailTo</span></span>](#soapmailto)
-   [<span data-ttu-id="b1488-176">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="b1488-176">SoapVRoot</span></span>](#soapvroot)
-   [<span data-ttu-id="b1488-177">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-177">SRPEnabled</span></span>](#srpenabled)
-   [<span data-ttu-id="b1488-178">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="b1488-178">SRPTrustLevel</span></span>](#srptrustlevel)

### <a name="3gigsupportenabled"></a><span data-ttu-id="b1488-179">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-179">3GigSupportEnabled</span></span>



| <span data-ttu-id="b1488-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-180">Entry</span></span> | <span data-ttu-id="b1488-181">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-181">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-182">Description</span></span>    | <span data-ttu-id="b1488-183">Indica si la aplicación puede utilizar 3 GB de memoria en su proceso.</span><span class="sxs-lookup"><span data-stu-id="b1488-183">Indicates whether the application can use 3 GB of memory in its process.</span></span> <span data-ttu-id="b1488-184">Si no está habilitado, la aplicación solo puede utilizar 2 GB de memoria.</span><span class="sxs-lookup"><span data-stu-id="b1488-184">If this is not enabled, the application can use only 2 GB of memory.</span></span> |
| <span data-ttu-id="b1488-185">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-185">Access</span></span>         | <span data-ttu-id="b1488-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-186">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="b1488-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-187">Type</span></span>           | <span data-ttu-id="b1488-188">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-188">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="b1488-189">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-189">Default</span></span>        | <span data-ttu-id="b1488-190">False</span><span class="sxs-lookup"><span data-stu-id="b1488-190">False</span></span>                                                                                                                                         |
| <span data-ttu-id="b1488-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-191">Minimum system</span></span> | <span data-ttu-id="b1488-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-192">Windows 2000</span></span>                                                                                                                                  |



 

### <a name="accesscheckslevel"></a><span data-ttu-id="b1488-193">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="b1488-193">AccessChecksLevel</span></span>



| <span data-ttu-id="b1488-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-194">Entry</span></span> | <span data-ttu-id="b1488-195">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-195">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-196">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-196">Description</span></span>    | <span data-ttu-id="b1488-197">Indica si las comprobaciones de acceso se realizan solo en el nivel de proceso o en el nivel de componente y de proceso.</span><span class="sxs-lookup"><span data-stu-id="b1488-197">Indicates whether access checks are performed at only the process level or at both the process and component level.</span></span> <span data-ttu-id="b1488-198">Se recomienda usar las constantes en la enumeración y no los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="b1488-198">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="b1488-199">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-199">Access</span></span>         | <span data-ttu-id="b1488-200">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-200">ReadWrite</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="b1488-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-201">Type</span></span>           | <span data-ttu-id="b1488-202">Valores posibles largos: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="b1488-202">Long Possible values: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                |
| <span data-ttu-id="b1488-203">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-203">Default</span></span>        | <span data-ttu-id="b1488-204">COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="b1488-204">COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                                                                               |
| <span data-ttu-id="b1488-205">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-205">Minimum system</span></span> | <span data-ttu-id="b1488-206">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-206">Windows 2000</span></span>                                                                                                                                                                                                    |



 

### <a name="activation"></a><span data-ttu-id="b1488-207">Activación</span><span class="sxs-lookup"><span data-stu-id="b1488-207">Activation</span></span>



| <span data-ttu-id="b1488-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-208">Entry</span></span> | <span data-ttu-id="b1488-209">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-209">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-210">Description</span></span>    | <span data-ttu-id="b1488-211">La activación local indica que los objetos de la aplicación se ejecutan en un proceso de servidor local dedicado (aplicación de servidor).</span><span class="sxs-lookup"><span data-stu-id="b1488-211">Local activation indicates that objects within the application run within a dedicated local server process (server application).</span></span> <span data-ttu-id="b1488-212">La activación en proceso indica que los objetos se ejecutan en el proceso de su creador (aplicación de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="b1488-212">In-process activation indicates that objects run in their creator's process (library application).</span></span> |
| <span data-ttu-id="b1488-213">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-213">Access</span></span>         | <span data-ttu-id="b1488-214">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-214">ReadWrite</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="b1488-215">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-215">Type</span></span>           | <span data-ttu-id="b1488-216">Valores posibles largos: COMAdminActivationInproc (0) COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="b1488-216">Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)</span></span>                                                                                                                                                        |
| <span data-ttu-id="b1488-217">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-217">Default</span></span>        | <span data-ttu-id="b1488-218">COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="b1488-218">COMAdminActivationLocal (1)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="b1488-219">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-219">Minimum system</span></span> | <span data-ttu-id="b1488-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-220">Windows 2000</span></span>                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a><span data-ttu-id="b1488-221">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-221">ApplicationAccessChecksEnabled</span></span>



| <span data-ttu-id="b1488-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-222">Entry</span></span> | <span data-ttu-id="b1488-223">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-223">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-224">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-224">Description</span></span>    | <span data-ttu-id="b1488-225">Indica si se realizan comprobaciones de acceso para la aplicación cuando los clientes realizan llamadas a ella.</span><span class="sxs-lookup"><span data-stu-id="b1488-225">Indicates whether access checks are performed for the application when clients make calls into it.</span></span> |
| <span data-ttu-id="b1488-226">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-226">Access</span></span>         | <span data-ttu-id="b1488-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-227">ReadWrite</span></span>                                                                                          |
| <span data-ttu-id="b1488-228">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-228">Type</span></span>           | <span data-ttu-id="b1488-229">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-229">Bool</span></span>                                                                                               |
| <span data-ttu-id="b1488-230">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-230">Default</span></span>        | <span data-ttu-id="b1488-231">True</span><span class="sxs-lookup"><span data-stu-id="b1488-231">True</span></span>                                                                                               |
| <span data-ttu-id="b1488-232">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-232">Minimum system</span></span> | <span data-ttu-id="b1488-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-233">Windows 2000</span></span>                                                                                       |



 

### <a name="applicationdirectory"></a><span data-ttu-id="b1488-234">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="b1488-234">ApplicationDirectory</span></span>



| <span data-ttu-id="b1488-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-235">Entry</span></span> | <span data-ttu-id="b1488-236">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-236">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-237">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-237">Description</span></span>    | <span data-ttu-id="b1488-238">Ruta de acceso completa a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-238">The full path to the application.</span></span> <span data-ttu-id="b1488-239">Esta información es necesaria cuando se configuran los ensamblados en paralelo (SxS).</span><span class="sxs-lookup"><span data-stu-id="b1488-239">This information is needed when you configure Side-by-Side (SxS) assemblies.</span></span> <span data-ttu-id="b1488-240">Los ensamblados en paralelo (SxS) permiten a las aplicaciones ASP especificar qué versión de una DLL del sistema compatible con SxS se va a usar, como MSVCRT, MSXML, COMCTL, GDIPLUS, etc.</span><span class="sxs-lookup"><span data-stu-id="b1488-240">Side-by-side (SxS) assemblies allow ASP applications to specify which version of an SxS-supported system DLL to use, such as MSVCRT, MSXML, COMCTL, GDIPLUS, and so on.</span></span> <span data-ttu-id="b1488-241">Por ejemplo, si la aplicación ASP se basa en la versión 2,0 de MSVCRT, puede asegurarse de que la aplicación siga usando la versión 2,0 de MSVCRT incluso después de aplicar los Service Packs al servidor.</span><span class="sxs-lookup"><span data-stu-id="b1488-241">For example, if your ASP application relies on MSVCRT version 2.0, you can ensure that your application still uses MSVCRT version 2.0 even after service packs are applied to the server.</span></span> <span data-ttu-id="b1488-242">Cualquier versión nueva de MSVCRT todavía está instalada en el equipo, pero la versión 2,0 permanece y se usa en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-242">Any new version of MSVCRT is still installed on the computer, but version 2.0 remains and is used by your application.</span></span> <span data-ttu-id="b1488-243">Los archivos DLL compatibles con SxS se almacenan en% WINDIR% \\ WinSxS.</span><span class="sxs-lookup"><span data-stu-id="b1488-243">SxS-supported DLLs are stored in %WINDIR%\\WinSxS.</span></span> |
| <span data-ttu-id="b1488-244">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-244">Access</span></span>         | <span data-ttu-id="b1488-245">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-245">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b1488-246">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-246">Type</span></span>           | <span data-ttu-id="b1488-247">String</span><span class="sxs-lookup"><span data-stu-id="b1488-247">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b1488-248">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-248">Default</span></span>        | <span data-ttu-id="b1488-249">""</span><span class="sxs-lookup"><span data-stu-id="b1488-249">""</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b1488-250">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-250">Minimum system</span></span> | <span data-ttu-id="b1488-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-251">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="b1488-252">Solo se puede usar una versión de un archivo DLL del sistema en cualquier grupo de aplicaciones, aunque esta característica se pueda configurar en el nivel de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-252">Only one version of a system DLL can be used in any application pool, even though this feature is configurable at the application level.</span></span> <span data-ttu-id="b1488-253">Por ejemplo, si la aplicación app1 usa MSVCRT, la versión 2,5 y la aplicación App2 usa MSVCRT, versión 2,4, app1 y App2 no deben estar en el mismo grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b1488-253">For example, if application App1 uses MSVCRT, version 2.5 and application App2 uses MSVCRT, version 2.4, then App1 and App2 should not be in the same application pool.</span></span> <span data-ttu-id="b1488-254">Si es así, la aplicación que se carga primero tiene la versión de MSVCRT cargada y la otra aplicación se ve obligada a usarla hasta que se descarguen las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b1488-254">If they are, the application that is loaded first has its version of MSVCRT loaded, and the other application is forced to use it until the applications are unloaded.</span></span>

 

<span data-ttu-id="b1488-255">Para obtener más información, vea la sección sobre los ensamblados en paralelo en [cambios en los servicios com+ en IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="b1488-255">For more information, see "Side-by-Side Assemblies" in [Changes in COM+ Services in IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span></span>

### <a name="applicationproxy"></a><span data-ttu-id="b1488-256">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="b1488-256">ApplicationProxy</span></span>



| <span data-ttu-id="b1488-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-257">Entry</span></span> | <span data-ttu-id="b1488-258">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-258">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="b1488-259">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-259">Description</span></span>    | <span data-ttu-id="b1488-260">Indica si la aplicación es un proxy de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-260">Indicates whether the application is an application proxy.</span></span> |
| <span data-ttu-id="b1488-261">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-261">Access</span></span>         | <span data-ttu-id="b1488-262">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1488-262">ReadOnly</span></span>                                                   |
| <span data-ttu-id="b1488-263">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-263">Type</span></span>           | <span data-ttu-id="b1488-264">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-264">Bool</span></span>                                                       |
| <span data-ttu-id="b1488-265">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-265">Default</span></span>        | <span data-ttu-id="b1488-266">False</span><span class="sxs-lookup"><span data-stu-id="b1488-266">False</span></span>                                                      |
| <span data-ttu-id="b1488-267">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-267">Minimum system</span></span> | <span data-ttu-id="b1488-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-268">Windows 2000</span></span>                                               |



 

### <a name="applicationproxyservername"></a><span data-ttu-id="b1488-269">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="b1488-269">ApplicationProxyServerName</span></span>



| <span data-ttu-id="b1488-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-270">Entry</span></span> | <span data-ttu-id="b1488-271">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-271">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-272">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-272">Description</span></span>    | <span data-ttu-id="b1488-273">Un nombre de servidor remoto que se usa al exportar el proxy de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-273">A remote server name used when exporting the application proxy.</span></span> <span data-ttu-id="b1488-274">Es este nombre de servidor al que apunta el proxy de aplicación cuando se instala en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="b1488-274">It is this server name that the application proxy points to when it is installed on a client computer.</span></span> |
| <span data-ttu-id="b1488-275">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-275">Access</span></span>         | <span data-ttu-id="b1488-276">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-276">ReadWrite</span></span>                                                                                                                                                              |
| <span data-ttu-id="b1488-277">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-277">Type</span></span>           | <span data-ttu-id="b1488-278">String</span><span class="sxs-lookup"><span data-stu-id="b1488-278">String</span></span>                                                                                                                                                                 |
| <span data-ttu-id="b1488-279">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-279">Default</span></span>        | <span data-ttu-id="b1488-280">""</span><span class="sxs-lookup"><span data-stu-id="b1488-280">""</span></span>                                                                                                                                                                     |
| <span data-ttu-id="b1488-281">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-281">Minimum system</span></span> | <span data-ttu-id="b1488-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-282">Windows 2000</span></span>                                                                                                                                                           |



 

### <a name="apppartitionid"></a><span data-ttu-id="b1488-283">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="b1488-283">AppPartitionID</span></span>



| <span data-ttu-id="b1488-284">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-284">Entry</span></span> | <span data-ttu-id="b1488-285">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-285">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="b1488-286">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-286">Description</span></span>    | <span data-ttu-id="b1488-287">Un GUID que representa el identificador de la partición de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-287">A GUID representing the application partition ID.</span></span> |
| <span data-ttu-id="b1488-288">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-288">Access</span></span>         | <span data-ttu-id="b1488-289">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1488-289">ReadOnly</span></span>                                          |
| <span data-ttu-id="b1488-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-290">Type</span></span>           | <span data-ttu-id="b1488-291">String</span><span class="sxs-lookup"><span data-stu-id="b1488-291">String</span></span>                                            |
| <span data-ttu-id="b1488-292">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-292">Default</span></span>        | <Generated>                                 |
| <span data-ttu-id="b1488-293">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-293">Minimum system</span></span> | <span data-ttu-id="b1488-294">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1488-294">Windows Server 2003</span></span>                               |



 

### <a name="authentication"></a><span data-ttu-id="b1488-295">Autenticación</span><span class="sxs-lookup"><span data-stu-id="b1488-295">Authentication</span></span>



| <span data-ttu-id="b1488-296">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-296">Entry</span></span> | <span data-ttu-id="b1488-297">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-297">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-298">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-298">Description</span></span>    | <span data-ttu-id="b1488-299">Establece el nivel de autenticación de las llamadas, con los valores correspondientes a la configuración de autenticación de llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="b1488-299">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="b1488-300">Cuando se elige COMAdminAuthenticationDefault, se usa el valor de la propiedad DefaultAuthenticationLevel de la colección [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="b1488-300">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="b1488-301">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-301">Access</span></span>         | <span data-ttu-id="b1488-302">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-302">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b1488-303">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-303">Type</span></span>           | <span data-ttu-id="b1488-304">Valores posibles largos: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="b1488-304">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="b1488-305">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-305">Default</span></span>        | <span data-ttu-id="b1488-306">COMAdminAuthenticationPacket (4)</span><span class="sxs-lookup"><span data-stu-id="b1488-306">COMAdminAuthenticationPacket (4)</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b1488-307">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-307">Minimum system</span></span> | <span data-ttu-id="b1488-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-308">Windows 2000</span></span>                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> <span data-ttu-id="b1488-309">En el caso de las aplicaciones de biblioteca (en proceso), los únicos valores válidos aquí son COMAdminAuthenticationDefault y COMAdminAuthenticationNone.</span><span class="sxs-lookup"><span data-stu-id="b1488-309">For library (in-process) applications, the only valid settings here are COMAdminAuthenticationDefault and COMAdminAuthenticationNone .</span></span> <span data-ttu-id="b1488-310">Se recomienda usar las constantes en la enumeración y no los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="b1488-310">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="authenticationcapability"></a><span data-ttu-id="b1488-311">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="b1488-311">AuthenticationCapability</span></span>



| <span data-ttu-id="b1488-312">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-312">Entry</span></span> | <span data-ttu-id="b1488-313">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-313">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-314">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-314">Description</span></span>    | <span data-ttu-id="b1488-315">Determina qué identidad se presenta cuando se suplantan las llamadas.</span><span class="sxs-lookup"><span data-stu-id="b1488-315">Determines what identity is presented when calls are impersonated.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="b1488-316">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-316">Access</span></span>         | <span data-ttu-id="b1488-317">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-317">ReadWrite</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="b1488-318">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-318">Type</span></span>           | <span data-ttu-id="b1488-319">Valores posibles largos: COMAdminAuthenticationCapabilitiesNone (0X0) COMAdminAuthenticationCapabilitiesSecureReference (0X2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="b1488-319">Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span> |
| <span data-ttu-id="b1488-320">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-320">Default</span></span>        | <span data-ttu-id="b1488-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="b1488-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span>                                                                                                                                                                                |
| <span data-ttu-id="b1488-322">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-322">Minimum system</span></span> | <span data-ttu-id="b1488-323">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-323">Windows 2000</span></span>                                                                                                                                                                                                                            |



 

### <a name="changeable"></a><span data-ttu-id="b1488-324">Sustituir</span><span class="sxs-lookup"><span data-stu-id="b1488-324">Changeable</span></span>



| <span data-ttu-id="b1488-325">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-325">Entry</span></span> | <span data-ttu-id="b1488-326">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-326">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-327">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-327">Description</span></span>    | <span data-ttu-id="b1488-328">Determina si los cambios en la configuración de la aplicación o en sus componentes están permitidos, ya sea mediante programación o a través de la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="b1488-328">Determines whether changes to the application settings or those of its components are allowed, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="b1488-329">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-329">Access</span></span>         | <span data-ttu-id="b1488-330">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-330">ReadWrite</span></span>                                                                                                                                                                     |
| <span data-ttu-id="b1488-331">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-331">Type</span></span>           | <span data-ttu-id="b1488-332">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-332">Bool</span></span>                                                                                                                                                                          |
| <span data-ttu-id="b1488-333">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-333">Default</span></span>        | <span data-ttu-id="b1488-334">True</span><span class="sxs-lookup"><span data-stu-id="b1488-334">True</span></span>                                                                                                                                                                          |
| <span data-ttu-id="b1488-335">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-335">Minimum system</span></span> | <span data-ttu-id="b1488-336">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-336">Windows 2000</span></span>                                                                                                                                                                  |



 

### <a name="commandline"></a><span data-ttu-id="b1488-337">CommandLine</span><span class="sxs-lookup"><span data-stu-id="b1488-337">CommandLine</span></span>



| <span data-ttu-id="b1488-338">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-338">Entry</span></span> | <span data-ttu-id="b1488-339">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-339">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-340">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-340">Description</span></span>    | <span data-ttu-id="b1488-341">Cadena de línea de comandos que se va a usar en la depuración.</span><span class="sxs-lookup"><span data-stu-id="b1488-341">A command-line string for use in debugging.</span></span> <span data-ttu-id="b1488-342">La aplicación puede iniciarse en un depurador con la línea de comandos especificada.</span><span class="sxs-lookup"><span data-stu-id="b1488-342">The application can be launched in a debugger with the specified command line.</span></span> |
| <span data-ttu-id="b1488-343">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-343">Access</span></span>         | <span data-ttu-id="b1488-344">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-344">ReadWrite</span></span>                                                                                                                  |
| <span data-ttu-id="b1488-345">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-345">Type</span></span>           | <span data-ttu-id="b1488-346">String</span><span class="sxs-lookup"><span data-stu-id="b1488-346">String</span></span>                                                                                                                     |
| <span data-ttu-id="b1488-347">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-347">Default</span></span>        | <span data-ttu-id="b1488-348">""</span><span class="sxs-lookup"><span data-stu-id="b1488-348">""</span></span>                                                                                                                         |
| <span data-ttu-id="b1488-349">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-349">Minimum system</span></span> | <span data-ttu-id="b1488-350">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-350">Windows 2000</span></span>                                                                                                               |



 

### <a name="concurrentapps"></a><span data-ttu-id="b1488-351">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="b1488-351">ConcurrentApps</span></span>



| <span data-ttu-id="b1488-352">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-352">Entry</span></span> | <span data-ttu-id="b1488-353">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-353">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-354">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-354">Description</span></span>    | <span data-ttu-id="b1488-355">Especifica el número máximo de aplicaciones agrupables que pueden ejecutarse simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="b1488-355">Specifies the maximum number of poolable applications that can run concurrently.</span></span> |
| <span data-ttu-id="b1488-356">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-356">Access</span></span>         | <span data-ttu-id="b1488-357">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-357">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="b1488-358">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-358">Type</span></span>           | <span data-ttu-id="b1488-359">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="b1488-359">Long (1-1048576)</span></span>                                                                 |
| <span data-ttu-id="b1488-360">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-360">Default</span></span>        | <span data-ttu-id="b1488-361">1</span><span class="sxs-lookup"><span data-stu-id="b1488-361">1</span></span>                                                                                |
| <span data-ttu-id="b1488-362">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-362">Minimum system</span></span> | <span data-ttu-id="b1488-363">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-363">Windows XP</span></span>                                                                       |



 

### <a name="createdby"></a><span data-ttu-id="b1488-364">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="b1488-364">CreatedBy</span></span>



| <span data-ttu-id="b1488-365">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-365">Entry</span></span> | <span data-ttu-id="b1488-366">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-366">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="b1488-367">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-367">Description</span></span>    | <span data-ttu-id="b1488-368">Cadena informativa para describir quién creó la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-368">Informational string to describe who created the application.</span></span> |
| <span data-ttu-id="b1488-369">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-369">Access</span></span>         | <span data-ttu-id="b1488-370">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-370">ReadWrite</span></span>                                                     |
| <span data-ttu-id="b1488-371">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-371">Type</span></span>           | <span data-ttu-id="b1488-372">String</span><span class="sxs-lookup"><span data-stu-id="b1488-372">String</span></span>                                                        |
| <span data-ttu-id="b1488-373">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-373">Default</span></span>        | <span data-ttu-id="b1488-374">""</span><span class="sxs-lookup"><span data-stu-id="b1488-374">""</span></span>                                                            |
| <span data-ttu-id="b1488-375">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-375">Minimum system</span></span> | <span data-ttu-id="b1488-376">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-376">Windows 2000</span></span>                                                  |



 

### <a name="crmenabled"></a><span data-ttu-id="b1488-377">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-377">CRMEnabled</span></span>



| <span data-ttu-id="b1488-378">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-378">Entry</span></span> | <span data-ttu-id="b1488-379">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-379">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="b1488-380">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-380">Description</span></span>    | <span data-ttu-id="b1488-381">Determina si está habilitado el Administrador de recursos de compensación.</span><span class="sxs-lookup"><span data-stu-id="b1488-381">Determines whether the Compensating Resource Manager is enabled.</span></span> |
| <span data-ttu-id="b1488-382">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-382">Access</span></span>         | <span data-ttu-id="b1488-383">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-383">ReadWrite</span></span>                                                        |
| <span data-ttu-id="b1488-384">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-384">Type</span></span>           | <span data-ttu-id="b1488-385">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-385">Bool</span></span>                                                             |
| <span data-ttu-id="b1488-386">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-386">Default</span></span>        | <span data-ttu-id="b1488-387">False</span><span class="sxs-lookup"><span data-stu-id="b1488-387">False</span></span>                                                            |
| <span data-ttu-id="b1488-388">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-388">Minimum system</span></span> | <span data-ttu-id="b1488-389">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-389">Windows 2000</span></span>                                                     |



 

### <a name="crmlogfile"></a><span data-ttu-id="b1488-390">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="b1488-390">CRMLogFile</span></span>



| <span data-ttu-id="b1488-391">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-391">Entry</span></span> | <span data-ttu-id="b1488-392">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-392">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-393">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-393">Description</span></span>    | <span data-ttu-id="b1488-394">Nombre y ruta de acceso del archivo para mantener el registro para el administrador de compensación de recursos (CRM).</span><span class="sxs-lookup"><span data-stu-id="b1488-394">Name and path of file for keeping the log for the compensating resource manager (CRM).</span></span> |
| <span data-ttu-id="b1488-395">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-395">Access</span></span>         | <span data-ttu-id="b1488-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-396">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="b1488-397">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-397">Type</span></span>           | <span data-ttu-id="b1488-398">String</span><span class="sxs-lookup"><span data-stu-id="b1488-398">String</span></span>                                                                                 |
| <span data-ttu-id="b1488-399">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-399">Default</span></span>        | <span data-ttu-id="b1488-400">""</span><span class="sxs-lookup"><span data-stu-id="b1488-400">""</span></span>                                                                                     |
| <span data-ttu-id="b1488-401">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-401">Minimum system</span></span> | <span data-ttu-id="b1488-402">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-402">Windows 2000</span></span>                                                                           |



 

### <a name="deleteable"></a><span data-ttu-id="b1488-403">Eliminable</span><span class="sxs-lookup"><span data-stu-id="b1488-403">Deleteable</span></span>



| <span data-ttu-id="b1488-404">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-404">Entry</span></span> | <span data-ttu-id="b1488-405">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-405">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-406">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-406">Description</span></span>    | <span data-ttu-id="b1488-407">Establece si se puede eliminar la aplicación, ya sea mediante programación o a través de la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="b1488-407">Sets whether the application can be deleted, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="b1488-408">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-408">Access</span></span>         | <span data-ttu-id="b1488-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-409">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="b1488-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-410">Type</span></span>           | <span data-ttu-id="b1488-411">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-411">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="b1488-412">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-412">Default</span></span>        | <span data-ttu-id="b1488-413">True</span><span class="sxs-lookup"><span data-stu-id="b1488-413">True</span></span>                                                                                                                        |
| <span data-ttu-id="b1488-414">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-414">Minimum system</span></span> | <span data-ttu-id="b1488-415">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-415">Windows 2000</span></span>                                                                                                                |



 

### <a name="description"></a><span data-ttu-id="b1488-416">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-416">Description</span></span>



| <span data-ttu-id="b1488-417">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-417">Entry</span></span> | <span data-ttu-id="b1488-418">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-418">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="b1488-419">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-419">Description</span></span>    | <span data-ttu-id="b1488-420">Describe la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-420">Describes the application.</span></span> |
| <span data-ttu-id="b1488-421">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-421">Access</span></span>         | <span data-ttu-id="b1488-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-422">ReadWrite</span></span>                  |
| <span data-ttu-id="b1488-423">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-423">Type</span></span>           | <span data-ttu-id="b1488-424">String</span><span class="sxs-lookup"><span data-stu-id="b1488-424">String</span></span>                     |
| <span data-ttu-id="b1488-425">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-425">Default</span></span>        | <span data-ttu-id="b1488-426">""</span><span class="sxs-lookup"><span data-stu-id="b1488-426">""</span></span>                         |
| <span data-ttu-id="b1488-427">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-427">Minimum system</span></span> | <span data-ttu-id="b1488-428">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-428">Windows 2000</span></span>               |



 

### <a name="dumpenabled"></a><span data-ttu-id="b1488-429">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-429">DumpEnabled</span></span>



| <span data-ttu-id="b1488-430">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-430">Entry</span></span> | <span data-ttu-id="b1488-431">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-431">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-432">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-432">Description</span></span>    | <span data-ttu-id="b1488-433">Habilita el volcado del estado de una aplicación COM+ en el momento en que se produjo un error en un directorio designado.</span><span class="sxs-lookup"><span data-stu-id="b1488-433">Enables the dump of the state of a COM+ application at the time of failure to a designated directory.</span></span> |
| <span data-ttu-id="b1488-434">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-434">Access</span></span>         | <span data-ttu-id="b1488-435">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-435">ReadWrite</span></span>                                                                                             |
| <span data-ttu-id="b1488-436">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-436">Type</span></span>           | <span data-ttu-id="b1488-437">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-437">Bool</span></span>                                                                                                  |
| <span data-ttu-id="b1488-438">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-438">Default</span></span>        | <span data-ttu-id="b1488-439">False</span><span class="sxs-lookup"><span data-stu-id="b1488-439">False</span></span>                                                                                                 |
| <span data-ttu-id="b1488-440">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-440">Minimum system</span></span> | <span data-ttu-id="b1488-441">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-441">Windows XP</span></span>                                                                                            |



 

> [!Note]  
> <span data-ttu-id="b1488-442">A partir de Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los archivos de volcado de memoria de COM+.</span><span class="sxs-lookup"><span data-stu-id="b1488-442">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="dumponexception"></a><span data-ttu-id="b1488-443">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="b1488-443">DumpOnException</span></span>



| <span data-ttu-id="b1488-444">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-444">Entry</span></span> | <span data-ttu-id="b1488-445">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-445">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-446">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-446">Description</span></span>    | <span data-ttu-id="b1488-447">Habilita el volcado del estado de una aplicación COM+ cuando la aplicación produce una excepción no controlada y finaliza con el tiempo de ejecución de COM+.</span><span class="sxs-lookup"><span data-stu-id="b1488-447">Enables the dump of the state of a COM+ application when the application causes an unhandled exception and is terminated by the COM+ runtime.</span></span> |
| <span data-ttu-id="b1488-448">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-448">Access</span></span>         | <span data-ttu-id="b1488-449">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-449">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="b1488-450">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-450">Type</span></span>           | <span data-ttu-id="b1488-451">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-451">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="b1488-452">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-452">Default</span></span>        | <span data-ttu-id="b1488-453">False</span><span class="sxs-lookup"><span data-stu-id="b1488-453">False</span></span>                                                                                                                                         |
| <span data-ttu-id="b1488-454">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-454">Minimum system</span></span> | <span data-ttu-id="b1488-455">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-455">Windows XP</span></span>                                                                                                                                    |



 

### <a name="dumponfailfast"></a><span data-ttu-id="b1488-456">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="b1488-456">DumpOnFailfast</span></span>



| <span data-ttu-id="b1488-457">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-457">Entry</span></span> | <span data-ttu-id="b1488-458">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-458">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-459">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-459">Description</span></span>    | <span data-ttu-id="b1488-460">Habilita el volcado del estado de una aplicación COM+ cuando se produce un error en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-460">Enables the dump of the state of a COM+ application when the application fails.</span></span> |
| <span data-ttu-id="b1488-461">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-461">Access</span></span>         | <span data-ttu-id="b1488-462">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-462">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="b1488-463">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-463">Type</span></span>           | <span data-ttu-id="b1488-464">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-464">Bool</span></span>                                                                            |
| <span data-ttu-id="b1488-465">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-465">Default</span></span>        | <span data-ttu-id="b1488-466">False</span><span class="sxs-lookup"><span data-stu-id="b1488-466">False</span></span>                                                                           |
| <span data-ttu-id="b1488-467">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-467">Minimum system</span></span> | <span data-ttu-id="b1488-468">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-468">Windows XP</span></span>                                                                      |



 

### <a name="dumppath"></a><span data-ttu-id="b1488-469">DumpPath</span><span class="sxs-lookup"><span data-stu-id="b1488-469">DumpPath</span></span>



| <span data-ttu-id="b1488-470">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-470">Entry</span></span> | <span data-ttu-id="b1488-471">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-471">Value</span></span> |
|----------------|--------------------------------------------------------------|
| <span data-ttu-id="b1488-472">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-472">Description</span></span>    | <span data-ttu-id="b1488-473">La ruta de acceso del directorio en el que se guardan los archivos de volcado.</span><span class="sxs-lookup"><span data-stu-id="b1488-473">The path of the directory in which the dump files are saved.</span></span> |
| <span data-ttu-id="b1488-474">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-474">Access</span></span>         | <span data-ttu-id="b1488-475">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-475">ReadWrite</span></span>                                                    |
| <span data-ttu-id="b1488-476">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-476">Type</span></span>           | <span data-ttu-id="b1488-477">String</span><span class="sxs-lookup"><span data-stu-id="b1488-477">String</span></span>                                                       |
| <span data-ttu-id="b1488-478">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-478">Default</span></span>        | <span data-ttu-id="b1488-479">"% SystemRoot% \\ system32 \\ com \\ DMP"</span><span class="sxs-lookup"><span data-stu-id="b1488-479">"%systemroot%\\system32\\com\\dmp"</span></span>                           |
| <span data-ttu-id="b1488-480">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-480">Minimum system</span></span> | <span data-ttu-id="b1488-481">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-481">Windows XP</span></span>                                                   |



 

> [!Note]  
> <span data-ttu-id="b1488-482">A partir de Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los archivos de volcado de memoria de COM+.</span><span class="sxs-lookup"><span data-stu-id="b1488-482">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="eventsenabled"></a><span data-ttu-id="b1488-483">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-483">EventsEnabled</span></span>



| <span data-ttu-id="b1488-484">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-484">Entry</span></span> | <span data-ttu-id="b1488-485">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-485">Value</span></span> |
|----------------|-----------------------------------------------------------|
| <span data-ttu-id="b1488-486">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-486">Description</span></span>    | <span data-ttu-id="b1488-487">Indica si los eventos están habilitados para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-487">Indicates whether events are enabled for the application.</span></span> |
| <span data-ttu-id="b1488-488">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-488">Access</span></span>         | <span data-ttu-id="b1488-489">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-489">ReadWrite</span></span>                                                 |
| <span data-ttu-id="b1488-490">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-490">Type</span></span>           | <span data-ttu-id="b1488-491">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-491">Bool</span></span>                                                      |
| <span data-ttu-id="b1488-492">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-492">Default</span></span>        | <span data-ttu-id="b1488-493">True</span><span class="sxs-lookup"><span data-stu-id="b1488-493">True</span></span>                                                      |
| <span data-ttu-id="b1488-494">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-494">Minimum system</span></span> | <span data-ttu-id="b1488-495">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-495">Windows 2000</span></span>                                              |



 

### <a name="id"></a><span data-ttu-id="b1488-496">id</span><span class="sxs-lookup"><span data-stu-id="b1488-496">ID</span></span>



| <span data-ttu-id="b1488-497">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-497">Entry</span></span> | <span data-ttu-id="b1488-498">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-498">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-499">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-499">Description</span></span>    | <span data-ttu-id="b1488-500">Un GUID que representa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-500">A GUID representing the application.</span></span> <span data-ttu-id="b1488-501">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="b1488-501">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b1488-502">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-502">Access</span></span>         | <span data-ttu-id="b1488-503">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b1488-503">WriteOnce</span></span>                                                                                                                                                            |
| <span data-ttu-id="b1488-504">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-504">Type</span></span>           | <span data-ttu-id="b1488-505">String</span><span class="sxs-lookup"><span data-stu-id="b1488-505">String</span></span>                                                                                                                                                               |
| <span data-ttu-id="b1488-506">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-506">Default</span></span>        | <Generated>                                                                                                                                                    |
| <span data-ttu-id="b1488-507">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-507">Minimum system</span></span> | <span data-ttu-id="b1488-508">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-508">Windows 2000</span></span>                                                                                                                                                         |



 

### <a name="identity"></a><span data-ttu-id="b1488-509">Identidad</span><span class="sxs-lookup"><span data-stu-id="b1488-509">Identity</span></span>



| <span data-ttu-id="b1488-510">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-510">Entry</span></span> | <span data-ttu-id="b1488-511">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-511">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-512">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-512">Description</span></span>    | <span data-ttu-id="b1488-513">Establece la identidad de proceso de servidor para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-513">Sets the server process identity for the application.</span></span> <span data-ttu-id="b1488-514">Especifique una cuenta de usuario válida o un "usuario interactivo" para que la aplicación asuma la identidad del usuario que ha iniciado la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="b1488-514">Specify a valid user account or "Interactive User" to have the application assume the identity of the current logged-on user.</span></span> <span data-ttu-id="b1488-515">También puede especificar las cadenas ' NT Authority \\ LocalService ', ' NT Authority \\ NetworkService ' y ' NT Authority \\ System '.</span><span class="sxs-lookup"><span data-stu-id="b1488-515">You can also specify the strings "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system".</span></span> <span data-ttu-id="b1488-516">La contraseña predeterminada para estas tres cuentas es "" (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="b1488-516">The default password for these three accounts is "" (empty string).</span></span> |
| <span data-ttu-id="b1488-517">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-517">Access</span></span>         |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b1488-518">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-518">Type</span></span>           |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b1488-519">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-519">Default</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b1488-520">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-520">Minimum system</span></span> | <span data-ttu-id="b1488-521">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-521">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="b1488-522">La propiedad de identidad no está habilitada para las aplicaciones de biblioteca, que se ejecutan en el proceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="b1488-522">The Identity property is not enabled for library applications, which run in the client process.</span></span>

<span data-ttu-id="b1488-523">La propiedad de contraseña debe establecerse al mismo tiempo que la identidad, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse.</span><span class="sxs-lookup"><span data-stu-id="b1488-523">The Password property should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="b1488-524">Si la contraseña y la identidad no se sincronizan, la aplicación no se puede iniciar hasta que un administrador la restablezca.</span><span class="sxs-lookup"><span data-stu-id="b1488-524">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="impersonationlevel"></a><span data-ttu-id="b1488-525">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="b1488-525">ImpersonationLevel</span></span>



| <span data-ttu-id="b1488-526">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-526">Entry</span></span> | <span data-ttu-id="b1488-527">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-527">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-528">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-528">Description</span></span>    | <span data-ttu-id="b1488-529">Establece el nivel de suplantación usado para las llamadas realizadas a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b1488-529">Sets impersonation level used for calls made to other applications.</span></span>                                                                                           |
| <span data-ttu-id="b1488-530">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-530">Access</span></span>         | <span data-ttu-id="b1488-531">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-531">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="b1488-532">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-532">Type</span></span>           | <span data-ttu-id="b1488-533">Valores posibles largos: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="b1488-533">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="b1488-534">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-534">Default</span></span>        | <span data-ttu-id="b1488-535">COMAdminImpersonationImpersonate (3)</span><span class="sxs-lookup"><span data-stu-id="b1488-535">COMAdminImpersonationImpersonate (3)</span></span>                                                                                                                          |
| <span data-ttu-id="b1488-536">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-536">Minimum system</span></span> | <span data-ttu-id="b1488-537">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-537">Windows 2000</span></span>                                                                                                                                                  |



 

### <a name="isenabled"></a><span data-ttu-id="b1488-538">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-538">IsEnabled</span></span>



| <span data-ttu-id="b1488-539">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-539">Entry</span></span> | <span data-ttu-id="b1488-540">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-540">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-541">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-541">Description</span></span>    | <span data-ttu-id="b1488-542">Si el componente o la aplicación COM+ está deshabilitado, IsEnabled es false.</span><span class="sxs-lookup"><span data-stu-id="b1488-542">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="b1488-543">Si el componente o la aplicación COM+ está habilitado, IsEnabled es true.</span><span class="sxs-lookup"><span data-stu-id="b1488-543">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="b1488-544">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-544">Access</span></span>         | <span data-ttu-id="b1488-545">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-545">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="b1488-546">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-546">Type</span></span>           | <span data-ttu-id="b1488-547">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-547">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="b1488-548">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-548">Default</span></span>        | <span data-ttu-id="b1488-549">True</span><span class="sxs-lookup"><span data-stu-id="b1488-549">True</span></span>                                                                                                                                      |
| <span data-ttu-id="b1488-550">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-550">Minimum system</span></span> | <span data-ttu-id="b1488-551">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-551">Windows XP</span></span>                                                                                                                                |



 

### <a name="issystem"></a><span data-ttu-id="b1488-552">IsSystem</span><span class="sxs-lookup"><span data-stu-id="b1488-552">IsSystem</span></span>



| <span data-ttu-id="b1488-553">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-553">Entry</span></span> | <span data-ttu-id="b1488-554">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-554">Value</span></span> |
|----------------|--------------------------------------|
| <span data-ttu-id="b1488-555">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-555">Description</span></span>    | <span data-ttu-id="b1488-556">Identifica las aplicaciones del sistema COM+.</span><span class="sxs-lookup"><span data-stu-id="b1488-556">Identifies COM+ system applications.</span></span> |
| <span data-ttu-id="b1488-557">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-557">Access</span></span>         | <span data-ttu-id="b1488-558">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1488-558">ReadOnly</span></span>                             |
| <span data-ttu-id="b1488-559">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-559">Type</span></span>           | <span data-ttu-id="b1488-560">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-560">Bool</span></span>                                 |
| <span data-ttu-id="b1488-561">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-561">Default</span></span>        | <span data-ttu-id="b1488-562">False</span><span class="sxs-lookup"><span data-stu-id="b1488-562">False</span></span>                                |
| <span data-ttu-id="b1488-563">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-563">Minimum system</span></span> | <span data-ttu-id="b1488-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-564">Windows 2000</span></span>                         |



 

### <a name="maxdumpcount"></a><span data-ttu-id="b1488-565">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="b1488-565">MaxDumpCount</span></span>



| <span data-ttu-id="b1488-566">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-566">Entry</span></span> | <span data-ttu-id="b1488-567">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-567">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-568">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-568">Description</span></span>    | <span data-ttu-id="b1488-569">Indica el número máximo de archivos que se van a generar antes de que se produzca la sobrescritura.</span><span class="sxs-lookup"><span data-stu-id="b1488-569">Indicates the maximum number of files to be generated before overwriting occurs.</span></span> |
| <span data-ttu-id="b1488-570">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-570">Access</span></span>         | <span data-ttu-id="b1488-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-571">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="b1488-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-572">Type</span></span>           | <span data-ttu-id="b1488-573">Long (1-200)</span><span class="sxs-lookup"><span data-stu-id="b1488-573">Long (1-200)</span></span>                                                                     |
| <span data-ttu-id="b1488-574">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-574">Default</span></span>        | <span data-ttu-id="b1488-575">5</span><span class="sxs-lookup"><span data-stu-id="b1488-575">5</span></span>                                                                                |
| <span data-ttu-id="b1488-576">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-576">Minimum system</span></span> | <span data-ttu-id="b1488-577">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-577">Windows XP</span></span>                                                                       |



 

### <a name="name"></a><span data-ttu-id="b1488-578">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1488-578">Name</span></span>



| <span data-ttu-id="b1488-579">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-579">Entry</span></span> | <span data-ttu-id="b1488-580">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-580">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-581">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-581">Description</span></span>    | <span data-ttu-id="b1488-582">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-582">The name of the application.</span></span> <span data-ttu-id="b1488-583">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="b1488-583">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b1488-584">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-584">Access</span></span>         | <span data-ttu-id="b1488-585">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-585">ReadWrite</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="b1488-586">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-586">Type</span></span>           | <span data-ttu-id="b1488-587">String</span><span class="sxs-lookup"><span data-stu-id="b1488-587">String</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="b1488-588">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-588">Default</span></span>        | <span data-ttu-id="b1488-589">"Nueva aplicación"</span><span class="sxs-lookup"><span data-stu-id="b1488-589">"New Application"</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="b1488-590">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-590">Minimum system</span></span> | <span data-ttu-id="b1488-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-591">Windows 2000</span></span>                                                                                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="b1488-592">Deben elegirse nombres únicos para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b1488-592">Unique names should be chosen for applications.</span></span> <span data-ttu-id="b1488-593">Si se crean varias aplicaciones con el mismo nombre, puede interferir con la referencia de las aplicaciones por nombre, lo que resulta en un comportamiento impredecible.</span><span class="sxs-lookup"><span data-stu-id="b1488-593">If multiple applications are created with the same name, it can interfere with referencing the applications by name, resulting in unpredictable behavior.</span></span>

 

### <a name="password"></a><span data-ttu-id="b1488-594">Contraseña</span><span class="sxs-lookup"><span data-stu-id="b1488-594">Password</span></span>



| <span data-ttu-id="b1488-595">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-595">Entry</span></span> | <span data-ttu-id="b1488-596">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-596">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="b1488-597">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-597">Description</span></span>    | <span data-ttu-id="b1488-598">Establece la contraseña utilizada por el proceso de servidor para iniciar sesión con la identidad.</span><span class="sxs-lookup"><span data-stu-id="b1488-598">Sets the password used by the server process to log on under the identity.</span></span> |
| <span data-ttu-id="b1488-599">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-599">Access</span></span>         | <span data-ttu-id="b1488-600">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="b1488-600">WriteOnly</span></span>                                                                  |
| <span data-ttu-id="b1488-601">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-601">Type</span></span>           | <span data-ttu-id="b1488-602">String</span><span class="sxs-lookup"><span data-stu-id="b1488-602">String</span></span>                                                                     |
| <span data-ttu-id="b1488-603">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-603">Default</span></span>        | <span data-ttu-id="b1488-604">""</span><span class="sxs-lookup"><span data-stu-id="b1488-604">""</span></span>                                                                         |
| <span data-ttu-id="b1488-605">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-605">Minimum system</span></span> | <span data-ttu-id="b1488-606">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-606">Windows 2000</span></span>                                                               |



 

<span data-ttu-id="b1488-607">La contraseña debe establecerse al mismo tiempo que la identidad, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse.</span><span class="sxs-lookup"><span data-stu-id="b1488-607">Password should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="b1488-608">Si la contraseña y la identidad no se sincronizan, la aplicación no se puede iniciar hasta que un administrador la restablezca.</span><span class="sxs-lookup"><span data-stu-id="b1488-608">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="qcauthenticatemsgs"></a><span data-ttu-id="b1488-609">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="b1488-609">QCAuthenticateMsgs</span></span>



| <span data-ttu-id="b1488-610">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-610">Entry</span></span> | <span data-ttu-id="b1488-611">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-611">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-612">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-612">Description</span></span>    | <span data-ttu-id="b1488-613">Indica en qué circunstancias se autentican las solicitudes en cola a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-613">Indicates under what circumstances queued requests to an application are authenticated.</span></span>                                                 |
| <span data-ttu-id="b1488-614">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-614">Access</span></span>         | <span data-ttu-id="b1488-615">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-615">ReadWrite</span></span>                                                                                                                               |
| <span data-ttu-id="b1488-616">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-616">Type</span></span>           | <span data-ttu-id="b1488-617">Valores posibles largos: COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2)</span><span class="sxs-lookup"><span data-stu-id="b1488-617">Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2)</span></span> |
| <span data-ttu-id="b1488-618">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-618">Default</span></span>        | <span data-ttu-id="b1488-619">COMAdminQCMessageAuthenticateSecureApps (0)</span><span class="sxs-lookup"><span data-stu-id="b1488-619">COMAdminQCMessageAuthenticateSecureApps (0)</span></span>                                                                                             |
| <span data-ttu-id="b1488-620">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-620">Minimum system</span></span> | <span data-ttu-id="b1488-621">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-621">Windows XP</span></span>                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a><span data-ttu-id="b1488-622">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="b1488-622">QCListenerMaxThreads</span></span>



| <span data-ttu-id="b1488-623">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-623">Entry</span></span> | <span data-ttu-id="b1488-624">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-624">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-625">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-625">Description</span></span>    | <span data-ttu-id="b1488-626">Indica el número máximo de subprocesos de agente de escucha simultáneos.</span><span class="sxs-lookup"><span data-stu-id="b1488-626">Indicates the maximum number of concurrent listener threads.</span></span> <span data-ttu-id="b1488-627">El intervalo válido para esta propiedad es de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="b1488-627">The valid range for this property is 0 to 1000.</span></span> <span data-ttu-id="b1488-628">En el caso de una aplicación recién creada, el valor se deriva del algoritmo que se usa actualmente para determinar el número predeterminado de subprocesos del agente de escucha: 16 veces el número de CPU del servidor.</span><span class="sxs-lookup"><span data-stu-id="b1488-628">For a newly created application, the setting is derived from the algorithm currently used for determining the default number of listener threads: 16 times the number of CPUs in the server.</span></span> |
| <span data-ttu-id="b1488-629">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-629">Access</span></span>         | <span data-ttu-id="b1488-630">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-630">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b1488-631">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-631">Type</span></span>           | <span data-ttu-id="b1488-632">Long (0-1000)</span><span class="sxs-lookup"><span data-stu-id="b1488-632">Long (0-1000)</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b1488-633">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-633">Default</span></span>        | <span data-ttu-id="b1488-634">0</span><span class="sxs-lookup"><span data-stu-id="b1488-634">0</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b1488-635">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-635">Minimum system</span></span> | <span data-ttu-id="b1488-636">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-636">Windows XP</span></span>                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="b1488-637">Esta propiedad también está disponible con la capacidad de lectura y escritura de la pestaña **puesta en cola** de la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="b1488-637">This property is also available with read/write capability from the **Queuing** tab of the Component Services administrative tool.</span></span>

 

### <a name="queuelistenerenabled"></a><span data-ttu-id="b1488-638">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-638">QueueListenerEnabled</span></span>



| <span data-ttu-id="b1488-639">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-639">Entry</span></span> | <span data-ttu-id="b1488-640">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-640">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-641">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-641">Description</span></span>    | <span data-ttu-id="b1488-642">Indica si el agente de escucha de componentes en cola está habilitado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-642">Indicates whether the queued components listener is enabled for the application.</span></span> <span data-ttu-id="b1488-643">Si está habilitada, el agente de escucha se inicia cuando se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-643">If enabled, the listener is launched when the application starts.</span></span> <span data-ttu-id="b1488-644">Esta propiedad solo surte efecto si QueuingEnabled está establecido en true.</span><span class="sxs-lookup"><span data-stu-id="b1488-644">This property takes effect only if QueuingEnabled is set to True.</span></span> |
| <span data-ttu-id="b1488-645">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-645">Access</span></span>         | <span data-ttu-id="b1488-646">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-646">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="b1488-647">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-647">Type</span></span>           | <span data-ttu-id="b1488-648">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-648">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="b1488-649">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-649">Default</span></span>        | <span data-ttu-id="b1488-650">False</span><span class="sxs-lookup"><span data-stu-id="b1488-650">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="b1488-651">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-651">Minimum system</span></span> | <span data-ttu-id="b1488-652">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-652">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a><span data-ttu-id="b1488-653">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-653">QueuingEnabled</span></span>



| <span data-ttu-id="b1488-654">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-654">Entry</span></span> | <span data-ttu-id="b1488-655">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-655">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-656">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-656">Description</span></span>    | <span data-ttu-id="b1488-657">Indica si el servicio de componentes en cola COM+ está habilitado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-657">Indicates whether the COM+ Queued Components service is enabled for the application.</span></span> |
| <span data-ttu-id="b1488-658">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-658">Access</span></span>         | <span data-ttu-id="b1488-659">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-659">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="b1488-660">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-660">Type</span></span>           | <span data-ttu-id="b1488-661">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-661">Bool</span></span>                                                                                 |
| <span data-ttu-id="b1488-662">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-662">Default</span></span>        | <span data-ttu-id="b1488-663">False</span><span class="sxs-lookup"><span data-stu-id="b1488-663">False</span></span>                                                                                |
| <span data-ttu-id="b1488-664">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-664">Minimum system</span></span> | <span data-ttu-id="b1488-665">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-665">Windows 2000</span></span>                                                                         |



 

### <a name="recycleactivationlimit"></a><span data-ttu-id="b1488-666">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-666">RecycleActivationLimit</span></span>



| <span data-ttu-id="b1488-667">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-667">Entry</span></span> | <span data-ttu-id="b1488-668">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-668">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-669">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-669">Description</span></span>    | <span data-ttu-id="b1488-670">Indica el número máximo de activaciones de los objetos configurados en la aplicación que se aceptan antes de reciclar el proceso.</span><span class="sxs-lookup"><span data-stu-id="b1488-670">Indicates the maximum number of activations of configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="b1488-671">El número predeterminado de activaciones es 0.</span><span class="sxs-lookup"><span data-stu-id="b1488-671">The default number of activations is 0.</span></span> |
| <span data-ttu-id="b1488-672">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-672">Access</span></span>         | <span data-ttu-id="b1488-673">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-673">ReadWrite</span></span>                                                                                                                                                            |
| <span data-ttu-id="b1488-674">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-674">Type</span></span>           | <span data-ttu-id="b1488-675">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="b1488-675">Long (0-1048576)</span></span>                                                                                                                                                     |
| <span data-ttu-id="b1488-676">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-676">Default</span></span>        | <span data-ttu-id="b1488-677">0</span><span class="sxs-lookup"><span data-stu-id="b1488-677">0</span></span>                                                                                                                                                                    |
| <span data-ttu-id="b1488-678">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-678">Minimum system</span></span> | <span data-ttu-id="b1488-679">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-679">Windows XP</span></span>                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a><span data-ttu-id="b1488-680">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-680">RecycleCallLimit</span></span>



| <span data-ttu-id="b1488-681">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-681">Entry</span></span> | <span data-ttu-id="b1488-682">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-682">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-683">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-683">Description</span></span>    | <span data-ttu-id="b1488-684">Indica el número máximo de llamadas para permitir que los objetos configurados en la aplicación acepten antes de reciclar el proceso.</span><span class="sxs-lookup"><span data-stu-id="b1488-684">Indicates the maximum number of calls to allow configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="b1488-685">El número predeterminado de llamadas es 0.</span><span class="sxs-lookup"><span data-stu-id="b1488-685">The default number of calls is 0.</span></span> |
| <span data-ttu-id="b1488-686">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-686">Access</span></span>         | <span data-ttu-id="b1488-687">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-687">ReadWrite</span></span>                                                                                                                                                      |
| <span data-ttu-id="b1488-688">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-688">Type</span></span>           | <span data-ttu-id="b1488-689">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="b1488-689">Long (0-1048576)</span></span>                                                                                                                                               |
| <span data-ttu-id="b1488-690">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-690">Default</span></span>        | <span data-ttu-id="b1488-691">0</span><span class="sxs-lookup"><span data-stu-id="b1488-691">0</span></span>                                                                                                                                                              |
| <span data-ttu-id="b1488-692">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-692">Minimum system</span></span> | <span data-ttu-id="b1488-693">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-693">Windows XP</span></span>                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a><span data-ttu-id="b1488-694">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="b1488-694">RecycleExpirationTimeout</span></span>



| <span data-ttu-id="b1488-695">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-695">Entry</span></span> | <span data-ttu-id="b1488-696">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-696">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-697">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-697">Description</span></span>    | <span data-ttu-id="b1488-698">Indica la cantidad de tiempo (en minutos) que se permite la ejecución de un proceso reciclado antes de cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="b1488-698">Indicates the amount of time (in minutes) to allow a recycled process to run before shutting it down.</span></span> <span data-ttu-id="b1488-699">La cuenta atrás comienza inmediatamente después de que se recicle el proceso.</span><span class="sxs-lookup"><span data-stu-id="b1488-699">The countdown begins immediately after the process is recycled.</span></span> <span data-ttu-id="b1488-700">El tiempo de espera de expiración máximo es de 1440 minutos (24 horas) y el valor predeterminado es 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="b1488-700">The maximum expiration time-out is 1440 minutes (24 hours), and the default is 15 minutes.</span></span> |
| <span data-ttu-id="b1488-701">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-701">Access</span></span>         | <span data-ttu-id="b1488-702">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-702">ReadWrite</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b1488-703">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-703">Type</span></span>           | <span data-ttu-id="b1488-704">Long (1-1440)</span><span class="sxs-lookup"><span data-stu-id="b1488-704">Long (1-1440)</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b1488-705">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-705">Default</span></span>        | <span data-ttu-id="b1488-706">15</span><span class="sxs-lookup"><span data-stu-id="b1488-706">15</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b1488-707">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-707">Minimum system</span></span> | <span data-ttu-id="b1488-708">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-708">Windows XP</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a><span data-ttu-id="b1488-709">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-709">RecycleLifetimeLimit</span></span>



| <span data-ttu-id="b1488-710">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-710">Entry</span></span> | <span data-ttu-id="b1488-711">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-711">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-712">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-712">Description</span></span>    | <span data-ttu-id="b1488-713">Indica el número máximo de minutos que se permite que un proceso se ejecute antes de reciclarlo.</span><span class="sxs-lookup"><span data-stu-id="b1488-713">Indicates the maximum number of minutes to allow a process to run before recycling it.</span></span> <span data-ttu-id="b1488-714">El límite de duración máximo es de 30240 minutos (21 días) y el valor predeterminado es 0 minutos.</span><span class="sxs-lookup"><span data-stu-id="b1488-714">The maximum lifetime limit is 30240 minutes (21 days), and the default is 0 minutes.</span></span> |
| <span data-ttu-id="b1488-715">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-715">Access</span></span>         | <span data-ttu-id="b1488-716">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-716">ReadWrite</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b1488-717">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-717">Type</span></span>           | <span data-ttu-id="b1488-718">Long (0-30240)</span><span class="sxs-lookup"><span data-stu-id="b1488-718">Long (0-30240)</span></span>                                                                                                                                                              |
| <span data-ttu-id="b1488-719">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-719">Default</span></span>        | <span data-ttu-id="b1488-720">0</span><span class="sxs-lookup"><span data-stu-id="b1488-720">0</span></span>                                                                                                                                                                           |
| <span data-ttu-id="b1488-721">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-721">Minimum system</span></span> | <span data-ttu-id="b1488-722">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-722">Windows XP</span></span>                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a><span data-ttu-id="b1488-723">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="b1488-723">RecycleMemoryLimit</span></span>



| <span data-ttu-id="b1488-724">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-724">Entry</span></span> | <span data-ttu-id="b1488-725">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-725">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-726">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-726">Description</span></span>    | <span data-ttu-id="b1488-727">Indica la cantidad máxima de uso de memoria (en kilobytes) permitida para un proceso antes de que se recicle.</span><span class="sxs-lookup"><span data-stu-id="b1488-727">Indicates the maximum amount of memory usage (in kilobytes) allowed a process before it's recycled.</span></span> <span data-ttu-id="b1488-728">Si el uso de memoria del proceso supera el número especificado durante un período superior a un minuto, el proceso se recicla.</span><span class="sxs-lookup"><span data-stu-id="b1488-728">If the process memory usage exceeds the specified number for a period longer than one minute, the process is recycled.</span></span> <span data-ttu-id="b1488-729">La cantidad predeterminada de uso de memoria es de 0 KB.</span><span class="sxs-lookup"><span data-stu-id="b1488-729">The default amount of memory usage is 0 KB.</span></span> |
| <span data-ttu-id="b1488-730">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-730">Access</span></span>         | <span data-ttu-id="b1488-731">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-731">ReadWrite</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b1488-732">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-732">Type</span></span>           | <span data-ttu-id="b1488-733">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="b1488-733">Long (0-1048576)</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b1488-734">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-734">Default</span></span>        | <span data-ttu-id="b1488-735">0</span><span class="sxs-lookup"><span data-stu-id="b1488-735">0</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b1488-736">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-736">Minimum system</span></span> | <span data-ttu-id="b1488-737">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-737">Windows XP</span></span>                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a><span data-ttu-id="b1488-738">Replicable</span><span class="sxs-lookup"><span data-stu-id="b1488-738">Replicable</span></span>



| <span data-ttu-id="b1488-739">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-739">Entry</span></span> | <span data-ttu-id="b1488-740">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-740">Value</span></span> |
|----------------|------------------------------------------------------|
| <span data-ttu-id="b1488-741">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-741">Description</span></span>    | <span data-ttu-id="b1488-742">Indica si la aplicación se puede replicar.</span><span class="sxs-lookup"><span data-stu-id="b1488-742">Indicates whether the application can be replicated.</span></span> |
| <span data-ttu-id="b1488-743">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-743">Access</span></span>         | <span data-ttu-id="b1488-744">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-744">ReadWrite</span></span>                                            |
| <span data-ttu-id="b1488-745">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-745">Type</span></span>           | <span data-ttu-id="b1488-746">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-746">Bool</span></span>                                                 |
| <span data-ttu-id="b1488-747">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-747">Default</span></span>        | <span data-ttu-id="b1488-748">True</span><span class="sxs-lookup"><span data-stu-id="b1488-748">True</span></span>                                                 |
| <span data-ttu-id="b1488-749">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-749">Minimum system</span></span> | <span data-ttu-id="b1488-750">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-750">Windows XP</span></span>                                           |



 

### <a name="runforever"></a><span data-ttu-id="b1488-751">RunForever</span><span class="sxs-lookup"><span data-stu-id="b1488-751">RunForever</span></span>



| <span data-ttu-id="b1488-752">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-752">Entry</span></span> | <span data-ttu-id="b1488-753">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-753">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-754">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-754">Description</span></span>    | <span data-ttu-id="b1488-755">Permite que un proceso de servidor continúe si una aplicación está inactiva.</span><span class="sxs-lookup"><span data-stu-id="b1488-755">Enables a server process to continue if an application is idle.</span></span> <span data-ttu-id="b1488-756">Si se establece en true, el proceso de servidor no se apaga cuando se deja inactivo.</span><span class="sxs-lookup"><span data-stu-id="b1488-756">If set to True, the server process does not shut down when left idle.</span></span> <span data-ttu-id="b1488-757">Si se establece en false, el proceso se cierra según el valor establecido por la propiedad ShutdownAfter.</span><span class="sxs-lookup"><span data-stu-id="b1488-757">If set to False, the process shuts down according to the value set by the ShutdownAfter property.</span></span> <span data-ttu-id="b1488-758">RunForever no está habilitado para las aplicaciones de biblioteca (en proceso).</span><span class="sxs-lookup"><span data-stu-id="b1488-758">RunForever is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="b1488-759">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-759">Access</span></span>         | <span data-ttu-id="b1488-760">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-760">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b1488-761">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-761">Type</span></span>           | <span data-ttu-id="b1488-762">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-762">Bool</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b1488-763">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-763">Default</span></span>        | <span data-ttu-id="b1488-764">False</span><span class="sxs-lookup"><span data-stu-id="b1488-764">False</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b1488-765">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-765">Minimum system</span></span> | <span data-ttu-id="b1488-766">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-766">Windows 2000</span></span>                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a><span data-ttu-id="b1488-767">ServiceName</span><span class="sxs-lookup"><span data-stu-id="b1488-767">ServiceName</span></span>



| <span data-ttu-id="b1488-768">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-768">Entry</span></span> | <span data-ttu-id="b1488-769">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-769">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-770">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-770">Description</span></span>    | <span data-ttu-id="b1488-771">El nombre de servicio correspondiente a la aplicación configurada para ejecutarse como una aplicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="b1488-771">The service name corresponding to the application configured to run as a service application.</span></span> <span data-ttu-id="b1488-772">Si este valor es **null**, la aplicación no está configurada para ejecutarse como un servicio.</span><span class="sxs-lookup"><span data-stu-id="b1488-772">If this value is **NULL**, the application is not configured to run as a service.</span></span> <span data-ttu-id="b1488-773">De lo contrario, la información de configuración para el servicio se puede encontrar mediante el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="b1488-773">Otherwise, the configuration information for the service can be found by using the service name.</span></span> |
| <span data-ttu-id="b1488-774">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-774">Access</span></span>         | <span data-ttu-id="b1488-775">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1488-775">ReadOnly</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b1488-776">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-776">Type</span></span>           | <span data-ttu-id="b1488-777">String</span><span class="sxs-lookup"><span data-stu-id="b1488-777">String</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b1488-778">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-778">Default</span></span>        | <span data-ttu-id="b1488-779">""</span><span class="sxs-lookup"><span data-stu-id="b1488-779">""</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b1488-780">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-780">Minimum system</span></span> | <span data-ttu-id="b1488-781">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-781">Windows XP</span></span>                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a><span data-ttu-id="b1488-782">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="b1488-782">ShutdownAfter</span></span>



| <span data-ttu-id="b1488-783">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-783">Entry</span></span> | <span data-ttu-id="b1488-784">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-784">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-785">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-785">Description</span></span>    | <span data-ttu-id="b1488-786">Establece el retraso antes de cerrar un proceso de servidor después de que se vuelva inactivo.</span><span class="sxs-lookup"><span data-stu-id="b1488-786">Sets the delay before shutting down a server process after it becomes idle.</span></span> <span data-ttu-id="b1488-787">La latencia de cierre oscila entre 0 y 1440 minutos (24 horas).</span><span class="sxs-lookup"><span data-stu-id="b1488-787">Shutdown latency ranges from 0 to 1440 minutes (24 hours).</span></span> <span data-ttu-id="b1488-788">Si RunForever se establece en true, esta propiedad se omite.</span><span class="sxs-lookup"><span data-stu-id="b1488-788">If RunForever is set to True, this property is ignored.</span></span> <span data-ttu-id="b1488-789">ShutdownAfter no está habilitado para las aplicaciones de biblioteca (en proceso).</span><span class="sxs-lookup"><span data-stu-id="b1488-789">ShutdownAfter is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="b1488-790">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-790">Access</span></span>         | <span data-ttu-id="b1488-791">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-791">ReadWrite</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b1488-792">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-792">Type</span></span>           | <span data-ttu-id="b1488-793">Long (0-1440)</span><span class="sxs-lookup"><span data-stu-id="b1488-793">Long (0-1440)</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b1488-794">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-794">Default</span></span>        | <span data-ttu-id="b1488-795">3</span><span class="sxs-lookup"><span data-stu-id="b1488-795">3</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b1488-796">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-796">Minimum system</span></span> | <span data-ttu-id="b1488-797">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1488-797">Windows 2000</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a><span data-ttu-id="b1488-798">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="b1488-798">SoapActivated</span></span>



| <span data-ttu-id="b1488-799">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-799">Entry</span></span> | <span data-ttu-id="b1488-800">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-800">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-801">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-801">Description</span></span>    | <span data-ttu-id="b1488-802">Indica si esta aplicación se expone para su consumo a través del protocolo SOAP.</span><span class="sxs-lookup"><span data-stu-id="b1488-802">Indicates whether this application is exposed for consumption via the SOAP protocol.</span></span> |
| <span data-ttu-id="b1488-803">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-803">Access</span></span>         | <span data-ttu-id="b1488-804">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-804">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="b1488-805">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-805">Type</span></span>           | <span data-ttu-id="b1488-806">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-806">Bool</span></span>                                                                                 |
| <span data-ttu-id="b1488-807">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-807">Default</span></span>        | <span data-ttu-id="b1488-808">False</span><span class="sxs-lookup"><span data-stu-id="b1488-808">False</span></span>                                                                                |
| <span data-ttu-id="b1488-809">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-809">Minimum system</span></span> | <span data-ttu-id="b1488-810">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1488-810">Windows Server 2003</span></span>                                                                  |



 

### <a name="soapbaseurl"></a><span data-ttu-id="b1488-811">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="b1488-811">SoapBaseUrl</span></span>



| <span data-ttu-id="b1488-812">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-812">Entry</span></span> | <span data-ttu-id="b1488-813">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-813">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-814">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-814">Description</span></span>    | <span data-ttu-id="b1488-815">Punto de conexión de la dirección URL en el que esta aplicación se expone a través del protocolo SOAP.</span><span class="sxs-lookup"><span data-stu-id="b1488-815">The URL endpoint at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="b1488-816">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-816">Access</span></span>         | <span data-ttu-id="b1488-817">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-817">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="b1488-818">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-818">Type</span></span>           | <span data-ttu-id="b1488-819">String</span><span class="sxs-lookup"><span data-stu-id="b1488-819">String</span></span>                                                                       |
| <span data-ttu-id="b1488-820">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-820">Default</span></span>        | <span data-ttu-id="b1488-821">""</span><span class="sxs-lookup"><span data-stu-id="b1488-821">""</span></span>                                                                           |
| <span data-ttu-id="b1488-822">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-822">Minimum system</span></span> | <span data-ttu-id="b1488-823">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1488-823">Windows Server 2003</span></span>                                                          |



 

### <a name="soapmailto"></a><span data-ttu-id="b1488-824">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="b1488-824">SoapMailTo</span></span>



| <span data-ttu-id="b1488-825">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-825">Entry</span></span> | <span data-ttu-id="b1488-826">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-826">Value</span></span> |
|----------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-827">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-827">Description</span></span>    | <span data-ttu-id="b1488-828">La dirección de correo electrónico en la que se expone esta aplicación a través del protocolo SOAP.</span><span class="sxs-lookup"><span data-stu-id="b1488-828">The email address at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="b1488-829">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-829">Access</span></span>         | <span data-ttu-id="b1488-830">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-830">ReadWrite</span></span>                                                                     |
| <span data-ttu-id="b1488-831">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-831">Type</span></span>           | <span data-ttu-id="b1488-832">String</span><span class="sxs-lookup"><span data-stu-id="b1488-832">String</span></span>                                                                        |
| <span data-ttu-id="b1488-833">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-833">Default</span></span>        | <span data-ttu-id="b1488-834">""</span><span class="sxs-lookup"><span data-stu-id="b1488-834">""</span></span>                                                                            |
| <span data-ttu-id="b1488-835">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-835">Minimum system</span></span> | <span data-ttu-id="b1488-836">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1488-836">Windows Server 2003</span></span>                                                           |



 

### <a name="soapvroot"></a><span data-ttu-id="b1488-837">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="b1488-837">SoapVRoot</span></span>



| <span data-ttu-id="b1488-838">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-838">Entry</span></span> | <span data-ttu-id="b1488-839">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-839">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-840">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-840">Description</span></span>    | <span data-ttu-id="b1488-841">El directorio raíz virtual de IIS en el que residen los scripts de acceso que exponen la aplicación a través del protocolo SOAP.</span><span class="sxs-lookup"><span data-stu-id="b1488-841">The IIS virtual root directory in which the access scripts that expose the application via the SOAP protocol reside.</span></span> |
| <span data-ttu-id="b1488-842">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-842">Access</span></span>         | <span data-ttu-id="b1488-843">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-843">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="b1488-844">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-844">Type</span></span>           | <span data-ttu-id="b1488-845">String</span><span class="sxs-lookup"><span data-stu-id="b1488-845">String</span></span>                                                                                                               |
| <span data-ttu-id="b1488-846">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-846">Default</span></span>        | <span data-ttu-id="b1488-847">""</span><span class="sxs-lookup"><span data-stu-id="b1488-847">""</span></span>                                                                                                                   |
| <span data-ttu-id="b1488-848">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-848">Minimum system</span></span> | <span data-ttu-id="b1488-849">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1488-849">Windows Server 2003</span></span>                                                                                                  |



 

### <a name="srpenabled"></a><span data-ttu-id="b1488-850">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="b1488-850">SRPEnabled</span></span>



| <span data-ttu-id="b1488-851">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-851">Entry</span></span> | <span data-ttu-id="b1488-852">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-852">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-853">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-853">Description</span></span>    | <span data-ttu-id="b1488-854">Determina la Directiva de restricción de software (SRP) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-854">Determines the software restriction policy (SRP) for the application.</span></span> <span data-ttu-id="b1488-855">Si se establece en true, se utiliza la propiedad SRPTrustLevel de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-855">If set to True, the SRPTrustLevel property for the application is used.</span></span> <span data-ttu-id="b1488-856">Si se establece en false, se usan las directivas de restricción de software de la configuración de seguridad local.</span><span class="sxs-lookup"><span data-stu-id="b1488-856">If set to False, the software restriction policies from the local security settings are used.</span></span> <span data-ttu-id="b1488-857">La configuración de seguridad local se controla mediante el complemento Directiva de seguridad local de Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="b1488-857">The local security settings are controlled through the Local Security Policy snap-in of the Microsoft Management Console.</span></span> |
| <span data-ttu-id="b1488-858">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-858">Access</span></span>         | <span data-ttu-id="b1488-859">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-859">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b1488-860">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-860">Type</span></span>           | <span data-ttu-id="b1488-861">Bool</span><span class="sxs-lookup"><span data-stu-id="b1488-861">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b1488-862">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-862">Default</span></span>        | <span data-ttu-id="b1488-863">False</span><span class="sxs-lookup"><span data-stu-id="b1488-863">False</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b1488-864">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-864">Minimum system</span></span> | <span data-ttu-id="b1488-865">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-865">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a><span data-ttu-id="b1488-866">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="b1488-866">SRPTrustLevel</span></span>



| <span data-ttu-id="b1488-867">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1488-867">Entry</span></span> | <span data-ttu-id="b1488-868">Value</span><span class="sxs-lookup"><span data-stu-id="b1488-868">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1488-869">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1488-869">Description</span></span>    | <span data-ttu-id="b1488-870">Indica el nivel de confianza de la Directiva de restricción de software (SRP) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-870">Indicates the software restriction policy (SRP) trust level of the application.</span></span> <span data-ttu-id="b1488-871">Esta propiedad solo se usa si la propiedad SRPEnabled está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="b1488-871">This property is used only if the SRPEnabled property is set to True.</span></span> <span data-ttu-id="b1488-872">El nivel de confianza de SRP hace referencia al nivel de confianza que desea dar a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1488-872">The SRP trust level refers to the level of trust that you are willing to give to an application.</span></span> <span data-ttu-id="b1488-873">Un nivel de confianza SRP sin restricciones se corresponde con \_ el \_ valor de enumeración LEVELID FULLYTRUSTED más seguro, mientras que un nivel de confianza SRP no permitido corresponde al \_ valor de enumeración de LEVELID no \_ permitido.</span><span class="sxs-lookup"><span data-stu-id="b1488-873">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="b1488-874">La enumeración para los niveles de confianza se define en Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="b1488-874">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="b1488-875">Access</span><span class="sxs-lookup"><span data-stu-id="b1488-875">Access</span></span>         | <span data-ttu-id="b1488-876">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1488-876">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b1488-877">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1488-877">Type</span></span>           | <span data-ttu-id="b1488-878">Valores posibles largos: LEVELID de seguridad no \_ \_ permitido (0X0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="b1488-878">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b1488-879">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1488-879">Default</span></span>        | <span data-ttu-id="b1488-880">Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="b1488-880">SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b1488-881">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="b1488-881">Minimum system</span></span> | <span data-ttu-id="b1488-882">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1488-882">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="b1488-883">Una aplicación en la que esté dispuesto a confiar con acceso sin restricciones debe tener la seguridad más estricta asociada.</span><span class="sxs-lookup"><span data-stu-id="b1488-883">An application that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="b1488-884">Las aplicaciones que no están restringidas pueden cargar solo componentes no restringidos, mientras que las aplicaciones no permitidas no podrán ejecutarse y, por lo tanto, no podrán cargar ningún componente.</span><span class="sxs-lookup"><span data-stu-id="b1488-884">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1488-885">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1488-885">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1488-886">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="b1488-886">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
