---
description: Contiene un solo objeto que corresponde al equipo cuyo catálogo está accediendo. Este objeto contiene información de configuración de nivel de equipo.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Colección LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807898"
---
# <a name="localcomputer-collection"></a><span data-ttu-id="7bf36-104">Colección LocalComputer</span><span class="sxs-lookup"><span data-stu-id="7bf36-104">LocalComputer collection</span></span>

<span data-ttu-id="7bf36-105">Contiene un solo objeto que corresponde al equipo cuyo catálogo está accediendo.</span><span class="sxs-lookup"><span data-stu-id="7bf36-105">Contains a single object that corresponds to the computer whose catalog you are accessing.</span></span> <span data-ttu-id="7bf36-106">Este objeto contiene información de configuración de nivel de equipo.</span><span class="sxs-lookup"><span data-stu-id="7bf36-106">This object holds computer level settings information.</span></span> <span data-ttu-id="7bf36-107">Si llama al método [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) en un objeto creado a partir de la clase [**COMAdminCatalog**](comadmincatalog.md) , el objeto de la colección **LocalComputer** contiene información sobre el equipo remoto cuyo catálogo está accediendo.</span><span class="sxs-lookup"><span data-stu-id="7bf36-107">If you call the [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) method on an object created from the [**COMAdminCatalog**](comadmincatalog.md) class, the object in the **LocalComputer** collection contains information about the remote computer whose catalog you are accessing.</span></span>

<span data-ttu-id="7bf36-108">Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7bf36-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="7bf36-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7bf36-109">Members</span></span>

<span data-ttu-id="7bf36-110">La colección **LocalComputer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="7bf36-110">The **LocalComputer** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="7bf36-111">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="7bf36-111">Related Collections</span></span>

<span data-ttu-id="7bf36-112">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="7bf36-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="7bf36-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="7bf36-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="7bf36-114">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="7bf36-114">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="7bf36-115">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="7bf36-115">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="7bf36-116">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="7bf36-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="7bf36-117">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="7bf36-117">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="7bf36-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7bf36-118">Properties</span></span>

