---
title: Clase ReplicationProvider1
description: La clase base para la instancia del proveedor.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory de la clase ReplicationProvider1
- Active Directory de la clase ReplicationProvider1, descrito
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079278"
---
# <a name="replicationprovider1-class"></a><span data-ttu-id="b70fb-105">Clase ReplicationProvider1</span><span class="sxs-lookup"><span data-stu-id="b70fb-105">ReplicationProvider1 class</span></span>

<span data-ttu-id="b70fb-106">La clase base para la instancia del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b70fb-106">The base class for the provider instance.</span></span>

<span data-ttu-id="b70fb-107">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b70fb-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70fb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b70fb-108">Syntax</span></span>

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a><span data-ttu-id="b70fb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b70fb-109">Members</span></span>

<span data-ttu-id="b70fb-110">La clase **ReplicationProvider1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b70fb-110">The **ReplicationProvider1** class has these types of members:</span></span>

-   [<span data-ttu-id="b70fb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b70fb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b70fb-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b70fb-112">Properties</span></span>

<span data-ttu-id="b70fb-113">La clase **ReplicationProvider1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b70fb-113">The **ReplicationProvider1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b70fb-114">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="b70fb-114">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b70fb-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-117">Identificador de clase que WMI usa para determinar si se carga o no un proveedor de alto rendimiento en el proceso de cliente o en el proceso WMI.</span><span class="sxs-lookup"><span data-stu-id="b70fb-117">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="b70fb-118">Si el proveedor y el cliente se encuentran en el mismo equipo, WMI carga el proveedor en proceso en el cliente mediante **ClientLoadableCLSID** como identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="b70fb-118">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="b70fb-119">Cuando el proveedor y el cliente se encuentran en equipos diferentes, WMI carga el proveedor en proceso en WMI.</span><span class="sxs-lookup"><span data-stu-id="b70fb-119">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="b70fb-120">WMI también usa **ClientLoadableCLSID** para admitir las operaciones de actualización.</span><span class="sxs-lookup"><span data-stu-id="b70fb-120">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="b70fb-121">Para obtener más información, vea [registrar un proveedor de High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span><span class="sxs-lookup"><span data-stu-id="b70fb-121">For more information, see [Registering a High-Performance Provider.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span></span>

<span data-ttu-id="b70fb-122">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-122">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="b70fb-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b70fb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-126">**GUID** que representa el identificador de clase (**CLSID**) del objeto com del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b70fb-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="b70fb-127">Este objeto COM debe contener una implementación de la interfaz [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="b70fb-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

<span data-ttu-id="b70fb-128">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-128">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-129">**Simultaneidad**</span><span class="sxs-lookup"><span data-stu-id="b70fb-129">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-130">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b70fb-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-132">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-132">Not used.</span></span>

<span data-ttu-id="b70fb-133">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-133">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-134">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="b70fb-134">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b70fb-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-137">Identifica el equipo en el que se va a iniciar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="b70fb-137">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="b70fb-138">Si el proveedor se ejecuta en el equipo local, es **null**.</span><span class="sxs-lookup"><span data-stu-id="b70fb-138">If the provider runs on the local computer it is **NULL**.</span></span>

<span data-ttu-id="b70fb-139">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-139">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-140">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="b70fb-140">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-141">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-143">Si es **true**, esta instancia está habilitada y se puede usar para completar las solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="b70fb-143">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

<span data-ttu-id="b70fb-144">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-144">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-145">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="b70fb-145">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b70fb-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b70fb-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-148">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span><span class="sxs-lookup"><span data-stu-id="b70fb-148">Qualifiers: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-149">Contiene el modelo de hospedaje del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b70fb-149">Contains the hosting model of the provider.</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-150">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="b70fb-150">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-151">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b70fb-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-153">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b70fb-153">Reserved.</span></span> <span data-ttu-id="b70fb-154">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="b70fb-154">The default value is zero (0).</span></span>

<span data-ttu-id="b70fb-155">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-155">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-156">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="b70fb-156">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-157">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b70fb-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-159">Conjunto de marcas que proporcionan información sobre la serialización.</span><span class="sxs-lookup"><span data-stu-id="b70fb-159">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="b70fb-160">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="b70fb-160">The default value is zero (0).</span></span>

<span data-ttu-id="b70fb-161">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-161">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b70fb-162"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="b70fb-162"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b70fb-163">Toda la inicialización de este proveedor debe estar serializada.</span><span class="sxs-lookup"><span data-stu-id="b70fb-163">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b70fb-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b70fb-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b70fb-165">Todas las inicializaciones de este proveedor en el mismo espacio de nombres se deben serializar.</span><span class="sxs-lookup"><span data-stu-id="b70fb-165">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="b70fb-166"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="b70fb-166"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="b70fb-167">No es necesaria ninguna serialización de inicialización.</span><span class="sxs-lookup"><span data-stu-id="b70fb-167">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b70fb-168">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="b70fb-168">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-169">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b70fb-169">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-171">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-171">Not used.</span></span>

<span data-ttu-id="b70fb-172">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-172">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-173">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="b70fb-173">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-174">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-176">**Windows Server 2003:** Esta propiedad está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="b70fb-176">**Windows Server 2003:** This property is disabled.</span></span>

<span data-ttu-id="b70fb-177">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-177">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-178">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b70fb-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b70fb-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-180">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-181">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b70fb-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-182">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b70fb-182">The provider name.</span></span>

<span data-ttu-id="b70fb-183">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-183">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-184">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="b70fb-184">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-185">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b70fb-185">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-186">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-187">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-187">Not used.</span></span>

<span data-ttu-id="b70fb-188">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-188">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-189">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="b70fb-189">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-190">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-191">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-192">Si es **true**, el proveedor se inicializa para cada configuración regional cuando un usuario se conecta al mismo espacio de nombres más de una vez con diferentes configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="b70fb-192">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="b70fb-193">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b70fb-193">The default value is **FALSE**.</span></span>

<span data-ttu-id="b70fb-194">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-194">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-195">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="b70fb-195">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-197">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-198">Si es **true**, el proveedor se inicializa una vez por cada usuario de NT LAN Manager (NTLM) que realiza solicitudes al proveedor.</span><span class="sxs-lookup"><span data-stu-id="b70fb-198">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="b70fb-199">Si es **false** (valor predeterminado), el proveedor se inicializa una vez para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b70fb-199">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

<span data-ttu-id="b70fb-200">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-200">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-201">**Pura**</span><span class="sxs-lookup"><span data-stu-id="b70fb-201">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-202">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-203">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-203">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-204">Si **es true**, el proveedor acuerda preparar la descarga llamando a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al método de **versión** de su interfaz principal.</span><span class="sxs-lookup"><span data-stu-id="b70fb-204">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="b70fb-205">Los proveedores que deben seguir siendo clientes de WMI después de no funcionar como proveedores deberían establecer **puro** en **false**.</span><span class="sxs-lookup"><span data-stu-id="b70fb-205">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="b70fb-206">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="b70fb-206">The default setting is **TRUE**.</span></span> <span data-ttu-id="b70fb-207">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="b70fb-207">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="b70fb-208">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-208">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-209">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b70fb-209">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b70fb-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-212">Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que determina el conjunto de usuarios que pueden llamar correctamente a [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para el proveedor desacoplado.</span><span class="sxs-lookup"><span data-stu-id="b70fb-212">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="b70fb-213">Para obtener más información, vea el tema [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) en la sección seguridad de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b70fb-213">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="b70fb-214">Este descriptor de seguridad solo se usa para los proveedores desacoplados y no afecta a otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="b70fb-214">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="b70fb-215">Para obtener más información, vea [incorporación de un proveedor en una aplicación](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span><span class="sxs-lookup"><span data-stu-id="b70fb-215">For more information, see [Incorporating a Provider in an Application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span></span>

<span data-ttu-id="b70fb-216">WMI realiza comprobaciones de acceso para los proveedores desacoplados que usan las interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) y [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="b70fb-216">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) interfaces.</span></span> <span data-ttu-id="b70fb-217">Si el descriptor de seguridad es **null**, solo las aplicaciones o servicios que se ejecutan en las cuentas LocalSystem, NetworkService y LocalService pueden ejecutar un proveedor desacoplado.</span><span class="sxs-lookup"><span data-stu-id="b70fb-217">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="b70fb-218">La siguiente cadena muestra un proveedor desacoplado que solo deben ejecutar los administradores integrados ". O:BAG: BAD: (A;; 0 x1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="b70fb-218">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="b70fb-219">Para obtener más información acerca de cómo establecer la propiedad **SecurityDescriptor** , vea [mantener la seguridad de WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).</span><span class="sxs-lookup"><span data-stu-id="b70fb-219">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).</span></span>

<span data-ttu-id="b70fb-220">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-220">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-221">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="b70fb-221">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-222">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-224">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-224">Not used.</span></span>

<span data-ttu-id="b70fb-225">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-225">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-226">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="b70fb-226">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-227">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-228">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-229">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-229">Not used.</span></span>

<span data-ttu-id="b70fb-230">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-230">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-231">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="b70fb-231">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-232">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-233">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-233">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-234">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-234">Not used.</span></span>

<span data-ttu-id="b70fb-235">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-235">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-236">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="b70fb-236">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-237">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-238">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-239">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-239">Not used.</span></span>

<span data-ttu-id="b70fb-240">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-240">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-241">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="b70fb-241">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-242">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-243">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-244">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-244">Not used.</span></span>

<span data-ttu-id="b70fb-245">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-245">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-246">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="b70fb-246">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-247">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b70fb-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-248">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-249">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b70fb-249">Not used.</span></span>

<span data-ttu-id="b70fb-250">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-250">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-251">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="b70fb-251">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-252">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b70fb-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-254">[Formato de fecha y hora](/windows/desktop/WmiSdk/date-and-time-format) que especifica el tiempo que WMI permite que el proveedor permanezca inactivo antes de que se descargue.</span><span class="sxs-lookup"><span data-stu-id="b70fb-254">[Date and Time Format](/windows/desktop/WmiSdk/date-and-time-format) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="b70fb-255">Normalmente, los proveedores solicitan que WMI espere más de cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="b70fb-255">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="b70fb-256">Para la versión actual de WMI, se omite el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b70fb-256">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="b70fb-257">WMI descarga el proveedor basándose en el valor de tiempo de espera de una clase interna en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="b70fb-257">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="b70fb-258">Se recomienda que los proveedores establezcan **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="b70fb-258">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="b70fb-259">Para obtener más información, vea [descargar un proveedor](/windows/desktop/WmiSdk/unloading-a-provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-259">For more information, see [Unloading a Provider](/windows/desktop/WmiSdk/unloading-a-provider).</span></span>

<span data-ttu-id="b70fb-260">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-260">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b70fb-261">**Versión**</span><span class="sxs-lookup"><span data-stu-id="b70fb-261">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b70fb-262">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b70fb-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b70fb-263">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b70fb-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b70fb-264">Versión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b70fb-264">Version of the provider.</span></span> <span data-ttu-id="b70fb-265">Las versiones admitidas son 1 y 2.</span><span class="sxs-lookup"><span data-stu-id="b70fb-265">The supported versions are 1 and 2.</span></span> <span data-ttu-id="b70fb-266">La versión 2 fortalece las comprobaciones de validez de todos los registros de propiedades asociados, en concreto la propiedad [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .</span><span class="sxs-lookup"><span data-stu-id="b70fb-266">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) property.</span></span>

<span data-ttu-id="b70fb-267">Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="b70fb-267">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b70fb-268">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b70fb-268">Remarks</span></span>

<span data-ttu-id="b70fb-269">Una instancia de esta clase representa el proveedor WMI para Dominio de Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="b70fb-269">An instance of this class represents the WMI provider for Active Directory Domain services.</span></span> <span data-ttu-id="b70fb-270">Los valores predeterminados son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b70fb-270">The defaults are as follows:</span></span>

-   <span data-ttu-id="b70fb-271">Name = "ReplProv1"</span><span class="sxs-lookup"><span data-stu-id="b70fb-271">Name = "ReplProv1"</span></span>
-   <span data-ttu-id="b70fb-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span><span class="sxs-lookup"><span data-stu-id="b70fb-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span></span>
-   <span data-ttu-id="b70fb-273">HostingModel = "NetworkServiceHost"</span><span class="sxs-lookup"><span data-stu-id="b70fb-273">HostingModel = "NetworkServiceHost"</span></span>

## <a name="requirements"></a><span data-ttu-id="b70fb-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b70fb-274">Requirements</span></span>



| <span data-ttu-id="b70fb-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="b70fb-275">Requirement</span></span> | <span data-ttu-id="b70fb-276">Value</span><span class="sxs-lookup"><span data-stu-id="b70fb-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b70fb-277">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b70fb-277">Minimum supported client</span></span><br/> | <span data-ttu-id="b70fb-278">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b70fb-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b70fb-279">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b70fb-279">Minimum supported server</span></span><br/> | <span data-ttu-id="b70fb-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b70fb-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b70fb-281">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b70fb-281">Namespace</span></span><br/>                | <span data-ttu-id="b70fb-282">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="b70fb-282">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="b70fb-283">MOF</span><span class="sxs-lookup"><span data-stu-id="b70fb-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b70fb-284"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b70fb-284"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="b70fb-285">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b70fb-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b70fb-286"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b70fb-286"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b70fb-287">Vea también</span><span class="sxs-lookup"><span data-stu-id="b70fb-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70fb-288">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="b70fb-288">**\_\_Win32Provider**</span></span>](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

