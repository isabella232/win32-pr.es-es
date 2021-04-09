---
title: Claves del registro y entradas para una tienda en línea de tipo 2
description: Claves del registro y entradas para una tienda en línea de tipo 2
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player tiendas en línea, registro
- tiendas en línea, registro
- tipo 2 tiendas en línea, registro
- registro, tipo 2 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149120"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a><span data-ttu-id="5ec95-107">Claves del registro y entradas para una tienda en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="5ec95-107">Registry Keys and Entries for a Type 2 Online Store</span></span>

> [!Note]  
> <span data-ttu-id="5ec95-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="5ec95-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5ec95-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="5ec95-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5ec95-110">Para que una tienda en línea de tipo 2 esté disponible en Windows Media Player, el proveedor de la tienda en línea debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="5ec95-110">To make a type 2 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="5ec95-111">En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="5ec95-111">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="5ec95-112">En la tabla siguiente se describen esos marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="5ec95-112">The following table describes those placeholders.</span></span>



| <span data-ttu-id="5ec95-113">Marcador de posición</span><span class="sxs-lookup"><span data-stu-id="5ec95-113">Placeholder</span></span>    | <span data-ttu-id="5ec95-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ec95-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec95-115">*keyName*</span><span class="sxs-lookup"><span data-stu-id="5ec95-115">*keyName*</span></span>      | <span data-ttu-id="5ec95-116">Cadena acordada entre Microsoft y la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="5ec95-116">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="5ec95-117">Esta cadena identifica de forma única la tienda en línea. Ejemplo: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="5ec95-117">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5ec95-118">*flags*</span><span class="sxs-lookup"><span data-stu-id="5ec95-118">*flags*</span></span>        | <span data-ttu-id="5ec95-119">Un or **bit a** bit de uno o más marcadores de capacidad de complemento estas marcas especifican si Windows Media Player debe llamar a métodos concretos de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) y [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span><span class="sxs-lookup"><span data-stu-id="5ec95-119">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) and [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span></span> <span data-ttu-id="5ec95-120">Para obtener información sobre las marcas admitidas, vea la tabla de marcas de capacidad de complementos que se indican a continuación de esta tabla. Ejemplo: 00000037</span><span class="sxs-lookup"><span data-stu-id="5ec95-120">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000037</span></span><br/> |
| <span data-ttu-id="5ec95-121">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="5ec95-121">*clsid*</span></span>        | <span data-ttu-id="5ec95-122">GUID que es el identificador de clase (CLSID) de la clase que implementa **IWMPSubscriptionService** en el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="5ec95-122">A GUID that is the class identifier (CLSID) for the class that implements **IWMPSubscriptionService** in the online store's plug-in.</span></span> <span data-ttu-id="5ec95-123">Este GUID debe estar en formato de registro, completar con las llaves. Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="5ec95-123">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="5ec95-124">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="5ec95-124">*friendlyname*</span></span> | <span data-ttu-id="5ec95-125">Un nombre descriptivo para la tienda en línea. Ejemplo: "servicio de música de Proseware"</span><span class="sxs-lookup"><span data-stu-id="5ec95-125">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="5ec95-126">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="5ec95-126">*pluginName*</span></span>   | <span data-ttu-id="5ec95-127">Un nombre para el complemento de la tienda en línea. Ejemplo: "complemento de servicio de Proseware"</span><span class="sxs-lookup"><span data-stu-id="5ec95-127">A name for the online store's plug-in.Example: "Proseware Service Plug-in"</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5ec95-128">*className*</span><span class="sxs-lookup"><span data-stu-id="5ec95-128">*className*</span></span>    | <span data-ttu-id="5ec95-129">Nombre de la clase que implementa **IWMPSubscriptionService** en el complemento de la tienda en línea. Ejemplo: "CProsewareService"</span><span class="sxs-lookup"><span data-stu-id="5ec95-129">The name of the class that implements **IWMPSubscriptionService** in the online store's plug-in.Example: "CProsewareService"</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5ec95-130">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="5ec95-130">*moduleName*</span></span>   | <span data-ttu-id="5ec95-131">Ruta de acceso completa al archivo DLL que implementa el complemento de la tienda en línea. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareService.dll"</span><span class="sxs-lookup"><span data-stu-id="5ec95-131">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareService.dll"</span></span><br/>                                                                                                                                                                                                                                                |



 

