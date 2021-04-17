---
description: Un método de proveedor es un método implementado por un proveedor de Instrumental de administración de Windows (WMI).
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: Llamar a un método de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ed8d05a1105c15f06b3df5f47006c5dafcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706768"
---
# <a name="calling-a-provider-method"></a><span data-ttu-id="d1906-103">Llamar a un método de proveedor</span><span class="sxs-lookup"><span data-stu-id="d1906-103">Calling a Provider Method</span></span>

<span data-ttu-id="d1906-104">Un método de proveedor es un método implementado por un proveedor de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d1906-104">A provider method is a method that is implemented by a Windows Management Instrumentation (WMI) provider.</span></span> <span data-ttu-id="d1906-105">El método se encuentra en una clase definida por un proveedor para representar datos de software o hardware.</span><span class="sxs-lookup"><span data-stu-id="d1906-105">The method is found in a class defined by a provider to represent data from software or hardware.</span></span> <span data-ttu-id="d1906-106">Por ejemplo, la clase de [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) tiene métodos para iniciar, detener, reanudar, pausar y cambiar servicios.</span><span class="sxs-lookup"><span data-stu-id="d1906-106">For example, the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class has methods to start, stop, resume, pause, and change services.</span></span>

<span data-ttu-id="d1906-107">Los métodos de proveedor no se deben confundir con los siguientes tipos de métodos:</span><span class="sxs-lookup"><span data-stu-id="d1906-107">Provider methods should not be confused with the following types of methods:</span></span>

