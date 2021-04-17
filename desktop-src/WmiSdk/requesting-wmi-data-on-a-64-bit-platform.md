---
description: De forma predeterminada, una aplicación o un script recibe datos del proveedor correspondiente cuando existen dos versiones de proveedores.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Solicitar datos WMI en una plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696802"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="34faf-103">Solicitar datos WMI en una plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="34faf-103">Requesting WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="34faf-104">De forma predeterminada, una aplicación o un script recibe datos del proveedor correspondiente cuando existen dos versiones de proveedores.</span><span class="sxs-lookup"><span data-stu-id="34faf-104">By default, an application or script receives data from the corresponding provider when two versions of providers exist.</span></span> <span data-ttu-id="34faf-105">El proveedor de 32 bits devuelve datos a una aplicación de 32 bits, incluidos todos los scripts, y el proveedor de 64 bits devuelve datos a las aplicaciones compiladas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-105">The 32-bit provider returns data to a 32-bit application, including all scripts, and the 64-bit provider returns data to the 64-bit compiled applications.</span></span> <span data-ttu-id="34faf-106">Sin embargo, una aplicación o un script puede solicitar datos del proveedor no predeterminado, si existe, notificando a WMI a través de marcas en llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="34faf-106">However, an application or script can request data from the nondefault provider, if it exists, by notifying WMI through flags on method calls.</span></span>

## <a name="context-flags"></a><span data-ttu-id="34faf-107">Marcas de contexto</span><span class="sxs-lookup"><span data-stu-id="34faf-107">Context Flags</span></span>

<span data-ttu-id="34faf-108">Las marcas de cadena **\_ \_ ProviderArchitecture** y **\_ \_ RequiredArchitecture** tienen un conjunto de valores administrados por WMI pero no definidos en los archivos de encabezado de SDK o de biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="34faf-108">The **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** string flags have a set of values handled by WMI but not defined in SDK header or type library files.</span></span> <span data-ttu-id="34faf-109">Los valores se colocan en un parámetro de contexto para indicar a WMI que debe solicitar datos del proveedor no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="34faf-109">The values are placed in a context parameter to signal WMI that it should request data from the nondefault provider.</span></span>

<span data-ttu-id="34faf-110">A continuación se enumeran las marcas y sus valores posibles.</span><span class="sxs-lookup"><span data-stu-id="34faf-110">The following lists the flags and their possible values.</span></span>

<dl> <dt>

<span data-ttu-id="34faf-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span><span class="sxs-lookup"><span data-stu-id="34faf-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="34faf-112">Valor entero, ya sea 32 o 64, que especifica la versión de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-112">Integer value, either 32 or 64, that specifies the 32-bit or 64-bit version.</span></span>

</dd> <dt>

<span data-ttu-id="34faf-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span><span class="sxs-lookup"><span data-stu-id="34faf-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="34faf-114">Valor booleano que se usa además de **\_ \_ ProviderArchitecture** para forzar la carga de la versión de proveedor especificada.</span><span class="sxs-lookup"><span data-stu-id="34faf-114">Boolean value used in addition to **\_\_ProviderArchitecture** to force load the specified provider version.</span></span> <span data-ttu-id="34faf-115">Si la versión no está disponible, WMI devuelve el error 0x80041013, **wbemErrProviderLoadFailure** para Visual Basic y **\_ error de \_ \_ carga del \_ proveedor de WBEM** para C++.</span><span class="sxs-lookup"><span data-stu-id="34faf-115">If the version is unavailable, then WMI returns the error 0x80041013, **wbemErrProviderLoadFailure** for Visual Basic and **WBEM\_E\_PROVIDER\_LOAD\_FAILURE** for C++.</span></span> <span data-ttu-id="34faf-116">El valor predeterminado de esta marca cuando no se especifica es **false**.</span><span class="sxs-lookup"><span data-stu-id="34faf-116">The default value for this flag when it is not specified is **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="34faf-117">En un sistema de 64 bits que tiene versiones en paralelo de un proveedor, una aplicación o un script de 32 bits reciben automáticamente datos del proveedor de 32 bits, a menos que se proporcionen estos marcadores e indiquen que se deben devolver los datos del proveedor de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-117">On a 64-bit system that has side-by-side versions of a provider, a 32-bit application or script automatically receives data from the 32-bit provider, unless these flags are supplied and indicate that the 64-bit provider data should be returned.</span></span>

## <a name="using-the-context-flags"></a><span data-ttu-id="34faf-118">Usar marcas de contexto</span><span class="sxs-lookup"><span data-stu-id="34faf-118">Using the Context Flags</span></span>

