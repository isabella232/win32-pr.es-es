---
title: Claves del registro y entradas para una tienda en línea de tipo 1
description: Claves del registro y entradas para una tienda en línea de tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player tiendas en línea, registro
- tiendas en línea, registro
- tipo 1 tiendas en línea, registro
- registro, tipo 1 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105685680"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a><span data-ttu-id="e8277-107">Claves del registro y entradas para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="e8277-107">Registry Keys and Entries for a Type 1 Online Store</span></span>

<span data-ttu-id="e8277-108">Para que una tienda en línea de tipo 1 esté disponible en Windows Media Player, el proveedor de la tienda en línea debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e8277-108">To make a type 1 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> <span data-ttu-id="e8277-109">Al establecer el valor de DllSurrogate en la cadena vacía, se indica que el tiempo de ejecución de COM cargará el complemento de la tienda en línea en el suplente de DLL predeterminado, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="e8277-109">Setting the value of DllSurrogate to the empty string indicates that the COM runtime will load the online store's plug-in into the default DLL surrogate, dllhost.exe.</span></span>

 

<span data-ttu-id="e8277-110">En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e8277-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="e8277-111">En la tabla siguiente se describen esos marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="e8277-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="e8277-112">Marcador de posición</span><span class="sxs-lookup"><span data-stu-id="e8277-112">Placeholder</span></span>    | <span data-ttu-id="e8277-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8277-113">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8277-114">*keyName*</span><span class="sxs-lookup"><span data-stu-id="e8277-114">*keyName*</span></span>      | <span data-ttu-id="e8277-115">Cadena acordada entre Microsoft y la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e8277-115">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="e8277-116">Esta cadena identifica de forma única la tienda en línea. Ejemplo: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="e8277-116">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="e8277-117">*flags*</span><span class="sxs-lookup"><span data-stu-id="e8277-117">*flags*</span></span>        | <span data-ttu-id="e8277-118">Un or **bit a** bit de uno o más marcadores de capacidad de complemento estas marcas especifican si Windows Media Player debe llamar a métodos concretos de [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span><span class="sxs-lookup"><span data-stu-id="e8277-118">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span></span> <span data-ttu-id="e8277-119">Para obtener información sobre las marcas admitidas, vea la tabla de marcas de capacidad de complementos que se indican a continuación de esta tabla. Ejemplo: 00000058</span><span class="sxs-lookup"><span data-stu-id="e8277-119">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000058</span></span><br/> |
| <span data-ttu-id="e8277-120">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="e8277-120">*clsid*</span></span>        | <span data-ttu-id="e8277-121">GUID que es el identificador de clase (CLSID) de la clase que implementa **IWMPContentPartner** en el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e8277-121">A GUID that is the class identifier (CLSID) for the class that implements **IWMPContentPartner** in the online store's plug-in.</span></span> <span data-ttu-id="e8277-122">Este GUID debe estar en formato de registro, completar con las llaves. Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="e8277-122">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                  |
| <span data-ttu-id="e8277-123">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="e8277-123">*friendlyname*</span></span> | <span data-ttu-id="e8277-124">Un nombre descriptivo para la tienda en línea. Ejemplo: "servicio de música de Proseware"</span><span class="sxs-lookup"><span data-stu-id="e8277-124">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="e8277-125">*appid*</span><span class="sxs-lookup"><span data-stu-id="e8277-125">*appid*</span></span>        | <span data-ttu-id="e8277-126">GUID que es el identificador de la aplicación (AppID) para el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e8277-126">A GUID that is the application identifier (AppID) for the online store's plug-in.</span></span> <span data-ttu-id="e8277-127">Este GUID debe estar en formato de registro, completar con las llaves. Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="e8277-127">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                |
| <span data-ttu-id="e8277-128">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="e8277-128">*pluginName*</span></span>   | <span data-ttu-id="e8277-129">Un nombre para el complemento de la tienda en línea. Ejemplo: "complemento de asociado de contenido de Proseware"</span><span class="sxs-lookup"><span data-stu-id="e8277-129">A name for the online store's plug-in.Example: "Proseware Content Partner Plug-in"</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="e8277-130">*className*</span><span class="sxs-lookup"><span data-stu-id="e8277-130">*className*</span></span>    | <span data-ttu-id="e8277-131">Nombre de la clase que implementa **IWMPContentpartner** en el complemento de la tienda en línea. Ejemplo: "CProsewarePartner"</span><span class="sxs-lookup"><span data-stu-id="e8277-131">The name of the class that implements **IWMPContentpartner** in the online store's plug-in.Example: "CProsewarePartner"</span></span><br/>                                                                                                                                                                                              |
| <span data-ttu-id="e8277-132">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="e8277-132">*moduleName*</span></span>   | <span data-ttu-id="e8277-133">Ruta de acceso completa al archivo DLL que implementa el complemento de la tienda en línea. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewarePartner.dll"</span><span class="sxs-lookup"><span data-stu-id="e8277-133">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewarePartner.dll"</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="e8277-134">*Threading*</span><span class="sxs-lookup"><span data-stu-id="e8277-134">*threading*</span></span>    | <span data-ttu-id="e8277-135">Tipo de apartamento en el que se ejecuta el complemento.</span><span class="sxs-lookup"><span data-stu-id="e8277-135">The type of apartment the plug-in runs in.</span></span> <span data-ttu-id="e8277-136">"ThreadingModel" = "Apartment" indica que el complemento se ejecuta en un contenedor uniproceso (STA).</span><span class="sxs-lookup"><span data-stu-id="e8277-136">"ThreadingModel"="Apartment" indicates that the plug-in runs in a single-threaded apartment (STA).</span></span> <span data-ttu-id="e8277-137">"ThreadingModel" = "Free" indica que el complemento se ejecuta en el contenedor multiproceso (MTA).</span><span class="sxs-lookup"><span data-stu-id="e8277-137">"ThreadingModel"="Free" indicates that the plug-in runs in the multithreaded apartment (MTA).</span></span>                                                                                     |



 