<span data-ttu-id="5ec95-132">En la tabla siguiente se describen las marcas de capacidad del complemento.</span><span class="sxs-lookup"><span data-stu-id="5ec95-132">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="5ec95-133">Marca</span><span class="sxs-lookup"><span data-stu-id="5ec95-133">Flag</span></span>                                    | <span data-ttu-id="5ec95-134">Value</span><span class="sxs-lookup"><span data-stu-id="5ec95-134">Value</span></span> | <span data-ttu-id="5ec95-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ec95-135">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec95-136">límite de suscripción \_ \_ ALLOWPLAY</span><span class="sxs-lookup"><span data-stu-id="5ec95-136">SUBSCRIPTION\_CAP\_ALLOWPLAY</span></span>            | <span data-ttu-id="5ec95-137">0X1</span><span class="sxs-lookup"><span data-stu-id="5ec95-137">0X1</span></span>   | <span data-ttu-id="5ec95-138">Windows Media Player debe llamar a [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span><span class="sxs-lookup"><span data-stu-id="5ec95-138">Windows Media Player should call [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span></span>                                                                                                                      |
| <span data-ttu-id="5ec95-139">límite de suscripción \_ \_ ALLOWCDBURN</span><span class="sxs-lookup"><span data-stu-id="5ec95-139">SUBSCRIPTION\_CAP\_ALLOWCDBURN</span></span>          | <span data-ttu-id="5ec95-140">0X2</span><span class="sxs-lookup"><span data-stu-id="5ec95-140">0X2</span></span>   | <span data-ttu-id="5ec95-141">Windows Media Player debe llamar a [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span><span class="sxs-lookup"><span data-stu-id="5ec95-141">Windows Media Player should call [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span></span>                                                                                                                  |
| <span data-ttu-id="5ec95-142">límite de suscripción \_ \_ ALLOWPDATRANSFER</span><span class="sxs-lookup"><span data-stu-id="5ec95-142">SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER</span></span>     | <span data-ttu-id="5ec95-143">0X4</span><span class="sxs-lookup"><span data-stu-id="5ec95-143">0X4</span></span>   | <span data-ttu-id="5ec95-144">Windows Media Player debe llamar a [IWMPSubscriptionService:: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span><span class="sxs-lookup"><span data-stu-id="5ec95-144">Windows Media Player should call [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span></span>                                                                                                        |
| <span data-ttu-id="5ec95-145">límite de suscripción \_ \_ BACKGROUNDPROCESSING</span><span class="sxs-lookup"><span data-stu-id="5ec95-145">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="5ec95-146">0X8</span><span class="sxs-lookup"><span data-stu-id="5ec95-146">0X8</span></span>   | <span data-ttu-id="5ec95-147">Windows Media Player debe llamar a [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span><span class="sxs-lookup"><span data-stu-id="5ec95-147">Windows Media Player should call [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span></span>                                                                                      |
| <span data-ttu-id="5ec95-148">límite de suscripción \_ \_ DEVICEAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="5ec95-148">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="5ec95-149">0X10</span><span class="sxs-lookup"><span data-stu-id="5ec95-149">0X10</span></span>  | <span data-ttu-id="5ec95-150">Windows Media Player debe llamar a [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span><span class="sxs-lookup"><span data-stu-id="5ec95-150">Windows Media Player should call [IWMPSubscriptionService2::deviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span></span>                                                                                                        |
| <span data-ttu-id="5ec95-151">límite de suscripción \_ \_ PREPAREFORSYNC</span><span class="sxs-lookup"><span data-stu-id="5ec95-151">SUBSCRIPTION\_CAP\_PREPAREFORSYNC</span></span>       | <span data-ttu-id="5ec95-152">0X20</span><span class="sxs-lookup"><span data-stu-id="5ec95-152">0X20</span></span>  | <span data-ttu-id="5ec95-153">Windows Media Player debe llamar a [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span><span class="sxs-lookup"><span data-stu-id="5ec95-153">Windows Media Player should call [IWMPSubscriptionService2::prepareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span></span>                                                                                                          |
| <span data-ttu-id="5ec95-154">Cap de suscripción \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="5ec95-154">SUBSCRIPTION\_V1\_CAPS</span></span>                  | <span data-ttu-id="5ec95-155">0XF</span><span class="sxs-lookup"><span data-stu-id="5ec95-155">0XF</span></span>   | <span data-ttu-id="5ec95-156">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ec95-156">Default.</span></span> <span data-ttu-id="5ec95-157">Este valor se usa si no se registra ninguno.</span><span class="sxs-lookup"><span data-stu-id="5ec95-157">This value is used if none is registered.</span></span> <span data-ttu-id="5ec95-158">Esto es equivalente a la combinación de Cap de suscripción \_ \_ ALLOWPLAY, el límite de la suscripción \_ ALLOWCDBURN, el límite de la \_ suscripción \_ \_ ALLOWPDATRANSFER y el límite de la suscripción \_ \_ BACKGROUNDPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="5ec95-158">This is equivalent to combining SUBSCRIPTION\_CAP\_ALLOWPLAY, SUBSCRIPTION\_CAP\_ALLOWCDBURN, SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER, and SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING.</span></span> |



 

<span data-ttu-id="5ec95-159">**Entradas del registro para desarrollo y pruebas**</span><span class="sxs-lookup"><span data-stu-id="5ec95-159">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="5ec95-160">Cuando empiece a desarrollar la tienda en línea, Microsoft le proporcionará dos claves: una clave de prueba y una clave de producción.</span><span class="sxs-lookup"><span data-stu-id="5ec95-160">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="5ec95-161">Durante la fase de desarrollo y pruebas, la tienda en línea aparecerá en Windows Media Player solo si la clave de prueba o la clave de producción se encuentra en el registro del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="5ec95-161">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="5ec95-162">Para obtener más información acerca de las claves de prueba y de producción, consulte [claves de prueba y producción para una tienda en línea de tipo 2](test-and-production-keys-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="5ec95-162">For more information about the test and production keys, see [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="5ec95-163">Coloque la clave de prueba o de producción en la siguiente ubicación del registro.</span><span class="sxs-lookup"><span data-stu-id="5ec95-163">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="5ec95-164">Tenga en cuenta que el valor de la entrada del registro TestParameter puede especificar varias claves de prueba o de producción.</span><span class="sxs-lookup"><span data-stu-id="5ec95-164">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="5ec95-165">Por ejemplo, supongamos que Proseware tiene una clave de prueba de "1234" y Contoso tiene una clave de prueba de "2345".</span><span class="sxs-lookup"><span data-stu-id="5ec95-165">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="5ec95-166">La siguiente entrada del registro especifica que los almacenes de pruebas para Proseware y contoso aparecerán en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5ec95-166">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="5ec95-167">**Entrada del registro ActiveService**</span><span class="sxs-lookup"><span data-stu-id="5ec95-167">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="5ec95-168">Cuando el usuario activa una tienda en línea, Windows Media Player escribe información en el registro que identifica la tienda en línea activa.</span><span class="sxs-lookup"><span data-stu-id="5ec95-168">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="5ec95-169">Windows Media Player coloca la información en la siguiente ubicación del registro en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="5ec95-169">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="5ec95-170">En la sintaxis del registro anterior, *serviceInfo* es un marcador de posición para una cadena que contiene información descriptiva acerca de la tienda en línea activa.</span><span class="sxs-lookup"><span data-stu-id="5ec95-170">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ec95-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ec95-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec95-172">**Referencia de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="5ec95-172">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





