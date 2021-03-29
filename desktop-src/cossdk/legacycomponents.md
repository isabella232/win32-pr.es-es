---
description: Contiene un objeto para cada componente no configurado en la colección de aplicaciones. Los componentes no configurados no pueden hacer uso de servicios COM+. Las propiedades expuestas por estos objetos contienen la configuración realizada en el nivel de componente.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Colección LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807280"
---
# <a name="legacycomponents-collection"></a><span data-ttu-id="f5c66-105">Colección LegacyComponents</span><span class="sxs-lookup"><span data-stu-id="f5c66-105">LegacyComponents collection</span></span>

<span data-ttu-id="f5c66-106">Contiene un objeto para cada componente no configurado en la colección de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f5c66-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="f5c66-107">Los componentes no configurados no pueden hacer uso de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="f5c66-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="f5c66-108">Las propiedades expuestas por estos objetos contienen la configuración realizada en el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="f5c66-109">Esta colección admite el método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , pero no el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="f5c66-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="f5c66-110">Para instalar o importar componentes en una aplicación, use métodos en el objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="f5c66-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f5c66-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f5c66-111">Members</span></span>

<span data-ttu-id="f5c66-112">La colección **LegacyComponents** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="f5c66-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f5c66-113">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="f5c66-113">Related Collections</span></span>

<span data-ttu-id="f5c66-114">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="f5c66-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f5c66-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f5c66-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f5c66-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f5c66-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f5c66-117">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="f5c66-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="f5c66-118">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5c66-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f5c66-119">**APLICACIONES**</span><span class="sxs-lookup"><span data-stu-id="f5c66-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="f5c66-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5c66-120">Properties</span></span>