<span data-ttu-id="e8277-138">En la tabla siguiente se describen las marcas de capacidad del complemento.</span><span class="sxs-lookup"><span data-stu-id="e8277-138">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="e8277-139">Marca</span><span class="sxs-lookup"><span data-stu-id="e8277-139">Flag</span></span>                                    | <span data-ttu-id="e8277-140">Value</span><span class="sxs-lookup"><span data-stu-id="e8277-140">Value</span></span> | <span data-ttu-id="e8277-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8277-141">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8277-142">límite de suscripción \_ \_ BACKGROUNDPROCESSING</span><span class="sxs-lookup"><span data-stu-id="e8277-142">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="e8277-143">0x8</span><span class="sxs-lookup"><span data-stu-id="e8277-143">0x8</span></span>   | <span data-ttu-id="e8277-144">Windows Media Player debe llamar a [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) para informar al complemento cuando debe iniciar y detener el procesamiento en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e8277-144">Windows Media Player should call [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) to inform the plug-in when it should start and stop background processing.</span></span>                                                                                                     |
| <span data-ttu-id="e8277-145">límite de suscripción \_ \_ DEVICEAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e8277-145">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="e8277-146">0x10</span><span class="sxs-lookup"><span data-stu-id="e8277-146">0x10</span></span>  | <span data-ttu-id="e8277-147">Windows Media Player debe llamar a [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span><span class="sxs-lookup"><span data-stu-id="e8277-147">Windows Media Player should call [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span></span>                                                                                                                                                                   |
| <span data-ttu-id="e8277-148">el \_ límite de suscripción \_ es \_ CONTENTPARTNER</span><span class="sxs-lookup"><span data-stu-id="e8277-148">SUBSCRIPTION\_CAP\_IS\_CONTENTPARTNER</span></span>   | <span data-ttu-id="e8277-149">0x40</span><span class="sxs-lookup"><span data-stu-id="e8277-149">0x40</span></span>  | <span data-ttu-id="e8277-150">Informa a Windows Media Player de que el complemento implementa la interfaz **IWMPContentPartner** .</span><span class="sxs-lookup"><span data-stu-id="e8277-150">Informs Windows Media Player that the plug-in implements the **IWMPContentPartner** interface.</span></span> <span data-ttu-id="e8277-151">Todos los complementos de la tienda en línea de tipo 1 deben establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="e8277-151">All type 1 online store plug-ins must set this flag.</span></span>                                                                                                                         |
| <span data-ttu-id="e8277-152">límite de suscripción \_ \_ ALTLOGIN</span><span class="sxs-lookup"><span data-stu-id="e8277-152">SUBSCRIPTION\_CAP\_ALTLOGIN</span></span>             | <span data-ttu-id="e8277-153">0x80</span><span class="sxs-lookup"><span data-stu-id="e8277-153">0x80</span></span>  | <span data-ttu-id="e8277-154">Informa a Windows Media Player de que el complemento admite un inicio de sesión alternativo.</span><span class="sxs-lookup"><span data-stu-id="e8277-154">Informs Windows Media Player that the plug-in supports an alternate login.</span></span> <span data-ttu-id="e8277-155">Si el complemento admite un inicio de sesión alternativo, Windows Media Player recupera la dirección URL de inicio de sesión y el título alternativos llamando a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="e8277-155">If the plug-in supports an alternate login, Windows Media Player retrieves the alternate login URL and caption by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span></span> |



 