<span data-ttu-id="34faf-119">Las aplicaciones de C++ pueden utilizar la interfaz [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) para comunicar el uso de un proveedor no predeterminado a WMI.</span><span class="sxs-lookup"><span data-stu-id="34faf-119">C++ applications can use the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface with [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to communicate the use of a nondefault provider to WMI.</span></span>

<span data-ttu-id="34faf-120">En scripting y Visual Basic, debe crear un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contenga las marcas del parámetro *ObjWbemNamedValueSet* de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="34faf-120">In scripting and Visual Basic, you must create a [**SWbemNamedValueSet**](swbemnamedvalueset.md) object containing the flags for the *objWbemNamedValueSet* parameter of [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="34faf-121">Para obtener más información sobre cómo configurar los objetos de parámetros para esta llamada, vea [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="34faf-121">For more information about setting up the parameters objects for this call, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="34faf-122">Puede ejecutar scripts y aplicaciones de forma segura con las marcas de contexto en sistemas operativos anteriores, porque WMI los omite en sistemas en los que no se implementan.</span><span class="sxs-lookup"><span data-stu-id="34faf-122">You can safely run scripts and applications using the context flags in older operating systems, because WMI ignores them in systems in which they are not implemented.</span></span> <span data-ttu-id="34faf-123">Mientras existan las versiones de 32 y 64 bits del proveedor del registro del sistema, tenga en cuenta que solo existe una versión del repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="34faf-123">While 32-bit and 64-bit versions of the System Registry provider exist, note that only one version of the WMI repository exists.</span></span>

## <a name="accessing-the-default-registry-hive"></a><span data-ttu-id="34faf-124">Acceso al subárbol del registro predeterminado</span><span class="sxs-lookup"><span data-stu-id="34faf-124">Accessing the Default Registry Hive</span></span>

<span data-ttu-id="34faf-125">En la siguiente serie de ejemplos se usa el [proveedor del registro](/previous-versions/windows/desktop/regprov/system-registry-provider), que tiene versiones en paralelo de 32 bits y de 64 bits preinstaladas en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-125">The following series of examples use the [Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which has side-by-side 32-bit and 64-bit versions preinstalled on 64-bit operating systems.</span></span> <span data-ttu-id="34faf-126">En estos ejemplos, los clientes de 32 bits obtienen los datos devueltos por el proveedor del nodo de 32 bits **HKEY \_ local \_ Machine \\ software \\ Wow6432Node \\ Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="34faf-126">In these examples, 32-bit clients get data returned by the provider from the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft**.</span></span> <span data-ttu-id="34faf-127">los clientes de 64 bits obtienen los datos devueltos por el proveedor del nodo de 64 bits **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Logging**.</span><span class="sxs-lookup"><span data-stu-id="34faf-127">64-bit clients get data returned by the provider from the 64-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Logging**.</span></span>

<span data-ttu-id="34faf-128">Los scripts muestran cómo llamar a los métodos de la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) del registro a través de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) para obtener datos del subárbol del registro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-128">The scripts show how to call the methods of the Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class through [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to obtain data from the 32-bit registry hive.</span></span>

<span data-ttu-id="34faf-129">El siguiente script obtiene datos del proveedor que coincide con el ancho de bits del autor de la llamada, en este caso 64 bits, porque es un script que se ejecuta en el host de script de Windows de 64 bits (WSH).</span><span class="sxs-lookup"><span data-stu-id="34faf-129">The following script gets back data from the provider that matches the bit width of the caller, in this case 64 bits, because it is a script running under the 64-bit Windows Script Host (WSH).</span></span> <span data-ttu-id="34faf-130">El script obtiene el valor del nodo del registro de 64 bits **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ cimom \\ Logging** , en lugar del nodo 32-bit **HKEY \_ local \_ Machine \\ software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="34faf-130">The script gets the value from the 64-bit registry node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM\\Logging** rather than the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\WBEM\\CIMOM**.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



<span data-ttu-id="34faf-131">Si el valor de **registro** del subárbol predeterminado está establecido en 1, la salida del script debe ser similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="34faf-131">If the **Logging** value in the default hive is set to 1, then the output from the script should look something like the following:</span></span>

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="34faf-132">Ejemplo: solicitar específicamente el subárbol del registro de 32 bits en un equipo de 64 bits</span><span class="sxs-lookup"><span data-stu-id="34faf-132">Example: Specifically Requesting the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="34faf-133">El siguiente ejemplo modificado del script predeterminado utiliza la marca de cadena **\_ \_ ProviderArchitecture** para solicitar acceso a los datos del registro de 32 bits en un equipo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-133">The following modified example of the default script uses the **\_\_ProviderArchitecture** string flag to request access to the 32-bit registry data on a 64-bit computer.</span></span> <span data-ttu-id="34faf-134">El autor de la llamada se conecta al subárbol de 32 bits con independencia de si se trata de una aplicación de 32 o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-134">The caller is connected to the 32-bit hive irrespective of whether it is a 32- or 64-bit application.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="34faf-135">Ejemplo: forzar a WMI a tener acceso al subárbol del registro de 32 bits en un equipo de 64 bits</span><span class="sxs-lookup"><span data-stu-id="34faf-135">Example: Forcing WMI to Access the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="34faf-136">La siguiente modificación del script anterior mediante la adición de las marcas **\_ \_ ProviderArchitecture** y **\_ \_ RequiredArchitecture** al parámetro de contexto obliga a WMI a cargar el proveedor de 32 bits y obtener los datos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="34faf-136">The following modification of the script above by adding the **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** flags to the context parameter forces WMI to load the 32-bit provider and get 32-bit data.</span></span> <span data-ttu-id="34faf-137">Si el proveedor no existe, se produce un error de carga del proveedor.</span><span class="sxs-lookup"><span data-stu-id="34faf-137">If the provider does not exist, then a provider load error occurs.</span></span> <span data-ttu-id="34faf-138">El objeto de contexto se debe proporcionar en la conexión a WMI llamando a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="34faf-138">The context object must be supplied in the connection to WMI by calling [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a><span data-ttu-id="34faf-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34faf-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34faf-140">Obtener y proporcionar datos en un equipo de 64 bits</span><span class="sxs-lookup"><span data-stu-id="34faf-140">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
