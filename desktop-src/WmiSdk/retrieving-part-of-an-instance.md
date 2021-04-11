---
description: Una recuperación de instancia parcial es cuando WMI recupera solo un subconjunto de las propiedades de una instancia.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Recuperar parte de una instancia de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d547ec2bbb7e3b53e22177cc0c48794dff22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276143"
---
# <a name="retrieving-part-of-a-wmi-instance"></a><span data-ttu-id="261f0-103">Recuperar parte de una instancia de WMI</span><span class="sxs-lookup"><span data-stu-id="261f0-103">Retrieving Part of a WMI Instance</span></span>

<span data-ttu-id="261f0-104">Una recuperación de instancia parcial es cuando WMI recupera solo un subconjunto de las propiedades de una instancia.</span><span class="sxs-lookup"><span data-stu-id="261f0-104">A partial-instance retrieval is when WMI retrieves only a subset of the properties of an instance.</span></span> <span data-ttu-id="261f0-105">Por ejemplo, WMI podría recuperar solo las propiedades de **nombre** y **clave** .</span><span class="sxs-lookup"><span data-stu-id="261f0-105">For example, WMI could retrieve only the **Name** and **Key** properties.</span></span> <span data-ttu-id="261f0-106">El uso más común de la recuperación de instancia parcial es en enumeraciones grandes que tienen varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="261f0-106">The most common use of partial-instance retrieval is on large enumerations that have multiple properties.</span></span>

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a><span data-ttu-id="261f0-107">Recuperar parte de una instancia de WMI mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="261f0-107">Retrieving Part of a WMI Instance Using PowerShell</span></span>

<span data-ttu-id="261f0-108">Puede recuperar una propiedad individual de una instancia mediante [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx); la propiedad se puede recuperar y mostrar de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="261f0-108">You can retrieve an individual property of an instance by using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); the property itself can be retrieved and displayed a number of ways.</span></span> <span data-ttu-id="261f0-109">Al igual que con la recuperación de una instancia de, PowerShell devolverá de forma predeterminada todas las instancias de una clase determinada. debe especificar un valor específico si desea recuperar una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="261f0-109">As with retrieving an instance, PowerShell will by default return all instances of a given class; you must specify a specific value if you wish to retrieve only a single instance.</span></span>

<span data-ttu-id="261f0-110">En el ejemplo de código siguiente se muestra el número de serie del volumen de una instancia de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="261f0-110">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a><span data-ttu-id="261f0-111">Recuperar parte de una instancia de WMI mediante C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="261f0-111">Retrieving Part of a WMI Instance Using C# (System.Management)</span></span>

<span data-ttu-id="261f0-112">Puede recuperar una propiedad individual de una instancia creando una nueva [ManagementObject](/dotnet/api/system.management.managementobject) con los detalles de una instancia específica.</span><span class="sxs-lookup"><span data-stu-id="261f0-112">You can retrieve an individual property of an instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject) using the details of a specific instance.</span></span> <span data-ttu-id="261f0-113">Después, puede recuperar implícitamente una o más propiedades de la instancia con el método [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) .</span><span class="sxs-lookup"><span data-stu-id="261f0-113">You can then implicitly retrieve one or more properties of the instance with the [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) method.</span></span>

> [!Note]  
> <span data-ttu-id="261f0-114">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="261f0-114">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="261f0-115">En el ejemplo de código siguiente se muestra el número de serie del volumen de una instancia de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="261f0-115">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a><span data-ttu-id="261f0-116">Recuperar parte de una instancia de WMI mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="261f0-116">Retrieving Part of a WMI Instance Using VBScript</span></span>

