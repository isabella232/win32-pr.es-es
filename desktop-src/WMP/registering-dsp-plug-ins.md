---
title: Registro de complementos de DSP
description: Registro de complementos de DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Complementos de Windows Media Player, entradas del registro
- complementos, entradas del registro
- Complementos de procesamiento de señal digital, entradas del registro
- Complementos DSP, entradas del registro
- registro, Complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994953"
---
# <a name="registering-dsp-plug-ins"></a><span data-ttu-id="01eeb-108">Registro de complementos de DSP</span><span class="sxs-lookup"><span data-stu-id="01eeb-108">Registering DSP Plug-ins</span></span>

<span data-ttu-id="01eeb-109">Para que el complemento de DSP esté disponible en Windows Media Player debe crear las siguientes subclaves y entradas del registro en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="01eeb-109">To make your DSP plug-in available in Windows Media Player you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



<span data-ttu-id="01eeb-110">En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos del complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="01eeb-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="01eeb-111">En la tabla siguiente se describen esos marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="01eeb-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="01eeb-112">Marcador de posición</span><span class="sxs-lookup"><span data-stu-id="01eeb-112">Placeholder</span></span>               | <span data-ttu-id="01eeb-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="01eeb-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01eeb-114">*PluginClsid*</span><span class="sxs-lookup"><span data-stu-id="01eeb-114">*PluginClsid*</span></span>             | <span data-ttu-id="01eeb-115">GUID que es el identificador de clase de la clase principal del complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="01eeb-115">A GUID that is the class identifier for the DSP plug-in's primary class.</span></span> <span data-ttu-id="01eeb-116">Esta es la clase que implementa **IMediaObject**, **IPluginEnable** y posiblemente **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="01eeb-116">This is the class that implements **IMediaObject**, **IPluginEnable**, and possibly **ISpecifyPropertyPages**.</span></span> <span data-ttu-id="01eeb-117">En un complemento de modo dual, esta clase también implementa **IMFTransform** y **IMFGetService**. Este GUID debe estar en formato de registro, completar con las llaves.</span><span class="sxs-lookup"><span data-stu-id="01eeb-117">In a dual-mode plug-in, this class also implements **IMFTransform** and **IMFGetService**.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="01eeb-118">Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="01eeb-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="01eeb-119">*PluginClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="01eeb-119">*PluginClassFriendlyName*</span></span> | <span data-ttu-id="01eeb-120">Un nombre descriptivo para la clase principal del complemento DSP. Ejemplo: "clase ProsewareDSP"</span><span class="sxs-lookup"><span data-stu-id="01eeb-120">A friendly name for the DSP plug-in's primary class.Example: "ProsewareDSP Class"</span></span><br/>                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="01eeb-121">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="01eeb-121">*PluginModuleName*</span></span>        | <span data-ttu-id="01eeb-122">Ruta de acceso completa al archivo DLL que implementa el complemento DSP. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="01eeb-122">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="01eeb-123">*Subprocesamiento*</span><span class="sxs-lookup"><span data-stu-id="01eeb-123">*Threading*</span></span>               | <span data-ttu-id="01eeb-124">Cadena que especifica el modelo de subprocesos para el complemento.</span><span class="sxs-lookup"><span data-stu-id="01eeb-124">A string that specifies the threading model for the plug-in.</span></span> <span data-ttu-id="01eeb-125">Si el complemento va a ejecutarse con Windows Media Player 11 en Windows Vista, esta entrada del registro debe ser igual a "both".</span><span class="sxs-lookup"><span data-stu-id="01eeb-125">If the plug-in is going to run with Windows Media Player 11 on Windows Vista, this registry entry must be equal to "Both".</span></span> <span data-ttu-id="01eeb-126">Si el complemento se va a ejecutar en Windows XP o en sistemas operativos anteriores, esta entrada del registro puede ser "Apartment" o "both".</span><span class="sxs-lookup"><span data-stu-id="01eeb-126">If the plug-in is going to run on Windows XP or older operating systems, this registry entry can be equal to either "Apartment" or "Both".</span></span>                                                                                           |



 

<span data-ttu-id="01eeb-127">Si el complemento de DSP implementa una interfaz personalizada y el complemento se va a ejecutar en Windows Media Player 11 en Windows Vista, debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="01eeb-127">If your DSP plug-in implements a custom interface and if your plug-in is going to run in Windows Media Player 11 on Windows Vista, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



<span data-ttu-id="01eeb-128">En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para nombres, valores numéricos y identificadores únicos globales (GUID) que son específicos del complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="01eeb-128">In the preceding registry syntax, the symbols in italic are placeholders for names, numeric values, and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="01eeb-129">En la tabla siguiente se describen esos marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="01eeb-129">The following table describes those placeholders.</span></span>



