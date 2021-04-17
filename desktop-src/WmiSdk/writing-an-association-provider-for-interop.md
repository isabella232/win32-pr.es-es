---
description: Un proveedor de asociaciones proporciona un mecanismo para registrar perfiles y asociarlos a perfiles que se implementan en distintos espacios de nombres.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Escribir un proveedor de Asociación para la interoperabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718585"
---
# <a name="writing-an-association-provider-for-interop"></a><span data-ttu-id="dab97-103">Escribir un proveedor de Asociación para la interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="dab97-103">Writing an Association Provider for Interop</span></span>

<span data-ttu-id="dab97-104">Un proveedor de asociaciones proporciona un mecanismo para registrar perfiles y asociarlos a perfiles que se implementan en distintos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="dab97-104">An association provider provides a mechanism to register profiles and associate them with profiles that are implemented in different namespaces.</span></span>

<span data-ttu-id="dab97-105">Los proveedores de asociación se utilizan para exponer perfiles estándar, como un perfil de energía.</span><span class="sxs-lookup"><span data-stu-id="dab97-105">Association providers are used to expose standard profiles, like a power profile.</span></span> <span data-ttu-id="dab97-106">Para ello, se escribe un proveedor de asociación en el espacio de nombres de la raíz o la interoperabilidad que expone las instancias de asociación implementando una clase, que se deriva de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dab97-106">This is accomplished by writing an association provider in the root/interop namespace that exposes association instances by implementing a class, which is derived from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span> <span data-ttu-id="dab97-107">El proveedor se debe registrar tanto en la raíz como en la interoperabilidad, y en el espacio de nombres/raíz <implemented> para admitir el cruce seguro del espacio de nombres cruzado.</span><span class="sxs-lookup"><span data-stu-id="dab97-107">The provider must be registered in both the root/interop and the root/<implemented> namespace to support cross namespace traversal.</span></span>

<span data-ttu-id="dab97-108">Instrumental de administración de Windows (WMI) carga el proveedor de asociación siempre que se ejecute una consulta de asociación en el espacio de nombres de la raíz o la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="dab97-108">Windows Management Instrumentation (WMI) loads the association provider whenever an association query is run in the root/interop namespace.</span></span>

<span data-ttu-id="dab97-109">**Para implementar un proveedor de Asociación para la interoperabilidad**</span><span class="sxs-lookup"><span data-stu-id="dab97-109">**To implement an association provider for interop**</span></span>