-   <span data-ttu-id="d1906-108">Métodos en [las clases del sistema de WMI](wmi-system-classes.md), [**como el método**](--systemsecurity-getsd.md) de [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-108">Methods on [WMI system classes](wmi-system-classes.md), such as the [**GetSD**](--systemsecurity-getsd.md) method on [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>
-   <span data-ttu-id="d1906-109">Métodos en objetos de la [API de scripting para WMI](scripting-api-for-wmi.md), como [**SWbemServices. instances**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-109">Methods on objects in the [Scripting API for WMI](scripting-api-for-wmi.md), such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>
-   <span data-ttu-id="d1906-110">Métodos de la [API de com para WMI](com-api-for-wmi.md), como [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="d1906-110">Methods in the [COM API for WMI](com-api-for-wmi.md), such as [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

## <a name="calling-a-provider-method-using-scripting"></a><span data-ttu-id="d1906-111">Llamar a un método de proveedor mediante scripting</span><span class="sxs-lookup"><span data-stu-id="d1906-111">Calling a Provider Method Using Scripting</span></span>

<span data-ttu-id="d1906-112">Cualquier lenguaje de automatización, como VBScript, PowerShell o Perl, puede llamar a un método WMI.</span><span class="sxs-lookup"><span data-stu-id="d1906-112">Any automation language, such as VBScript, PowerShell, or Perl, can call a WMI method.</span></span> <span data-ttu-id="d1906-113">Algunos lenguajes pueden usar el [acceso directo](/windows), pero otros deben usar [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) para ejecutar el método de proveedor indirectamente.</span><span class="sxs-lookup"><span data-stu-id="d1906-113">Some languages can use [direct access](/windows), but others must use [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to execute the provider method indirectly.</span></span>

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

<span data-ttu-id="d1906-114">En el procedimiento siguiente se describe cómo llamar a un método de proveedor mediante la API de scripting y el uso de acceso directo.</span><span class="sxs-lookup"><span data-stu-id="d1906-114">The following procedure describes how to call a provider method using the Scripting API and using direct access.</span></span>

<span data-ttu-id="d1906-115">**Para llamar a un método de proveedor mediante la API de scripting y el acceso directo**</span><span class="sxs-lookup"><span data-stu-id="d1906-115">**To call a provider method using the Scripting API and direct access**</span></span>

1.  <span data-ttu-id="d1906-116">Use este enfoque para VBScript o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d1906-116">Use this approach for VBScript or PowerShell.</span></span>
2.  <span data-ttu-id="d1906-117">Determine si el método que desea ejecutar está implementado.</span><span class="sxs-lookup"><span data-stu-id="d1906-117">Determine if the method you want to execute is implemented.</span></span>

    <span data-ttu-id="d1906-118">Algunas clases tienen métodos definidos que no son compatibles con un proveedor.</span><span class="sxs-lookup"><span data-stu-id="d1906-118">Some classes have methods defined that are not supported by a provider.</span></span> <span data-ttu-id="d1906-119">Si un método no está implementado, no se puede ejecutar.</span><span class="sxs-lookup"><span data-stu-id="d1906-119">If a method is not implemented, you cannot execute it.</span></span> <span data-ttu-id="d1906-120">Puede determinar si un método se implementa comprobando si el método tiene el calificador [**implementado**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="d1906-120">You can determine if a method is implemented by checking if the method has the [**Implemented**](standard-wmi-qualifiers.md) qualifier.</span></span> <span data-ttu-id="d1906-121">Para obtener más información, vea [calificadores de WMI](wmi-qualifiers.md) y [obtener acceso a un calificador de WMI](accessing-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-121">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Accessing a WMI Qualifier](accessing-a-qualifier.md).</span></span> <span data-ttu-id="d1906-122">También puede determinar si un método de clase de proveedor tiene establecido el calificador **implementado** mediante la ejecución de la utilidad de Wbemtest.exe no compatible, disponible en cualquier sistema operativo con WMI instalado.</span><span class="sxs-lookup"><span data-stu-id="d1906-122">You can also determine if a provider class method has the **Implemented** qualifier set by running the unsupported Wbemtest.exe utility, available on any operating system with WMI installed.</span></span>

3.  <span data-ttu-id="d1906-123">Determine si el método que desea ejecutar es un [*método estático*](gloss-s.md) o un método no estático.</span><span class="sxs-lookup"><span data-stu-id="d1906-123">Determine if the method you want to execute is a [*static method*](gloss-s.md) or a nonstatic method.</span></span>

    <span data-ttu-id="d1906-124">Los métodos estáticos solo se aplican a las clases WMI y no a instancias específicas de una clase.</span><span class="sxs-lookup"><span data-stu-id="d1906-124">Static methods apply only to WMI classes and not to specific instances of a class.</span></span> <span data-ttu-id="d1906-125">Por ejemplo, el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) es un método estático porque se usa para crear un nuevo proceso sin una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="d1906-125">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is a static method because use it to create a new process without an instance of this class.</span></span> <span data-ttu-id="d1906-126">Los métodos no estáticos solo se aplican a las instancias de una clase.</span><span class="sxs-lookup"><span data-stu-id="d1906-126">Nonstatic methods apply only to instances of a class.</span></span> <span data-ttu-id="d1906-127">Por ejemplo, el método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) de la clase de **\_ proceso de Win32** es un método no estático, ya que solo tiene sentido finalizar un proceso si existe una instancia de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="d1906-127">For example, the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method of the **Win32\_Process** class is a nonstatic method because it only makes sense to terminate a process if an instance of that process exists.</span></span> <span data-ttu-id="d1906-128">Puede determinar si un método es estático comprobando si el calificador [**estático**](standard-wmi-qualifiers.md) está asociado al método.</span><span class="sxs-lookup"><span data-stu-id="d1906-128">You can determine if a method is static by checking if the [**Static**](standard-wmi-qualifiers.md) qualifier is associated with the method.</span></span>

4.  <span data-ttu-id="d1906-129">Recupere la clase o instancia que contiene el método que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="d1906-129">Retrieve the class or instance that contains the method you want to execute.</span></span>

    <span data-ttu-id="d1906-130">Para obtener más información, consulte [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-130">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

5.  <span data-ttu-id="d1906-131">Configure las opciones de seguridad que pueda necesitar el método.</span><span class="sxs-lookup"><span data-stu-id="d1906-131">Set up any security settings that the method may require.</span></span>

    <span data-ttu-id="d1906-132">A menudo, puede determinar los privilegios que requiere un método examinando los valores del calificador [**privileges**](swbemsecurity-privileges.md) del método.</span><span class="sxs-lookup"><span data-stu-id="d1906-132">You can often determine the privileges that a method requires by examining the values in the [**Privileges**](swbemsecurity-privileges.md) qualifier of the method.</span></span> <span data-ttu-id="d1906-133">Por ejemplo, el método [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) de clase de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requiere la configuración del privilegio "SeShutdownPrivilege".</span><span class="sxs-lookup"><span data-stu-id="d1906-133">For example, the [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) method requires you to set the "SeShutdownPrivilege" privilege.</span></span> <span data-ttu-id="d1906-134">Para obtener más información, vea [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-134">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

6.  <span data-ttu-id="d1906-135">Llame al método y examine el valor devuelto para determinar si el método se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d1906-135">Call the method and examine the return value to determine if the method was successful.</span></span>

<span data-ttu-id="d1906-136">En el ejemplo de código siguiente se crea un proceso de Bloc de notas y se obtiene el identificador de proceso mediante el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="d1906-136">The following code example creates a Notepad process and gets the process ID using direct access.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_Process")

Error = objWMIService.Create("notepad.exe", null, _
    null, intProcessID)
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & intProcessID & "."
Else
    Wscript.Echo "Notepad could not be started due to error " _
       & Error & "."
End If  
```


```PowerShell

try
{ 
    $myProcess = ([wmiclass]&quot;win32_process&quot;).create(&quot;notepad.exe&quot;, $null, $null) 
}
catch 
{
    &quot;Notepad could not be started due to the following error:&quot; 
    $error[0]
    return 
}
#else
&quot;Notepad was started with a process ID of &quot; + $myProcess.ProcessID
```





<span id="indirect_access"></span><span id="INDIRECT_ACCESS"></span>

<span data-ttu-id="d1906-137">En el procedimiento siguiente se describe cómo llamar a un método de proveedor mediante la API de scripting y el [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-137">The following procedure describes how to call a provider method using the Scripting API and the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="d1906-138">**Para llamar a un método de proveedor mediante la API de scripting y SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="d1906-138">**To call a provider method using the Scripting API and SWbemServices.ExecMethod**</span></span>

1.  <span data-ttu-id="d1906-139">Recupere la definición de clase WMI para ejecutar un método estático.</span><span class="sxs-lookup"><span data-stu-id="d1906-139">Retrieve the WMI class definition to execute a static method.</span></span> <span data-ttu-id="d1906-140">Recupere la instancia de clase WMI para ejecutar un método no estático.</span><span class="sxs-lookup"><span data-stu-id="d1906-140">Retrieve the WMI class instance to execute a nonstatic method.</span></span>
2.  <span data-ttu-id="d1906-141">Recupere el método que se va a ejecutar desde la colección [**SWbemObject. Methods \_**](swbemobject-methods-.md) de la clase o la instancia mediante el método [**SWbemObjectSet. Item**](swbemobjectset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d1906-141">Retrieve the method to execute from the [**SWbemObject.Methods\_**](swbemobject-methods-.md) collection of your class or instance by using the [**SWbemObjectSet.Item**](swbemobjectset-item.md) method.</span></span>
3.  <span data-ttu-id="d1906-142">Obtenga un objeto [**Parameters**](swbemmethod-inparameters.md) para el método y configure los parámetros tal y como se describe en [construir objetos Parameters](constructing-inparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-142">Obtain an [**InParameters**](swbemmethod-inparameters.md) object for the method and set up the parameters as described in [Constructing InParameters Objects](constructing-inparameters-objects.md).</span></span>
4.  <span data-ttu-id="d1906-143">Llame al método **SWbemServices.ExecMethod** para ejecutar y asignar el valor devuelto a un objeto [**SWbemObject**](swbemobject.md) para almacenar los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="d1906-143">Call the **SWbemServices.ExecMethod** method to execute and assign the return value to an [**SWbemObject**](swbemobject.md) object to store the output parameters.</span></span>
5.  <span data-ttu-id="d1906-144">Compruebe los valores del objeto Output Parameters para comprobar que el método se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d1906-144">Check the values in the output parameters object to verify that the method executed correctly.</span></span>

<span data-ttu-id="d1906-145">El siguiente ejemplo de código de VBScript realiza la misma operación que el script anterior mediante el enfoque indirecto mediante la llamada a [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-145">The following VBScript code example performs the same operation as the previous script by the indirect approach through calling [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")

Set objProcess = objWMIService.Get("Win32_Process")

' Obtain an InParameters object specific to 
'   the Win32_Process.Create method.
Set objInParam = _
    objProcess.Methods_("Create").inParameters.SpawnInstance_()

' Add the input parameters. 
objInParam.Properties_.item("CommandLine") = "Notepad"
objInParam.Properties_.item("CurrentDirectory") = NULL
objInParam.Properties_.item("ProcessStartupInformation") = NULL


Set objOutParams = objProcess.ExecMethod_("Create", objInParam) 
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & objOutParams.ProcessId 
Else
    Wscript.Echo "Notepad could not be started due to error " & _
       objOutParams.ReturnValue
End If
```




<span data-ttu-id="d1906-146">En el procedimiento siguiente se describe cómo llamar a un método de proveedor mediante C++.</span><span class="sxs-lookup"><span data-stu-id="d1906-146">The following procedure describes how to call a provider method using C++.</span></span>

<span data-ttu-id="d1906-147">**Para llamar a un método de proveedor mediante C++**</span><span class="sxs-lookup"><span data-stu-id="d1906-147">**To call a provider method using C++**</span></span>

1.  <span data-ttu-id="d1906-148">Conéctese a WMI.</span><span class="sxs-lookup"><span data-stu-id="d1906-148">Connect to WMI.</span></span>

    <span data-ttu-id="d1906-149">Para llamar a un método en WMI, primero debe tener una conexión de trabajo a un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="d1906-149">To call a method in WMI, first you must have a working connection to a WMI namespace.</span></span> <span data-ttu-id="d1906-150">Para obtener más información, vea [crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md) e [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-150">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md) and [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="d1906-151">En el ejemplo siguiente se muestra cómo conectarse a WMI.</span><span class="sxs-lookup"><span data-stu-id="d1906-151">The following example shows how to connect to WMI.</span></span> <span data-ttu-id="d1906-152">Para obtener más información acerca de los problemas de seguridad en las llamadas del proveedor WMI, vea [mantener la seguridad WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-152">For more information about security issues in WMI provider calls, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

```C++
    HRESULT hr = CoInitialize(0);
        hr  =  CoInitializeSecurity(
                NULL, 
                -1, 
                NULL, 
                NULL,
                RPC_C_AUTHN_LEVEL_DEFAULT, 
                RPC_C_IMP_LEVEL_IMPERSONATE, 
                NULL, 
                EOAC_NONE, 
                NULL); 
        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
                CLSCTX_INPROC_SERVER,
                IID_IWbemLocator, (LPVOID *) &pLocator);
        hr = pLocator->ConnectServer(path, NULL, NULL, 
                NULL, 0, NULL, NULL, &pNamespace);
```

    

2.  <span data-ttu-id="d1906-153">Llame a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar la definición de la clase del método al que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="d1906-153">Call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve the definition of the class of the method you want to call.</span></span>

    <span data-ttu-id="d1906-154">El método [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) devuelve un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunta a la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="d1906-154">The [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the class definition.</span></span>

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  <span data-ttu-id="d1906-155">Para los métodos que requieren parámetros de entrada, llame al método [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para obtener el objeto de la clase de parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1906-155">For methods that require input parameters, call the [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method to get the input parameter class object.</span></span>

    <span data-ttu-id="d1906-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) devuelve un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunta a la clase de parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1906-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the input parameter class.</span></span>

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  <span data-ttu-id="d1906-157">Genere una instancia de la clase de parámetro de entrada con una llamada al método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="d1906-157">Generate an instance of the input parameter class with a call to the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  <span data-ttu-id="d1906-158">Establezca las propiedades de la clase de parámetro de entrada con una llamada al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="d1906-158">Set the properties of the input parameter class with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  <span data-ttu-id="d1906-159">Invoque el método con una llamada a [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="d1906-159">Invoke the method with a call to [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span>

    <span data-ttu-id="d1906-160">En el caso de [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI devuelve los parámetros de salida de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d1906-160">For [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI returns any output parameters in the call.</span></span> <span data-ttu-id="d1906-161">En el caso de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI devuelve los parámetros de salida a través de una llamada a [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-161">For [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI returns any output parameters through a call to [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="d1906-162">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d1906-162">For more information, see [Calling a Method](calling-a-method.md).</span></span>

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

<span data-ttu-id="d1906-163">El código siguiente es un ejemplo completo para llamar a un método de proveedor.</span><span class="sxs-lookup"><span data-stu-id="d1906-163">The following code is a complete example for calling a provider method.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    IWbemLocator *pLocator = NULL;
    IWbemServices *pNamespace = 0;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutInst = NULL;
    IWbemClassObject * pInClass = NULL;
    IWbemClassObject * pInInst = NULL;
  
    BSTR path = SysAllocString(L"root\\default");
    BSTR ClassPath = SysAllocString(L"TestMeth");
    BSTR MethodName = SysAllocString(L"Echo");
    BSTR ArgName = SysAllocString(L"sInArg");
    BSTR Text;

    // Initialize COM and connect to WMI.

    HRESULT hr = CoInitialize(0);
    hr  =  CoInitializeSecurity(NULL, -1, NULL, NULL,RPC_C_AUTHN_LEVEL_DEFAULT, 
                                RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE, NULL); 
    hr = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,
                          IID_IWbemLocator, (LPVOID *) &pLocator);
    hr = pLocator->ConnectServer(path, NULL, NULL, NULL, 0, NULL, NULL, &pNamespace);

    // Get the class object for the method definition.

    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);

    // Get the input-argument class object and 
    // create an instance.

    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL); 
    hr = pInClass->SpawnInstance(0, &pInInst);

    // Set the property.

    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);

    // Call the method.

    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
    
    // Display the results. Note that the return 
    // value is in the property "ReturnValue"
    // and the returned string is in the 
    // property "sOutArg".

    hr = pOutInst->GetObjectText(0, &Text);
    printf("\nThe object text is:\n%S", Text);

    // Free up resources.

    SysFreeString(path);
    SysFreeString(ClassPath);
    SysFreeString(MethodName);
    SysFreeString(ArgName);
    SysFreeString(Text);
    pClass->Release();
    pInInst->Release();
    pInClass->Release();
    pOutInst->Release();
    pLocator->Release();
    pNamespace->Release();
    CoUninitialize();
    printf("Terminating normally\n");
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d1906-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1906-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1906-165">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="d1906-165">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