| <span data-ttu-id="01eeb-130">Marcador de posición</span><span class="sxs-lookup"><span data-stu-id="01eeb-130">Placeholder</span></span>           | <span data-ttu-id="01eeb-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="01eeb-131">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01eeb-132">*ProxyStubClsid*</span><span class="sxs-lookup"><span data-stu-id="01eeb-132">*ProxyStubClsid*</span></span>      | <span data-ttu-id="01eeb-133">GUID que es el identificador de clase de la clase que implementa los proxies y códigos auxiliares para las interfaces personalizadas del complemento DSP. Este GUID debe estar en formato de registro, completar con las llaves.</span><span class="sxs-lookup"><span data-stu-id="01eeb-133">A GUID that is the class identifier for the class that implements the proxies and stubs for the DSP plug-in's custom interfaces.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="01eeb-134">Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="01eeb-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="01eeb-135">*ProxyStubModuleName*</span><span class="sxs-lookup"><span data-stu-id="01eeb-135">*ProxyStubModuleName*</span></span> | <span data-ttu-id="01eeb-136">Ruta de acceso completa al archivo DLL que implementa las interfaces de proxy y de código auxiliar para el complemento DSP. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareDspPS.dll"</span><span class="sxs-lookup"><span data-stu-id="01eeb-136">The fully qualified path to the DLL that implements the proxy and stub interfaces for the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDspPS.dll"</span></span><br/>                                                                                               |
| <span data-ttu-id="01eeb-137">*CustomInterfaceId*</span><span class="sxs-lookup"><span data-stu-id="01eeb-137">*CustomInterfaceId*</span></span>   | <span data-ttu-id="01eeb-138">GUID que es el identificador de interfaz de una interfaz personalizada implementada por el complemento DSP. Este GUID debe estar en formato de registro, completar con las llaves.</span><span class="sxs-lookup"><span data-stu-id="01eeb-138">A GUID that is the interface identifier for a custom interface that is implemented by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="01eeb-139">Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="01eeb-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                           |
| <span data-ttu-id="01eeb-140">*CustomInterfaceName*</span><span class="sxs-lookup"><span data-stu-id="01eeb-140">*CustomInterfaceName*</span></span> | <span data-ttu-id="01eeb-141">Nombre de una interfaz personalizada implementada por el complemento DSP. Ejemplo: "IProsewareDsp"</span><span class="sxs-lookup"><span data-stu-id="01eeb-141">The name of a custom interface that is implemented by the DSP plug-in.Example: "IProsewareDsp"</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="01eeb-142">*NumberOfMethods*</span><span class="sxs-lookup"><span data-stu-id="01eeb-142">*NumberOfMethods*</span></span>     | <span data-ttu-id="01eeb-143">El número de métodos, incluidos los métodos heredados, definidos por una interfaz personalizada. Ejemplo: "5"</span><span class="sxs-lookup"><span data-stu-id="01eeb-143">The number of methods, including inherited methods, defined by a custom interface.Example: "5"</span></span><br/>                                                                                                                                                                  |



 

<span data-ttu-id="01eeb-144">Si el complemento de DSP proporciona una página de propiedades, debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="01eeb-144">If your DSP plug-in provides a property page, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="01eeb-145">En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos del complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="01eeb-145">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="01eeb-146">En la tabla siguiente se describen esos marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="01eeb-146">The following table describes those placeholders.</span></span>



| <span data-ttu-id="01eeb-147">Marcador de posición</span><span class="sxs-lookup"><span data-stu-id="01eeb-147">Placeholder</span></span>                 | <span data-ttu-id="01eeb-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="01eeb-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01eeb-149">*PropPageClsid*</span><span class="sxs-lookup"><span data-stu-id="01eeb-149">*PropPageClsid*</span></span>             | <span data-ttu-id="01eeb-150">GUID que es el identificador de clase de la clase de página de propiedades que proporciona el complemento DSP. Este GUID debe estar en formato de registro, completar con las llaves.</span><span class="sxs-lookup"><span data-stu-id="01eeb-150">A GUID that is the class identifier for the property page class provided by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="01eeb-151">Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="01eeb-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="01eeb-152">*PropPageClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="01eeb-152">*PropPageClassFriendlyName*</span></span> | <span data-ttu-id="01eeb-153">Nombre descriptivo para la clase de página de propiedades. Ejemplo: "clase de página de propiedades ProsewareDSP"</span><span class="sxs-lookup"><span data-stu-id="01eeb-153">A friendly name for the property page class.Example: "ProsewareDSP Property Page Class"</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="01eeb-154">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="01eeb-154">*PluginModuleName*</span></span>          | <span data-ttu-id="01eeb-155">Ruta de acceso completa al archivo DLL que implementa el complemento DSP. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="01eeb-155">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                               |



 

