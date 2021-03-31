---
title: Valores del registro del método de autenticación de EAP
description: Obtenga información sobre los valores del registro del método de autenticación de EAP. Estos valores de registro específicos son necesarios para los métodos de autenticación de EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995641"
---
# <a name="eap-authenticator-method-registry-values"></a><span data-ttu-id="7cdee-104">Valores del registro del método de autenticación de EAP</span><span class="sxs-lookup"><span data-stu-id="7cdee-104">EAP Authenticator Method Registry Values</span></span>

<span data-ttu-id="7cdee-105">Los métodos de autenticación de EAP requieren valores de registro específicos.</span><span class="sxs-lookup"><span data-stu-id="7cdee-105">Specific registry values are required for EAP authenticator methods.</span></span>

## <a name="eap-authenticator-method-dll-paths"></a><span data-ttu-id="7cdee-106">Rutas de acceso DLL del método de autenticador EAP</span><span class="sxs-lookup"><span data-stu-id="7cdee-106">EAP Authenticator Method DLL Paths</span></span>

<span data-ttu-id="7cdee-107">La ruta de acceso siguiente especifica la ubicación del registro para los archivos dll normales del método de autenticación de EAP.</span><span class="sxs-lookup"><span data-stu-id="7cdee-107">The following path specifies the registry location for regular EAP authenticator method DLLs.</span></span>

<span data-ttu-id="7cdee-108">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="7cdee-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="7cdee-109">Por ejemplo, una ruta de acceso de registro de instalación del método de autenticación de EAP dada una **AuthorId** de "311" (que indica que "Microsoft" es el autor) y un **EapTypeId** de "40", aparece de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="7cdee-109">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="7cdee-110">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="7cdee-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="7cdee-111">La ruta de acceso siguiente especifica la ubicación del registro para los archivos DLL del método de autenticador EAP extendido.</span><span class="sxs-lookup"><span data-stu-id="7cdee-111">The following path specifies the registry location for extended EAP authenticator method DLLs.</span></span>

<span data-ttu-id="7cdee-112">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ \* &lt; VendorType&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="7cdee-112">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;VendorType&gt;**\*</span></span>