<span data-ttu-id="261f0-117">Puede recuperar una propiedad individual de una instancia mediante [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="261f0-117">You can retrieve an individual property of an instance by using [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="261f0-118">En el ejemplo de código siguiente se muestra el número de serie del volumen de una instancia de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="261f0-118">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a><span data-ttu-id="261f0-119">Recuperar parte de una instancia de WMI mediante C++</span><span class="sxs-lookup"><span data-stu-id="261f0-119">Retrieving Part of a WMI Instance Using C++</span></span>

<span data-ttu-id="261f0-120">El procedimiento siguiente se utiliza para solicitar una recuperación de instancia parcial mediante C++.</span><span class="sxs-lookup"><span data-stu-id="261f0-120">The following procedure is used to request a partial-instance retrieval using C++.</span></span>

<span data-ttu-id="261f0-121">**Para solicitar una recuperación de instancia parcial mediante C++**</span><span class="sxs-lookup"><span data-stu-id="261f0-121">**To request a partial-instance retrieval using C++**</span></span>

1.  <span data-ttu-id="261f0-122">Cree un objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="261f0-122">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="261f0-123">Un objeto de contexto es un objeto que WMI utiliza para pasar más información a un proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="261f0-123">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="261f0-124">En este caso, se usa el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para indicar al proveedor que procese una recuperación de instancia parcial.</span><span class="sxs-lookup"><span data-stu-id="261f0-124">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to process a partial-instance retrieval.</span></span>

2.  <span data-ttu-id="261f0-125">Agregue \_ \_ Get \_ extensions, \_ \_ Get \_ ext \_ Client \_ request y otros valores con nombre que describan las propiedades que desea recuperar al objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="261f0-125">Add \_\_GET\_EXTENSIONS, \_\_GET\_EXT\_CLIENT\_REQUEST, and any other named values that describe the properties you want to retrieve to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object.</span></span>

    <span data-ttu-id="261f0-126">En la tabla siguiente se enumeran los distintos valores con nombre que se usan en la llamada de recuperación.</span><span class="sxs-lookup"><span data-stu-id="261f0-126">The following table lists the different named values use in your retrieval call.</span></span>

    

    | <span data-ttu-id="261f0-127">Valor con nombre</span><span class="sxs-lookup"><span data-stu-id="261f0-127">Named value</span></span>                              | <span data-ttu-id="261f0-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="261f0-128">Description</span></span>                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="261f0-129">\_\_OBTENER \_ extensiones</span><span class="sxs-lookup"><span data-stu-id="261f0-129">\_\_GET\_EXTENSIONS</span></span><br/>           | <span data-ttu-id="261f0-130">**VT \_ BOOL** se establece en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="261f0-130">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="261f0-131">Se utiliza para indicar que se están utilizando operaciones de recuperación de instancia parcial.</span><span class="sxs-lookup"><span data-stu-id="261f0-131">Used to signal that partial-instance retrieval operations are being used.</span></span> <span data-ttu-id="261f0-132">Esto permite una comprobación rápida y sencilla sin tener que enumerar todo el objeto de contexto.</span><span class="sxs-lookup"><span data-stu-id="261f0-132">This allows a quick, single check without having to enumerate the entire context object.</span></span> <span data-ttu-id="261f0-133">Si se usa cualquiera de los otros valores, este debe ser.</span><span class="sxs-lookup"><span data-stu-id="261f0-133">If any of the other values are used, this one must be.</span></span><br/> |
    | <span data-ttu-id="261f0-134">\_\_OBTENER \_ \_ propiedades ext</span><span class="sxs-lookup"><span data-stu-id="261f0-134">\_\_GET\_EXT\_PROPERTIES</span></span><br/>      | <span data-ttu-id="261f0-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadenas que enumera las propiedades que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="261f0-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings listing the properties to be retrieved.</span></span> <span data-ttu-id="261f0-136">No se puede especificar simultáneamente \_ \_ \_ solo con \_ las claves Get ext \_ .</span><span class="sxs-lookup"><span data-stu-id="261f0-136">Cannot be simultaneously specified with \_\_GET\_EXT\_KEYS\_ONLY.</span></span><br/> <span data-ttu-id="261f0-137">Un asterisco " \* " es un nombre de propiedad no válido para \_ \_ obtener \_ \_ propiedades ext.</span><span class="sxs-lookup"><span data-stu-id="261f0-137">An asterisk "\*" is an invalid property name for \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                    |
    | <span data-ttu-id="261f0-138">\_\_OBTENER \_ \_ solo claves \_ ext</span><span class="sxs-lookup"><span data-stu-id="261f0-138">\_\_GET\_EXT\_KEYS\_ONLY</span></span><br/>      | <span data-ttu-id="261f0-139">**VT \_ BOOL** se establece en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="261f0-139">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="261f0-140">Indica que solo se deben proporcionar claves en el objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="261f0-140">Indicates that only keys should be provided in the returned object.</span></span> <span data-ttu-id="261f0-141">No se puede especificar simultáneamente con \_ \_ \_ \_ las propiedades Get ext.</span><span class="sxs-lookup"><span data-stu-id="261f0-141">Cannot be simultaneously specified with \_\_GET\_EXT\_PROPERTIES.</span></span> <span data-ttu-id="261f0-142">En su lugar, tiene prioridad sobre \_ \_ \_ \_ las propiedades Get ext.</span><span class="sxs-lookup"><span data-stu-id="261f0-142">Instead, takes precedence over \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                            |
    | <span data-ttu-id="261f0-143">\_\_OBTENER \_ \_ solicitud de cliente ext \_</span><span class="sxs-lookup"><span data-stu-id="261f0-143">\_\_GET\_EXT\_CLIENT\_REQUEST</span></span><br/> | <span data-ttu-id="261f0-144">**VT \_ BOOL** se establece en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="261f0-144">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="261f0-145">Indica que el llamador era el que escribió el valor en el objeto de contexto y que no se propagó desde otra operación dependiente.</span><span class="sxs-lookup"><span data-stu-id="261f0-145">Indicates that the caller was the one who wrote the value into the context object and that it was not propagated from another dependent operation.</span></span><br/>                                                                        |

    

     

3.  <span data-ttu-id="261f0-146">Pase el objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) en cualquier llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) a través del parámetro *pCtx* .</span><span class="sxs-lookup"><span data-stu-id="261f0-146">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) through the *pCtx* parameter.</span></span>

    <span data-ttu-id="261f0-147">Al pasar el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) se indica al proveedor que permita recuperaciones de instancias parciales.</span><span class="sxs-lookup"><span data-stu-id="261f0-147">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance retrievals.</span></span> <span data-ttu-id="261f0-148">En una recuperación de instancia completa, debe establecer *pCtx* en un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="261f0-148">In a full-instance retrieval, you would set *pCtx* to a **null** value.</span></span> <span data-ttu-id="261f0-149">Si el proveedor no admite la recuperación parcial de instancias, recibirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="261f0-149">If the provider does not support partial-instance retrieval, you will receive an error message.</span></span>