<span data-ttu-id="01eeb-156">**Llamando a IWMPPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="01eeb-156">**Calling IWMPPluginRegistrar**</span></span>

<span data-ttu-id="01eeb-157">Además de las subclaves del registro y las entradas descritas en las listas y las tablas anteriores, debe crear algunas claves y entradas del registro mediante una llamada a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="01eeb-157">In addition to the registry subkeys and entries described in the preceding lists and tables, you must create some registry keys and entries by calling [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span></span> <span data-ttu-id="01eeb-158">Este método realiza el registro necesario para permitir que Windows Media Player reconozca el complemento y lo presente como una opción al usuario.</span><span class="sxs-lookup"><span data-stu-id="01eeb-158">This method performs the necessary registration to enable Windows Media Player to recognize your plug-in and present it as an option to the user.</span></span>

<span data-ttu-id="01eeb-159">Llame a **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** en la función **DllRegisterServer** del complemento y llame a [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) en la función **DllUnregisterServer** del complemento.</span><span class="sxs-lookup"><span data-stu-id="01eeb-159">Call **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in your plug-in's **DllRegisterServer** function, and call [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in your plug-in's **DllUnregisterServer** function.</span></span> <span data-ttu-id="01eeb-160">Para obtener un puntero a una interfaz **IWMPMediaPluginRegistrar** , llame a **COCREATEINSTANCE**, pasando CLSID \_ WMPMediaPluginRegistrar como identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="01eeb-160">To get a pointer to an **IWMPMediaPluginRegistrar** interface, call **CoCreateInstance**, passing CLSID\_WMPMediaPluginRegistrar as the Class ID.</span></span> <span data-ttu-id="01eeb-161">La constante \_ WMPMediaPluginRegistrar de CLSID se define en wmpservices. h.</span><span class="sxs-lookup"><span data-stu-id="01eeb-161">The constant CLSID\_WMPMediaPluginRegistrar is defined in wmpservices.h.</span></span>

<span data-ttu-id="01eeb-162">**Registro en el Asistente para complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="01eeb-162">**Registration in the DSP Plug-in Wizard**</span></span>

<span data-ttu-id="01eeb-163">El Asistente para complementos de DSP, que se incluye en el Windows SDK, genera código de ejemplo basado en Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="01eeb-163">The DSP plug-in wizard, which is included in the Windows SDK, generates sample code that is based on Active Template Library (ATL).</span></span> <span data-ttu-id="01eeb-164">La función **DllRegisterServer** del complemento de ejemplo llama a la función **RegisterServer** de ATL, que crea subclaves del registro y entradas de acuerdo con dos archivos de script del registro en el proyecto de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="01eeb-164">The sample plug-in's **DllRegisterServer** function calls ATL's **RegisterServer** function, which creates registry subkeys and entries according to two registry script files in the Visual Studio project.</span></span> <span data-ttu-id="01eeb-165">El archivo *projectname*. RGS contiene el script para registrar la clase principal del complemento y el archivo *projectname* PropPage. RGS contiene el script para registrar la clase de página de propiedades del complemento.</span><span class="sxs-lookup"><span data-stu-id="01eeb-165">The file *ProjectName*.rgs contains the script for registering the plug-in's main class, and the file *ProjectName* PropPage.rgs contains the script for registering the plug-in's property page class.</span></span> <span data-ttu-id="01eeb-166">La función **DllRegisterServer** del complemento de ejemplo también llama a **IWMPPluginRegistrar:: WMPRegisterPlayerPlugin**.</span><span class="sxs-lookup"><span data-stu-id="01eeb-166">The sample plug-in's **DllRegisterServer** function also calls **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.</span></span>

<span data-ttu-id="01eeb-167">El Asistente para complementos DSP también genera código para un componente de código auxiliar de proxy que es un archivo. dll de registro automático.</span><span class="sxs-lookup"><span data-stu-id="01eeb-167">The DSP plug-in wizard also generates code for a proxy-stub component that is a self-registering .dll file.</span></span> <span data-ttu-id="01eeb-168">El código de registro de ese archivo está en dlldata. cpp.</span><span class="sxs-lookup"><span data-stu-id="01eeb-168">The registration code for that file is in dlldata.cpp.</span></span> <span data-ttu-id="01eeb-169">Las **\_ rutinas** de macro DLLDATA se expanden para incluir una implementación de **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="01eeb-169">The macro **DLLDATA\_ROUTINES** expands to include an implementation of **DllRegisterServer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01eeb-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01eeb-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01eeb-171">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="01eeb-171">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="01eeb-172">**IWMPMediaPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="01eeb-172">**IWMPMediaPluginRegistrar**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