<span data-ttu-id="e8277-156">**Entradas del registro para desarrollo y pruebas**</span><span class="sxs-lookup"><span data-stu-id="e8277-156">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="e8277-157">Cuando empiece a desarrollar la tienda en línea, Microsoft le proporcionará dos claves: una clave de prueba y una clave de producción.</span><span class="sxs-lookup"><span data-stu-id="e8277-157">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="e8277-158">Durante la fase de desarrollo y pruebas, la tienda en línea aparecerá en Windows Media Player solo si la clave de prueba o la clave de producción se encuentra en el registro del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e8277-158">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="e8277-159">Para obtener más información acerca de las claves de prueba y de producción, consulte [claves de prueba y de producción para una tienda en línea de tipo 1](test-and-production-keys-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="e8277-159">For more information about the test and production keys, see [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="e8277-160">Coloque la clave de prueba o de producción en la siguiente ubicación del registro.</span><span class="sxs-lookup"><span data-stu-id="e8277-160">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="e8277-161">Tenga en cuenta que el valor de la entrada del registro TestParameter puede especificar varias claves de prueba o de producción.</span><span class="sxs-lookup"><span data-stu-id="e8277-161">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="e8277-162">Por ejemplo, supongamos que Proseware tiene una clave de prueba de "1234" y Contoso tiene una clave de prueba de "2345".</span><span class="sxs-lookup"><span data-stu-id="e8277-162">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="e8277-163">La siguiente entrada del registro especifica que los almacenes de pruebas para Proseware y contoso aparecerán en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e8277-163">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="e8277-164">**Entrada del registro ActiveService**</span><span class="sxs-lookup"><span data-stu-id="e8277-164">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="e8277-165">Cuando el usuario activa una tienda en línea, Windows Media Player escribe información en el registro que identifica la tienda en línea activa.</span><span class="sxs-lookup"><span data-stu-id="e8277-165">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="e8277-166">Windows Media Player coloca la información en la siguiente ubicación del registro en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e8277-166">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="e8277-167">En la sintaxis del registro anterior, *serviceInfo* es un marcador de posición para una cadena que contiene información descriptiva acerca de la tienda en línea activa.</span><span class="sxs-lookup"><span data-stu-id="e8277-167">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8277-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8277-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8277-169">**Referencia de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e8277-169">**Reference for Type 1 Online Stores**</span></span>](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