<span data-ttu-id="261f0-150">Si el proveedor no puede cumplir con la operación de instancia parcial, el proveedor continúa como si no hubiera especificado el objeto de contexto, o bien devuelve un **\_ \_ \_ parámetro no compatible de WBEM E**.</span><span class="sxs-lookup"><span data-stu-id="261f0-150">If the provider cannot comply with the partial-instance operation, the provider either proceeds as if you did not enter the context object, or else returns **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="261f0-151">En el ejemplo siguiente se describe cómo realizar una recuperación de instancia completa de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)y, a continuación, se realiza una recuperación de instancia parcial de la propiedad **\_ LogicalDisk. Caption de Win32** .</span><span class="sxs-lookup"><span data-stu-id="261f0-151">The following example describes how to perform a full instance retrieval of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), and then performs a partial-instance retrieval of the **Win32\_LogicalDisk.Caption** property.</span></span>


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



<span data-ttu-id="261f0-152">Cuando se ejecuta, el ejemplo de código anterior escribe la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="261f0-152">When executed, the previous code example writes the following information.</span></span> <span data-ttu-id="261f0-153">La descripción del primer objeto es de la recuperación de instancia completa.</span><span class="sxs-lookup"><span data-stu-id="261f0-153">The first object description is from the full-instance retrieval.</span></span> <span data-ttu-id="261f0-154">La descripción del segundo objeto procede de la recuperación parcial de la instancia.</span><span class="sxs-lookup"><span data-stu-id="261f0-154">The second object description is from the partial-instance retrieval.</span></span> <span data-ttu-id="261f0-155">En la última sección se muestra que recibe un valor **null** si solicita una propiedad que no se solicitó en la llamada [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) original.</span><span class="sxs-lookup"><span data-stu-id="261f0-155">The last section shows that you receive a **null** value if you request a property that was not requested in the original [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) call.</span></span>

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

<span data-ttu-id="261f0-156">El ejemplo anterior genera el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="261f0-156">The following output is generated by the previous example.</span></span>

``` syntax
file system variable is null - expected
Press any key to continue
```

 

