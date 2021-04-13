---
title: Valores del registro del método EAP peer
description: Obtenga información sobre los valores de registro específicos necesarios para los métodos de EAP del mismo nivel. Vea una lista de valores del registro y vea los recursos adicionales disponibles.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359426"
---
# <a name="eap-peer-method-registry-values"></a><span data-ttu-id="24c9b-104">Valores del registro del método EAP peer</span><span class="sxs-lookup"><span data-stu-id="24c9b-104">EAP Peer Method Registry Values</span></span>

<span data-ttu-id="24c9b-105">Se requieren valores de registro específicos para los métodos EAP del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="24c9b-105">Specific registry values are required for EAP peer methods.</span></span>

## <a name="eap-peer-method-dll-paths"></a><span data-ttu-id="24c9b-106">Rutas de acceso DLL del método EAP del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="24c9b-106">EAP Peer Method DLL Paths</span></span>

<span data-ttu-id="24c9b-107">La ruta de acceso siguiente especifica la ubicación del registro para los archivos dll normales del método EAP del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="24c9b-107">The following path specifies the registry location for regular EAP peer method DLLs.</span></span>

<span data-ttu-id="24c9b-108">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="24c9b-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="24c9b-109">Por ejemplo, una ruta de acceso de registro de instalación de método EAP dada una **AuthorId** de "311" (que indica que "Microsoft" es el autor) y un **EapTypeId** de "40", aparece de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="24c9b-109">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="24c9b-110">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="24c9b-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="24c9b-111">La ruta de acceso siguiente especifica la ubicación del registro para los archivos DLL del método EAP extendido.</span><span class="sxs-lookup"><span data-stu-id="24c9b-111">The following path specifies the registry location for extended EAP method DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="24c9b-112">Los archivos dll de método EAP extendido se admiten en Windows Vista con Service Pack 1 (SP1) o posterior.</span><span class="sxs-lookup"><span data-stu-id="24c9b-112">Extended EAP method DLLs are supported in Windows Vista with Service Pack 1 (SP1) or later.</span></span>

 