<span data-ttu-id="f5c66-121">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="f5c66-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f5c66-122">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="f5c66-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="f5c66-123">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="f5c66-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="f5c66-124">AppID</span><span class="sxs-lookup"><span data-stu-id="f5c66-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="f5c66-125">AppName</span><span class="sxs-lookup"><span data-stu-id="f5c66-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="f5c66-126">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="f5c66-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="f5c66-127">Bits</span><span class="sxs-lookup"><span data-stu-id="f5c66-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="f5c66-128">ClassName</span><span class="sxs-lookup"><span data-stu-id="f5c66-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="f5c66-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="f5c66-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="f5c66-130">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="f5c66-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="f5c66-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="f5c66-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="f5c66-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="f5c66-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="f5c66-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f5c66-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="f5c66-134">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="f5c66-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="f5c66-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="f5c66-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="f5c66-136">LocalService (Servicio local)</span><span class="sxs-lookup"><span data-stu-id="f5c66-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="f5c66-137">Contraseña</span><span class="sxs-lookup"><span data-stu-id="f5c66-137">Password</span></span>](#password)
-   [<span data-ttu-id="f5c66-138">ProgID</span><span class="sxs-lookup"><span data-stu-id="f5c66-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="f5c66-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="f5c66-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="f5c66-140">RunAs</span><span class="sxs-lookup"><span data-stu-id="f5c66-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="f5c66-141">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="f5c66-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="f5c66-142">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="f5c66-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="f5c66-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="f5c66-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="f5c66-144">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="f5c66-144">AccessPermissions</span></span>



| <span data-ttu-id="f5c66-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-145">Entry</span></span> | <span data-ttu-id="f5c66-146">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-147">Description</span></span>    | <span data-ttu-id="f5c66-148">Especifica las cuentas de usuario a las que se permite o deniega el acceso al componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="f5c66-149">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-149">Access</span></span>         | <span data-ttu-id="f5c66-150">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="f5c66-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-151">Type</span></span>           | <span data-ttu-id="f5c66-152">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-152">String</span></span>                                                                          |
| <span data-ttu-id="f5c66-153">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-153">Default</span></span>        | <span data-ttu-id="f5c66-154">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-154">N/A</span></span>                                                                             |
| <span data-ttu-id="f5c66-155">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-155">Minimum system</span></span> | <span data-ttu-id="f5c66-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="f5c66-157">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="f5c66-157">ActivateAtStorage</span></span>



| <span data-ttu-id="f5c66-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-158">Entry</span></span> | <span data-ttu-id="f5c66-159">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="f5c66-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-160">Description</span></span>    | <span data-ttu-id="f5c66-161">Especifica si se debe ejecutar el servidor en la máquina de almacenamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="f5c66-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="f5c66-162">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-162">Access</span></span>         | <span data-ttu-id="f5c66-163">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="f5c66-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-164">Type</span></span>           | <span data-ttu-id="f5c66-165">Valores de cadena posibles: "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="f5c66-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="f5c66-166">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-166">Default</span></span>        | <span data-ttu-id="f5c66-167">"N"</span><span class="sxs-lookup"><span data-stu-id="f5c66-167">"N"</span></span>                                                              |
| <span data-ttu-id="f5c66-168">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-168">Minimum system</span></span> | <span data-ttu-id="f5c66-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="f5c66-170">AppID</span><span class="sxs-lookup"><span data-stu-id="f5c66-170">AppID</span></span>



| <span data-ttu-id="f5c66-171">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-171">Entry</span></span> | <span data-ttu-id="f5c66-172">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="f5c66-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-173">Description</span></span>    | <span data-ttu-id="f5c66-174">El id. de aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5c66-174">The application ID.</span></span> |
| <span data-ttu-id="f5c66-175">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-175">Access</span></span>         | <span data-ttu-id="f5c66-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-176">ReadOnly</span></span>            |
| <span data-ttu-id="f5c66-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-177">Type</span></span>           | <span data-ttu-id="f5c66-178">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-178">String</span></span>              |
| <span data-ttu-id="f5c66-179">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-179">Default</span></span>        | <span data-ttu-id="f5c66-180">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-180">N/A</span></span>                 |
| <span data-ttu-id="f5c66-181">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-181">Minimum system</span></span> | <span data-ttu-id="f5c66-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="f5c66-183">AppName</span><span class="sxs-lookup"><span data-stu-id="f5c66-183">AppName</span></span>



| <span data-ttu-id="f5c66-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-184">Entry</span></span> | <span data-ttu-id="f5c66-185">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="f5c66-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-186">Description</span></span>    | <span data-ttu-id="f5c66-187">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5c66-187">The name of the application.</span></span> |
| <span data-ttu-id="f5c66-188">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-188">Access</span></span>         | <span data-ttu-id="f5c66-189">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-189">ReadOnly</span></span>                     |
| <span data-ttu-id="f5c66-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-190">Type</span></span>           | <span data-ttu-id="f5c66-191">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-191">String</span></span>                       |
| <span data-ttu-id="f5c66-192">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-192">Default</span></span>        | <span data-ttu-id="f5c66-193">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-193">N/A</span></span>                          |
| <span data-ttu-id="f5c66-194">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-194">Minimum system</span></span> | <span data-ttu-id="f5c66-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="f5c66-196">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="f5c66-196">AuthenticationLevel</span></span>



| <span data-ttu-id="f5c66-197">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-197">Entry</span></span> | <span data-ttu-id="f5c66-198">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-199">Description</span></span>    | <span data-ttu-id="f5c66-200">Establece el nivel de autenticación de las llamadas, con los valores correspondientes a la configuración de autenticación de llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="f5c66-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="f5c66-201">Cuando se elige COMAdminAuthenticationDefault, se usa el valor de la propiedad DefaultAuthenticationLevel de la colección [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="f5c66-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="f5c66-202">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-202">Access</span></span>         | <span data-ttu-id="f5c66-203">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f5c66-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-204">Type</span></span>           | <span data-ttu-id="f5c66-205">Valores posibles largos: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="f5c66-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="f5c66-206">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-206">Default</span></span>        | <span data-ttu-id="f5c66-207">COMAdminAuthenticationDefault (0)</span><span class="sxs-lookup"><span data-stu-id="f5c66-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f5c66-208">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-208">Minimum system</span></span> | <span data-ttu-id="f5c66-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="f5c66-210">Se recomienda usar las constantes en la enumeración y no los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="f5c66-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="f5c66-211">Valor de bits</span><span class="sxs-lookup"><span data-stu-id="f5c66-211">Bitness</span></span>



| <span data-ttu-id="f5c66-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-212">Entry</span></span> | <span data-ttu-id="f5c66-213">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-214">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-214">Description</span></span>    | <span data-ttu-id="f5c66-215">Representa el tipo de bits binario del componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="f5c66-216">En los sistemas que usan Windows de 64 bits, esta propiedad distingue entre los componentes de 64 bits y los componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f5c66-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="f5c66-217">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-217">Access</span></span>         | <span data-ttu-id="f5c66-218">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="f5c66-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-219">Type</span></span>           | <span data-ttu-id="f5c66-220">Valores posibles largos: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)</span><span class="sxs-lookup"><span data-stu-id="f5c66-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="f5c66-221">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-221">Default</span></span>        | <span data-ttu-id="f5c66-222">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="f5c66-223">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-223">Minimum system</span></span> | <span data-ttu-id="f5c66-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="f5c66-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="f5c66-225">ClassName</span></span>



| <span data-ttu-id="f5c66-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-226">Entry</span></span> | <span data-ttu-id="f5c66-227">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="f5c66-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-228">Description</span></span>    | <span data-ttu-id="f5c66-229">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="f5c66-229">The name of the class.</span></span> |
| <span data-ttu-id="f5c66-230">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-230">Access</span></span>         | <span data-ttu-id="f5c66-231">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-231">ReadOnly</span></span>               |
| <span data-ttu-id="f5c66-232">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-232">Type</span></span>           | <span data-ttu-id="f5c66-233">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-233">String</span></span>                 |
| <span data-ttu-id="f5c66-234">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-234">Default</span></span>        | <span data-ttu-id="f5c66-235">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-235">N/A</span></span>                    |
| <span data-ttu-id="f5c66-236">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-236">Minimum system</span></span> | <span data-ttu-id="f5c66-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="f5c66-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="f5c66-238">CLSID</span></span>



| <span data-ttu-id="f5c66-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-239">Entry</span></span> | <span data-ttu-id="f5c66-240">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-241">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-241">Description</span></span>    | <span data-ttu-id="f5c66-242">GUID del componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-242">A GUID for the component.</span></span> <span data-ttu-id="f5c66-243">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="f5c66-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f5c66-244">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-244">Access</span></span>         | <span data-ttu-id="f5c66-245">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="f5c66-246">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-246">Type</span></span>           | <span data-ttu-id="f5c66-247">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="f5c66-248">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-248">Default</span></span>        | <span data-ttu-id="f5c66-249">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="f5c66-250">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-250">Minimum system</span></span> | <span data-ttu-id="f5c66-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="f5c66-252">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="f5c66-252">DllSurrogate</span></span>



| <span data-ttu-id="f5c66-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-253">Entry</span></span> | <span data-ttu-id="f5c66-254">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="f5c66-255">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-255">Description</span></span>    | <span data-ttu-id="f5c66-256">Especifica la ruta de acceso completa a una aplicación de servidor de surragate.</span><span class="sxs-lookup"><span data-stu-id="f5c66-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="f5c66-257">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-257">Access</span></span>         | <span data-ttu-id="f5c66-258">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="f5c66-259">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-259">Type</span></span>           | <span data-ttu-id="f5c66-260">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-260">String</span></span>                                                     |
| <span data-ttu-id="f5c66-261">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-261">Default</span></span>        | <span data-ttu-id="f5c66-262">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-262">N/A</span></span>                                                        |
| <span data-ttu-id="f5c66-263">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-263">Minimum system</span></span> | <span data-ttu-id="f5c66-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="f5c66-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="f5c66-265">InprocHandler32</span></span>



| <span data-ttu-id="f5c66-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-266">Entry</span></span> | <span data-ttu-id="f5c66-267">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="f5c66-268">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-268">Description</span></span>    | <span data-ttu-id="f5c66-269">Especifica la ruta de acceso completa a un archivo DLL de controlador personalizado en proceso de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f5c66-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="f5c66-270">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-270">Access</span></span>         | <span data-ttu-id="f5c66-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="f5c66-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-272">Type</span></span>           | <span data-ttu-id="f5c66-273">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-273">String</span></span>                                                             |
| <span data-ttu-id="f5c66-274">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-274">Default</span></span>        | <span data-ttu-id="f5c66-275">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-275">N/A</span></span>                                                                |
| <span data-ttu-id="f5c66-276">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-276">Minimum system</span></span> | <span data-ttu-id="f5c66-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="f5c66-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="f5c66-278">InprocServer32</span></span>



| <span data-ttu-id="f5c66-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-279">Entry</span></span> | <span data-ttu-id="f5c66-280">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="f5c66-281">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-281">Description</span></span>    | <span data-ttu-id="f5c66-282">Especifica la ruta de acceso completa a un archivo DLL de servidor en proceso de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f5c66-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="f5c66-283">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-283">Access</span></span>         | <span data-ttu-id="f5c66-284">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="f5c66-285">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-285">Type</span></span>           | <span data-ttu-id="f5c66-286">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-286">String</span></span>                                                     |
| <span data-ttu-id="f5c66-287">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-287">Default</span></span>        | <span data-ttu-id="f5c66-288">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-288">N/A</span></span>                                                        |
| <span data-ttu-id="f5c66-289">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-289">Minimum system</span></span> | <span data-ttu-id="f5c66-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="f5c66-291">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f5c66-291">IsEnabled</span></span>



| <span data-ttu-id="f5c66-292">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-292">Entry</span></span> | <span data-ttu-id="f5c66-293">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-294">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-294">Description</span></span>    | <span data-ttu-id="f5c66-295">Si el componente o la aplicación COM+ está deshabilitado, IsEnabled es false.</span><span class="sxs-lookup"><span data-stu-id="f5c66-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="f5c66-296">Si el componente o la aplicación COM+ está habilitado, IsEnabled es true.</span><span class="sxs-lookup"><span data-stu-id="f5c66-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="f5c66-297">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-297">Access</span></span>         | <span data-ttu-id="f5c66-298">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="f5c66-299">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-299">Type</span></span>           | <span data-ttu-id="f5c66-300">Bool</span><span class="sxs-lookup"><span data-stu-id="f5c66-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="f5c66-301">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-301">Default</span></span>        | <span data-ttu-id="f5c66-302">True</span><span class="sxs-lookup"><span data-stu-id="f5c66-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="f5c66-303">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-303">Minimum system</span></span> | <span data-ttu-id="f5c66-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="f5c66-305">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="f5c66-305">LaunchPermissions</span></span>



| <span data-ttu-id="f5c66-306">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-306">Entry</span></span> | <span data-ttu-id="f5c66-307">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-308">Description</span></span>    | <span data-ttu-id="f5c66-309">Especifica las cuentas de usuario a las que se permite o se deniega el permiso para iniciar este componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="f5c66-310">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-310">Access</span></span>         | <span data-ttu-id="f5c66-311">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="f5c66-312">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-312">Type</span></span>           | <span data-ttu-id="f5c66-313">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-313">String</span></span>                                                                                 |
| <span data-ttu-id="f5c66-314">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-314">Default</span></span>        | <span data-ttu-id="f5c66-315">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="f5c66-316">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-316">Minimum system</span></span> | <span data-ttu-id="f5c66-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="f5c66-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="f5c66-318">LocalServer32</span></span>



| <span data-ttu-id="f5c66-319">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-319">Entry</span></span> | <span data-ttu-id="f5c66-320">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-321">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-321">Description</span></span>    | <span data-ttu-id="f5c66-322">Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f5c66-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="f5c66-323">Para ayudar a proteger la seguridad del sistema, utilice cadenas entre comillas en la ruta de acceso para indicar dónde finaliza el nombre del archivo ejecutable y los argumentos comienzan.</span><span class="sxs-lookup"><span data-stu-id="f5c66-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="f5c66-324">Por ejemplo, " \\ C: archivos de la \\ compañía de archivos de programa \\ \\Application.exe\\ " parám1 parám2 ".</span><span class="sxs-lookup"><span data-stu-id="f5c66-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="f5c66-325">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-325">Access</span></span>         | <span data-ttu-id="f5c66-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f5c66-327">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-327">Type</span></span>           | <span data-ttu-id="f5c66-328">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f5c66-329">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-329">Default</span></span>        | <span data-ttu-id="f5c66-330">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f5c66-331">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-331">Minimum system</span></span> | <span data-ttu-id="f5c66-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="f5c66-333">LocalService (Servicio local)</span><span class="sxs-lookup"><span data-stu-id="f5c66-333">LocalService</span></span>



| <span data-ttu-id="f5c66-334">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-334">Entry</span></span> | <span data-ttu-id="f5c66-335">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="f5c66-336">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-336">Description</span></span>    | <span data-ttu-id="f5c66-337">Especifica la ruta de acceso completa a la aplicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="f5c66-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="f5c66-338">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-338">Access</span></span>         | <span data-ttu-id="f5c66-339">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="f5c66-340">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-340">Type</span></span>           | <span data-ttu-id="f5c66-341">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-341">String</span></span>                                              |
| <span data-ttu-id="f5c66-342">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-342">Default</span></span>        | <span data-ttu-id="f5c66-343">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-343">N/A</span></span>                                                 |
| <span data-ttu-id="f5c66-344">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-344">Minimum system</span></span> | <span data-ttu-id="f5c66-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="f5c66-346">Contraseña</span><span class="sxs-lookup"><span data-stu-id="f5c66-346">Password</span></span>



| <span data-ttu-id="f5c66-347">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-347">Entry</span></span> | <span data-ttu-id="f5c66-348">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-349">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-349">Description</span></span>    | <span data-ttu-id="f5c66-350">Establece la contraseña utilizada por el proceso de servidor para iniciar sesión con la identidad de ejecución especificada.</span><span class="sxs-lookup"><span data-stu-id="f5c66-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="f5c66-351">La contraseña debe establecerse al mismo tiempo que la identidad runas, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), ya que la contraseña y la identidad se validan antes de guardarse.</span><span class="sxs-lookup"><span data-stu-id="f5c66-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="f5c66-352">Si la contraseña y la identidad no se sincronizan, el componente no se puede iniciar hasta que los restablezca un administrador.</span><span class="sxs-lookup"><span data-stu-id="f5c66-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="f5c66-353">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-353">Access</span></span>         | <span data-ttu-id="f5c66-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f5c66-355">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-355">Type</span></span>           | <span data-ttu-id="f5c66-356">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f5c66-357">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-357">Default</span></span>        | <span data-ttu-id="f5c66-358">NULL</span><span class="sxs-lookup"><span data-stu-id="f5c66-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f5c66-359">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-359">Minimum system</span></span> | <span data-ttu-id="f5c66-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="f5c66-361">ProgID</span><span class="sxs-lookup"><span data-stu-id="f5c66-361">ProgID</span></span>



