---
description: Cuando se instala un proveedor de red, la aplicación debe crear las claves y los valores del registro que se describen en este tema.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Claves del registro de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002182"
---
# <a name="authentication-registry-keys"></a><span data-ttu-id="779e3-103">Claves del registro de autenticación</span><span class="sxs-lookup"><span data-stu-id="779e3-103">Authentication Registry Keys</span></span>

<span data-ttu-id="779e3-104">Cuando se instala un proveedor de red, la aplicación debe crear las claves y los valores del registro que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="779e3-104">When it installs a network provider, your application should create the registry keys and values described in this topic.</span></span> <span data-ttu-id="779e3-105">Estas claves y valores proporcionan información al MPR sobre los proveedores de red instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="779e3-105">These keys and values provide information to the MPR about the network providers installed on the system.</span></span> <span data-ttu-id="779e3-106">El MPR comprueba estas claves cuando se inicia y carga los archivos DLL del proveedor de red que encuentra.</span><span class="sxs-lookup"><span data-stu-id="779e3-106">The MPR checks these keys when it starts and loads the network provider DLLs that it finds.</span></span>

<span data-ttu-id="779e3-107">Antes de crear un conjunto de claves que contengan información sobre el proveedor de red, debe agregar el nombre de su proveedor de red a la clave de **orden** .</span><span class="sxs-lookup"><span data-stu-id="779e3-107">Before you create a set of keys to hold information about your network provider, you should add the name of your network provider to the **order** key.</span></span> <span data-ttu-id="779e3-108">Esta clave es una subclave de la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="779e3-108">This key is a subkey of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

<span data-ttu-id="779e3-109">La clave **Order** contiene un valor único, **ProviderOrder**, que enumera los proveedores instalados y especifica el orden en que se deben probar durante las operaciones que atraviesan los proveedores hasta que se encuentra un proveedor de aceptación.</span><span class="sxs-lookup"><span data-stu-id="779e3-109">The **order** key contains a single value, **ProviderOrder**, which lists the installed providers and specifies the order in which they should be tried during operations that cycle through providers until an accepting provider is found.</span></span>

<span data-ttu-id="779e3-110">El valor **ProviderOrder** contiene una lista separada por comas de nombres de clave.</span><span class="sxs-lookup"><span data-stu-id="779e3-110">The **ProviderOrder** value contains a comma-separated list of key names.</span></span> <span data-ttu-id="779e3-111">Cada nombre de clave de **ProviderOrder** identifica un proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="779e3-111">Each key name in **ProviderOrder** identifies a network provider.</span></span> <span data-ttu-id="779e3-112">Cuando MPR recorre los proveedores, los llama en el orden en que aparecen en esta lista.</span><span class="sxs-lookup"><span data-stu-id="779e3-112">When MPR cycles through the providers, it calls them in the order in which they appear in this list.</span></span>

<span data-ttu-id="779e3-113">El nombre del proveedor establecido en **ProviderOrder** también debe usarse como el nombre de la clave del registro que contiene información sobre ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="779e3-113">The provider name set in **ProviderOrder** should also be used as the name of the registry key that contains information about that provider.</span></span> <span data-ttu-id="779e3-114">Las claves del registro específicas del proveedor se crean como subclaves de la clave siguiente:</span><span class="sxs-lookup"><span data-stu-id="779e3-114">The provider-specific registry keys are created as subkeys of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="779e3-115">En otras palabras, los nombres de proveedor especificados en **ProviderOrder** son la ruta de acceso al registro de las claves específicas del proveedor de red, con respecto a la ruta de acceso siguiente:</span><span class="sxs-lookup"><span data-stu-id="779e3-115">In other words, the provider names specified in **ProviderOrder** are the path to the registry of the network provider-specific keys, relative to the following path:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="779e3-116">Cuando se instala el servicio de proveedor de red, la aplicación de instalación debe agregar una clave de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="779e3-116">When your network provider service is installed, the installation application should add a key as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