1.  <span data-ttu-id="dab97-110">Derive una clase de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) y cree una instancia estática de esta clase derivada en el \\ espacio de nombres de interoperabilidad raíz.</span><span class="sxs-lookup"><span data-stu-id="dab97-110">Derive a class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and create a static instance of this derived class in the root\\interop namespace.</span></span> <span data-ttu-id="dab97-111">Como mínimo, las siguientes propiedades deben propagarse con valores válidos:</span><span class="sxs-lookup"><span data-stu-id="dab97-111">At a minimum, the following properties must be propagated with valid values:</span></span>

    -   <span data-ttu-id="dab97-112">[**ID**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dab97-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="dab97-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dab97-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="dab97-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dab97-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="dab97-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dab97-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span></span>

    <span data-ttu-id="dab97-116">Aunque [**InstanceID**](/previous-versions//ee309375(v=vs.85)) define de forma única la instancia de **\_ RegisteredProfile de CIM**, la combinación de **RegisteredName**, **RegisteredOrganization** y **RegisteredVersion** debe identificar de forma única el perfil registrado dentro del ámbito de la organización.</span><span class="sxs-lookup"><span data-stu-id="dab97-116">Even though [**InstanceID**](/previous-versions//ee309375(v=vs.85)) uniquely defines the instance of the **CIM\_RegisteredProfile**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="dab97-117">Para obtener más información acerca de las propiedades individuales, consulte [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dab97-117">For more information about the individual properties, see [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

    <span data-ttu-id="dab97-118">En el ejemplo de código siguiente se describe la sintaxis para derivar la clase **ProcessProfile** de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) y rellenar la instancia estática.</span><span class="sxs-lookup"><span data-stu-id="dab97-118">The following code example describes the syntax for deriving the **ProcessProfile** class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and populating the static instance.</span></span>

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > <span data-ttu-id="dab97-119">En el caso de los clientes de Windows, la propiedad **RegisteredOrganization** debe establecerse en 1 y la propiedad **OtherRegisteredOrganization** establecida en "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="dab97-119">For Windows clients, the **RegisteredOrganization** property must be set to 1 and the **OtherRegisteredOrganization** property set to "Microsoft".</span></span>

     

2.  <span data-ttu-id="dab97-120">Cree un proveedor que devuelva instancias de Asociación de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span><span class="sxs-lookup"><span data-stu-id="dab97-120">Create a provider that returns association instances of [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span></span> <span data-ttu-id="dab97-121">Se trata de un proceso de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="dab97-121">This is a two-step process.</span></span>

    1.  <span data-ttu-id="dab97-122">Cree una clase que se derive de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en los espacios de nombres de interoperabilidad e implementación.</span><span class="sxs-lookup"><span data-stu-id="dab97-122">Create a class that is derived from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in both the interop and implementation namespaces.</span></span> <span data-ttu-id="dab97-123">Dado que los distintos proveedores pueden implementar el mismo perfil, el nombre de la clase debe ser único.</span><span class="sxs-lookup"><span data-stu-id="dab97-123">Because the same profile can be implemented by different vendors, the name of the class should be unique.</span></span> <span data-ttu-id="dab97-124">La Convención de nomenclatura recomendada es " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ".</span><span class="sxs-lookup"><span data-stu-id="dab97-124">The recommended naming convention is "<Organization>\_<ProductName>\_<ClassName>\_<Version>".</span></span> <span data-ttu-id="dab97-125">Tanto la propiedad **ConformantStandard** como la propiedad **ManagedElement** deben especificar el calificador **msft \_ targetNamespace** que contiene el espacio de nombres al que pertenece esta clase.</span><span class="sxs-lookup"><span data-stu-id="dab97-125">Either the **ConformantStandard** or the **ManagedElement** property must specify the **MSFT\_TargetNamespace** qualifier that contains the namespace to which this class belongs.</span></span>

        <span data-ttu-id="dab97-126">En el ejemplo de código siguiente se describe la sintaxis para derivar la \_ clase Microsoft Process \_ ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el \\ espacio de nombres de interoperabilidad raíz.</span><span class="sxs-lookup"><span data-stu-id="dab97-126">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\interop namespace.</span></span> <span data-ttu-id="dab97-127">En este ejemplo, el \_ elemento administrado por el proceso de Win32 hace referencia al \\ espacio de nombres root cimv2 mediante el calificador de **msft \_ targetNamespace** .</span><span class="sxs-lookup"><span data-stu-id="dab97-127">In this example, the Win32\_Process managed element references the root\\cimv2 namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="dab97-128">En el ejemplo de código siguiente se describe la sintaxis para derivar la \_ clase Microsoft Process \_ ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="dab97-128">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="dab97-129">En este ejemplo, el estándar compatible con [**\_ RegisteredProfile de CIM**](/previous-versions//ee309375(v=vs.85)) hace referencia al \\ espacio de nombres de interoperabilidad raíz mediante el calificador de **msft \_ targetNamespace** .</span><span class="sxs-lookup"><span data-stu-id="dab97-129">In this example, the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conformant standard references the root\\interop namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="dab97-130">Si no se especifica el calificador de **msft \_ targetNamespace** en la propiedad que hace referencia al espacio de nombres implementado, el filtro **ResultClass** de la instrucción "ASSOCIATORS of" no funcionará.</span><span class="sxs-lookup"><span data-stu-id="dab97-130">If the **MSFT\_TargetNamespace** qualifier is not specified on the property that is referencing the implemented namespace, the **ResultClass** filter of "Associators of" statement will not work.</span></span> <span data-ttu-id="dab97-131">Por ejemplo, si no se especifica el calificador de **msft \_ targetNamespace** , la siguiente línea de comandos de Windows PowerShell no devolverá un objeto: **Get-WMIObject-Query "associatorsrs de {ProcessProfile. InstanceId = ' Process '} donde ResultClass = ' \_ proceso Win32 '"**.</span><span class="sxs-lookup"><span data-stu-id="dab97-131">For example, if the **MSFT\_TargetNamespace** qualifier is not specified, the following Windows PowerShell command-line will not return an object: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32\_Process'"**.</span></span>

        <span data-ttu-id="dab97-132">El calificador de **msft \_ targetNamespace** no puede apuntar a un espacio de nombres de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="dab97-132">The **MSFT\_TargetNamespace** qualifier cannot point to a namespace on a remote computer.</span></span> <span data-ttu-id="dab97-133">Por ejemplo, no se admite el siguiente espacio de nombres: msft \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ interoperabilidad de raíz).</span><span class="sxs-lookup"><span data-stu-id="dab97-133">For example, the following namespace is not supported: MSFT\_TargetNamespace(\\\\\\\\<RemoteMachine>\\\\root\\\\interop).</span></span>

    2.  <span data-ttu-id="dab97-134">Escriba un proveedor que devuelva instancias de la clase derivada creada.</span><span class="sxs-lookup"><span data-stu-id="dab97-134">Write a provider that returns instances of the created derived class.</span></span> <span data-ttu-id="dab97-135">Para obtener más información, consulte [escribir un proveedor de instancias](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dab97-135">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span> <span data-ttu-id="dab97-136">Al acceder a las instancias entre espacios de nombres, es posible que tenga que tener acceso a los niveles de seguridad del cliente.</span><span class="sxs-lookup"><span data-stu-id="dab97-136">When you access cross-namespace instances, you might have to access the security levels for the client.</span></span> <span data-ttu-id="dab97-137">Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="dab97-137">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

        <span data-ttu-id="dab97-138">El proveedor de asociación debe implementar los métodos [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) y [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="dab97-138">The association provider should implement both the [**IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) and [**IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span> <span data-ttu-id="dab97-139">La implementación del método [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) es opcional.</span><span class="sxs-lookup"><span data-stu-id="dab97-139">Implementing the [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method is optional.</span></span> <span data-ttu-id="dab97-140">Dado que se puede tener acceso a este proveedor desde la \\ interoperabilidad raíz y los \\ <implemented> espacios de nombres raíz, no debe haber una dependencia explícita en un espacio de nombres dentro del proveedor.</span><span class="sxs-lookup"><span data-stu-id="dab97-140">Because this provider can be accessed from both the root\\interop and the root\\<implemented> namespaces, there should not be an explicit dependency on a namespace inside the provider.</span></span>

3.  <span data-ttu-id="dab97-141">Registre el proveedor de asociación en la \\ interoperabilidad raíz y en los \\ <implemented> espacios de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="dab97-141">Register the association provider in both the root\\interop and the root\\<implemented> namespaces.</span></span> <span data-ttu-id="dab97-142">Para obtener más información, vea [registrar un proveedor de instancias](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dab97-142">For more information, see [Registering an Instance Provider](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="dab97-143">En el ejemplo de código siguiente se describe la sintaxis para registrar el proveedor de asociación en el \\ espacio de nombres de interoperabilidad raíz.</span><span class="sxs-lookup"><span data-stu-id="dab97-143">The following code example describes the syntax to register the association provider in the root\\interop namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    <span data-ttu-id="dab97-144">En el ejemplo de código siguiente se describe la sintaxis para registrar el proveedor de asociación en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="dab97-144">The following code example describes the syntax to register the association provider in the root\\cimv2 namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  <span data-ttu-id="dab97-145">Coloque el esquema del [**\_ ElementConformsToProfile de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el espacio de nombres implementado.</span><span class="sxs-lookup"><span data-stu-id="dab97-145">Place the schema for the [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) into the implemented namespace.</span></span> <span data-ttu-id="dab97-146">En el caso de los clientes de Windows, este es el archivo Interop. mof que se encuentra en la carpeta% SystemRoot% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="dab97-146">For Windows clients this is the interop.mof file that is located in the %systemroot%\\system32\\wbem folder.</span></span>
5.  <span data-ttu-id="dab97-147">Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="dab97-147">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="dab97-148">WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="dab97-148">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="dab97-149">El método [**tializeIWbemProviderInit.Ini**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) debe implementarse de forma que permita que se llame para dos espacios de nombres diferentes.</span><span class="sxs-lookup"><span data-stu-id="dab97-149">The [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method should be implemented in a way that allows it to be called for two different namespaces.</span></span> <span data-ttu-id="dab97-150">Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dab97-150">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dab97-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dab97-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab97-152">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="dab97-152">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

<span data-ttu-id="dab97-153">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dab97-153">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dab97-154">Escribir un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="dab97-154">Writing an Instance Provider</span></span>](writing-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="dab97-155">Registrar un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="dab97-155">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

 