| <span data-ttu-id="f5c66-362">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-362">Entry</span></span> | <span data-ttu-id="f5c66-363">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-364">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-364">Description</span></span>    | <span data-ttu-id="f5c66-365">Nombre que identifica el componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-365">A name identifying the component.</span></span> <span data-ttu-id="f5c66-366">Esta propiedad se devuelve cuando se llama al método de la propiedad Name en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="f5c66-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f5c66-367">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-367">Access</span></span>         | <span data-ttu-id="f5c66-368">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="f5c66-369">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-369">Type</span></span>           | <span data-ttu-id="f5c66-370">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="f5c66-371">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-371">Default</span></span>        | <span data-ttu-id="f5c66-372">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="f5c66-373">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-373">Minimum system</span></span> | <span data-ttu-id="f5c66-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="f5c66-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="f5c66-375">RemoteServer</span></span>



| <span data-ttu-id="f5c66-376">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-376">Entry</span></span> | <span data-ttu-id="f5c66-377">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="f5c66-378">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-378">Description</span></span>    | <span data-ttu-id="f5c66-379">Especifica el equipo del servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="f5c66-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="f5c66-380">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-380">Access</span></span>         | <span data-ttu-id="f5c66-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-381">ReadWrite</span></span>                             |
| <span data-ttu-id="f5c66-382">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-382">Type</span></span>           | <span data-ttu-id="f5c66-383">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-383">String</span></span>                                |
| <span data-ttu-id="f5c66-384">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-384">Default</span></span>        | <span data-ttu-id="f5c66-385">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-385">N/A</span></span>                                   |
| <span data-ttu-id="f5c66-386">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-386">Minimum system</span></span> | <span data-ttu-id="f5c66-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="f5c66-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="f5c66-388">RunAs</span></span>