<span data-ttu-id="24c9b-113">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="24c9b-113">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="24c9b-114">Por ejemplo, una ruta de acceso de registro de instalación de método EAP dada una **AuthorId** de "311" (que indica que "Microsoft" es el autor), un **VendorId** de "311" y un valor de **EapTypeId** de "40", aparece de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="24c9b-114">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="24c9b-115">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="24c9b-115">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="24c9b-116">Para obtener más información sobre la asignación de tipos de método EAP, consulte la sección 6,2 de [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="24c9b-116">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="24c9b-117">Valores del registro</span><span class="sxs-lookup"><span data-stu-id="24c9b-117">Registry Values</span></span>

<span data-ttu-id="24c9b-118">Se requieren los siguientes valores del registro de método del mismo nivel de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="24c9b-118">The following EAPHost peer method registry values are required.</span></span>

-   [<span data-ttu-id="24c9b-119">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-119">PeerDllPath</span></span>](#peerdllpath)
-   [<span data-ttu-id="24c9b-120">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="24c9b-120">PeerFriendlyName</span></span>](#peerfriendlyname)
-   [<span data-ttu-id="24c9b-121">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="24c9b-121">PeerInvokePasswordDialog</span></span>](#peerinvokepassworddialog)
-   [<span data-ttu-id="24c9b-122">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="24c9b-122">PeerInvokeUsernameDialog</span></span>](#peerinvokeusernamedialog)

<span data-ttu-id="24c9b-123">Se recomiendan los siguientes valores del registro del método AP peer.</span><span class="sxs-lookup"><span data-stu-id="24c9b-123">The following AP peer method registry values are recommended.</span></span>

-   [<span data-ttu-id="24c9b-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24c9b-124">Properties</span></span>](#properties)

<span data-ttu-id="24c9b-125">Los siguientes valores del registro del método AP del mismo nivel son opcionales.</span><span class="sxs-lookup"><span data-stu-id="24c9b-125">The following AP peer method registry values are optional.</span></span>

-   [<span data-ttu-id="24c9b-126">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-126">PeerConfigUIPath</span></span>](#peerconfiguipath)
-   [<span data-ttu-id="24c9b-127">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-127">PeerIdentityPath</span></span>](#peeridentitypath)
-   [<span data-ttu-id="24c9b-128">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-128">PeerInteractiveUIPath</span></span>](#peerinteractiveuipath)
-   [<span data-ttu-id="24c9b-129">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="24c9b-129">PeerRequireConfigUI</span></span>](#peerrequireconfigui)

### <a name="peerconfiguipath"></a><span data-ttu-id="24c9b-130">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-130">PeerConfigUIPath</span></span>



| <span data-ttu-id="24c9b-131">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-131">Constant Value</span></span> | <span data-ttu-id="24c9b-132">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-132">PeerConfigUIPath</span></span>                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9b-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-133">Type</span></span>           | <span data-ttu-id="24c9b-134">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="24c9b-134">REG\_EXPAND\_SZ</span></span>                                                                                                                                        |
| <span data-ttu-id="24c9b-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-135">Description</span></span>    | <span data-ttu-id="24c9b-136">La ruta de acceso al archivo DLL que contiene la implementación del cuadro de diálogo de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="24c9b-136">The path to the DLL that contains the implementation of the user configuration dialog.</span></span> <span data-ttu-id="24c9b-137">Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="24c9b-137">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerdllpath"></a><span data-ttu-id="24c9b-138">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-138">PeerDllPath</span></span>



| <span data-ttu-id="24c9b-139">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-139">Constant Value</span></span> | <span data-ttu-id="24c9b-140">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-140">PeerDllPath</span></span>                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9b-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-141">Type</span></span>           | <span data-ttu-id="24c9b-142">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="24c9b-142">REG\_EXPAND\_SZ</span></span>                                                                                 |
| <span data-ttu-id="24c9b-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-143">Description</span></span>    | <span data-ttu-id="24c9b-144">Ruta de acceso al archivo DLL del método EAP.</span><span class="sxs-lookup"><span data-stu-id="24c9b-144">The path to the EAP method DLL.</span></span> <span data-ttu-id="24c9b-145">Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="24c9b-145">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerfriendlyname"></a><span data-ttu-id="24c9b-146">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="24c9b-146">PeerFriendlyName</span></span>



| <span data-ttu-id="24c9b-147">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-147">Constant Value</span></span> | <span data-ttu-id="24c9b-148">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="24c9b-148">PeerFriendlyName</span></span>                                                     |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="24c9b-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-149">Type</span></span>           | <span data-ttu-id="24c9b-150">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="24c9b-150">REG\_SZ</span></span>                                                              |
| <span data-ttu-id="24c9b-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-151">Description</span></span>    | <span data-ttu-id="24c9b-152">Cadena que contiene el nombre descriptivo (para mostrar) del método EAP.</span><span class="sxs-lookup"><span data-stu-id="24c9b-152">String that contains the friendly (display) name for the EAP method.</span></span> |



 

### <a name="peeridentitypath"></a><span data-ttu-id="24c9b-153">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-153">PeerIdentityPath</span></span>



| <span data-ttu-id="24c9b-154">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-154">Constant Value</span></span> | <span data-ttu-id="24c9b-155">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-155">PeerIdentityPath</span></span>                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9b-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-156">Type</span></span>           | <span data-ttu-id="24c9b-157">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="24c9b-157">REG\_EXPAND\_SZ</span></span>                                                                                                                                      |
| <span data-ttu-id="24c9b-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-158">Description</span></span>    | <span data-ttu-id="24c9b-159">La ruta de acceso al archivo DLL que contiene la implementación de las funciones de identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="24c9b-159">The path to the DLL that contains the implementation of the user identity functions.</span></span> <span data-ttu-id="24c9b-160">Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="24c9b-160">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinteractiveuipath"></a><span data-ttu-id="24c9b-161">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-161">PeerInteractiveUIPath</span></span>



| <span data-ttu-id="24c9b-162">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-162">Constant Value</span></span> | <span data-ttu-id="24c9b-163">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="24c9b-163">PeerInteractiveUIPath</span></span>                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9b-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-164">Type</span></span>           | <span data-ttu-id="24c9b-165">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="24c9b-165">REG\_EXPAND\_SZ</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="24c9b-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-166">Description</span></span>    | <span data-ttu-id="24c9b-167">La ruta de acceso al archivo DLL que contiene la implementación de la interfaz de usuario interactiva utilizada para obtener información de usuario durante la ejecución del método EAP.</span><span class="sxs-lookup"><span data-stu-id="24c9b-167">The path to the DLL that contains the implementation of the interactive user interface used to obtain user information during execution of the EAP method.</span></span> <span data-ttu-id="24c9b-168">Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="24c9b-168">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinvokepassworddialog"></a><span data-ttu-id="24c9b-169">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="24c9b-169">PeerInvokePasswordDialog</span></span>



| <span data-ttu-id="24c9b-170">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-170">Constant Value</span></span> | <span data-ttu-id="24c9b-171">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="24c9b-171">PeerInvokePasswordDialog</span></span>                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9b-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-172">Type</span></span>           | <span data-ttu-id="24c9b-173">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="24c9b-173">REG\_DWORD</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="24c9b-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-174">Description</span></span>    | <span data-ttu-id="24c9b-175">1: para obtener credenciales mediante el cuadro de diálogo contraseña y dominio de EAPHost genérico.</span><span class="sxs-lookup"><span data-stu-id="24c9b-175">1- to get credentials using the generic EAPHost password and domain dialog box.</span></span> <span data-ttu-id="24c9b-176">0: para usar un cuadro de diálogo personalizado.</span><span class="sxs-lookup"><span data-stu-id="24c9b-176">0 - to use a custom dialog box.</span></span> <span data-ttu-id="24c9b-177">Si se usa el cuadro de diálogo genérico, el método [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) establece las credenciales.</span><span class="sxs-lookup"><span data-stu-id="24c9b-177">If the generic dialog box is used, credentials are set by the [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span> |



 

### <a name="peerinvokeusernamedialog"></a><span data-ttu-id="24c9b-178">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="24c9b-178">PeerInvokeUsernameDialog</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24c9b-179">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-179">Constant Value</span></span></th>
<th><span data-ttu-id="24c9b-180">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="24c9b-180">PeerInvokeUsernameDialog</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24c9b-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-181">Type</span></span></td>
<td><span data-ttu-id="24c9b-182">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="24c9b-182">REG_DWORD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c9b-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-183">Description</span></span></td>
<td><ul>
<li><span data-ttu-id="24c9b-184">1: para obtener credenciales mediante el cuadro de diálogo nombre de usuario de EAPHost genérico.</span><span class="sxs-lookup"><span data-stu-id="24c9b-184">1 - to get credentials using the generic EAPHost user name dialog box.</span></span></li>
<li><span data-ttu-id="24c9b-185">0: para usar un cuadro de diálogo personalizado.</span><span class="sxs-lookup"><span data-stu-id="24c9b-185">0- to use a custom dialog box.</span></span></li>
</ul>
<span data-ttu-id="24c9b-186">Si se usa el cuadro de diálogo genérico, el método [<strong>EapPeerSetCredentials</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials) establece las credenciales.</span><span class="sxs-lookup"><span data-stu-id="24c9b-186">If the generic dialog box is used, credentials are set by the [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a><span data-ttu-id="24c9b-187">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="24c9b-187">PeerRequireConfigUI</span></span>



| <span data-ttu-id="24c9b-188">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-188">Constant Value</span></span> | <span data-ttu-id="24c9b-189">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="24c9b-189">PeerRequireConfigUI</span></span>                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9b-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-190">Type</span></span>           | <span data-ttu-id="24c9b-191">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="24c9b-191">REG\_DWORD</span></span>                                                                                 |
| <span data-ttu-id="24c9b-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-192">Description</span></span>    | <span data-ttu-id="24c9b-193">0 si se implementa un cuadro de diálogo de interfaz de usuario de configuración para este método; 1 si no lo está.</span><span class="sxs-lookup"><span data-stu-id="24c9b-193">0 if a configuration user interface dialog is implemented for this method; 1 if it is not.</span></span> |



 

### <a name="properties"></a><span data-ttu-id="24c9b-194">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24c9b-194">Properties</span></span>



| <span data-ttu-id="24c9b-195">Valor constante</span><span class="sxs-lookup"><span data-stu-id="24c9b-195">Constant Value</span></span> | <span data-ttu-id="24c9b-196">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24c9b-196">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9b-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="24c9b-197">Type</span></span>           | <span data-ttu-id="24c9b-198">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="24c9b-198">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="24c9b-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="24c9b-199">Description</span></span>    | <span data-ttu-id="24c9b-200">Los bits de la DWORD se establecen para indicar la compatibilidad con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="24c9b-200">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="24c9b-201">Para obtener una lista de valores admitidos, consulte [**propiedades del método EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="24c9b-201">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="24c9b-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24c9b-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c9b-203">Claves del registro del método de autenticación de EAP</span><span class="sxs-lookup"><span data-stu-id="24c9b-203">EAP Authenticator Method Registry Keys</span></span>](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="24c9b-204">Configuración del registro para tipos de EAP expandidos</span><span class="sxs-lookup"><span data-stu-id="24c9b-204">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="24c9b-205">Uso de EAPHost</span><span class="sxs-lookup"><span data-stu-id="24c9b-205">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="24c9b-206">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="24c9b-206">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 