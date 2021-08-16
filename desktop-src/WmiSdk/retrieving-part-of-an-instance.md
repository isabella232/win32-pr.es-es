---
description: Una recuperación de instancia parcial es cuando WMI recupera solo un subconjunto de las propiedades de una instancia.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Recuperar parte de una instancia de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cce9d809e5203b7c00f2b2297403f835d98f37ff86641e297673ee50e579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316219"
---
# <a name="retrieving-part-of-a-wmi-instance"></a>Recuperar parte de una instancia de WMI

Una recuperación de instancia parcial es cuando WMI recupera solo un subconjunto de las propiedades de una instancia. Por ejemplo, WMI solo podría recuperar las **propiedades Nombre** **y** Clave. El uso más común de la recuperación de instancias parciales es en enumeraciones grandes que tienen varias propiedades.

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a>Recuperar parte de una instancia de WMI mediante PowerShell

Puede recuperar una propiedad individual de una instancia mediante [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); la propia propiedad se puede recuperar y mostrar de varias maneras. Al igual que con la recuperación de una instancia, PowerShell devolverá de forma predeterminada todas las instancias de una clase determinada. Debe especificar un valor específico si desea recuperar solo una instancia de .

En el ejemplo de código siguiente se muestra el número de serie del volumen de una instancia de la [**clase \_ LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a>Recuperar parte de una instancia de WMI mediante C# (System.Management)

Puede recuperar una propiedad individual de una instancia mediante la creación de un [objeto ManagementObject](/dotnet/api/system.management.managementobject) con los detalles de una instancia específica. A continuación, puede recuperar implícitamente una o varias propiedades de la instancia con el [método GetPropertyValue.](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_)

> [!Note]  
> **System.Management era el** espacio de nombres .NET original que se usaba para acceder a WMI; sin embargo, las API de este espacio de nombres suelen ser más lentas y no escalan tan bien con respecto a sus homólogos **de Microsoft.Management.Infrastructure** más modernos.

 

En el ejemplo de código siguiente se muestra el número de serie del volumen de una instancia de la [**clase \_ LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a>Recuperar parte de una instancia wmi mediante VBScript

Puede recuperar una propiedad individual de una instancia mediante [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

En el ejemplo de código siguiente se muestra el número de serie del volumen de una instancia de la [**clase \_ LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a>Recuperar parte de una instancia de WMI mediante C++

El procedimiento siguiente se usa para solicitar una recuperación de instancia parcial mediante C++.

**Para solicitar una recuperación de instancia parcial mediante C++**

1.  Cree un [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Un objeto de contexto es un objeto que WMI usa para pasar más información a un proveedor WMI. En este caso, está usando el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para indicar al proveedor que procese una recuperación de instancia parcial.

2.  Agregue GET EXTENSIONS, GET EXT CLIENT REQUEST y cualquier otro valor con nombre que describa las propiedades que desea recuperar en \_ \_ \_ el objeto \_ \_ \_ \_ \_ [**IWbemContext.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)

    En la tabla siguiente se enumeran los distintos valores con nombre que se usan en la llamada de recuperación.

    

    | Valor con nombre                              | Descripción                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_\_GET \_ EXTENSIONS<br/>           | **VT \_ BOOL establecido** en **VARIANT \_ TRUE.** Se usa para indicar que se están utilizando operaciones de recuperación de instancias parciales. Esto permite una comprobación rápida y única sin tener que enumerar todo el objeto de contexto. Si se usa cualquiera de los demás valores, este debe ser .<br/> |
    | \_\_GET \_ EXT \_ PROPERTIES<br/>      | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadenas que enumeran las propiedades que se recuperarán. No se puede especificar simultáneamente con \_ \_ GET EXT KEYS \_ \_ \_ ONLY.<br/> Un asterisco " \* " es un nombre de propiedad no válido para GET EXT \_ \_ \_ \_ PROPERTIES.<br/>                    |
    | \_\_OBTENER \_ SOLO \_ CLAVES \_ EXT<br/>      | **VT \_ BOOL establecido** en **VARIANT \_ TRUE.** Indica que solo se deben proporcionar claves en el objeto devuelto. No se puede especificar simultáneamente con \_ \_ GET EXT \_ \_ PROPERTIES. En su lugar, tiene prioridad sobre \_ \_ GET EXT \_ \_ PROPERTIES.<br/>                            |
    | \_\_GET \_ EXT \_ CLIENT \_ REQUEST<br/> | **VT \_ BOOL establecido** en **VARIANT \_ TRUE.** Indica que el autor de la llamada fue quien escribió el valor en el objeto de contexto y que no se propague desde otra operación dependiente.<br/>                                                                        |

    

     

3.  Pase el objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) a cualquier llamada a [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) [**IWbemServices::CreateInstanceEnum o**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) mediante el *parámetro pCtx.*

    Pasar el [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) indica al proveedor que permita recuperaciones de instancias parciales. En una recuperación de instancia completa, establecería *pCtx* en un **valor** NULL. Si el proveedor no admite la recuperación de instancias parciales, recibirá un mensaje de error.

Si el proveedor no puede cumplir con la operación de instancia parcial, el proveedor continúa como si no hubiera especificado el objeto de contexto o devuelve **WBEM \_ E \_ UNSUPPORTED \_ PARAMETER**.

En el ejemplo siguiente se describe cómo realizar una recuperación de instancia completa de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)y, a continuación, realiza una recuperación de instancia parcial de la propiedad **\_ LogicalDisk.Caption de Win32.**


```C++
#include <stdio.h>
#define _WIN32_DCOM
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#include <iostream>
using namespace std;
#include <comdef.h>


void main(void)
{
    HRESULT hr;
    _bstr_t bstrNamespace;
    IWbemLocator *pWbemLocator = NULL;
    IWbemServices *pServices = NULL;
    IWbemClassObject *pDrive = NULL;
    

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                         RPC_C_AUTHN_LEVEL_CONNECT,
                         RPC_C_IMP_LEVEL_IMPERSONATE,
                         NULL, EOAC_NONE, 0);
 
    if (FAILED(hr))
    {
       CoUninitialize();
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       return;
    }

    hr = CoCreateInstance(CLSID_WbemLocator, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemLocator, 
                          (void**) &pWbemLocator);
    if( FAILED(hr) ) 
    {
        CoUninitialize();
        printf("failed CoCreateInstance\n");
        return;
    }
    
    bstrNamespace = L"root\\cimv2";
    hr = pWbemLocator->ConnectServer(bstrNamespace, 
              NULL, NULL, NULL, 0, NULL, NULL, &pServices);
    if( FAILED(hr) ) 
    {
        pWbemLocator->Release();
        CoUninitialize();
        printf("failed ConnectServer\n");
        return;
    }
    pWbemLocator->Release();
    printf("Successfully connected to namespace.\n");

    
    BSTR bstrPath = 
         SysAllocString(L"Win32_LogicalDisk.DeviceID=\"C:\"");
   // *******************************************************//
   // Perform a full-instance retrieval. 
   // *******************************************************//
    hr = pServices->GetObject(bstrPath,
                              0,0, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed GetObject\n");
        return;
    }    
    // Display the object
    BSTR  bstrDriveObj;
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    pDrive->Release();
    pDrive = NULL;

   // *****************************************************//
   // Perform a partial-instance retrieval. 
   // *****************************************************//
    
    IWbemContext  *pctxDrive; // Create context object
    hr = CoCreateInstance(CLSID_WbemContext, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemContext, 
                          (void**) &pctxDrive);
    if (FAILED(hr))
    {
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("create instance failed for context object.\n");
        return;
    }
    
    VARIANT  vExtensions;
    VARIANT  vClient;
    VARIANT  vPropertyList;
    VARIANT  vProperty;
    SAFEARRAY  *psaProperties;
    SAFEARRAYBOUND saBounds;
    LONG  lArrayIndex = 0;
    
    // Add named values to the context object. 
    VariantInit(&vExtensions);
    V_VT(&vExtensions) = VT_BOOL;
    V_BOOL(&vExtensions) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXTENSIONS"), 
        0, &vExtensions);
    VariantClear(&vExtensions);

    VariantInit(&vClient);
    V_VT(&vClient) = VT_BOOL;
    V_BOOL(&vClient) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_CLIENT_REQUEST"), 
       0, &vClient);
    VariantClear(&vClient);
    // Create an array of properties to return.
    saBounds.cElements = 1;
    saBounds.lLbound = 0;
    psaProperties = SafeArrayCreate(VT_BSTR, 1, &saBounds);

    // Add the Caption property to the array.
    VariantInit(&vProperty);
    V_VT(&vProperty) = VT_BSTR;
    V_BSTR(&vProperty) = _bstr_t(L"Caption");
    SafeArrayPutElement(psaProperties, &lArrayIndex, 
       V_BSTR(&vProperty));
    VariantClear(&vProperty);
    
    VariantInit(&vPropertyList);
    V_VT(&vPropertyList) = VT_ARRAY | VT_BSTR;
    V_ARRAY(&vPropertyList) = psaProperties;
    // Put the array in the named value __GET_EXT_PROPERTIES.
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_PROPERTIES"), 
        0, &vPropertyList);
    VariantClear(&vPropertyList);
    SafeArrayDestroy(psaProperties);

    // Pass the context object as the pCtx parameter of GetObject.
    hr = pServices->GetObject(bstrPath, 0, pctxDrive, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed property GetObject\n");
        return;
    }    
    // Display the object
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    SysFreeString(bstrPath);

    VARIANT vFileSystem;
    // Attempt to get a property that was not requested.
    // The following should return a NULL property if
    // the partial-instance retrieval succeeded.

    hr = pDrive->Get(_bstr_t(L"FileSystem"), 0,
                       &vFileSystem, NULL, NULL);

    if( FAILED(hr) )
    { 
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("failed get for file system\n");
        return;
    }    
 
    if (V_VT(&vFileSystem) == VT_NULL)
        printf("file system variable is null - expected\n");
    else
        printf("FileSystem = %S\n", V_BSTR(&vFileSystem));
    
    VariantClear(&vFileSystem);

    pDrive->Release();    
    pctxDrive->Release();
    pServices->Release();
    pServices = NULL;    // MUST be set to NULL
    CoUninitialize();
    return;  // -- program successfully completed
};
```



Cuando se ejecuta, el ejemplo de código anterior escribe la siguiente información. La primera descripción del objeto es de la recuperación de instancia completa. La segunda descripción del objeto es de la recuperación de instancia parcial. En la última sección se muestra que recibe un **valor NULL** si solicita una propiedad que no se solicitó en la [**llamada GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) original.

``` syntax
Successfully connected to namespace

instance of Win32_LogicalDisk
{
        Caption = "C:";
        Compressed = FALSE;
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        FileSystem = "NTFS";
        FreeSpace = "3085668352";
        MaximumComponentLength = 255;
        MediaType = 12;
        Name = "C:";
        Size = "4581445632";
        SupportsFileBasedCompression = TRUE;
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "TITUS";
        VolumeName = "titus-c";
        VolumeSerialNumber = "7CB4B90E";
};

instance of Win32_LogicalDisk
{
        Caption = "C:";
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        MediaType = 12;
        Name = "C:";
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "MySystem";
};
```

El ejemplo anterior genera la salida siguiente.

``` syntax
file system variable is null - expected
Press any key to continue
```

 