| <span data-ttu-id="f5c66-389">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-389">Entry</span></span> | <span data-ttu-id="f5c66-390">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-391">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-391">Description</span></span>    | <span data-ttu-id="f5c66-392">Especifica el usuario bajo cuya identidad se ejecutará el componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="f5c66-393">La contraseña debe establecerse al mismo tiempo que la identidad runas, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), ya que la contraseña y la identidad se validan antes de guardarse.</span><span class="sxs-lookup"><span data-stu-id="f5c66-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="f5c66-394">Si la contraseña y la identidad no se sincronizan, el componente no se puede iniciar hasta que los restablezca un administrador.</span><span class="sxs-lookup"><span data-stu-id="f5c66-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="f5c66-395">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-395">Access</span></span>         | <span data-ttu-id="f5c66-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f5c66-397">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-397">Type</span></span>           | <span data-ttu-id="f5c66-398">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f5c66-399">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-399">Default</span></span>        | <span data-ttu-id="f5c66-400">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f5c66-401">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-401">Minimum system</span></span> | <span data-ttu-id="f5c66-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="f5c66-403">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="f5c66-403">ServiceParameter</span></span>



| <span data-ttu-id="f5c66-404">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-404">Entry</span></span> | <span data-ttu-id="f5c66-405">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-406">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-406">Description</span></span>    | <span data-ttu-id="f5c66-407">Especifica los parámetros que se pasan a la aplicación cuando se invoca como una aplicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="f5c66-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="f5c66-408">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-408">Access</span></span>         | <span data-ttu-id="f5c66-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="f5c66-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-410">Type</span></span>           | <span data-ttu-id="f5c66-411">String</span><span class="sxs-lookup"><span data-stu-id="f5c66-411">String</span></span>                                                                                    |
| <span data-ttu-id="f5c66-412">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-412">Default</span></span>        | <span data-ttu-id="f5c66-413">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="f5c66-414">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-414">Minimum system</span></span> | <span data-ttu-id="f5c66-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="f5c66-416">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="f5c66-416">SRPTrustLevel</span></span>