<span data-ttu-id="779e3-117">Donde *providerName* es el nombre del proveedor de red tal y como se especifica en el valor **ProviderOrder** de la clave **Order** .</span><span class="sxs-lookup"><span data-stu-id="779e3-117">Where *ProviderName* is the name of the network provider as specified in the **ProviderOrder** value of the **order** key.</span></span> <span data-ttu-id="779e3-118">El valor de **Grupo** de la clave *providerName* debe establecerse en "NetworkProvider".</span><span class="sxs-lookup"><span data-stu-id="779e3-118">The **Group** value under the *ProviderName* key should be set to "NetworkProvider".</span></span> <span data-ttu-id="779e3-119">Esto identifica el servicio como en el grupo de proveedores de red.</span><span class="sxs-lookup"><span data-stu-id="779e3-119">This identifies the service as being in the network provider group.</span></span>

<span data-ttu-id="779e3-120">También debe crear una subclave de *providerName*, **networkprovider**.</span><span class="sxs-lookup"><span data-stu-id="779e3-120">You must also create a subkey of *ProviderName*, **networkprovider**.</span></span> <span data-ttu-id="779e3-121">Esta clave contiene los siguientes valores que describen el proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="779e3-121">This key contains the following values that describe the network provider.</span></span>



| <span data-ttu-id="779e3-122">Value</span><span class="sxs-lookup"><span data-stu-id="779e3-122">Value</span></span>                       | <span data-ttu-id="779e3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="779e3-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779e3-124">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="779e3-124">**Name**</span></span><br/>         | <span data-ttu-id="779e3-125">Contiene el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="779e3-125">Contains the name of the provider.</span></span> <span data-ttu-id="779e3-126">Este nombre se muestra al usuario como el nombre de la red en los cuadros de diálogo examinar y debe coincidir con el campo **lpProvider** devuelto en las estructuras [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) .</span><span class="sxs-lookup"><span data-stu-id="779e3-126">This name is displayed to the user as the name of the network in the browse dialog boxes and should match the **lpProvider** field returned in [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures.</span></span> <span data-ttu-id="779e3-127">Este nombre debe ser una variación del nombre del producto, preferiblemente también con alguna indicación de la empresa, de modo que sea claro y único.</span><span class="sxs-lookup"><span data-stu-id="779e3-127">This name should be some variation of the product name, preferably with some indication of the company as well, so that it is clear and unique.</span></span> <span data-ttu-id="779e3-128">Por ejemplo, "MS-LanMan" es un buen nombre, mientras que "The net" sería una opción deficiente.</span><span class="sxs-lookup"><span data-stu-id="779e3-128">"MS-LanMan" for example is a good name, whereas "The Net" would be a poor choice.</span></span><br/> |
| <span data-ttu-id="779e3-129">**ProviderPath**</span><span class="sxs-lookup"><span data-stu-id="779e3-129">**ProviderPath**</span></span><br/> | <span data-ttu-id="779e3-130">Contiene la ruta de acceso completa del archivo DLL que implementa el proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="779e3-130">Contains the full path of the DLL that implements the network provider.</span></span> <span data-ttu-id="779e3-131">MPR llama a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) en esta ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="779e3-131">MPR calls [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) on this path.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="779e3-132">Los siguientes valores solo los usan los proveedores de red que admiten las funciones de administración de credenciales, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) y [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span><span class="sxs-lookup"><span data-stu-id="779e3-132">The following values are used only by network providers that support the credential management functions, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span></span>



| <span data-ttu-id="779e3-133">Value</span><span class="sxs-lookup"><span data-stu-id="779e3-133">Value</span></span>                              | <span data-ttu-id="779e3-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="779e3-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779e3-135">**Clase**</span><span class="sxs-lookup"><span data-stu-id="779e3-135">**Class**</span></span><br/>               | <span data-ttu-id="779e3-136">**DWORD** que identifica la clase, o tipo, de la funcionalidad del proveedor que admite este proveedor.</span><span class="sxs-lookup"><span data-stu-id="779e3-136">A **DWORD** that identifies the class, or type, of provider functionality that this provider supports.</span></span> <span data-ttu-id="779e3-137">Los valores pueden estar Unidos por el operador **o** cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="779e3-137">Values may be joined by the **OR** operator when appropriate.</span></span> <span data-ttu-id="779e3-138">Los valores válidos son la \_ clase de red WN \_ , la clase de credencial WN, la clase \_ \_ \_ AUTHENT primaria WN y la \_ \_ \_ clase de servicio WN \_ .</span><span class="sxs-lookup"><span data-stu-id="779e3-138">Valid values for this are WN\_NETWORK\_CLASS, WN\_CREDENTIAL\_CLASS, WN\_PRIMARY\_AUTHENT\_CLASS, and WN\_SERVICE\_CLASS.</span></span><br/> <span data-ttu-id="779e3-139">Aunque un proveedor puede admitir la funcionalidad principal del autenticador, se usará otro medio para determinar qué autenticador es principal.</span><span class="sxs-lookup"><span data-stu-id="779e3-139">Although a provider may support primary authenticator functionality, another means will be used to determine which authenticator is primary.</span></span><br/> <span data-ttu-id="779e3-140">**Windows XP/2000:** No se admite el cambio de autenticadores principales, por lo que este valor se omite.</span><span class="sxs-lookup"><span data-stu-id="779e3-140">**Windows XP/2000:** Switching primary authenticators is not supported, so this value is ignored.</span></span> <br/> |
| <span data-ttu-id="779e3-141">**AuthentProviderPath**</span><span class="sxs-lookup"><span data-stu-id="779e3-141">**AuthentProviderPath**</span></span><br/> | <span data-ttu-id="779e3-142">Este es el nombre de archivo completo para el archivo DLL que exporta las funciones de administración de credenciales.</span><span class="sxs-lookup"><span data-stu-id="779e3-142">This is the fully qualified file name for the DLL that exports the Credential Management Functions.</span></span> <span data-ttu-id="779e3-143">Este valor es útil (pero no obligatorio) solo cuando el proveedor se identifica como una clase de credencial o como un \_ \_ proveedor de clase AUTHENT principal \_ .</span><span class="sxs-lookup"><span data-stu-id="779e3-143">This value is useful (but not required) only when the provider is identified as being a CREDENTIAL\_CLASS or PRIMARY\_AUTHENT\_CLASS provider.</span></span> <span data-ttu-id="779e3-144">Si este valor no está presente para un proveedor de esta clase, se espera que las funciones de administración de credenciales se exporten desde el archivo DLL identificado por el valor de ProviderPath.</span><span class="sxs-lookup"><span data-stu-id="779e3-144">If this value is not present for a provider of this class, the credential management functions are expected to be exported from the DLL identified by the ProviderPath value.</span></span> <span data-ttu-id="779e3-145">Este valor solo se utiliza si es deseable empaquetar las funciones de red y las funciones del administrador de credenciales en archivos dll independientes.</span><span class="sxs-lookup"><span data-stu-id="779e3-145">This value is used only if it is desirable to package the network functions and the credential manager functions in separate DLLs.</span></span><br/>  |



 

<span data-ttu-id="779e3-146">Además de los valores que se usan para registrar proveedores de redes y administradores de credenciales, puede Agregar un valor al registro para registrar un archivo DLL para recibir notificaciones de conexión.</span><span class="sxs-lookup"><span data-stu-id="779e3-146">In addition to the values used to register network providers and credential managers, you can add a value to the registry to register a DLL to receive connection notifications.</span></span> <span data-ttu-id="779e3-147">Para ello, cree un valor REG \_ Expand \_ en la clave siguiente:</span><span class="sxs-lookup"><span data-stu-id="779e3-147">To do so, create a REG\_EXPAND\_SZ value under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

<span data-ttu-id="779e3-148">Este valor debe especificar la ruta de acceso a un archivo DLL que implementa la [API de notificación de conexión](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="779e3-148">This value should specify the path to a DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span> <span data-ttu-id="779e3-149">El nombre de este valor puede ser el que desee, siempre y cuando no se produzca ningún conflicto con los nombres de valor preexistentes.</span><span class="sxs-lookup"><span data-stu-id="779e3-149">The name of this value can be anything you want, as long as it does not conflict with preexisting value names.</span></span>

## <a name="example"></a><span data-ttu-id="779e3-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="779e3-150">Example</span></span>

<span data-ttu-id="779e3-151">En el ejemplo siguiente se muestran las claves del registro para un sistema que tiene instalados dos proveedores de red: LanmanWorkStation y AnotherNetSvc.</span><span class="sxs-lookup"><span data-stu-id="779e3-151">The following example shows the registry keys for a system that has two network providers installed: LanmanWorkStation and AnotherNetSvc.</span></span> <span data-ttu-id="779e3-152">AnotherNetSvc también es un administrador de credenciales.</span><span class="sxs-lookup"><span data-stu-id="779e3-152">AnotherNetSvc is also a credential manager.</span></span> <span data-ttu-id="779e3-153">En el ejemplo, los nombres de clave están en negrita y los nombres de valor están en cursiva.</span><span class="sxs-lookup"><span data-stu-id="779e3-153">In the example, key names are bold and value names are italic.</span></span>

<span data-ttu-id="779e3-154">**HKEY \_ \_** \\ **Sistema del** equipo local \\ **CurrentControlSet** \\ **control** \\ **NetworkProvider** \\ **orden**</span><span class="sxs-lookup"><span data-stu-id="779e3-154">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**order**</span></span>

<span data-ttu-id="779e3-155">*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"</span><span class="sxs-lookup"><span data-stu-id="779e3-155">*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"</span></span>

<span data-ttu-id="779e3-156">**HKEY \_ Sistema \_ del equipo local** NetworkProvider de los \\  \\  \\  \\  \\ **notificantes**</span><span class="sxs-lookup"><span data-stu-id="779e3-156">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="779e3-157">*MyNotifyApp* = "c: \\ Connect \\connect.dll"</span><span class="sxs-lookup"><span data-stu-id="779e3-157">*MyNotifyApp* = "c:\\connect\\connect.dll"</span></span>

<span data-ttu-id="779e3-158">**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**</span><span class="sxs-lookup"><span data-stu-id="779e3-158">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**</span></span>\\

<span data-ttu-id="779e3-159">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="779e3-159">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="779e3-160">**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="779e3-160">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**\\**NetworkProvider**</span></span>

<span data-ttu-id="779e3-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span><span class="sxs-lookup"><span data-stu-id="779e3-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span></span>

<span data-ttu-id="779e3-162">*Class* = 0x00000001 ( \_ clase de red WN \_ )</span><span class="sxs-lookup"><span data-stu-id="779e3-162">*Class* = 0x00000001 (WN\_NETWORK\_CLASS)</span></span>

<span data-ttu-id="779e3-163">**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**</span><span class="sxs-lookup"><span data-stu-id="779e3-163">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**</span></span>\\

<span data-ttu-id="779e3-164">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="779e3-164">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="779e3-165">**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="779e3-165">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**\\**NetworkProvider**</span></span>

<span data-ttu-id="779e3-166">*Name* = "otra red"*ProviderPath* = "c: \\ otra \\anet.dll"</span><span class="sxs-lookup"><span data-stu-id="779e3-166">*Name* = "Another Network"*ProviderPath* = "c:\\another\\anet.dll"</span></span>

<span data-ttu-id="779e3-167">*Class* = 0x00000003 ( \_ clase de credencial de clase de red WN \_ \| \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="779e3-167">*Class* = 0x00000003 (WN\_NETWORK\_CLASS \| WN\_CREDENTIAL\_CLASS)</span></span>

<span data-ttu-id="779e3-168">*AuthentProviderPath* = "c: \\ otro \\anetCM.dll"</span><span class="sxs-lookup"><span data-stu-id="779e3-168">*AuthentProviderPath* = "c:\\another\\anetCM.dll"</span></span>

 