<span data-ttu-id="7bf36-119">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="7bf36-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="7bf36-120">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="7bf36-120">ApplicationProxyRSN</span></span>](#applicationproxyrsn)
-   [<span data-ttu-id="7bf36-121">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-121">CISEnabled</span></span>](#cisenabled)
-   [<span data-ttu-id="7bf36-122">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-122">DCOMEnabled</span></span>](#dcomenabled)
-   [<span data-ttu-id="7bf36-123">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="7bf36-123">DefaultAuthenticationLevel</span></span>](#defaultauthenticationlevel)
-   [<span data-ttu-id="7bf36-124">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="7bf36-124">DefaultImpersonationLevel</span></span>](#defaultimpersonationlevel)
-   [<span data-ttu-id="7bf36-125">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="7bf36-125">DefaultToInternetPorts</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="7bf36-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-126">Description</span></span>](#description)
-   [<span data-ttu-id="7bf36-127">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-127">DSPartitionLookupEnabled</span></span>](#dspartitionlookupenabled)
-   [<span data-ttu-id="7bf36-128">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="7bf36-128">InternetPortsListed</span></span>](#internetportslisted)
-   [<span data-ttu-id="7bf36-129">IsRouter</span><span class="sxs-lookup"><span data-stu-id="7bf36-129">IsRouter</span></span>](#isrouter)
-   [<span data-ttu-id="7bf36-130">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="7bf36-130">LoadBalancingCLSID</span></span>](#loadbalancingclsid)
-   [<span data-ttu-id="7bf36-131">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-131">LocalPartitionLookupEnabled</span></span>](#localpartitionlookupenabled)
-   [<span data-ttu-id="7bf36-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="7bf36-132">Name</span></span>](#name)
-   [<span data-ttu-id="7bf36-133">Identifica</span><span class="sxs-lookup"><span data-stu-id="7bf36-133">OperatingSystem</span></span>](#operatingsystem)
-   [<span data-ttu-id="7bf36-134">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-134">PartitionsEnabled</span></span>](#partitionsenabled)
-   [<span data-ttu-id="7bf36-135">Puertos</span><span class="sxs-lookup"><span data-stu-id="7bf36-135">Ports</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="7bf36-136">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-136">ResourcePoolingEnabled</span></span>](#resourcepoolingenabled)
-   [<span data-ttu-id="7bf36-137">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-137">RPCProxyEnabled</span></span>](#rpcproxyenabled)
-   [<span data-ttu-id="7bf36-138">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-138">SecureReferencesEnabled</span></span>](#securereferencesenabled)
-   [<span data-ttu-id="7bf36-139">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-139">SecurityTrackingEnabled</span></span>](#securitytrackingenabled)
-   [<span data-ttu-id="7bf36-140">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="7bf36-140">SRPActivateAsActivatorChecks</span></span>](#srpactivateasactivatorchecks)
-   [<span data-ttu-id="7bf36-141">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="7bf36-141">SRPRunningObjectChecks</span></span>](#srprunningobjectchecks)
-   [<span data-ttu-id="7bf36-142">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="7bf36-142">TransactionTimeout</span></span>](#transactiontimeout)

### <a name="applicationproxyrsn"></a><span data-ttu-id="7bf36-143">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="7bf36-143">ApplicationProxyRSN</span></span>



| <span data-ttu-id="7bf36-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-144">Entry</span></span> | <span data-ttu-id="7bf36-145">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-145">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="7bf36-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-146">Description</span></span>    | <span data-ttu-id="7bf36-147">Nombre del servidor remoto que usan los proxies de aplicación de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7bf36-147">Remote server name used by application proxies by default.</span></span> |
| <span data-ttu-id="7bf36-148">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-148">Access</span></span>         | <span data-ttu-id="7bf36-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-149">ReadWrite</span></span>                                                  |
| <span data-ttu-id="7bf36-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-150">Type</span></span>           | <span data-ttu-id="7bf36-151">String</span><span class="sxs-lookup"><span data-stu-id="7bf36-151">String</span></span>                                                     |
| <span data-ttu-id="7bf36-152">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-152">Default</span></span>        | <span data-ttu-id="7bf36-153">""</span><span class="sxs-lookup"><span data-stu-id="7bf36-153">""</span></span>                                                         |
| <span data-ttu-id="7bf36-154">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-154">Minimum system</span></span> | <span data-ttu-id="7bf36-155">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-155">Windows 2000</span></span>                                               |



 

### <a name="cisenabled"></a><span data-ttu-id="7bf36-156">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-156">CISEnabled</span></span>



| <span data-ttu-id="7bf36-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-157">Entry</span></span> | <span data-ttu-id="7bf36-158">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-158">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="7bf36-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-159">Description</span></span>    | <span data-ttu-id="7bf36-160">Indica si los servicios de Internet de COM están habilitados.</span><span class="sxs-lookup"><span data-stu-id="7bf36-160">Indicates whether COM Internet Services is enabled.</span></span> |
| <span data-ttu-id="7bf36-161">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-161">Access</span></span>         | <span data-ttu-id="7bf36-162">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-162">ReadWrite</span></span>                                           |
| <span data-ttu-id="7bf36-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-163">Type</span></span>           | <span data-ttu-id="7bf36-164">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-164">Bool</span></span>                                                |
| <span data-ttu-id="7bf36-165">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-165">Default</span></span>        | <span data-ttu-id="7bf36-166">False</span><span class="sxs-lookup"><span data-stu-id="7bf36-166">False</span></span>                                               |
| <span data-ttu-id="7bf36-167">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-167">Minimum system</span></span> | <span data-ttu-id="7bf36-168">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-168">Windows 2000</span></span>                                        |



 

### <a name="dcomenabled"></a><span data-ttu-id="7bf36-169">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-169">DCOMEnabled</span></span>



| <span data-ttu-id="7bf36-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-170">Entry</span></span> | <span data-ttu-id="7bf36-171">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-171">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="7bf36-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-172">Description</span></span>    | <span data-ttu-id="7bf36-173">Establézcalo en true para habilitar DCOM en el equipo.</span><span class="sxs-lookup"><span data-stu-id="7bf36-173">Set to True to enable DCOM on the computer.</span></span> |
| <span data-ttu-id="7bf36-174">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-174">Access</span></span>         | <span data-ttu-id="7bf36-175">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-175">ReadWrite</span></span>                                   |
| <span data-ttu-id="7bf36-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-176">Type</span></span>           | <span data-ttu-id="7bf36-177">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-177">Bool</span></span>                                        |
| <span data-ttu-id="7bf36-178">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-178">Default</span></span>        | <span data-ttu-id="7bf36-179">True</span><span class="sxs-lookup"><span data-stu-id="7bf36-179">True</span></span>                                        |
| <span data-ttu-id="7bf36-180">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-180">Minimum system</span></span> | <span data-ttu-id="7bf36-181">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-181">Windows 2000</span></span>                                |



 

### <a name="defaultauthenticationlevel"></a><span data-ttu-id="7bf36-182">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="7bf36-182">DefaultAuthenticationLevel</span></span>



| <span data-ttu-id="7bf36-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-183">Entry</span></span> | <span data-ttu-id="7bf36-184">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-184">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-185">Description</span></span>    | <span data-ttu-id="7bf36-186">Nivel de autenticación que usan las aplicaciones que tienen autenticación establecida en el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7bf36-186">Authentication level used by applications that have Authentication set to Default.</span></span> <span data-ttu-id="7bf36-187">Los valores corresponden a la configuración de autenticación de llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="7bf36-187">Values correspond to the Remote Procedure Call (RPC) authentication settings.</span></span>                                                                                         |
| <span data-ttu-id="7bf36-188">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-188">Access</span></span>         | <span data-ttu-id="7bf36-189">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-189">ReadWrite</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="7bf36-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-190">Type</span></span>           | <span data-ttu-id="7bf36-191">Valores posibles largos: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="7bf36-191">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span> |
| <span data-ttu-id="7bf36-192">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-192">Default</span></span>        | <span data-ttu-id="7bf36-193">COMAdminAuthenticationConnect (2)</span><span class="sxs-lookup"><span data-stu-id="7bf36-193">COMAdminAuthenticationConnect (2)</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="7bf36-194">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-194">Minimum system</span></span> | <span data-ttu-id="7bf36-195">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-195">Windows 2000</span></span>                                                                                                                                                                                                                                             |



 

> [!Note]  
> <span data-ttu-id="7bf36-196">COMAdminAuthenticationDefault se asigna a COMAdminAuthenticationConnect cuando COM llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7bf36-196">COMAdminAuthenticationDefault is mapped to COMAdminAuthenticationConnect when COM calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="7bf36-197">Se recomienda usar las constantes en la enumeración y no los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="7bf36-197">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="defaultimpersonationlevel"></a><span data-ttu-id="7bf36-198">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="7bf36-198">DefaultImpersonationLevel</span></span>



| <span data-ttu-id="7bf36-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-199">Entry</span></span> | <span data-ttu-id="7bf36-200">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-200">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-201">Description</span></span>    | <span data-ttu-id="7bf36-202">Nivel de suplantación para permitir si no se establece uno.</span><span class="sxs-lookup"><span data-stu-id="7bf36-202">Impersonation level to allow if one is not set.</span></span>                                                                                                               |
| <span data-ttu-id="7bf36-203">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-203">Access</span></span>         | <span data-ttu-id="7bf36-204">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-204">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="7bf36-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-205">Type</span></span>           | <span data-ttu-id="7bf36-206">Valores posibles largos: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="7bf36-206">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="7bf36-207">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-207">Default</span></span>        | <span data-ttu-id="7bf36-208">COMAdminImpersonationIdentify (2)</span><span class="sxs-lookup"><span data-stu-id="7bf36-208">COMAdminImpersonationIdentify (2)</span></span>                                                                                                                             |
| <span data-ttu-id="7bf36-209">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-209">Minimum system</span></span> | <span data-ttu-id="7bf36-210">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-210">Windows 2000</span></span>                                                                                                                                                  |



 

> [!Note]  
> <span data-ttu-id="7bf36-211">Se recomienda usar las constantes de la enumeración, y no los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="7bf36-211">It is recommended that you use the constants in the enumeration, and not the numeric values.</span></span>

 

### <a name="defaulttointernetports"></a><span data-ttu-id="7bf36-212">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="7bf36-212">DefaultToInternetPorts</span></span>



| <span data-ttu-id="7bf36-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-213">Entry</span></span> | <span data-ttu-id="7bf36-214">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-214">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-215">Description</span></span>    | <span data-ttu-id="7bf36-216">Determina si el tipo predeterminado de Puerto proporcionado debe ser Internet (true) o intranet (false).</span><span class="sxs-lookup"><span data-stu-id="7bf36-216">Determines whether the default type of port provided should be Internet (True) or intranet (False).</span></span> |
| <span data-ttu-id="7bf36-217">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-217">Access</span></span>         | <span data-ttu-id="7bf36-218">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-218">ReadWrite</span></span>                                                                                           |
| <span data-ttu-id="7bf36-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-219">Type</span></span>           | <span data-ttu-id="7bf36-220">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-220">Bool</span></span>                                                                                                |
| <span data-ttu-id="7bf36-221">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-221">Default</span></span>        | <span data-ttu-id="7bf36-222">False</span><span class="sxs-lookup"><span data-stu-id="7bf36-222">False</span></span>                                                                                               |
| <span data-ttu-id="7bf36-223">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-223">Minimum system</span></span> | <span data-ttu-id="7bf36-224">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-224">Windows 2000</span></span>                                                                                        |



 

### <a name="description"></a><span data-ttu-id="7bf36-225">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-225">Description</span></span>



| <span data-ttu-id="7bf36-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-226">Entry</span></span> | <span data-ttu-id="7bf36-227">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-227">Value</span></span> |
|----------------|--------------------------------|
| <span data-ttu-id="7bf36-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-228">Description</span></span>    | <span data-ttu-id="7bf36-229">Descripción del equipo.</span><span class="sxs-lookup"><span data-stu-id="7bf36-229">A description of the computer.</span></span> |
| <span data-ttu-id="7bf36-230">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-230">Access</span></span>         | <span data-ttu-id="7bf36-231">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-231">ReadWrite</span></span>                      |
| <span data-ttu-id="7bf36-232">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-232">Type</span></span>           | <span data-ttu-id="7bf36-233">String</span><span class="sxs-lookup"><span data-stu-id="7bf36-233">String</span></span>                         |
| <span data-ttu-id="7bf36-234">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-234">Default</span></span>        | <span data-ttu-id="7bf36-235">""</span><span class="sxs-lookup"><span data-stu-id="7bf36-235">""</span></span>                             |
| <span data-ttu-id="7bf36-236">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-236">Minimum system</span></span> | <span data-ttu-id="7bf36-237">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-237">Windows 2000</span></span>                   |



 

### <a name="dspartitionlookupenabled"></a><span data-ttu-id="7bf36-238">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-238">DSPartitionLookupEnabled</span></span>



| <span data-ttu-id="7bf36-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-239">Entry</span></span> | <span data-ttu-id="7bf36-240">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-240">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-241">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-241">Description</span></span>    | <span data-ttu-id="7bf36-242">Indica si el usuario de las asignaciones de particiones está protegido en el almacén de dominio.</span><span class="sxs-lookup"><span data-stu-id="7bf36-242">Indicates whether the user of the partition mappings is checked into the domain store.</span></span> |
| <span data-ttu-id="7bf36-243">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-243">Access</span></span>         | <span data-ttu-id="7bf36-244">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-244">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="7bf36-245">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-245">Type</span></span>           | <span data-ttu-id="7bf36-246">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-246">Bool</span></span>                                                                                   |
| <span data-ttu-id="7bf36-247">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-247">Default</span></span>        | <span data-ttu-id="7bf36-248">True</span><span class="sxs-lookup"><span data-stu-id="7bf36-248">True</span></span>                                                                                   |
| <span data-ttu-id="7bf36-249">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-249">Minimum system</span></span> | <span data-ttu-id="7bf36-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bf36-250">Windows Server 2003</span></span>                                                                    |



 

### <a name="internetportslisted"></a><span data-ttu-id="7bf36-251">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="7bf36-251">InternetPortsListed</span></span>



| <span data-ttu-id="7bf36-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-252">Entry</span></span> | <span data-ttu-id="7bf36-253">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-253">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-254">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-254">Description</span></span>    | <span data-ttu-id="7bf36-255">Determina si los puertos enumerados en la propiedad Ports se van a usar para Internet (true) o para intranet (false).</span><span class="sxs-lookup"><span data-stu-id="7bf36-255">Determines whether the ports listed in the Ports property are to be used for Internet (True) or for intranet (False).</span></span> |
| <span data-ttu-id="7bf36-256">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-256">Access</span></span>         | <span data-ttu-id="7bf36-257">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-257">ReadWrite</span></span>                                                                                                             |
| <span data-ttu-id="7bf36-258">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-258">Type</span></span>           | <span data-ttu-id="7bf36-259">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-259">Bool</span></span>                                                                                                                  |
| <span data-ttu-id="7bf36-260">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-260">Default</span></span>        | <span data-ttu-id="7bf36-261">False</span><span class="sxs-lookup"><span data-stu-id="7bf36-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="7bf36-262">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-262">Minimum system</span></span> | <span data-ttu-id="7bf36-263">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-263">Windows 2000</span></span>                                                                                                          |



 

### <a name="isrouter"></a><span data-ttu-id="7bf36-264">IsRouter</span><span class="sxs-lookup"><span data-stu-id="7bf36-264">IsRouter</span></span>



| <span data-ttu-id="7bf36-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-265">Entry</span></span> | <span data-ttu-id="7bf36-266">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-266">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-267">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-267">Description</span></span>    | <span data-ttu-id="7bf36-268">Establézcalo en true si el equipo es un enrutador para el servicio de equilibrio de carga de componentes (CLB).</span><span class="sxs-lookup"><span data-stu-id="7bf36-268">Set to True if the computer is a router for the component load balancing (CLB) service.</span></span> <span data-ttu-id="7bf36-269">Esta propiedad solo se puede establecer en true si el servicio de equilibrio de carga de componentes está instalado actualmente en el equipo; de lo contrario, los errores con COMAdmin \_ E \_ requieren una \_ \_ plataforma diferente.</span><span class="sxs-lookup"><span data-stu-id="7bf36-269">This property can be set to True only if the component load balancing service is currently installed on the computer; otherwise, it errors with COMADMIN\_E\_REQUIRES\_DIFFERENT\_PLATFORM.</span></span> |
| <span data-ttu-id="7bf36-270">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-270">Access</span></span>         | <span data-ttu-id="7bf36-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-271">ReadWrite</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7bf36-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-272">Type</span></span>           | <span data-ttu-id="7bf36-273">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-273">Bool</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7bf36-274">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-274">Default</span></span>        | <span data-ttu-id="7bf36-275">False</span><span class="sxs-lookup"><span data-stu-id="7bf36-275">False</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7bf36-276">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-276">Minimum system</span></span> | <span data-ttu-id="7bf36-277">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-277">Windows 2000</span></span>                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="7bf36-278">Si esta propiedad se establece en true, el servidor CLB se configura y se inicia en el inicio.</span><span class="sxs-lookup"><span data-stu-id="7bf36-278">If this property is set to True, the CLB server is configured and starts at startup.</span></span> <span data-ttu-id="7bf36-279">El servidor se agrega a la colección ApplicationCluster si aún no está presente.</span><span class="sxs-lookup"><span data-stu-id="7bf36-279">The server is added to the ApplicationCluster collection if it is not already present.</span></span>

### <a name="loadbalancingclsid"></a><span data-ttu-id="7bf36-280">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="7bf36-280">LoadBalancingCLSID</span></span>



| <span data-ttu-id="7bf36-281">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-281">Entry</span></span> | <span data-ttu-id="7bf36-282">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-282">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="7bf36-283">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-283">Description</span></span>    | <span data-ttu-id="7bf36-284">CLSID del objeto que se va a equilibrar.</span><span class="sxs-lookup"><span data-stu-id="7bf36-284">The CLSID of the object to balance.</span></span> |
| <span data-ttu-id="7bf36-285">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-285">Access</span></span>         | <span data-ttu-id="7bf36-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-286">ReadWrite</span></span>                           |
| <span data-ttu-id="7bf36-287">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-287">Type</span></span>           | <span data-ttu-id="7bf36-288">String</span><span class="sxs-lookup"><span data-stu-id="7bf36-288">String</span></span>                              |
| <span data-ttu-id="7bf36-289">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-289">Default</span></span>        | <span data-ttu-id="7bf36-290">NULL</span><span class="sxs-lookup"><span data-stu-id="7bf36-290">NULL</span></span>                                |
| <span data-ttu-id="7bf36-291">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-291">Minimum system</span></span> | <span data-ttu-id="7bf36-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bf36-292">Windows XP</span></span>                          |



 

### <a name="localpartitionlookupenabled"></a><span data-ttu-id="7bf36-293">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-293">LocalPartitionLookupEnabled</span></span>



| <span data-ttu-id="7bf36-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-294">Entry</span></span> | <span data-ttu-id="7bf36-295">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-295">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-296">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-296">Description</span></span>    | <span data-ttu-id="7bf36-297">Indica si el usuario de las asignaciones de particiones está protegido en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="7bf36-297">Indicates whether the user of the partition mappings is checked into the local store.</span></span> |
| <span data-ttu-id="7bf36-298">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-298">Access</span></span>         | <span data-ttu-id="7bf36-299">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-299">ReadWrite</span></span>                                                                             |
| <span data-ttu-id="7bf36-300">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-300">Type</span></span>           | <span data-ttu-id="7bf36-301">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-301">Bool</span></span>                                                                                  |
| <span data-ttu-id="7bf36-302">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-302">Default</span></span>        | <span data-ttu-id="7bf36-303">True</span><span class="sxs-lookup"><span data-stu-id="7bf36-303">True</span></span>                                                                                  |
| <span data-ttu-id="7bf36-304">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-304">Minimum system</span></span> | <span data-ttu-id="7bf36-305">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bf36-305">Windows Server 2003</span></span>                                                                   |



 

### <a name="name"></a><span data-ttu-id="7bf36-306">Nombre</span><span class="sxs-lookup"><span data-stu-id="7bf36-306">Name</span></span>



| <span data-ttu-id="7bf36-307">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-307">Entry</span></span> | <span data-ttu-id="7bf36-308">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-308">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-309">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-309">Description</span></span>    | <span data-ttu-id="7bf36-310">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="7bf36-310">The name of the computer.</span></span> <span data-ttu-id="7bf36-311">Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="7bf36-311">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="7bf36-312">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-312">Access</span></span>         | <span data-ttu-id="7bf36-313">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="7bf36-313">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7bf36-314">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-314">Type</span></span>           | <span data-ttu-id="7bf36-315">String</span><span class="sxs-lookup"><span data-stu-id="7bf36-315">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7bf36-316">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-316">Default</span></span>        | <span data-ttu-id="7bf36-317">"Mi PC"</span><span class="sxs-lookup"><span data-stu-id="7bf36-317">"My Computer"</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7bf36-318">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-318">Minimum system</span></span> | <span data-ttu-id="7bf36-319">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-319">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a><span data-ttu-id="7bf36-320">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7bf36-320">OperatingSystem</span></span>



| <span data-ttu-id="7bf36-321">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-321">Entry</span></span> | <span data-ttu-id="7bf36-322">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-322">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-323">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-323">Description</span></span>    | <span data-ttu-id="7bf36-324">El sistema operativo instalado en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7bf36-324">The operating system installed on the local computer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7bf36-325">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-325">Access</span></span>         | <span data-ttu-id="7bf36-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7bf36-327">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-327">Type</span></span>           | <span data-ttu-id="7bf36-328">Valores posibles largos: COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16)</span><span class="sxs-lookup"><span data-stu-id="7bf36-328">Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3\_1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16)</span></span> |
| <span data-ttu-id="7bf36-329">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-329">Default</span></span>        | <span data-ttu-id="7bf36-330">COMAdminOSNotInitialized (0)</span><span class="sxs-lookup"><span data-stu-id="7bf36-330">COMAdminOSNotInitialized (0)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7bf36-331">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-331">Minimum system</span></span> | <span data-ttu-id="7bf36-332">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-332">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a><span data-ttu-id="7bf36-333">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-333">PartitionsEnabled</span></span>



| <span data-ttu-id="7bf36-334">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-334">Entry</span></span> | <span data-ttu-id="7bf36-335">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-335">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-336">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-336">Description</span></span>    | <span data-ttu-id="7bf36-337">Indica si se pueden usar particiones COM+ en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7bf36-337">Indicates whether COM+ partitions can be used on the local computer.</span></span> <span data-ttu-id="7bf36-338">Si esta propiedad es false, cualquier intento de usar particiones COM+ produce un error.</span><span class="sxs-lookup"><span data-stu-id="7bf36-338">If this property is False, any attempt to use COM+ partitions results in an error.</span></span> |
| <span data-ttu-id="7bf36-339">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-339">Access</span></span>         | <span data-ttu-id="7bf36-340">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-340">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="7bf36-341">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-341">Type</span></span>           | <span data-ttu-id="7bf36-342">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-342">Bool</span></span>                                                                                                                                                    |
| <span data-ttu-id="7bf36-343">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-343">Default</span></span>        | <span data-ttu-id="7bf36-344">False</span><span class="sxs-lookup"><span data-stu-id="7bf36-344">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7bf36-345">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-345">Minimum system</span></span> | <span data-ttu-id="7bf36-346">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bf36-346">Windows Server 2003</span></span>                                                                                                                                     |



 

### <a name="ports"></a><span data-ttu-id="7bf36-347">Puertos</span><span class="sxs-lookup"><span data-stu-id="7bf36-347">Ports</span></span>



| <span data-ttu-id="7bf36-348">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-348">Entry</span></span> | <span data-ttu-id="7bf36-349">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-349">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-350">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-350">Description</span></span>    | <span data-ttu-id="7bf36-351">Cadena que describe los puertos que son para el uso de Internet o de la intranet, dependiendo de la propiedad InternetPortsListed. por ejemplo, "500-599:600-800".</span><span class="sxs-lookup"><span data-stu-id="7bf36-351">A string describing ports that are for either Internet or intranet use, depending on the InternetPortsListed property; for example, "500-599: 600-800".</span></span> |
| <span data-ttu-id="7bf36-352">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-352">Access</span></span>         | <span data-ttu-id="7bf36-353">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-353">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="7bf36-354">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-354">Type</span></span>           | <span data-ttu-id="7bf36-355">String</span><span class="sxs-lookup"><span data-stu-id="7bf36-355">String</span></span>                                                                                                                                                  |
| <span data-ttu-id="7bf36-356">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-356">Default</span></span>        | <span data-ttu-id="7bf36-357">""</span><span class="sxs-lookup"><span data-stu-id="7bf36-357">""</span></span>                                                                                                                                                      |
| <span data-ttu-id="7bf36-358">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-358">Minimum system</span></span> | <span data-ttu-id="7bf36-359">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-359">Windows 2000</span></span>                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a><span data-ttu-id="7bf36-360">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-360">ResourcePoolingEnabled</span></span>



| <span data-ttu-id="7bf36-361">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-361">Entry</span></span> | <span data-ttu-id="7bf36-362">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-362">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="7bf36-363">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-363">Description</span></span>    | <span data-ttu-id="7bf36-364">Habilita el uso de dispensadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bf36-364">Enables use of resource dispensers.</span></span> |
| <span data-ttu-id="7bf36-365">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-365">Access</span></span>         | <span data-ttu-id="7bf36-366">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-366">ReadWrite</span></span>                           |
| <span data-ttu-id="7bf36-367">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-367">Type</span></span>           | <span data-ttu-id="7bf36-368">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-368">Bool</span></span>                                |
| <span data-ttu-id="7bf36-369">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-369">Default</span></span>        | <span data-ttu-id="7bf36-370">True</span><span class="sxs-lookup"><span data-stu-id="7bf36-370">True</span></span>                                |
| <span data-ttu-id="7bf36-371">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-371">Minimum system</span></span> | <span data-ttu-id="7bf36-372">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-372">Windows 2000</span></span>                        |



 

### <a name="rpcproxyenabled"></a><span data-ttu-id="7bf36-373">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-373">RPCProxyEnabled</span></span>



| <span data-ttu-id="7bf36-374">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-374">Entry</span></span> | <span data-ttu-id="7bf36-375">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-375">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-376">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-376">Description</span></span>    | <span data-ttu-id="7bf36-377">Controla si el proxy IIS de RPC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7bf36-377">Controls whether the RPC IIS proxy is enabled.</span></span> <span data-ttu-id="7bf36-378">El proxy IIS de RPC se usa junto con IIS para reenviar las llamadas al mecanismo de RPC desde IIS y es uno de los componentes principales de los servicios de Internet COM, que se habilita estableciendo CISEnabled en true.</span><span class="sxs-lookup"><span data-stu-id="7bf36-378">The RPC IIS proxy is used in conjunction with IIS to forward calls to the RPC mechanism from IIS and is one of the core pieces of COM Internet Services, which is enabled by setting CISEnabled to True.</span></span> <span data-ttu-id="7bf36-379">Para obtener más información sobre RPCProxyEnabled, consulte [seguridad de http RPC](/windows/desktop/Rpc/rpc-over-http-security).</span><span class="sxs-lookup"><span data-stu-id="7bf36-379">For more information on RPCProxyEnabled, see [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span></span> |
| <span data-ttu-id="7bf36-380">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-380">Access</span></span>         | <span data-ttu-id="7bf36-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-381">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="7bf36-382">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-382">Type</span></span>           | <span data-ttu-id="7bf36-383">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-383">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7bf36-384">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-384">Default</span></span>        | <span data-ttu-id="7bf36-385">False</span><span class="sxs-lookup"><span data-stu-id="7bf36-385">False</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7bf36-386">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-386">Minimum system</span></span> | <span data-ttu-id="7bf36-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-387">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a><span data-ttu-id="7bf36-388">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-388">SecureReferencesEnabled</span></span>



| <span data-ttu-id="7bf36-389">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-389">Entry</span></span> | <span data-ttu-id="7bf36-390">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-391">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-391">Description</span></span>    | <span data-ttu-id="7bf36-392">Aplica en los equipos DCOM las llamadas entre procesos a los métodos [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) están protegidos.</span><span class="sxs-lookup"><span data-stu-id="7bf36-392">Enforces in DCOM computers that cross-process calls to [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are secured.</span></span> |
| <span data-ttu-id="7bf36-393">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-393">Access</span></span>         | <span data-ttu-id="7bf36-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-394">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="7bf36-395">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-395">Type</span></span>           | <span data-ttu-id="7bf36-396">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-396">Bool</span></span>                                                                                                                                                                      |
| <span data-ttu-id="7bf36-397">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-397">Default</span></span>        | <span data-ttu-id="7bf36-398">False</span><span class="sxs-lookup"><span data-stu-id="7bf36-398">False</span></span>                                                                                                                                                                     |
| <span data-ttu-id="7bf36-399">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-399">Minimum system</span></span> | <span data-ttu-id="7bf36-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-400">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a><span data-ttu-id="7bf36-401">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="7bf36-401">SecurityTrackingEnabled</span></span>



| <span data-ttu-id="7bf36-402">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-402">Entry</span></span> | <span data-ttu-id="7bf36-403">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-403">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="7bf36-404">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-404">Description</span></span>    | <span data-ttu-id="7bf36-405">Establézcalo en true si está habilitado el seguimiento de seguridad en los objetos.</span><span class="sxs-lookup"><span data-stu-id="7bf36-405">Set to True if security tracking is enabled on objects.</span></span> |
| <span data-ttu-id="7bf36-406">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-406">Access</span></span>         | <span data-ttu-id="7bf36-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-407">ReadWrite</span></span>                                               |
| <span data-ttu-id="7bf36-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-408">Type</span></span>           | <span data-ttu-id="7bf36-409">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-409">Bool</span></span>                                                    |
| <span data-ttu-id="7bf36-410">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-410">Default</span></span>        | <span data-ttu-id="7bf36-411">True</span><span class="sxs-lookup"><span data-stu-id="7bf36-411">True</span></span>                                                    |
| <span data-ttu-id="7bf36-412">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-412">Minimum system</span></span> | <span data-ttu-id="7bf36-413">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-413">Windows 2000</span></span>                                            |



 

### <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="7bf36-414">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="7bf36-414">SRPActivateAsActivatorChecks</span></span>



| <span data-ttu-id="7bf36-415">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-415">Entry</span></span> | <span data-ttu-id="7bf36-416">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-416">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-417">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-417">Description</span></span>    | <span data-ttu-id="7bf36-418">Determina el modo en que la Directiva de restricción de software (SRP) controla las conexiones de activación como activador.</span><span class="sxs-lookup"><span data-stu-id="7bf36-418">Determines how the software restriction policy (SRP) handles activate-as-activator connections.</span></span> <span data-ttu-id="7bf36-419">Si se establece en true, el nivel de confianza de SRP configurado para el objeto de servidor se compara con el nivel de confianza de SRP del objeto de cliente y se utiliza el nivel de confianza mayor (más riguroso) para ejecutar el objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="7bf36-419">If set to True, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and the higher (more stringent) trust level is used to run the server object.</span></span> <span data-ttu-id="7bf36-420">Si se establece en false, el objeto de servidor se ejecuta con el nivel de confianza de SRP del objeto de cliente, independientemente del nivel de confianza de SRP con el que está configurado el servidor.</span><span class="sxs-lookup"><span data-stu-id="7bf36-420">If set to False, the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which the server is configured.</span></span> |
| <span data-ttu-id="7bf36-421">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-421">Access</span></span>         | <span data-ttu-id="7bf36-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-422">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7bf36-423">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-423">Type</span></span>           | <span data-ttu-id="7bf36-424">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-424">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7bf36-425">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-425">Default</span></span>        | <span data-ttu-id="7bf36-426">True</span><span class="sxs-lookup"><span data-stu-id="7bf36-426">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7bf36-427">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-427">Minimum system</span></span> | <span data-ttu-id="7bf36-428">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bf36-428">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a><span data-ttu-id="7bf36-429">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="7bf36-429">SRPRunningObjectChecks</span></span>



| <span data-ttu-id="7bf36-430">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-430">Entry</span></span> | <span data-ttu-id="7bf36-431">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-431">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-432">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-432">Description</span></span>    | <span data-ttu-id="7bf36-433">Determina la forma en que la Directiva de restricción de software (SRP) controla las conexiones a los procesos existentes.</span><span class="sxs-lookup"><span data-stu-id="7bf36-433">Determines how the software restriction policy (SRP) handles attempted connections to existing processes.</span></span> <span data-ttu-id="7bf36-434">Si se establece en false, los intentos de conexión a objetos en ejecución no se comprueban para los niveles de confianza de SRP correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7bf36-434">If set to False, attempts to connect to running objects are not checked for appropriate SRP trust levels.</span></span> <span data-ttu-id="7bf36-435">Si se establece en true, el objeto que se está ejecutando debe tener un nivel de confianza SRP igual o superior (más estricto) que el objeto de cliente.</span><span class="sxs-lookup"><span data-stu-id="7bf36-435">If set to True, the running object must have an equal or higher (more stringent) SRP trust level than the client object.</span></span> <span data-ttu-id="7bf36-436">Por ejemplo, un objeto de cliente con un nivel de confianza SRP sin restricciones no puede conectarse a un objeto en ejecución con un nivel de confianza SRP no permitido.</span><span class="sxs-lookup"><span data-stu-id="7bf36-436">For example, a client object with an Unrestricted SRP trust level cannot connect to a running object with a Disallowed SRP trust level.</span></span> |
| <span data-ttu-id="7bf36-437">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-437">Access</span></span>         | <span data-ttu-id="7bf36-438">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-438">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7bf36-439">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-439">Type</span></span>           | <span data-ttu-id="7bf36-440">Bool</span><span class="sxs-lookup"><span data-stu-id="7bf36-440">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7bf36-441">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-441">Default</span></span>        | <span data-ttu-id="7bf36-442">True</span><span class="sxs-lookup"><span data-stu-id="7bf36-442">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7bf36-443">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-443">Minimum system</span></span> | <span data-ttu-id="7bf36-444">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bf36-444">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a><span data-ttu-id="7bf36-445">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="7bf36-445">TransactionTimeout</span></span>



| <span data-ttu-id="7bf36-446">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bf36-446">Entry</span></span> | <span data-ttu-id="7bf36-447">Value</span><span class="sxs-lookup"><span data-stu-id="7bf36-447">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf36-448">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf36-448">Description</span></span>    | <span data-ttu-id="7bf36-449">Debe establecerse en un valor suficiente en segundos si realiza numerosas operaciones dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="7bf36-449">Should be set to a sufficient value in seconds if you are doing numerous operations within a transaction.</span></span> <span data-ttu-id="7bf36-450">El período de tiempo de espera predeterminado es de 60 segundos y el período de tiempo de espera máximo es de 3600 segundos (1 hora).</span><span class="sxs-lookup"><span data-stu-id="7bf36-450">The default time-out period is 60 seconds, and the maximum time-out period is 3600 seconds (1 hour).</span></span> <span data-ttu-id="7bf36-451">Al establecer esta propiedad en 0 se deshabilitan los tiempos de espera de la transacción.</span><span class="sxs-lookup"><span data-stu-id="7bf36-451">Setting this property to 0 disables transaction time-outs.</span></span> <span data-ttu-id="7bf36-452">Esta propiedad se puede reemplazar por componentes individuales mediante la propiedad ComponentTransactionTimeout de la colección de [**componentes**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="7bf36-452">This property can be overridden by individual components by using the ComponentTransactionTimeout property of the [**Components**](components.md) collection.</span></span> |
| <span data-ttu-id="7bf36-453">Access</span><span class="sxs-lookup"><span data-stu-id="7bf36-453">Access</span></span>         | <span data-ttu-id="7bf36-454">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7bf36-454">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7bf36-455">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bf36-455">Type</span></span>           | <span data-ttu-id="7bf36-456">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="7bf36-456">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7bf36-457">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bf36-457">Default</span></span>        | <span data-ttu-id="7bf36-458">60</span><span class="sxs-lookup"><span data-stu-id="7bf36-458">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7bf36-459">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="7bf36-459">Minimum system</span></span> | <span data-ttu-id="7bf36-460">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bf36-460">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a><span data-ttu-id="7bf36-461">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7bf36-461">Example</span></span>

<span data-ttu-id="7bf36-462">En el siguiente ejemplo de Microsoft Visual Basic se muestra cómo conectarse a un equipo remoto y obtener su propiedad SecurityTrackingEnabled mediante la colección **LocalComputer** del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="7bf36-462">The following Microsoft Visual Basic example demonstrates how to connect to a remote computer and get its SecurityTrackingEnabled property by using the **LocalComputer** collection of the remote computer.</span></span> <span data-ttu-id="7bf36-463">Para usar este ejemplo, agregue la biblioteca de tipos de administración de COM+ como referencia a su proyecto de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7bf36-463">To use this example, add the COM+ Admin Type Library as a reference to your Visual Basic project.</span></span>


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



<span data-ttu-id="7bf36-464">Para usar la función, proporcione un valor de cadena para el nombre del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="7bf36-464">To use the function, provide a string value for the name of the remote computer.</span></span> <span data-ttu-id="7bf36-465">En el siguiente código de Visual Basic se muestra cómo conectarse al equipo denominado "nombreDeEquipoRemoto".</span><span class="sxs-lookup"><span data-stu-id="7bf36-465">The following Visual Basic code shows how to connect to the computer named "RemoteComputerName".</span></span>


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a><span data-ttu-id="7bf36-466">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bf36-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf36-467">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7bf36-467">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
