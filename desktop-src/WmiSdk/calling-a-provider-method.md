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
# <a name="calling-a-provider-method"></a>Llamar a un método de proveedor

Un método de proveedor es un método implementado por un proveedor de Instrumental de administración de Windows (WMI). El método se encuentra en una clase definida por un proveedor para representar datos de software o hardware. Por ejemplo, la clase de [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) tiene métodos para iniciar, detener, reanudar, pausar y cambiar servicios.

Los métodos de proveedor no se deben confundir con los siguientes tipos de métodos:

-   Métodos en [las clases del sistema de WMI](wmi-system-classes.md), [**como el método**](--systemsecurity-getsd.md) de [**\_ \_ SystemSecurity**](--systemsecurity.md).
-   Métodos en objetos de la [API de scripting para WMI](scripting-api-for-wmi.md), como [**SWbemServices. instances**](swbemservices-instancesof.md).
-   Métodos de la [API de com para WMI](com-api-for-wmi.md), como [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

## <a name="calling-a-provider-method-using-scripting"></a>Llamar a un método de proveedor mediante scripting

Cualquier lenguaje de automatización, como VBScript, PowerShell o Perl, puede llamar a un método WMI. Algunos lenguajes pueden usar el [acceso directo](/windows), pero otros deben usar [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) para ejecutar el método de proveedor indirectamente.

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

En el procedimiento siguiente se describe cómo llamar a un método de proveedor mediante la API de scripting y el uso de acceso directo.

**Para llamar a un método de proveedor mediante la API de scripting y el acceso directo**

1.  Use este enfoque para VBScript o PowerShell.
2.  Determine si el método que desea ejecutar está implementado.

    Algunas clases tienen métodos definidos que no son compatibles con un proveedor. Si un método no está implementado, no se puede ejecutar. Puede determinar si un método se implementa comprobando si el método tiene el calificador [**implementado**](standard-wmi-qualifiers.md) . Para obtener más información, vea [calificadores de WMI](wmi-qualifiers.md) y [obtener acceso a un calificador de WMI](accessing-a-qualifier.md). También puede determinar si un método de clase de proveedor tiene establecido el calificador **implementado** mediante la ejecución de la utilidad de Wbemtest.exe no compatible, disponible en cualquier sistema operativo con WMI instalado.

3.  Determine si el método que desea ejecutar es un [*método estático*](gloss-s.md) o un método no estático.

    Los métodos estáticos solo se aplican a las clases WMI y no a instancias específicas de una clase. Por ejemplo, el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) es un método estático porque se usa para crear un nuevo proceso sin una instancia de esta clase. Los métodos no estáticos solo se aplican a las instancias de una clase. Por ejemplo, el método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) de la clase de **\_ proceso de Win32** es un método no estático, ya que solo tiene sentido finalizar un proceso si existe una instancia de ese proceso. Puede determinar si un método es estático comprobando si el calificador [**estático**](standard-wmi-qualifiers.md) está asociado al método.

4.  Recupere la clase o instancia que contiene el método que desea ejecutar.

    Para obtener más información, consulte [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).

5.  Configure las opciones de seguridad que pueda necesitar el método.

    A menudo, puede determinar los privilegios que requiere un método examinando los valores del calificador [**privileges**](swbemsecurity-privileges.md) del método. Por ejemplo, el método [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) de clase de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requiere la configuración del privilegio "SeShutdownPrivilege". Para obtener más información, vea [ejecutar operaciones con privilegios](executing-privileged-operations.md).

6.  Llame al método y examine el valor devuelto para determinar si el método se ejecutó correctamente.

En el ejemplo de código siguiente se crea un proceso de Bloc de notas y se obtiene el identificador de proceso mediante el acceso directo.


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

En el procedimiento siguiente se describe cómo llamar a un método de proveedor mediante la API de scripting y el [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

**Para llamar a un método de proveedor mediante la API de scripting y SWbemServices.ExecMethod**

1.  Recupere la definición de clase WMI para ejecutar un método estático. Recupere la instancia de clase WMI para ejecutar un método no estático.
2.  Recupere el método que se va a ejecutar desde la colección [**SWbemObject. Methods \_**](swbemobject-methods-.md) de la clase o la instancia mediante el método [**SWbemObjectSet. Item**](swbemobjectset-item.md) .
3.  Obtenga un objeto [**Parameters**](swbemmethod-inparameters.md) para el método y configure los parámetros tal y como se describe en [construir objetos Parameters](constructing-inparameters-objects.md).
4.  Llame al método **SWbemServices.ExecMethod** para ejecutar y asignar el valor devuelto a un objeto [**SWbemObject**](swbemobject.md) para almacenar los parámetros de salida.
5.  Compruebe los valores del objeto Output Parameters para comprobar que el método se ejecutó correctamente.

El siguiente ejemplo de código de VBScript realiza la misma operación que el script anterior mediante el enfoque indirecto mediante la llamada a [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).


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




En el procedimiento siguiente se describe cómo llamar a un método de proveedor mediante C++.

**Para llamar a un método de proveedor mediante C++**

1.  Conéctese a WMI.

    Para llamar a un método en WMI, primero debe tener una conexión de trabajo a un espacio de nombres WMI. Para obtener más información, vea [crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md) e [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).

    En el ejemplo siguiente se muestra cómo conectarse a WMI. Para obtener más información acerca de los problemas de seguridad en las llamadas del proveedor WMI, vea [mantener la seguridad WMI](maintaining-wmi-security.md).

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

    

2.  Llame a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar la definición de la clase del método al que desea llamar.

    El método [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) devuelve un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunta a la definición de clase.

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  Para los métodos que requieren parámetros de entrada, llame al método [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para obtener el objeto de la clase de parámetro de entrada.

    [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) devuelve un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunta a la clase de parámetro de entrada.

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  Genere una instancia de la clase de parámetro de entrada con una llamada al método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  Establezca las propiedades de la clase de parámetro de entrada con una llamada al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  Invoque el método con una llamada a [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).

    En el caso de [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI devuelve los parámetros de salida de la llamada. En el caso de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI devuelve los parámetros de salida a través de una llamada a [**IWbemObjectSink**](iwbemobjectsink.md). Para obtener más información, consulte [llamar a un método](calling-a-method.md).

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

El código siguiente es un ejemplo completo para llamar a un método de proveedor.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
