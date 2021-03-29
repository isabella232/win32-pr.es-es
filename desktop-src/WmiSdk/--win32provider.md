---
description: Registra información sobre la implementación física de un proveedor en WMI. Los proveedores que no establecen la propiedad HostingModel se cargan, de forma predeterminada, para ejecutarse en un proceso de Wmiprvse.exe como NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: __Win32Provider (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002836"
---
# <a name="__win32provider-class"></a><span data-ttu-id="d50a7-104">\_\_Clase Win32Provider</span><span class="sxs-lookup"><span data-stu-id="d50a7-104">\_\_Win32Provider class</span></span>

<span data-ttu-id="d50a7-105">La clase del sistema **\_ \_ Win32Provider** registra información sobre la implementación física de un proveedor en WMI.</span><span class="sxs-lookup"><span data-stu-id="d50a7-105">The **\_\_Win32Provider** system class registers information about the physical implementation of a provider in WMI.</span></span> <span data-ttu-id="d50a7-106">Los proveedores que no establecen la propiedad **HostingModel** se cargan, de forma predeterminada, para ejecutarse en un proceso de Wmiprvse.exe como **NetworkServiceHostOrSelfHost**.</span><span class="sxs-lookup"><span data-stu-id="d50a7-106">Providers that do not set the **HostingModel** property are loaded, by default, to run in a Wmiprvse.exe process as **NetworkServiceHostOrSelfHost**.</span></span>

<span data-ttu-id="d50a7-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d50a7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d50a7-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d50a7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d50a7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d50a7-109">Syntax</span></span>

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="d50a7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d50a7-110">Members</span></span>

<span data-ttu-id="d50a7-111">La clase **\_ \_ Win32Provider** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d50a7-111">The **\_\_Win32Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="d50a7-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d50a7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d50a7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d50a7-113">Properties</span></span>

<span data-ttu-id="d50a7-114">La clase **\_ \_ Win32Provider** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d50a7-114">The **\_\_Win32Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d50a7-115">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="d50a7-115">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d50a7-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-118">Identificador de clase que WMI usa para determinar si se carga o no un proveedor de alto rendimiento en el proceso de cliente o en el proceso WMI.</span><span class="sxs-lookup"><span data-stu-id="d50a7-118">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="d50a7-119">Si el proveedor y el cliente se encuentran en el mismo equipo, WMI carga el proveedor en proceso en el cliente mediante **ClientLoadableCLSID** como identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="d50a7-119">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="d50a7-120">Cuando el proveedor y el cliente se encuentran en equipos diferentes, WMI carga el proveedor en proceso en WMI.</span><span class="sxs-lookup"><span data-stu-id="d50a7-120">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="d50a7-121">WMI también usa **ClientLoadableCLSID** para admitir las operaciones de actualización.</span><span class="sxs-lookup"><span data-stu-id="d50a7-121">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="d50a7-122">Para obtener más información, vea [registrar un proveedor de High-Performance.](registering-a-high-performance-provider.md)</span><span class="sxs-lookup"><span data-stu-id="d50a7-122">For more information, see [Registering a High-Performance Provider.](registering-a-high-performance-provider.md)</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="d50a7-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d50a7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-126">**GUID** que representa el identificador de clase (**CLSID**) del objeto com del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d50a7-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="d50a7-127">Este objeto COM debe contener una implementación de la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="d50a7-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-128">**Simultaneidad**</span><span class="sxs-lookup"><span data-stu-id="d50a7-128">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d50a7-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-131">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-131">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-132">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="d50a7-132">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d50a7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-135">Identifica el equipo en el que se va a iniciar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d50a7-135">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="d50a7-136">Si el proveedor se ejecuta en el equipo local, es **null**.</span><span class="sxs-lookup"><span data-stu-id="d50a7-136">If the provider runs on the local computer it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-137">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="d50a7-137">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-140">Si es **true**, esta instancia está habilitada y se puede usar para completar las solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="d50a7-140">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-141">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="d50a7-141">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d50a7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-144">Esta propiedad se compone de los valores de las propiedades **HostingGroup** y **HostingSpecification** de los [**\_ proveedores msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .</span><span class="sxs-lookup"><span data-stu-id="d50a7-144">This property is composed of values from the [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** and **HostingSpecification** properties.</span></span> <span data-ttu-id="d50a7-145">El valor de esta propiedad especifica cómo WMI carga el proveedor y la cuenta de seguridad con la que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="d50a7-145">The value of this property specifies how WMI loads the provider and the security account it runs under.</span></span> <span data-ttu-id="d50a7-146">Para obtener más información sobre cómo establecer la propiedad **HostingModel** , vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md) y [registro de un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d50a7-146">For more information about setting the **HostingModel** property, see [Provider Hosting and Security](provider-hosting-and-security.md) and [Registering a Provider](registering-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-147">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="d50a7-147">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-148">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d50a7-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-150">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d50a7-150">Reserved.</span></span> <span data-ttu-id="d50a7-151">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="d50a7-151">The default value is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-152">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="d50a7-152">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d50a7-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-155">Conjunto de marcas que proporcionan información sobre la serialización.</span><span class="sxs-lookup"><span data-stu-id="d50a7-155">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="d50a7-156">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="d50a7-156">The default value is zero (0).</span></span>

<dt>

<span data-ttu-id="d50a7-157">0</span><span class="sxs-lookup"><span data-stu-id="d50a7-157">0</span></span>
</dt> <dd>

<span data-ttu-id="d50a7-158">Toda la inicialización de este proveedor debe estar serializada.</span><span class="sxs-lookup"><span data-stu-id="d50a7-158">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-159">1</span><span class="sxs-lookup"><span data-stu-id="d50a7-159">1</span></span>
</dt> <dd>

<span data-ttu-id="d50a7-160">Todas las inicializaciones de este proveedor en el mismo espacio de nombres se deben serializar.</span><span class="sxs-lookup"><span data-stu-id="d50a7-160">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-161">2</span><span class="sxs-lookup"><span data-stu-id="d50a7-161">2</span></span>
</dt> <dd>

<span data-ttu-id="d50a7-162">No es necesaria ninguna serialización de inicialización.</span><span class="sxs-lookup"><span data-stu-id="d50a7-162">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d50a7-163">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="d50a7-163">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-164">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d50a7-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-166">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-167">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="d50a7-167">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-168">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-170">TBD</span><span class="sxs-lookup"><span data-stu-id="d50a7-170">TBD</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-171">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d50a7-171">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d50a7-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-174">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d50a7-174">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-175">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d50a7-175">The provider name.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-176">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="d50a7-176">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-177">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d50a7-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-179">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-180">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="d50a7-180">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-181">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-183">Si es **true**, el proveedor se inicializa para cada configuración regional cuando un usuario se conecta al mismo espacio de nombres más de una vez con diferentes configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="d50a7-183">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="d50a7-184">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d50a7-184">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-185">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="d50a7-185">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-186">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-188">Si es **true**, el proveedor se inicializa una vez por cada usuario de NT LAN Manager (NTLM) que realiza solicitudes al proveedor.</span><span class="sxs-lookup"><span data-stu-id="d50a7-188">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="d50a7-189">Si es **false** (valor predeterminado), el proveedor se inicializa una vez para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d50a7-189">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-190">**Pura**</span><span class="sxs-lookup"><span data-stu-id="d50a7-190">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-191">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-193">Si **es true**, el proveedor acuerda preparar la descarga llamando a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al método de **versión** de su interfaz principal.</span><span class="sxs-lookup"><span data-stu-id="d50a7-193">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="d50a7-194">Los proveedores que deben seguir siendo clientes de WMI después de no funcionar como proveedores deberían establecer **puro** en **false**.</span><span class="sxs-lookup"><span data-stu-id="d50a7-194">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="d50a7-195">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="d50a7-195">The default setting is **TRUE**.</span></span> <span data-ttu-id="d50a7-196">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="d50a7-196">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-197">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d50a7-197">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d50a7-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-199">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-200">Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que determina el conjunto de usuarios que pueden llamar correctamente a [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para el proveedor desacoplado.</span><span class="sxs-lookup"><span data-stu-id="d50a7-200">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="d50a7-201">Para obtener más información, vea el tema [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) en la sección seguridad de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d50a7-201">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="d50a7-202">Este descriptor de seguridad solo se usa para los proveedores desacoplados y no afecta a otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="d50a7-202">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="d50a7-203">Para obtener más información, vea [incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="d50a7-203">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="d50a7-204">WMI realiza comprobaciones de acceso para los proveedores desacoplados que usan las interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="d50a7-204">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](iwbemobjectsink.md) interfaces.</span></span> <span data-ttu-id="d50a7-205">Si el descriptor de seguridad es **null**, solo las aplicaciones o servicios que se ejecutan en las cuentas LocalSystem, NetworkService y LocalService pueden ejecutar un proveedor desacoplado.</span><span class="sxs-lookup"><span data-stu-id="d50a7-205">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="d50a7-206">La siguiente cadena muestra un proveedor desacoplado que solo deben ejecutar los administradores integrados ". O:BAG: BAD: (A;; 0 x1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="d50a7-206">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="d50a7-207">Para obtener más información acerca de cómo establecer la propiedad **SecurityDescriptor** , vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="d50a7-207">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-208">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="d50a7-208">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-209">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-210">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-211">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-212">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="d50a7-212">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-213">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-215">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-216">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="d50a7-216">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-217">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-218">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-219">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-219">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-220">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="d50a7-220">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-221">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-222">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-223">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-223">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-224">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="d50a7-224">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-225">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-227">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-227">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-228">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="d50a7-228">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-229">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d50a7-229">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-230">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-230">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-231">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d50a7-231">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-232">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="d50a7-232">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-233">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d50a7-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-234">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-234">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-235">[Formato de fecha y hora](date-and-time-format.md) que especifica el tiempo que WMI permite que el proveedor permanezca inactivo antes de que se descargue.</span><span class="sxs-lookup"><span data-stu-id="d50a7-235">[Date and Time Format](date-and-time-format.md) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="d50a7-236">Normalmente, los proveedores solicitan que WMI espere más de cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="d50a7-236">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="d50a7-237">Para la versión actual de WMI, se omite el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d50a7-237">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="d50a7-238">WMI descarga el proveedor basándose en el valor de tiempo de espera de una clase interna en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="d50a7-238">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="d50a7-239">Se recomienda que los proveedores establezcan **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="d50a7-239">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="d50a7-240">Para obtener más información, vea [descargar un proveedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d50a7-240">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="d50a7-241">**Versión**</span><span class="sxs-lookup"><span data-stu-id="d50a7-241">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d50a7-242">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d50a7-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d50a7-243">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d50a7-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d50a7-244">Versión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d50a7-244">Version of the provider.</span></span> <span data-ttu-id="d50a7-245">Las versiones admitidas son 1 y 2.</span><span class="sxs-lookup"><span data-stu-id="d50a7-245">The supported versions are 1 and 2.</span></span> <span data-ttu-id="d50a7-246">La versión 2 fortalece las comprobaciones de validez de todos los registros de propiedades asociados, en concreto la propiedad [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="d50a7-246">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d50a7-247">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d50a7-247">Remarks</span></span>

<span data-ttu-id="d50a7-248">La clase **\_ \_ Win32Provider** se deriva de [**\_ \_ Provider**](--provider.md).</span><span class="sxs-lookup"><span data-stu-id="d50a7-248">The **\_\_Win32Provider** class is derived from [**\_\_Provider**](--provider.md).</span></span>

<span data-ttu-id="d50a7-249">La mayoría de los proveedores pueden aceptar los valores predeterminados para la propiedad **InitializationReentrancy** .</span><span class="sxs-lookup"><span data-stu-id="d50a7-249">Most providers can accept the default values for the **InitializationReentrancy** property.</span></span> <span data-ttu-id="d50a7-250">Sin embargo, si un proveedor puede admitir la inicialización simultánea para usuarios independientes, esta propiedad se puede establecer en 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="d50a7-250">However, if a provider can support simultaneous initialization for separate users, this property can be set to 1 (one).</span></span> <span data-ttu-id="d50a7-251">Si es necesaria la inicialización serializada, **InitializationReentrancy** sigue siendo 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d50a7-251">If serialized initialization is necessary, **InitializationReentrancy** remains 0 (zero).</span></span> <span data-ttu-id="d50a7-252">En ambas instancias, **PerUserInitialization** se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="d50a7-252">In both instances, **PerUserInitialization** is set to **TRUE**.</span></span>

<span data-ttu-id="d50a7-253">Un proveedor puro o un proveedor que establece la propiedad **Pure** en **true** solo existe para las solicitudes de servicio de las aplicaciones y WMI.</span><span class="sxs-lookup"><span data-stu-id="d50a7-253">A pure provider or a provider that sets the **Pure** property to **TRUE**, exists only to service requests from applications and WMI.</span></span> <span data-ttu-id="d50a7-254">La mayoría de los proveedores son proveedores puros.</span><span class="sxs-lookup"><span data-stu-id="d50a7-254">Most providers are pure providers.</span></span> <span data-ttu-id="d50a7-255">Un proveedor no puro es la excepción.</span><span class="sxs-lookup"><span data-stu-id="d50a7-255">A nonpure provider is the exception.</span></span> <span data-ttu-id="d50a7-256">Los proveedores no puros pasan al rol de cliente después de completar las solicitudes de servicio.</span><span class="sxs-lookup"><span data-stu-id="d50a7-256">Nonpure providers transition to the role of client after they complete servicing requests.</span></span>

<span data-ttu-id="d50a7-257">Un ejemplo de un proveedor no puro es un proveedor de inserciones que empieza a emitir consultas y realiza solicitudes de WMI después de completar la inicialización.</span><span class="sxs-lookup"><span data-stu-id="d50a7-257">An example of a nonpure provider is a push provider that starts to issue queries, and makes requests of WMI after it completes initialization.</span></span> <span data-ttu-id="d50a7-258">Un proveedor de inserciones no tiene responsabilidades salvo para actualizar el repositorio CIM con datos en el momento de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="d50a7-258">A push provider does not have responsibilities except to update the CIM repository with data at initialization time.</span></span> <span data-ttu-id="d50a7-259">Después de actualizar el repositorio, un proveedor de inserciones puede esperar a que se descargue o pasar al rol de cliente.</span><span class="sxs-lookup"><span data-stu-id="d50a7-259">After updating the repository, a push provider can wait to be unloaded, or transition to the role of client.</span></span> <span data-ttu-id="d50a7-260">El proveedor de inserciones que espera que se descargue es un proveedor puro.</span><span class="sxs-lookup"><span data-stu-id="d50a7-260">The push provider that waits to be unloaded is a pure provider.</span></span> <span data-ttu-id="d50a7-261">El proveedor de inserciones que participa en las actividades del cliente no es puro.</span><span class="sxs-lookup"><span data-stu-id="d50a7-261">The push provider that participates in client activities is nonpure.</span></span>

<span data-ttu-id="d50a7-262">WMI debe ser capaz de distinguir los proveedores puros de los proveedores no puros para que pueda determinar cuándo es seguro apagar.</span><span class="sxs-lookup"><span data-stu-id="d50a7-262">WMI must be able to distinguish pure providers from non-pure providers so that it can determine when it is safe to shut down.</span></span> <span data-ttu-id="d50a7-263">WMI debe esperar a que se completen todas las operaciones que implican proveedores no puros antes de poder cerrarse de forma segura.</span><span class="sxs-lookup"><span data-stu-id="d50a7-263">WMI must wait for all operations that involve non-pure providers to complete before it can shut down safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="d50a7-264">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d50a7-264">Requirements</span></span>



| <span data-ttu-id="d50a7-265">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50a7-265">Requirement</span></span> | <span data-ttu-id="d50a7-266">Value</span><span class="sxs-lookup"><span data-stu-id="d50a7-266">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d50a7-267">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d50a7-267">Minimum supported client</span></span><br/> | <span data-ttu-id="d50a7-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d50a7-268">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d50a7-269">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d50a7-269">Minimum supported server</span></span><br/> | <span data-ttu-id="d50a7-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d50a7-270">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d50a7-271">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d50a7-271">Namespace</span></span><br/>                | <span data-ttu-id="d50a7-272">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="d50a7-272">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d50a7-273">Vea también</span><span class="sxs-lookup"><span data-stu-id="d50a7-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50a7-274">**\_\_Proveedor**</span><span class="sxs-lookup"><span data-stu-id="d50a7-274">**\_\_Provider**</span></span>](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[<span data-ttu-id="d50a7-275">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d50a7-275">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d50a7-276">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="d50a7-276">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