<span data-ttu-id="7cdee-113">Por ejemplo, una ruta de acceso de registro de instalación del método de autenticador de EAP dado un valor de **AuthorId** de "311" (que indica que "Microsoft" es el autor), un **VendorId** de "311" y un valor de **EapTypeId** de "40", aparece de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="7cdee-113">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="7cdee-114">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="7cdee-114">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="7cdee-115">Para obtener más información sobre la asignación de tipos de método EAP, consulte la sección 6,2 de [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="7cdee-115">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="7cdee-116">Valores del registro</span><span class="sxs-lookup"><span data-stu-id="7cdee-116">Registry Values</span></span>

<span data-ttu-id="7cdee-117">Se requieren los siguientes valores del registro del método de autenticación.</span><span class="sxs-lookup"><span data-stu-id="7cdee-117">The following authenticator method registry values are required.</span></span>

-   [<span data-ttu-id="7cdee-118">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="7cdee-118">AuthenticatorDllPath</span></span>](#authenticatordllpath)
-   [<span data-ttu-id="7cdee-119">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7cdee-119">AuthenticatorFriendlyName</span></span>](#authenticatorfriendlyname)

<span data-ttu-id="7cdee-120">Además de los valores del registro anteriores, se recomienda el siguiente valor del registro del método de autenticación.</span><span class="sxs-lookup"><span data-stu-id="7cdee-120">Besides the above registry values, the following authenticator method registry value is recommended.</span></span>

-   [<span data-ttu-id="7cdee-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cdee-121">Properties</span></span>](#properties)

<span data-ttu-id="7cdee-122">Los valores restantes del registro del método de autenticación son opcionales.</span><span class="sxs-lookup"><span data-stu-id="7cdee-122">The remaining authenticator method registry values are optional.</span></span>

-   [<span data-ttu-id="7cdee-123">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="7cdee-123">ConfigCLSID</span></span>](#configclsid)
-   [<span data-ttu-id="7cdee-124">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="7cdee-124">StandaloneSupported</span></span>](#standalonesupported)

## <a name="authenticatordllpath"></a><span data-ttu-id="7cdee-125">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="7cdee-125">AuthenticatorDllPath</span></span>



| <span data-ttu-id="7cdee-126">Valor constante</span><span class="sxs-lookup"><span data-stu-id="7cdee-126">Constant Value</span></span> | <span data-ttu-id="7cdee-127">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="7cdee-127">AuthenticatorDllPath</span></span>                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdee-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cdee-128">Type</span></span>           | <span data-ttu-id="7cdee-129">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7cdee-129">REG\_EXPAND\_SZ</span></span>                                                                                               |
| <span data-ttu-id="7cdee-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cdee-130">Description</span></span>    | <span data-ttu-id="7cdee-131">La ruta de acceso al archivo DLL del método de autenticación EAP.</span><span class="sxs-lookup"><span data-stu-id="7cdee-131">The path to the EAP authenticator method DLL.</span></span> <span data-ttu-id="7cdee-132">Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="7cdee-132">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

## <a name="authenticatorfriendlyname"></a><span data-ttu-id="7cdee-133">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7cdee-133">AuthenticatorFriendlyName</span></span>



| <span data-ttu-id="7cdee-134">Valor constante</span><span class="sxs-lookup"><span data-stu-id="7cdee-134">Constant Value</span></span> | <span data-ttu-id="7cdee-135">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7cdee-135">AuthenticatorFriendlyName</span></span>                                                          |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdee-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cdee-136">Type</span></span>           | <span data-ttu-id="7cdee-137">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7cdee-137">REG\_SZ</span></span>                                                                            |
| <span data-ttu-id="7cdee-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cdee-138">Description</span></span>    | <span data-ttu-id="7cdee-139">Cadena que contiene el nombre descriptivo (para mostrar) del método de autenticación de EAP.</span><span class="sxs-lookup"><span data-stu-id="7cdee-139">String that contains the friendly (display) name for the EAP authenticator method.</span></span> |



 

## <a name="configclsid"></a><span data-ttu-id="7cdee-140">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="7cdee-140">ConfigCLSID</span></span>



| <span data-ttu-id="7cdee-141">Valor constante</span><span class="sxs-lookup"><span data-stu-id="7cdee-141">Constant Value</span></span> | <span data-ttu-id="7cdee-142">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="7cdee-142">ConfigCLSID</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdee-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cdee-143">Type</span></span>           | <span data-ttu-id="7cdee-144">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7cdee-144">REG\_SZ</span></span>                                                                                                                               |
| <span data-ttu-id="7cdee-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cdee-145">Description</span></span>    | <span data-ttu-id="7cdee-146">Cadena que contiene el GUID de la clase de configuración para este método de autenticación, con el formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="7cdee-146">String that contains the configuration class GUID for this authenticator method, in the format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span></span> |



 

## <a name="properties"></a><span data-ttu-id="7cdee-147">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cdee-147">Properties</span></span>



| <span data-ttu-id="7cdee-148">Valor constante</span><span class="sxs-lookup"><span data-stu-id="7cdee-148">Constant Value</span></span> | <span data-ttu-id="7cdee-149">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cdee-149">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdee-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cdee-150">Type</span></span>           | <span data-ttu-id="7cdee-151">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7cdee-151">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="7cdee-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cdee-152">Description</span></span>    | <span data-ttu-id="7cdee-153">Los bits de la DWORD se establecen para indicar la compatibilidad con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7cdee-153">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="7cdee-154">Para obtener una lista de valores admitidos, consulte [**propiedades del método EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7cdee-154">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="standalonesupported"></a><span data-ttu-id="7cdee-155">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="7cdee-155">StandaloneSupported</span></span>



| <span data-ttu-id="7cdee-156">Valor constante</span><span class="sxs-lookup"><span data-stu-id="7cdee-156">Constant Value</span></span> | <span data-ttu-id="7cdee-157">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="7cdee-157">StandaloneSupported</span></span>                                             |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="7cdee-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cdee-158">Type</span></span>           | <span data-ttu-id="7cdee-159">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7cdee-159">REG\_DWORD</span></span>                                                      |
| <span data-ttu-id="7cdee-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cdee-160">Description</span></span>    | <span data-ttu-id="7cdee-161">0 si se trata de un método de autenticación independiente; 1 si no lo está.</span><span class="sxs-lookup"><span data-stu-id="7cdee-161">0 if this is a standalone authenticator method; 1 if it is not.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7cdee-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7cdee-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cdee-163">Claves del registro del método EAP del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="7cdee-163">EAP Peer Method Registry Keys</span></span>](eap-peer-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="7cdee-164">Configuración del registro para tipos de EAP expandidos</span><span class="sxs-lookup"><span data-stu-id="7cdee-164">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="7cdee-165">Uso de EAPHost</span><span class="sxs-lookup"><span data-stu-id="7cdee-165">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="7cdee-166">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="7cdee-166">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




