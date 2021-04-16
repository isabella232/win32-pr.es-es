---
description: Contiene un objeto para cada componente de la aplicación relacionada.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Colección de componentes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539315"
---
# <a name="components-collection"></a><span data-ttu-id="aeab7-103">Colección de componentes</span><span class="sxs-lookup"><span data-stu-id="aeab7-103">Components collection</span></span>

<span data-ttu-id="aeab7-104">Contiene un objeto para cada componente de la aplicación relacionada.</span><span class="sxs-lookup"><span data-stu-id="aeab7-104">Contains an object for each component in the related application.</span></span> <span data-ttu-id="aeab7-105">La colección de **componentes** siempre está relacionada con un objeto de la colección de [**aplicaciones**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="aeab7-105">The **Components** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="aeab7-106">Las propiedades expuestas por estos objetos contienen la configuración realizada en el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-106">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="aeab7-107">Esta colección admite el método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , pero no el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="aeab7-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="aeab7-108">Para instalar o importar componentes en una aplicación, use métodos en el objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="aeab7-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="aeab7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="aeab7-109">Members</span></span>

<span data-ttu-id="aeab7-110">La colección de **componentes** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="aeab7-110">The **Components** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="aeab7-111">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="aeab7-111">Related Collections</span></span>

<span data-ttu-id="aeab7-112">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="aeab7-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="aeab7-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="aeab7-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="aeab7-114">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="aeab7-114">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)
-   [<span data-ttu-id="aeab7-115">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="aeab7-115">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="aeab7-116">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="aeab7-116">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="aeab7-117">**RolesForComponent**</span><span class="sxs-lookup"><span data-stu-id="aeab7-117">**RolesForComponent**</span></span>](rolesforcomponent.md)
-   [<span data-ttu-id="aeab7-118">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="aeab7-118">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

<span data-ttu-id="aeab7-119">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="aeab7-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="aeab7-120">**APLICACIONES**</span><span class="sxs-lookup"><span data-stu-id="aeab7-120">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="aeab7-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeab7-121">Properties</span></span>

<span data-ttu-id="aeab7-122">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="aeab7-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="aeab7-123">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="aeab7-123">AllowInprocSubscribers</span></span>](#allowinprocsubscribers)
-   [<span data-ttu-id="aeab7-124">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="aeab7-124">ApplicationID</span></span>](#applicationid)
-   [<span data-ttu-id="aeab7-125">Bits</span><span class="sxs-lookup"><span data-stu-id="aeab7-125">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="aeab7-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="aeab7-126">CLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="aeab7-127">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-127">ComponentAccessChecksEnabled</span></span>](#componentaccesschecksenabled)
-   [<span data-ttu-id="aeab7-128">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="aeab7-128">ComponentTransactionTimeout</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="aeab7-129">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-129">ComponentTransactionTimeoutEnabled</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="aeab7-130">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="aeab7-130">COMTIIntrinsics</span></span>](#comtiintrinsics)
-   [<span data-ttu-id="aeab7-131">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-131">ConstructionEnabled</span></span>](#constructionenabled)
-   [<span data-ttu-id="aeab7-132">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="aeab7-132">ConstructorString</span></span>](#constructorstring)
-   [<span data-ttu-id="aeab7-133">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="aeab7-133">CreationTimeout</span></span>](#creationtimeout)
-   [<span data-ttu-id="aeab7-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-134">Description</span></span>](#description)
-   [<span data-ttu-id="aeab7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="aeab7-135">DLL</span></span>](#dll)
-   [<span data-ttu-id="aeab7-136">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-136">EventTrackingEnabled</span></span>](#eventtrackingenabled)
-   [<span data-ttu-id="aeab7-137">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="aeab7-137">ExceptionClass</span></span>](#exceptionclass)
-   [<span data-ttu-id="aeab7-138">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="aeab7-138">FireInParallel</span></span>](#fireinparallel)
-   [<span data-ttu-id="aeab7-139">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="aeab7-139">IISIntrinsics</span></span>](#iisintrinsics)
-   [<span data-ttu-id="aeab7-140">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="aeab7-140">InitializeServerApplication</span></span>](#initializeserverapplication)
-   [<span data-ttu-id="aeab7-141">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-141">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="aeab7-142">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="aeab7-142">IsEventClass</span></span>](#iseventclass)
-   [<span data-ttu-id="aeab7-143">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="aeab7-143">IsInstalled</span></span>](#isinstalled)
-   [<span data-ttu-id="aeab7-144">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="aeab7-144">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="aeab7-145">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="aeab7-145">JustInTimeActivation</span></span>](#justintimeactivation)
-   [<span data-ttu-id="aeab7-146">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="aeab7-146">LoadBalancingSupported</span></span>](#loadbalancingsupported)
-   [<span data-ttu-id="aeab7-147">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="aeab7-147">MaxPoolSize</span></span>](#maxpoolsize)
-   [<span data-ttu-id="aeab7-148">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="aeab7-148">MinPoolSize</span></span>](#minpoolsize)
-   [<span data-ttu-id="aeab7-149">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="aeab7-149">MultiInterfacePublisherFilterCLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="aeab7-150">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="aeab7-150">MustRunInClientContext</span></span>](#mustruninclientcontext)
-   [<span data-ttu-id="aeab7-151">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="aeab7-151">MustRunInDefaultContext</span></span>](#mustrunindefaultcontext)
-   [<span data-ttu-id="aeab7-152">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-152">ObjectPoolingEnabled</span></span>](#objectpoolingenabled)
-   [<span data-ttu-id="aeab7-153">ProgID</span><span class="sxs-lookup"><span data-stu-id="aeab7-153">ProgID</span></span>](#progid)
-   [<span data-ttu-id="aeab7-154">PublisherID</span><span class="sxs-lookup"><span data-stu-id="aeab7-154">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="aeab7-155">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="aeab7-155">SoapAssemblyName</span></span>](#soapassemblyname)
-   [<span data-ttu-id="aeab7-156">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="aeab7-156">SoapTypeName</span></span>](#soaptypename)
-   [<span data-ttu-id="aeab7-157">Sincronización</span><span class="sxs-lookup"><span data-stu-id="aeab7-157">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="aeab7-158">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="aeab7-158">ThreadingModel</span></span>](#threadingmodel)
-   [<span data-ttu-id="aeab7-159">Transacción</span><span class="sxs-lookup"><span data-stu-id="aeab7-159">Transaction</span></span>](#componenttransactiontimeout)
-   [<span data-ttu-id="aeab7-160">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="aeab7-160">TxIsolationLevel</span></span>](#txisolationlevel)
-   [<span data-ttu-id="aeab7-161">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="aeab7-161">VersionBuild</span></span>](#versionbuild)
-   [<span data-ttu-id="aeab7-162">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="aeab7-162">VersionMajor</span></span>](#versionmajor)
-   [<span data-ttu-id="aeab7-163">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="aeab7-163">VersionMinor</span></span>](#versionminor)
-   [<span data-ttu-id="aeab7-164">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="aeab7-164">VersionSubBuild</span></span>](#versionsubbuild)

### <a name="allowinprocsubscribers"></a><span data-ttu-id="aeab7-165">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="aeab7-165">AllowInprocSubscribers</span></span>



| <span data-ttu-id="aeab7-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-166">Entry</span></span> | <span data-ttu-id="aeab7-167">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-167">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="aeab7-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-168">Description</span></span>    | <span data-ttu-id="aeab7-169">Habilita en los suscriptores de proceso si el componente es una clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-169">Enables in process subscribers if the component is an event class.</span></span> |
| <span data-ttu-id="aeab7-170">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-170">Access</span></span>         | <span data-ttu-id="aeab7-171">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-171">ReadWrite</span></span>                                                          |
| <span data-ttu-id="aeab7-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-172">Type</span></span>           | <span data-ttu-id="aeab7-173">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-173">Bool</span></span>                                                               |
| <span data-ttu-id="aeab7-174">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-174">Default</span></span>        | <span data-ttu-id="aeab7-175">True</span><span class="sxs-lookup"><span data-stu-id="aeab7-175">True</span></span>                                                               |
| <span data-ttu-id="aeab7-176">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-176">Minimum system</span></span> | <span data-ttu-id="aeab7-177">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-177">Windows 2000</span></span>                                                       |



 

### <a name="applicationid"></a><span data-ttu-id="aeab7-178">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="aeab7-178">ApplicationID</span></span>



| <span data-ttu-id="aeab7-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-179">Entry</span></span> | <span data-ttu-id="aeab7-180">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-180">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-181">Description</span></span>    | <span data-ttu-id="aeab7-182">GUID de la aplicación que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-182">The GUID for the application containing the component.</span></span> <span data-ttu-id="aeab7-183">Debe ser un GUID de aplicación válido, que se comprueba antes de que se llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="aeab7-183">Must be a valid application's GUID, which is verified before [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) is called.</span></span> <span data-ttu-id="aeab7-184">Si este valor se cambia para ser un GUID para una aplicación diferente, el componente se mueve a esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeab7-184">If this value is changed to be a GUID for a different application, the component moves to that application.</span></span> |
| <span data-ttu-id="aeab7-185">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-185">Access</span></span>         | <span data-ttu-id="aeab7-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-186">ReadWrite</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="aeab7-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-187">Type</span></span>           | <span data-ttu-id="aeab7-188">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-188">String</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="aeab7-189">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-189">Default</span></span>        | <span data-ttu-id="aeab7-190">N/D</span><span class="sxs-lookup"><span data-stu-id="aeab7-190">N/A</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="aeab7-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-191">Minimum system</span></span> | <span data-ttu-id="aeab7-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-192">Windows 2000</span></span>                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a><span data-ttu-id="aeab7-193">Valor de bits</span><span class="sxs-lookup"><span data-stu-id="aeab7-193">Bitness</span></span>



| <span data-ttu-id="aeab7-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-194">Entry</span></span> | <span data-ttu-id="aeab7-195">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-195">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-196">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-196">Description</span></span>    | <span data-ttu-id="aeab7-197">Representa el tipo de bits binario de un componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-197">Represents the binary bitness type of a component.</span></span> <span data-ttu-id="aeab7-198">En los sistemas que usan Windows de 64 bits, esta propiedad distingue entre los componentes de 64 bits y los componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aeab7-198">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="aeab7-199">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-199">Access</span></span>         | <span data-ttu-id="aeab7-200">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-200">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="aeab7-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-201">Type</span></span>           | <span data-ttu-id="aeab7-202">Valores posibles largos: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)</span><span class="sxs-lookup"><span data-stu-id="aeab7-202">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                       |
| <span data-ttu-id="aeab7-203">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-203">Default</span></span>        | <span data-ttu-id="aeab7-204">N/D</span><span class="sxs-lookup"><span data-stu-id="aeab7-204">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="aeab7-205">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-205">Minimum system</span></span> | <span data-ttu-id="aeab7-206">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aeab7-206">Windows XP</span></span>                                                                                                                                                          |



 

### <a name="clsid"></a><span data-ttu-id="aeab7-207">CLSID</span><span class="sxs-lookup"><span data-stu-id="aeab7-207">CLSID</span></span>



| <span data-ttu-id="aeab7-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-208">Entry</span></span> | <span data-ttu-id="aeab7-209">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-209">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-210">Description</span></span>    | <span data-ttu-id="aeab7-211">GUID del componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-211">A GUID for the component.</span></span> <span data-ttu-id="aeab7-212">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="aeab7-212">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="aeab7-213">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-213">Access</span></span>         | <span data-ttu-id="aeab7-214">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-214">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="aeab7-215">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-215">Type</span></span>           | <span data-ttu-id="aeab7-216">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-216">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="aeab7-217">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-217">Default</span></span>        | <span data-ttu-id="aeab7-218">N/D</span><span class="sxs-lookup"><span data-stu-id="aeab7-218">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="aeab7-219">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-219">Minimum system</span></span> | <span data-ttu-id="aeab7-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-220">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a><span data-ttu-id="aeab7-221">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-221">ComponentAccessChecksEnabled</span></span>



| <span data-ttu-id="aeab7-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-222">Entry</span></span> | <span data-ttu-id="aeab7-223">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-223">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-224">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-224">Description</span></span>    | <span data-ttu-id="aeab7-225">Indica si las comprobaciones de acceso basadas en roles se realizan en llamadas al componente y funcionan junto con las propiedades AccessChecksLevel y ApplicationAccessChecksEnabled en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeab7-225">Indicates whether role-based access checks are performed on calls into the component and works in conjunction with the AccessChecksLevel and ApplicationAccessChecksEnabled properties on the application.</span></span> |
| <span data-ttu-id="aeab7-226">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-226">Access</span></span>         | <span data-ttu-id="aeab7-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-227">ReadWrite</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="aeab7-228">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-228">Type</span></span>           | <span data-ttu-id="aeab7-229">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-229">Bool</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="aeab7-230">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-230">Default</span></span>        | <span data-ttu-id="aeab7-231">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-231">False</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="aeab7-232">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-232">Minimum system</span></span> | <span data-ttu-id="aeab7-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-233">Windows 2000</span></span>                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a><span data-ttu-id="aeab7-234">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="aeab7-234">ComponentTransactionTimeout</span></span>



| <span data-ttu-id="aeab7-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-235">Entry</span></span> | <span data-ttu-id="aeab7-236">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-236">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-237">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-237">Description</span></span>    | <span data-ttu-id="aeab7-238">Cuando se utiliza en una transacción, especifica el período de tiempo en el que este componente hace que se agote el tiempo de espera de la transacción. El valor predeterminado es 60 segundos y no puede ser superior a 3600 segundos (1 hora).</span><span class="sxs-lookup"><span data-stu-id="aeab7-238">When used in a transaction, specifies the time period in which this component causes the transaction to time out. The default is 60 seconds and cannot be longer than 3600 seconds (1 hour).</span></span> <span data-ttu-id="aeab7-239">El valor de tiempo de espera se puede establecer en 0, especificando un período de tiempo de espera de transacción infinito.</span><span class="sxs-lookup"><span data-stu-id="aeab7-239">The time-out value can be set to 0, specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="aeab7-240">Para usar esta propiedad, ComponentTransactionTimeoutEnabled debe ser true.</span><span class="sxs-lookup"><span data-stu-id="aeab7-240">For this property to be used, ComponentTransactionTimeoutEnabled must be True.</span></span> <span data-ttu-id="aeab7-241">El valor de esta propiedad invalida el tiempo de espera de la transacción global especificado por la propiedad TransactionTimeout de la colección [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="aeab7-241">The value of this property overrides the global transaction time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection.</span></span> |
| <span data-ttu-id="aeab7-242">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-242">Access</span></span>         | <span data-ttu-id="aeab7-243">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-243">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="aeab7-244">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-244">Type</span></span>           | <span data-ttu-id="aeab7-245">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="aeab7-245">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="aeab7-246">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-246">Default</span></span>        | <span data-ttu-id="aeab7-247">60</span><span class="sxs-lookup"><span data-stu-id="aeab7-247">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="aeab7-248">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-248">Minimum system</span></span> | <span data-ttu-id="aeab7-249">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-249">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a><span data-ttu-id="aeab7-250">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-250">ComponentTransactionTimeoutEnabled</span></span>



| <span data-ttu-id="aeab7-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-251">Entry</span></span> | <span data-ttu-id="aeab7-252">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-252">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-253">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-253">Description</span></span>    | <span data-ttu-id="aeab7-254">Especifica si el período de tiempo de espera de la transacción está habilitado para este componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-254">Specifies whether the transaction time-out period is enabled for this component.</span></span> <span data-ttu-id="aeab7-255">De forma predeterminada, la característica de tiempo de espera de la transacción está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="aeab7-255">By default, the transaction time-out feature is disabled.</span></span> <span data-ttu-id="aeab7-256">Cuando esta propiedad es true, se usa el tiempo de espera especificado por ComponentTransactionTimeout.</span><span class="sxs-lookup"><span data-stu-id="aeab7-256">When this property is True, the time-out specified by ComponentTransactionTimeout is used.</span></span> <span data-ttu-id="aeab7-257">Cuando esta propiedad es false, se usa el tiempo de espera especificado por la propiedad TransactionTimeout de la colección [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="aeab7-257">When this property is False, the time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="aeab7-258">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-258">Access</span></span>         | <span data-ttu-id="aeab7-259">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-259">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="aeab7-260">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-260">Type</span></span>           | <span data-ttu-id="aeab7-261">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-261">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="aeab7-262">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-262">Default</span></span>        | <span data-ttu-id="aeab7-263">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-263">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="aeab7-264">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-264">Minimum system</span></span> | <span data-ttu-id="aeab7-265">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-265">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a><span data-ttu-id="aeab7-266">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="aeab7-266">COMTIIntrinsics</span></span>



| <span data-ttu-id="aeab7-267">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-267">Entry</span></span> | <span data-ttu-id="aeab7-268">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-268">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-269">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-269">Description</span></span>    | <span data-ttu-id="aeab7-270">Permite pasar propiedades de contexto desde el integrador de transacciones COM (COMTI) al contexto de esta clase.</span><span class="sxs-lookup"><span data-stu-id="aeab7-270">Enables passing of context properties from the COM Transaction Integrator (COMTI) into the context for this class.</span></span> <span data-ttu-id="aeab7-271">El COMTI facilita la tarea de envolver transacciones de gran sistema y lógica de negocios como componentes COM.</span><span class="sxs-lookup"><span data-stu-id="aeab7-271">The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.</span></span> |
| <span data-ttu-id="aeab7-272">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-272">Access</span></span>         | <span data-ttu-id="aeab7-273">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-273">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="aeab7-274">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-274">Type</span></span>           | <span data-ttu-id="aeab7-275">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-275">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="aeab7-276">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-276">Default</span></span>        | <span data-ttu-id="aeab7-277">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-277">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="aeab7-278">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-278">Minimum system</span></span> | <span data-ttu-id="aeab7-279">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-279">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a><span data-ttu-id="aeab7-280">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-280">ConstructionEnabled</span></span>



| <span data-ttu-id="aeab7-281">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-281">Entry</span></span> | <span data-ttu-id="aeab7-282">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-282">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-283">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-283">Description</span></span>    | <span data-ttu-id="aeab7-284">Determina si el ConstructorString se pasa al objeto cuando se construye.</span><span class="sxs-lookup"><span data-stu-id="aeab7-284">Determines whether the ConstructorString is passed to the object when it is constructed.</span></span> |
| <span data-ttu-id="aeab7-285">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-285">Access</span></span>         | <span data-ttu-id="aeab7-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-286">ReadWrite</span></span>                                                                                |
| <span data-ttu-id="aeab7-287">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-287">Type</span></span>           | <span data-ttu-id="aeab7-288">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-288">Bool</span></span>                                                                                     |
| <span data-ttu-id="aeab7-289">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-289">Default</span></span>        | <span data-ttu-id="aeab7-290">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-290">False</span></span>                                                                                    |
| <span data-ttu-id="aeab7-291">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-291">Minimum system</span></span> | <span data-ttu-id="aeab7-292">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-292">Windows 2000</span></span>                                                                             |



 

### <a name="constructorstring"></a><span data-ttu-id="aeab7-293">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="aeab7-293">ConstructorString</span></span>



| <span data-ttu-id="aeab7-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-294">Entry</span></span> | <span data-ttu-id="aeab7-295">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-295">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-296">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-296">Description</span></span>    | <span data-ttu-id="aeab7-297">Cadena de inicialización para la construcción de componentes.</span><span class="sxs-lookup"><span data-stu-id="aeab7-297">Initialization string for component construction.</span></span> <span data-ttu-id="aeab7-298">Puede crear objetos diferentes del mismo componente genérico mediante cadenas de constructor de objeto.</span><span class="sxs-lookup"><span data-stu-id="aeab7-298">You can create different objects from the same generic component by using object constructor strings.</span></span> <span data-ttu-id="aeab7-299">Si ConstructionEnabled es false, se omite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="aeab7-299">If ConstructionEnabled is False, this property is ignored.</span></span> |
| <span data-ttu-id="aeab7-300">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-300">Access</span></span>         | <span data-ttu-id="aeab7-301">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-301">ReadWrite</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="aeab7-302">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-302">Type</span></span>           | <span data-ttu-id="aeab7-303">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-303">String</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="aeab7-304">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-304">Default</span></span>        | <span data-ttu-id="aeab7-305">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-305">""</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="aeab7-306">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-306">Minimum system</span></span> | <span data-ttu-id="aeab7-307">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-307">Windows 2000</span></span>                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a><span data-ttu-id="aeab7-308">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="aeab7-308">CreationTimeout</span></span>



| <span data-ttu-id="aeab7-309">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-309">Entry</span></span> | <span data-ttu-id="aeab7-310">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-310">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-311">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-311">Description</span></span>    | <span data-ttu-id="aeab7-312">Al crear el objeto, se devuelve el número de milisegundos antes de que se devuelva un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="aeab7-312">When creating the object, number of milliseconds before a time-out error is returned.</span></span> <span data-ttu-id="aeab7-313">El tiempo de espera máximo es de 2147483647 milisegundos (unos 25 días).</span><span class="sxs-lookup"><span data-stu-id="aeab7-313">The maximum time-out is 2147483647 milliseconds (about 25 days).</span></span> |
| <span data-ttu-id="aeab7-314">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-314">Access</span></span>         | <span data-ttu-id="aeab7-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-315">ReadWrite</span></span>                                                                                                                                              |
| <span data-ttu-id="aeab7-316">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-316">Type</span></span>           | <span data-ttu-id="aeab7-317">Long (0-2147483647)</span><span class="sxs-lookup"><span data-stu-id="aeab7-317">Long (0-2147483647)</span></span>                                                                                                                                    |
| <span data-ttu-id="aeab7-318">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-318">Default</span></span>        | <span data-ttu-id="aeab7-319">0</span><span class="sxs-lookup"><span data-stu-id="aeab7-319">0</span></span>                                                                                                                                                      |
| <span data-ttu-id="aeab7-320">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-320">Minimum system</span></span> | <span data-ttu-id="aeab7-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-321">Windows 2000</span></span>                                                                                                                                           |



 

### <a name="description"></a><span data-ttu-id="aeab7-322">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-322">Description</span></span>



| <span data-ttu-id="aeab7-323">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-323">Entry</span></span> | <span data-ttu-id="aeab7-324">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-324">Value</span></span> |
|----------------|--------------------------|
| <span data-ttu-id="aeab7-325">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-325">Description</span></span>    | <span data-ttu-id="aeab7-326">Describe el componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-326">Describes the component.</span></span> |
| <span data-ttu-id="aeab7-327">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-327">Access</span></span>         | <span data-ttu-id="aeab7-328">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-328">ReadWrite</span></span>                |
| <span data-ttu-id="aeab7-329">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-329">Type</span></span>           | <span data-ttu-id="aeab7-330">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-330">String</span></span>                   |
| <span data-ttu-id="aeab7-331">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-331">Default</span></span>        | <span data-ttu-id="aeab7-332">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-332">""</span></span>                       |
| <span data-ttu-id="aeab7-333">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-333">Minimum system</span></span> | <span data-ttu-id="aeab7-334">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-334">Windows 2000</span></span>             |



 

### <a name="dll"></a><span data-ttu-id="aeab7-335">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aeab7-335">DLL</span></span>



| <span data-ttu-id="aeab7-336">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-336">Entry</span></span> | <span data-ttu-id="aeab7-337">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-337">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="aeab7-338">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-338">Description</span></span>    | <span data-ttu-id="aeab7-339">Nombre y ruta de acceso del archivo que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-339">The name and path of the file containing the component.</span></span> |
| <span data-ttu-id="aeab7-340">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-340">Access</span></span>         | <span data-ttu-id="aeab7-341">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-341">ReadOnly</span></span>                                                |
| <span data-ttu-id="aeab7-342">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-342">Type</span></span>           | <span data-ttu-id="aeab7-343">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-343">String</span></span>                                                  |
| <span data-ttu-id="aeab7-344">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-344">Default</span></span>        | <span data-ttu-id="aeab7-345">N/D</span><span class="sxs-lookup"><span data-stu-id="aeab7-345">N/A</span></span>                                                     |
| <span data-ttu-id="aeab7-346">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-346">Minimum system</span></span> | <span data-ttu-id="aeab7-347">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-347">Windows 2000</span></span>                                            |



 

### <a name="eventtrackingenabled"></a><span data-ttu-id="aeab7-348">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-348">EventTrackingEnabled</span></span>



| <span data-ttu-id="aeab7-349">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-349">Entry</span></span> | <span data-ttu-id="aeab7-350">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-350">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-351">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-351">Description</span></span>    | <span data-ttu-id="aeab7-352">Determina si se realiza el seguimiento de los eventos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-352">Determines whether events are tracked.</span></span> <span data-ttu-id="aeab7-353">Los eventos incluyen acciones como el cierre de la aplicación; creación y liberación de objetos; referencias a objetos, coherencia, activación y desactivación; llamadas al método, devuelve y excepciones; Inicio de la transacción, preparación para confirmar y anular; conexión, asignación y reciclaje del dispensador de recursos; asignación y reciclaje de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-353">Events include actions such as application shutdown; object creation and release; object references, consistency, activation, and deactivation; method calls, returns, and exceptions; transaction startup, preparing to commit, and abort; resource dispenser connection, allocation, and recycling; thread allocation and recycling.</span></span> |
| <span data-ttu-id="aeab7-354">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-354">Access</span></span>         | <span data-ttu-id="aeab7-355">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-355">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="aeab7-356">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-356">Type</span></span>           | <span data-ttu-id="aeab7-357">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-357">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="aeab7-358">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-358">Default</span></span>        | <span data-ttu-id="aeab7-359">True</span><span class="sxs-lookup"><span data-stu-id="aeab7-359">True</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="aeab7-360">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-360">Minimum system</span></span> | <span data-ttu-id="aeab7-361">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-361">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a><span data-ttu-id="aeab7-362">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="aeab7-362">ExceptionClass</span></span>



| <span data-ttu-id="aeab7-363">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-363">Entry</span></span> | <span data-ttu-id="aeab7-364">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-364">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-365">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-365">Description</span></span>    | <span data-ttu-id="aeab7-366">El CLSID, que puede ser un GUID o una cadena de moniker, para activar un programa alternativo durante el proceso de tratar con un programa de componentes en cola con errores repetidamente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-366">The CLSID, which can be a GUID or a moniker string, to activate an alternative program during the process of dealing with a repeatedly failing queued components program.</span></span> |
| <span data-ttu-id="aeab7-367">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-367">Access</span></span>         | <span data-ttu-id="aeab7-368">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-368">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="aeab7-369">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-369">Type</span></span>           | <span data-ttu-id="aeab7-370">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-370">String</span></span>                                                                                                                                                                    |
| <span data-ttu-id="aeab7-371">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-371">Default</span></span>        | <span data-ttu-id="aeab7-372">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-372">""</span></span>                                                                                                                                                                        |
| <span data-ttu-id="aeab7-373">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-373">Minimum system</span></span> | <span data-ttu-id="aeab7-374">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-374">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="fireinparallel"></a><span data-ttu-id="aeab7-375">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="aeab7-375">FireInParallel</span></span>



| <span data-ttu-id="aeab7-376">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-376">Entry</span></span> | <span data-ttu-id="aeab7-377">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-377">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-378">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-378">Description</span></span>    | <span data-ttu-id="aeab7-379">Permite que los eventos se activen en paralelo si el componente es una clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-379">Enables events to be fired in parallel if the component is an event class.</span></span> |
| <span data-ttu-id="aeab7-380">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-380">Access</span></span>         | <span data-ttu-id="aeab7-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-381">ReadWrite</span></span>                                                                  |
| <span data-ttu-id="aeab7-382">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-382">Type</span></span>           | <span data-ttu-id="aeab7-383">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-383">Bool</span></span>                                                                       |
| <span data-ttu-id="aeab7-384">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-384">Default</span></span>        | <span data-ttu-id="aeab7-385">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-385">False</span></span>                                                                      |
| <span data-ttu-id="aeab7-386">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-386">Minimum system</span></span> | <span data-ttu-id="aeab7-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-387">Windows 2000</span></span>                                                               |



 

### <a name="iisintrinsics"></a><span data-ttu-id="aeab7-388">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="aeab7-388">IISIntrinsics</span></span>



| <span data-ttu-id="aeab7-389">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-389">Entry</span></span> | <span data-ttu-id="aeab7-390">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-391">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-391">Description</span></span>    | <span data-ttu-id="aeab7-392">Habilita el paso de propiedades de contexto de IIS, como un objeto de sesión de aplicación o un objeto de sesión de usuario, en el contexto de esta clase.</span><span class="sxs-lookup"><span data-stu-id="aeab7-392">Enables passing of IIS context properties, such as an application session object or a user session object, into the context for this class.</span></span> |
| <span data-ttu-id="aeab7-393">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-393">Access</span></span>         | <span data-ttu-id="aeab7-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-394">ReadWrite</span></span>                                                                                                                                   |
| <span data-ttu-id="aeab7-395">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-395">Type</span></span>           | <span data-ttu-id="aeab7-396">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-396">Bool</span></span>                                                                                                                                        |
| <span data-ttu-id="aeab7-397">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-397">Default</span></span>        | <span data-ttu-id="aeab7-398">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-398">False</span></span>                                                                                                                                       |
| <span data-ttu-id="aeab7-399">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-399">Minimum system</span></span> | <span data-ttu-id="aeab7-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-400">Windows 2000</span></span>                                                                                                                                |



 

### <a name="initializeserverapplication"></a><span data-ttu-id="aeab7-401">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="aeab7-401">InitializeServerApplication</span></span>



| <span data-ttu-id="aeab7-402">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-402">Entry</span></span> | <span data-ttu-id="aeab7-403">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-403">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-404">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-404">Description</span></span>    | <span data-ttu-id="aeab7-405">Indica si el componente se utiliza para inicializar una aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="aeab7-405">Indicates whether the component is used to initialize a server application.</span></span> |
| <span data-ttu-id="aeab7-406">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-406">Access</span></span>         | <span data-ttu-id="aeab7-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-407">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="aeab7-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-408">Type</span></span>           | <span data-ttu-id="aeab7-409">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-409">Bool</span></span>                                                                        |
| <span data-ttu-id="aeab7-410">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-410">Default</span></span>        | <span data-ttu-id="aeab7-411">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-411">False</span></span>                                                                       |
| <span data-ttu-id="aeab7-412">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-412">Minimum system</span></span> | <span data-ttu-id="aeab7-413">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aeab7-413">Windows Server 2003</span></span>                                                         |



 

### <a name="isenabled"></a><span data-ttu-id="aeab7-414">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-414">IsEnabled</span></span>



| <span data-ttu-id="aeab7-415">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-415">Entry</span></span> | <span data-ttu-id="aeab7-416">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-416">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-417">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-417">Description</span></span>    | <span data-ttu-id="aeab7-418">False si el componente o la aplicación COM+ están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="aeab7-418">False if the COM+ application or component is disabled.</span></span> <span data-ttu-id="aeab7-419">Si el componente o la aplicación COM+ está habilitado, IsEnabled es true.</span><span class="sxs-lookup"><span data-stu-id="aeab7-419">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="aeab7-420">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-420">Access</span></span>         | <span data-ttu-id="aeab7-421">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-421">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="aeab7-422">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-422">Type</span></span>           | <span data-ttu-id="aeab7-423">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-423">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="aeab7-424">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-424">Default</span></span>        | <span data-ttu-id="aeab7-425">True</span><span class="sxs-lookup"><span data-stu-id="aeab7-425">True</span></span>                                                                                                                        |
| <span data-ttu-id="aeab7-426">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-426">Minimum system</span></span> | <span data-ttu-id="aeab7-427">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aeab7-427">Windows XP</span></span>                                                                                                                  |



 

### <a name="iseventclass"></a><span data-ttu-id="aeab7-428">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="aeab7-428">IsEventClass</span></span>



| <span data-ttu-id="aeab7-429">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-429">Entry</span></span> | <span data-ttu-id="aeab7-430">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-430">Value</span></span> |
|----------------|----------------------------------------------------|
| <span data-ttu-id="aeab7-431">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-431">Description</span></span>    | <span data-ttu-id="aeab7-432">Indica si el componente es una clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-432">Indicates whether the component is an event class.</span></span> |
| <span data-ttu-id="aeab7-433">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-433">Access</span></span>         | <span data-ttu-id="aeab7-434">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-434">ReadOnly</span></span>                                           |
| <span data-ttu-id="aeab7-435">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-435">Type</span></span>           | <span data-ttu-id="aeab7-436">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-436">Bool</span></span>                                               |
| <span data-ttu-id="aeab7-437">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-437">Default</span></span>        | <span data-ttu-id="aeab7-438">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-438">False</span></span>                                              |
| <span data-ttu-id="aeab7-439">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-439">Minimum system</span></span> | <span data-ttu-id="aeab7-440">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-440">Windows 2000</span></span>                                       |



 

### <a name="isinstalled"></a><span data-ttu-id="aeab7-441">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="aeab7-441">IsInstalled</span></span>



| <span data-ttu-id="aeab7-442">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-442">Entry</span></span> | <span data-ttu-id="aeab7-443">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-443">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="aeab7-444">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-444">Description</span></span>    | <span data-ttu-id="aeab7-445">Indica si el componente está instalado en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeab7-445">Indicates whether the component is installed in an application.</span></span> |
| <span data-ttu-id="aeab7-446">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-446">Access</span></span>         | <span data-ttu-id="aeab7-447">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-447">ReadOnly</span></span>                                                        |
| <span data-ttu-id="aeab7-448">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-448">Type</span></span>           | <span data-ttu-id="aeab7-449">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-449">Bool</span></span>                                                            |
| <span data-ttu-id="aeab7-450">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-450">Default</span></span>        | <span data-ttu-id="aeab7-451">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-451">False</span></span>                                                           |
| <span data-ttu-id="aeab7-452">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-452">Minimum system</span></span> | <span data-ttu-id="aeab7-453">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aeab7-453">Windows Server 2003</span></span>                                             |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="aeab7-454">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="aeab7-454">IsPrivateComponent</span></span>



| <span data-ttu-id="aeab7-455">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-455">Entry</span></span> | <span data-ttu-id="aeab7-456">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-456">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-457">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-457">Description</span></span>    | <span data-ttu-id="aeab7-458">Determina si una aplicación de servidor es un componente privado.</span><span class="sxs-lookup"><span data-stu-id="aeab7-458">Determines whether a server application is a private component.</span></span> <span data-ttu-id="aeab7-459">Un componente privado en una aplicación de servidor solo se puede activar desde dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeab7-459">A private component in a server application can be activated only from within the application.</span></span> <span data-ttu-id="aeab7-460">Por ejemplo, si llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en un componente privado, se produce un error de fuera de proceso pero se realiza correctamente en proceso.</span><span class="sxs-lookup"><span data-stu-id="aeab7-460">For example, if you call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on a private component, it fails from out-of-process but succeeds in-process.</span></span> <span data-ttu-id="aeab7-461">Por el contrario, si llama a **CoCreateInstance** en un componente público, se realizará correctamente en proceso y fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="aeab7-461">In contrast, if you call **CoCreateInstance** on a public component, it succeeds both in-process and out-of-process.</span></span> |
| <span data-ttu-id="aeab7-462">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-462">Access</span></span>         | <span data-ttu-id="aeab7-463">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-463">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="aeab7-464">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-464">Type</span></span>           | <span data-ttu-id="aeab7-465">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-465">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="aeab7-466">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-466">Default</span></span>        | <span data-ttu-id="aeab7-467">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-467">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="aeab7-468">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-468">Minimum system</span></span> | <span data-ttu-id="aeab7-469">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aeab7-469">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a><span data-ttu-id="aeab7-470">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="aeab7-470">JustInTimeActivation</span></span>



| <span data-ttu-id="aeab7-471">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-471">Entry</span></span> | <span data-ttu-id="aeab7-472">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-472">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-473">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-473">Description</span></span>    | <span data-ttu-id="aeab7-474">Determina si la [activación JIT](enabling-jit-activation-for-a-component.md) está habilitada para el componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-474">Determines whether [JIT activation](enabling-jit-activation-for-a-component.md) is enabled for the component.</span></span> <span data-ttu-id="aeab7-475">Esta propiedad se establece en true cuando la [compatibilidad con transacciones](setting-the-transaction-attribute.md) está establecida en Required, requiere New o Supported.</span><span class="sxs-lookup"><span data-stu-id="aeab7-475">This property is set to True when [transaction support](setting-the-transaction-attribute.md) is set to Required, Requires New, or Supported.</span></span> <span data-ttu-id="aeab7-476">Cuando JustInTimeActivation se establece en true, la [compatibilidad con la sincronización](setting-the-synchronization-attribute.md) debe establecerse en Required (el valor predeterminado) o requiere New.</span><span class="sxs-lookup"><span data-stu-id="aeab7-476">When JustInTimeActivation is set to True, [synchronization support](setting-the-synchronization-attribute.md) must be set to Required (the default) or Requires New.</span></span> |
| <span data-ttu-id="aeab7-477">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-477">Access</span></span>         | <span data-ttu-id="aeab7-478">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-478">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="aeab7-479">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-479">Type</span></span>           | <span data-ttu-id="aeab7-480">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-480">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="aeab7-481">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-481">Default</span></span>        | <span data-ttu-id="aeab7-482">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-482">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="aeab7-483">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-483">Minimum system</span></span> | <span data-ttu-id="aeab7-484">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-484">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a><span data-ttu-id="aeab7-485">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="aeab7-485">LoadBalancingSupported</span></span>



| <span data-ttu-id="aeab7-486">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-486">Entry</span></span> | <span data-ttu-id="aeab7-487">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-487">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-488">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-488">Description</span></span>    | <span data-ttu-id="aeab7-489">Si el servicio de equilibrio de carga de componentes está instalado y habilitado en el servidor, determina si el componente participa en el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="aeab7-489">If the component load balancing service is installed and enabled on the server, determines whether the component participates in load balancing.</span></span> |
| <span data-ttu-id="aeab7-490">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-490">Access</span></span>         | <span data-ttu-id="aeab7-491">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-491">ReadWrite</span></span>                                                                                                                                        |
| <span data-ttu-id="aeab7-492">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-492">Type</span></span>           | <span data-ttu-id="aeab7-493">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-493">Bool</span></span>                                                                                                                                             |
| <span data-ttu-id="aeab7-494">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-494">Default</span></span>        | <span data-ttu-id="aeab7-495">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-495">False</span></span>                                                                                                                                            |
| <span data-ttu-id="aeab7-496">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-496">Minimum system</span></span> | <span data-ttu-id="aeab7-497">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-497">Windows 2000</span></span>                                                                                                                                     |



 

### <a name="maxpoolsize"></a><span data-ttu-id="aeab7-498">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="aeab7-498">MaxPoolSize</span></span>



| <span data-ttu-id="aeab7-499">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-499">Entry</span></span> | <span data-ttu-id="aeab7-500">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-500">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="aeab7-501">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-501">Description</span></span>    | <span data-ttu-id="aeab7-502">Número máximo de objetos agrupados.</span><span class="sxs-lookup"><span data-stu-id="aeab7-502">Maximum number of objects pooled.</span></span> |
| <span data-ttu-id="aeab7-503">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-503">Access</span></span>         | <span data-ttu-id="aeab7-504">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-504">ReadWrite</span></span>                         |
| <span data-ttu-id="aeab7-505">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-505">Type</span></span>           | <span data-ttu-id="aeab7-506">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="aeab7-506">Long (1-1048576)</span></span>                  |
| <span data-ttu-id="aeab7-507">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-507">Default</span></span>        | <span data-ttu-id="aeab7-508">1 048 576</span><span class="sxs-lookup"><span data-stu-id="aeab7-508">1048576</span></span>                           |
| <span data-ttu-id="aeab7-509">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-509">Minimum system</span></span> | <span data-ttu-id="aeab7-510">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-510">Windows 2000</span></span>                      |



 

### <a name="minpoolsize"></a><span data-ttu-id="aeab7-511">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="aeab7-511">MinPoolSize</span></span>



| <span data-ttu-id="aeab7-512">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-512">Entry</span></span> | <span data-ttu-id="aeab7-513">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-513">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="aeab7-514">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-514">Description</span></span>    | <span data-ttu-id="aeab7-515">Número mínimo de objetos agrupados.</span><span class="sxs-lookup"><span data-stu-id="aeab7-515">Minimum number of objects pooled.</span></span> |
| <span data-ttu-id="aeab7-516">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-516">Access</span></span>         | <span data-ttu-id="aeab7-517">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-517">ReadWrite</span></span>                         |
| <span data-ttu-id="aeab7-518">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-518">Type</span></span>           | <span data-ttu-id="aeab7-519">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="aeab7-519">Long (0-1048576)</span></span>                  |
| <span data-ttu-id="aeab7-520">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-520">Default</span></span>        | <span data-ttu-id="aeab7-521">0</span><span class="sxs-lookup"><span data-stu-id="aeab7-521">0</span></span>                                 |
| <span data-ttu-id="aeab7-522">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-522">Minimum system</span></span> | <span data-ttu-id="aeab7-523">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-523">Windows 2000</span></span>                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a><span data-ttu-id="aeab7-524">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="aeab7-524">MultiInterfacePublisherFilterCLSID</span></span>



| <span data-ttu-id="aeab7-525">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-525">Entry</span></span> | <span data-ttu-id="aeab7-526">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-526">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-527">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-527">Description</span></span>    | <span data-ttu-id="aeab7-528">CLSID del filtro de publicador utilizado si el componente es una clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-528">CLSID for the publisher filter used if the component is an event class.</span></span> |
| <span data-ttu-id="aeab7-529">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-529">Access</span></span>         | <span data-ttu-id="aeab7-530">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-530">ReadWrite</span></span>                                                               |
| <span data-ttu-id="aeab7-531">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-531">Type</span></span>           | <span data-ttu-id="aeab7-532">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-532">String</span></span>                                                                  |
| <span data-ttu-id="aeab7-533">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-533">Default</span></span>        | <span data-ttu-id="aeab7-534">N/D</span><span class="sxs-lookup"><span data-stu-id="aeab7-534">N/A</span></span>                                                                     |
| <span data-ttu-id="aeab7-535">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-535">Minimum system</span></span> | <span data-ttu-id="aeab7-536">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-536">Windows 2000</span></span>                                                            |



 

### <a name="mustruninclientcontext"></a><span data-ttu-id="aeab7-537">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="aeab7-537">MustRunInClientContext</span></span>



| <span data-ttu-id="aeab7-538">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-538">Entry</span></span> | <span data-ttu-id="aeab7-539">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-539">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-540">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-540">Description</span></span>    | <span data-ttu-id="aeab7-541">Indica que el componente debe activarse en el contexto del autor de la llamada original.</span><span class="sxs-lookup"><span data-stu-id="aeab7-541">Indicates that component must be activated in its original caller's context.</span></span> <span data-ttu-id="aeab7-542">De lo contrario, se produce un error en la activación.</span><span class="sxs-lookup"><span data-stu-id="aeab7-542">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="aeab7-543">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-543">Access</span></span>         | <span data-ttu-id="aeab7-544">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-544">ReadWrite</span></span>                                                                                                 |
| <span data-ttu-id="aeab7-545">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-545">Type</span></span>           | <span data-ttu-id="aeab7-546">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-546">Bool</span></span>                                                                                                      |
| <span data-ttu-id="aeab7-547">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-547">Default</span></span>        | <span data-ttu-id="aeab7-548">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-548">False</span></span>                                                                                                     |
| <span data-ttu-id="aeab7-549">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-549">Minimum system</span></span> | <span data-ttu-id="aeab7-550">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aeab7-550">Windows XP</span></span>                                                                                                |



 

### <a name="mustrunindefaultcontext"></a><span data-ttu-id="aeab7-551">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="aeab7-551">MustRunInDefaultContext</span></span>



| <span data-ttu-id="aeab7-552">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-552">Entry</span></span> | <span data-ttu-id="aeab7-553">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-553">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-554">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-554">Description</span></span>    | <span data-ttu-id="aeab7-555">Indica que el componente se debe activar en el contexto del llamador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aeab7-555">Indicates that the component must be activated in the default caller's context.</span></span> <span data-ttu-id="aeab7-556">De lo contrario, se produce un error en la activación.</span><span class="sxs-lookup"><span data-stu-id="aeab7-556">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="aeab7-557">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-557">Access</span></span>         | <span data-ttu-id="aeab7-558">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-558">ReadWrite</span></span>                                                                                                    |
| <span data-ttu-id="aeab7-559">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-559">Type</span></span>           | <span data-ttu-id="aeab7-560">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-560">Bool</span></span>                                                                                                         |
| <span data-ttu-id="aeab7-561">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-561">Default</span></span>        | <span data-ttu-id="aeab7-562">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-562">False</span></span>                                                                                                        |
| <span data-ttu-id="aeab7-563">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-563">Minimum system</span></span> | <span data-ttu-id="aeab7-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-564">Windows 2000</span></span>                                                                                                 |



 

### <a name="objectpoolingenabled"></a><span data-ttu-id="aeab7-565">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="aeab7-565">ObjectPoolingEnabled</span></span>



| <span data-ttu-id="aeab7-566">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-566">Entry</span></span> | <span data-ttu-id="aeab7-567">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-567">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-568">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-568">Description</span></span>    | <span data-ttu-id="aeab7-569">Determina si la [agrupación de objetos com+](com--object-pooling.md) está habilitada para el componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-569">Determines whether [COM+ object pooling](com--object-pooling.md) is enabled for the component.</span></span> |
| <span data-ttu-id="aeab7-570">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-570">Access</span></span>         | <span data-ttu-id="aeab7-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-571">ReadWrite</span></span>                                                                                       |
| <span data-ttu-id="aeab7-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-572">Type</span></span>           | <span data-ttu-id="aeab7-573">Bool</span><span class="sxs-lookup"><span data-stu-id="aeab7-573">Bool</span></span>                                                                                            |
| <span data-ttu-id="aeab7-574">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-574">Default</span></span>        | <span data-ttu-id="aeab7-575">False</span><span class="sxs-lookup"><span data-stu-id="aeab7-575">False</span></span>                                                                                           |
| <span data-ttu-id="aeab7-576">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-576">Minimum system</span></span> | <span data-ttu-id="aeab7-577">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-577">Windows 2000</span></span>                                                                                    |



 

### <a name="progid"></a><span data-ttu-id="aeab7-578">ProgID</span><span class="sxs-lookup"><span data-stu-id="aeab7-578">ProgID</span></span>



| <span data-ttu-id="aeab7-579">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-579">Entry</span></span> | <span data-ttu-id="aeab7-580">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-580">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-581">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-581">Description</span></span>    | <span data-ttu-id="aeab7-582">Nombre descriptivo que se usa para identificar el componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-582">A friendly name used for identifying the component.</span></span> <span data-ttu-id="aeab7-583">Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="aeab7-583">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="aeab7-584">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-584">Access</span></span>         | <span data-ttu-id="aeab7-585">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-585">ReadOnly</span></span>                                                                                                                                                                              |
| <span data-ttu-id="aeab7-586">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-586">Type</span></span>           | <span data-ttu-id="aeab7-587">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-587">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="aeab7-588">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-588">Default</span></span>        | <span data-ttu-id="aeab7-589">N/D</span><span class="sxs-lookup"><span data-stu-id="aeab7-589">N/A</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="aeab7-590">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-590">Minimum system</span></span> | <span data-ttu-id="aeab7-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-591">Windows 2000</span></span>                                                                                                                                                                          |



 

### <a name="publisherid"></a><span data-ttu-id="aeab7-592">PublisherID</span><span class="sxs-lookup"><span data-stu-id="aeab7-592">PublisherID</span></span>



| <span data-ttu-id="aeab7-593">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-593">Entry</span></span> | <span data-ttu-id="aeab7-594">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-594">Value</span></span> |
|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-595">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-595">Description</span></span>    | <span data-ttu-id="aeab7-596">Identificador del publicador de eventos si el componente es una clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-596">Identifier for the event publisher if the component is an event class.</span></span> |
| <span data-ttu-id="aeab7-597">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-597">Access</span></span>         | <span data-ttu-id="aeab7-598">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-598">ReadWrite</span></span>                                                              |
| <span data-ttu-id="aeab7-599">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-599">Type</span></span>           | <span data-ttu-id="aeab7-600">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-600">String</span></span>                                                                 |
| <span data-ttu-id="aeab7-601">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-601">Default</span></span>        | <span data-ttu-id="aeab7-602">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-602">""</span></span>                                                                     |
| <span data-ttu-id="aeab7-603">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-603">Minimum system</span></span> | <span data-ttu-id="aeab7-604">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-604">Windows 2000</span></span>                                                           |



 

### <a name="soapassemblyname"></a><span data-ttu-id="aeab7-605">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="aeab7-605">SoapAssemblyName</span></span>



| <span data-ttu-id="aeab7-606">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-606">Entry</span></span> | <span data-ttu-id="aeab7-607">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-607">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-608">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-608">Description</span></span>    | <span data-ttu-id="aeab7-609">GUID que identifica el ensamblado de GAC que se ejecuta cuando se invoca el componente como un servicio SOAP.</span><span class="sxs-lookup"><span data-stu-id="aeab7-609">A GUID identifying the GAC assembly that is run when the component is invoked as a SOAP service.</span></span> |
| <span data-ttu-id="aeab7-610">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-610">Access</span></span>         | <span data-ttu-id="aeab7-611">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-611">ReadWrite</span></span>                                                                                        |
| <span data-ttu-id="aeab7-612">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-612">Type</span></span>           | <span data-ttu-id="aeab7-613">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-613">String</span></span>                                                                                           |
| <span data-ttu-id="aeab7-614">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-614">Default</span></span>        | <span data-ttu-id="aeab7-615">NULL</span><span class="sxs-lookup"><span data-stu-id="aeab7-615">NULL</span></span>                                                                                             |
| <span data-ttu-id="aeab7-616">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-616">Minimum system</span></span> | <span data-ttu-id="aeab7-617">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aeab7-617">Windows Server 2003</span></span>                                                                              |



 

### <a name="soaptypename"></a><span data-ttu-id="aeab7-618">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="aeab7-618">SoapTypeName</span></span>



| <span data-ttu-id="aeab7-619">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-619">Entry</span></span> | <span data-ttu-id="aeab7-620">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-620">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-621">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-621">Description</span></span>    | <span data-ttu-id="aeab7-622">El nombre de tipo administrado para un componente que se puede invocar como un servicio SOAP.</span><span class="sxs-lookup"><span data-stu-id="aeab7-622">The managed type name for a component that can be invoked as a SOAP service.</span></span> |
| <span data-ttu-id="aeab7-623">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-623">Access</span></span>         | <span data-ttu-id="aeab7-624">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-624">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="aeab7-625">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-625">Type</span></span>           | <span data-ttu-id="aeab7-626">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-626">String</span></span>                                                                       |
| <span data-ttu-id="aeab7-627">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-627">Default</span></span>        | <span data-ttu-id="aeab7-628">NULL</span><span class="sxs-lookup"><span data-stu-id="aeab7-628">NULL</span></span>                                                                         |
| <span data-ttu-id="aeab7-629">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-629">Minimum system</span></span> | <span data-ttu-id="aeab7-630">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aeab7-630">Windows Server 2003</span></span>                                                          |



 

### <a name="synchronization"></a><span data-ttu-id="aeab7-631">Synchronization</span><span class="sxs-lookup"><span data-stu-id="aeab7-631">Synchronization</span></span>



| <span data-ttu-id="aeab7-632">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-632">Entry</span></span> | <span data-ttu-id="aeab7-633">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-633">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-634">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-634">Description</span></span>    | <span data-ttu-id="aeab7-635">Determina la [sincronización](setting-the-synchronization-attribute.md) de llamadas para el componente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-635">Determines call [synchronization](setting-the-synchronization-attribute.md) for the component.</span></span>                                                                                                     |
| <span data-ttu-id="aeab7-636">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-636">Access</span></span>         | <span data-ttu-id="aeab7-637">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-637">ReadWrite</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="aeab7-638">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-638">Type</span></span>           | <span data-ttu-id="aeab7-639">Valores posibles largos: COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="aeab7-639">Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4)</span></span> |
| <span data-ttu-id="aeab7-640">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-640">Default</span></span>        | <span data-ttu-id="aeab7-641">COMAdminSynchronizationIgnored (0)</span><span class="sxs-lookup"><span data-stu-id="aeab7-641">COMAdminSynchronizationIgnored (0)</span></span>                                                                                                                                                                  |
| <span data-ttu-id="aeab7-642">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-642">Minimum system</span></span> | <span data-ttu-id="aeab7-643">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-643">Windows 2000</span></span>                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a><span data-ttu-id="aeab7-644">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="aeab7-644">ThreadingModel</span></span>



| <span data-ttu-id="aeab7-645">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-645">Entry</span></span> | <span data-ttu-id="aeab7-646">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-646">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-647">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-647">Description</span></span>    | <span data-ttu-id="aeab7-648">Determina cómo se asignan las instancias del componente a los subprocesos para la ejecución del método.</span><span class="sxs-lookup"><span data-stu-id="aeab7-648">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="aeab7-649">Los valores corresponden a los modelos de subprocesos COM.</span><span class="sxs-lookup"><span data-stu-id="aeab7-649">Values correspond to COM threading models.</span></span>                                                                                        |
| <span data-ttu-id="aeab7-650">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-650">Access</span></span>         | <span data-ttu-id="aeab7-651">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-651">ReadOnly</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="aeab7-652">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-652">Type</span></span>           | <span data-ttu-id="aeab7-653">Valores posibles largos: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5)</span><span class="sxs-lookup"><span data-stu-id="aeab7-653">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5)</span></span> |
| <span data-ttu-id="aeab7-654">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-654">Default</span></span>        | <span data-ttu-id="aeab7-655">N/D</span><span class="sxs-lookup"><span data-stu-id="aeab7-655">N/A</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="aeab7-656">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-656">Minimum system</span></span> | <span data-ttu-id="aeab7-657">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-657">Windows 2000</span></span>                                                                                                                                                                                                              |



 

### <a name="transaction"></a><span data-ttu-id="aeab7-658">Transacción</span><span class="sxs-lookup"><span data-stu-id="aeab7-658">Transaction</span></span>



| <span data-ttu-id="aeab7-659">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-659">Entry</span></span> | <span data-ttu-id="aeab7-660">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-660">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-661">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-661">Description</span></span>    | <span data-ttu-id="aeab7-662">Determina cómo un componente admite [transacciones](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="aeab7-662">Determines how a component supports [transactions](setting-the-transaction-attribute.md).</span></span> <span data-ttu-id="aeab7-663">Se recomienda usar las constantes en la enumeración y no los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="aeab7-663">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="aeab7-664">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-664">Access</span></span>         | <span data-ttu-id="aeab7-665">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-665">ReadWrite</span></span>                                                                                                                                                                              |
| <span data-ttu-id="aeab7-666">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-666">Type</span></span>           | <span data-ttu-id="aeab7-667">Valores posibles largos: COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="aeab7-667">Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)</span></span>        |
| <span data-ttu-id="aeab7-668">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-668">Default</span></span>        | <span data-ttu-id="aeab7-669">COMAdminTransactionNone (1)</span><span class="sxs-lookup"><span data-stu-id="aeab7-669">COMAdminTransactionNone (1)</span></span>                                                                                                                                                            |
| <span data-ttu-id="aeab7-670">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-670">Minimum system</span></span> | <span data-ttu-id="aeab7-671">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-671">Windows 2000</span></span>                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a><span data-ttu-id="aeab7-672">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="aeab7-672">TxIsolationLevel</span></span>



| <span data-ttu-id="aeab7-673">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-673">Entry</span></span> | <span data-ttu-id="aeab7-674">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-674">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeab7-675">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-675">Description</span></span>    | <span data-ttu-id="aeab7-676">Indica los niveles de aislamiento de transacción.</span><span class="sxs-lookup"><span data-stu-id="aeab7-676">Indicates the transaction isolation levels.</span></span> <span data-ttu-id="aeab7-677">Hay cinco niveles de aislamiento: ninguno, lectura no confirmada, lectura confirmada, lectura repetible y serializada.</span><span class="sxs-lookup"><span data-stu-id="aeab7-677">There are five isolation levels: none, read uncommitted, read committed, repeatable read, and serialized.</span></span> <span data-ttu-id="aeab7-678">El nivel de aislamiento predeterminado es serializado.</span><span class="sxs-lookup"><span data-stu-id="aeab7-678">The default isolation level is serialized.</span></span>                           |
| <span data-ttu-id="aeab7-679">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-679">Access</span></span>         | <span data-ttu-id="aeab7-680">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aeab7-680">ReadWrite</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="aeab7-681">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-681">Type</span></span>           | <span data-ttu-id="aeab7-682">Valores posibles largos: COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="aeab7-682">Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4)</span></span> |
| <span data-ttu-id="aeab7-683">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-683">Default</span></span>        | <span data-ttu-id="aeab7-684">COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="aeab7-684">COMAdminTxIsolationLevelSerializable (4)</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="aeab7-685">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-685">Minimum system</span></span> | <span data-ttu-id="aeab7-686">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aeab7-686">Windows XP</span></span>                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a><span data-ttu-id="aeab7-687">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="aeab7-687">VersionBuild</span></span>



| <span data-ttu-id="aeab7-688">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-688">Entry</span></span> | <span data-ttu-id="aeab7-689">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-689">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="aeab7-690">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-690">Description</span></span>    | <span data-ttu-id="aeab7-691">Identificador de compilación de versión.</span><span class="sxs-lookup"><span data-stu-id="aeab7-691">Version build identifier.</span></span> |
| <span data-ttu-id="aeab7-692">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-692">Access</span></span>         | <span data-ttu-id="aeab7-693">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-693">ReadOnly</span></span>                  |
| <span data-ttu-id="aeab7-694">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-694">Type</span></span>           | <span data-ttu-id="aeab7-695">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-695">String</span></span>                    |
| <span data-ttu-id="aeab7-696">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-696">Default</span></span>        | <span data-ttu-id="aeab7-697">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-697">""</span></span>                        |
| <span data-ttu-id="aeab7-698">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-698">Minimum system</span></span> | <span data-ttu-id="aeab7-699">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-699">Windows 2000</span></span>              |



 

### <a name="versionmajor"></a><span data-ttu-id="aeab7-700">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="aeab7-700">VersionMajor</span></span>



| <span data-ttu-id="aeab7-701">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-701">Entry</span></span> | <span data-ttu-id="aeab7-702">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-702">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="aeab7-703">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-703">Description</span></span>    | <span data-ttu-id="aeab7-704">Identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="aeab7-704">Version identifier.</span></span> |
| <span data-ttu-id="aeab7-705">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-705">Access</span></span>         | <span data-ttu-id="aeab7-706">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-706">ReadOnly</span></span>            |
| <span data-ttu-id="aeab7-707">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-707">Type</span></span>           | <span data-ttu-id="aeab7-708">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-708">String</span></span>              |
| <span data-ttu-id="aeab7-709">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-709">Default</span></span>        | <span data-ttu-id="aeab7-710">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-710">""</span></span>                  |
| <span data-ttu-id="aeab7-711">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-711">Minimum system</span></span> | <span data-ttu-id="aeab7-712">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-712">Windows 2000</span></span>        |



 

### <a name="versionminor"></a><span data-ttu-id="aeab7-713">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="aeab7-713">VersionMinor</span></span>



| <span data-ttu-id="aeab7-714">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-714">Entry</span></span> | <span data-ttu-id="aeab7-715">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-715">Value</span></span> |
|----------------|-------------------------|
| <span data-ttu-id="aeab7-716">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-716">Description</span></span>    | <span data-ttu-id="aeab7-717">Subidentificador de versión.</span><span class="sxs-lookup"><span data-stu-id="aeab7-717">Version sub-identifier.</span></span> |
| <span data-ttu-id="aeab7-718">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-718">Access</span></span>         | <span data-ttu-id="aeab7-719">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-719">ReadOnly</span></span>                |
| <span data-ttu-id="aeab7-720">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-720">Type</span></span>           | <span data-ttu-id="aeab7-721">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-721">String</span></span>                  |
| <span data-ttu-id="aeab7-722">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-722">Default</span></span>        | <span data-ttu-id="aeab7-723">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-723">""</span></span>                      |
| <span data-ttu-id="aeab7-724">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-724">Minimum system</span></span> | <span data-ttu-id="aeab7-725">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-725">Windows 2000</span></span>            |



 

### <a name="versionsubbuild"></a><span data-ttu-id="aeab7-726">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="aeab7-726">VersionSubBuild</span></span>



| <span data-ttu-id="aeab7-727">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeab7-727">Entry</span></span> | <span data-ttu-id="aeab7-728">Value</span><span class="sxs-lookup"><span data-stu-id="aeab7-728">Value</span></span> |
|----------------|-------------------------------|
| <span data-ttu-id="aeab7-729">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeab7-729">Description</span></span>    | <span data-ttu-id="aeab7-730">Identificador de subcompilación de versión.</span><span class="sxs-lookup"><span data-stu-id="aeab7-730">Version sub-build identifier.</span></span> |
| <span data-ttu-id="aeab7-731">Access</span><span class="sxs-lookup"><span data-stu-id="aeab7-731">Access</span></span>         | <span data-ttu-id="aeab7-732">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="aeab7-732">ReadOnly</span></span>                      |
| <span data-ttu-id="aeab7-733">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeab7-733">Type</span></span>           | <span data-ttu-id="aeab7-734">String</span><span class="sxs-lookup"><span data-stu-id="aeab7-734">String</span></span>                        |
| <span data-ttu-id="aeab7-735">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="aeab7-735">Default</span></span>        | <span data-ttu-id="aeab7-736">""</span><span class="sxs-lookup"><span data-stu-id="aeab7-736">""</span></span>                            |
| <span data-ttu-id="aeab7-737">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="aeab7-737">Minimum system</span></span> | <span data-ttu-id="aeab7-738">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="aeab7-738">Windows 2000</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="aeab7-739">Vea también</span><span class="sxs-lookup"><span data-stu-id="aeab7-739">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeab7-740">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="aeab7-740">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