| <span data-ttu-id="f5c66-417">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-417">Entry</span></span> | <span data-ttu-id="f5c66-418">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-419">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-419">Description</span></span>    | <span data-ttu-id="f5c66-420">Indica el nivel de confianza de la Directiva de restricción de software (SRP) del componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="f5c66-421">El nivel de confianza de SRP hace referencia al nivel de confianza que desea dar a un componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="f5c66-422">Un nivel de confianza SRP sin restricciones se corresponde con \_ el \_ valor de enumeración LEVELID FULLYTRUSTED más seguro, mientras que un nivel de confianza SRP no permitido corresponde al \_ valor de enumeración de LEVELID no \_ permitido.</span><span class="sxs-lookup"><span data-stu-id="f5c66-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="f5c66-423">La enumeración para los niveles de confianza se define en Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="f5c66-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="f5c66-424">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-424">Access</span></span>         | <span data-ttu-id="f5c66-425">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5c66-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f5c66-426">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-426">Type</span></span>           | <span data-ttu-id="f5c66-427">Valores posibles largos: LEVELID de seguridad no \_ \_ permitido (0X0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="f5c66-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f5c66-428">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-428">Default</span></span>        | <span data-ttu-id="f5c66-429">\_FULLYTRUSTED LEVELID \_ Safe</span><span class="sxs-lookup"><span data-stu-id="f5c66-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f5c66-430">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-430">Minimum system</span></span> | <span data-ttu-id="f5c66-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="f5c66-432">Un componente que esté dispuesto a confiar en el acceso sin restricciones debe tener la seguridad más estricta asociada.</span><span class="sxs-lookup"><span data-stu-id="f5c66-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="f5c66-433">Las aplicaciones que no están restringidas pueden cargar solo componentes no restringidos, mientras que las aplicaciones no permitidas no podrán ejecutarse y, por lo tanto, no podrán cargar ningún componente.</span><span class="sxs-lookup"><span data-stu-id="f5c66-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="f5c66-434">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="f5c66-434">ThreadingModel</span></span>



| <span data-ttu-id="f5c66-435">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5c66-435">Entry</span></span> | <span data-ttu-id="f5c66-436">Value</span><span class="sxs-lookup"><span data-stu-id="f5c66-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c66-437">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c66-437">Description</span></span>    | <span data-ttu-id="f5c66-438">Determina cómo se asignan las instancias del componente a los subprocesos para la ejecución del método.</span><span class="sxs-lookup"><span data-stu-id="f5c66-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="f5c66-439">Los valores corresponden a los modelos de subprocesos COM.</span><span class="sxs-lookup"><span data-stu-id="f5c66-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="f5c66-440">Access</span><span class="sxs-lookup"><span data-stu-id="f5c66-440">Access</span></span>         | <span data-ttu-id="f5c66-441">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5c66-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="f5c66-442">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5c66-442">Type</span></span>           | <span data-ttu-id="f5c66-443">Valores posibles largos: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4)</span><span class="sxs-lookup"><span data-stu-id="f5c66-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="f5c66-444">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5c66-444">Default</span></span>        | <span data-ttu-id="f5c66-445">N/D</span><span class="sxs-lookup"><span data-stu-id="f5c66-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="f5c66-446">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f5c66-446">Minimum system</span></span> | <span data-ttu-id="f5c66-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c66-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="f5c66-448">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5c66-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c66-449">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="f5c66-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
