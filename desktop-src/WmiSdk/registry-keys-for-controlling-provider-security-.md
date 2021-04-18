---
description: Para mejorar la seguridad del proceso de host de proveedor compartido (wmiprvse.exe) de Instrumental de administración de Windows (WMI), se realizaron cambios en las plataformas de Windows que protegen el proceso de host de proveedor con un identificador de seguridad de servicio (SID).
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Claves y valores del registro para controlar la seguridad del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707275"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a><span data-ttu-id="ad7f1-103">Claves y valores del registro para controlar la seguridad del proveedor</span><span class="sxs-lookup"><span data-stu-id="ad7f1-103">Registry Keys and Values for Controlling Provider Security</span></span>

<span data-ttu-id="ad7f1-104">Para mejorar la seguridad del proceso de host de proveedor compartido (wmiprvse.exe) de Instrumental de administración de Windows (WMI), se realizaron cambios en las plataformas de Windows que protegen el proceso de host de proveedor con un [*identificador de seguridad de servicio (SID)*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-104">To enhance the security of the Windows Management Instrumentation (WMI) shared provider host process (wmiprvse.exe), changes were made to Windows platforms that secure the provider host process with a [*service security identifier (SID)*](gloss-s.md).</span></span> <span data-ttu-id="ad7f1-105">Estos cambios presentan los siguientes modos de ejecución para el host compartido WMI: seguro y compatible.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-105">These changes introduce the following running modes for the WMI shared host: secure and compatible.</span></span>

<span data-ttu-id="ad7f1-106">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="ad7f1-106">The following sections are covered in this topic:</span></span>

-   [<span data-ttu-id="ad7f1-107">Modos seguro y compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-107">Secure and Compatible Modes</span></span>](#secure-and-compatible-modes)
-   [<span data-ttu-id="ad7f1-108">Claves y valores del registro</span><span class="sxs-lookup"><span data-stu-id="ad7f1-108">Registry Keys and Values</span></span>](#registry-keys-and-values)
-   [<span data-ttu-id="ad7f1-109">Configuración de un proveedor para que se ejecute en modo seguro o compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-109">Configuring a Provider to Run in Secure or Compatible Mode</span></span>](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a><span data-ttu-id="ad7f1-110">Modos seguro y compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-110">Secure and Compatible Modes</span></span>

<span data-ttu-id="ad7f1-111">A partir de Windows 7, se agregaron los dos modos de ejecución siguientes para el proceso de host compartido de WMI:</span><span class="sxs-lookup"><span data-stu-id="ad7f1-111">Starting in Windows 7, the following two running modes for the WMI shared host process were added:</span></span>

<dl> <dt>

<span data-ttu-id="ad7f1-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Modo seguro</span><span class="sxs-lookup"><span data-stu-id="ad7f1-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Secure mode</span></span>
</dt> <dd>

<span data-ttu-id="ad7f1-113">Los recursos del proceso de host del proveedor WMI están protegidos con un [*SID de servicio*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-113">WMI provider host process resources are secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="ad7f1-114">Solo el *SID del servicio* tiene permisos para estos recursos.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-114">Only the *service SID* has permissions for these resources.</span></span>

</dd> <dt>

<span data-ttu-id="ad7f1-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Modo compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Compatible mode</span></span>
</dt> <dd>

<span data-ttu-id="ad7f1-116">El proceso de host del proveedor compartido WMI no está protegido con un [*SID de servicio*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-116">The WMI shared provider host process is not secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="ad7f1-117">El proceso de host del proveedor permite el acceso a las cuentas NetworkService o LocalService en función del modelo de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-117">The provider host process allows access to the NetworkService or LocalService accounts depending on the hosting model.</span></span> <span data-ttu-id="ad7f1-118">Para obtener más información sobre los modelos de hospedaje, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-118">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

<span data-ttu-id="ad7f1-119">**Windows Vista y Windows Server 2008:** Para tener acceso a las claves y los valores del registro para controlar los modos seguros y compatibles para el proceso de host del proveedor, debe instalar la actualización de seguridad en [KB 959454](https://support.microsoft.com/kb/959454).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-119">**Windows Vista and Windows Server 2008:** To access the registry keys and values for controlling secure and compatible modes for the provider host process, you must install the security update in [KB 959454](https://support.microsoft.com/kb/959454).</span></span> <span data-ttu-id="ad7f1-120">Para obtener más información, vea el [boletín de seguridad de Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-120">For more information, see the [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span></span>

## <a name="registry-keys-and-values"></a><span data-ttu-id="ad7f1-121">Claves y valores del registro</span><span class="sxs-lookup"><span data-stu-id="ad7f1-121">Registry Keys and Values</span></span>

<span data-ttu-id="ad7f1-122">La configuración de modo seguro y compatible se especifica a través de las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-122">The secure and compatible mode settings are specified through registry keys.</span></span> <span data-ttu-id="ad7f1-123">Las claves del registro para WMI se encuentran en el registro en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="ad7f1-123">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<span data-ttu-id="ad7f1-124">Se han agregado las siguientes claves del registro y el valor **DWORD** descritos en la siguiente lista para controlar el comportamiento de los proveedores WMI.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-124">The following registry keys and **DWORD** value described in the following list were added to control the behavior of WMI providers.</span></span>

<dl> <dt>

<span data-ttu-id="ad7f1-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="ad7f1-126">Esta clave controla el comportamiento de los proveedores individuales.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-126">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="ad7f1-127">Todos los proveedores que se enumeran en esta clave siempre se ejecutan en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-127">All of the providers that are listed in this key always run in secure mode.</span></span> <span data-ttu-id="ad7f1-128">Todos los proveedores de bandeja de entrada que se incluyen con Windows aparecen en esta clave y se ejecutan en modo seguro de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-128">All inbox providers that are shipped with Windows are listed under this key, and are run in secure mode by default.</span></span>

<span data-ttu-id="ad7f1-129">Esta clave tiene prioridad sobre los proveedores enumerados en la clave **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="ad7f1-129">This key takes precedence over providers listed in the **CompatibleHostProviders** key.</span></span>

</dd> <dt>

<span data-ttu-id="ad7f1-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="ad7f1-131">Esta clave controla el comportamiento de los proveedores individuales.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-131">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="ad7f1-132">Todos los proveedores que se enumeran en esta clave siempre se ejecutan en modo compatible.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-132">All providers that are listed in this key always run in compatible mode.</span></span> <span data-ttu-id="ad7f1-133">Esta clave está vacía de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-133">This key is empty by default.</span></span>

<span data-ttu-id="ad7f1-134">Si un proveedor se enumera en la clave **SecuredHostProviders** y en la clave **CompatibleHostProviders** , el proveedor se ejecuta en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-134">If a provider is listed both in the **SecuredHostProviders** key and in the **CompatibleHostProviders** key, the provider is run in secure mode.</span></span>

> [!Note]  
> <span data-ttu-id="ad7f1-135">La clave **CompatibleHostProviders** proporciona compatibilidad de aplicaciones para aplicaciones de terceros si la clave **DefaultSecuredHost** se establece en 1 y se sabe que el proveedor no funciona en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-135">The **CompatibleHostProviders** key provides application compatibility for third-party applications if the **DefaultSecuredHost** key is set to 1 and the provider is known to not function in secure mode.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad7f1-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span></span>
</dt> <dd>

<span data-ttu-id="ad7f1-137">Un valor **DWORD** del registro global que determina si todos los proveedores, que no se enumeran en las claves **SecuredHostProviders** o **CompatibleHostProviders** , se ejecutan en el modo seguro o compatible.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-137">A global registry **DWORD** value that determines whether all of the providers, which are not listed in the **SecuredHostProviders** or **CompatibleHostProviders** keys, are run in the secure or compatible mode.</span></span> <span data-ttu-id="ad7f1-138">Este valor **DWORD** permite al administrador decidir en qué modo debe ejecutarse un proveedor de terceros.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-138">This **DWORD** value lets the administrator decide under which mode a third-party provider must run.</span></span> <span data-ttu-id="ad7f1-139">De forma predeterminada, este valor se establece en cero y todos los proveedores de terceros se ejecutan en modo compatible.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-139">By default, this value is set to zero and all third-party providers are run in compatible mode.</span></span> <span data-ttu-id="ad7f1-140">Los administradores pueden hacer que su equipo sea más seguro de forma predeterminada si se establece el valor de **DefaultSecuredHost** en 1.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-140">Administrators can make their computer more secure by default by setting the **DefaultSecuredHost** value to 1.</span></span>

> [!Note]  
> <span data-ttu-id="ad7f1-141">El valor **DefaultSecuredHost** no afecta a las demás claves del registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-141">The **DefaultSecuredHost** value does not affect the other registry keys.</span></span> <span data-ttu-id="ad7f1-142">Los proveedores que se enumeran en la clave **SecuredHostProviders** permanecen en modo seguro y los que aparecen en la clave **CompatibleHostProviders** permanecen en modo compatible.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-142">The providers that are listed in the **SecuredHostProviders** key remain in secure mode, and the ones that are listed in the **CompatibleHostProviders** key remain in compatible mode.</span></span>

 

<span data-ttu-id="ad7f1-143">Las siguientes opciones son posibles:</span><span class="sxs-lookup"><span data-stu-id="ad7f1-143">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="ad7f1-144"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="ad7f1-144"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="ad7f1-145">Especifica que los proveedores se ejecuten en modo compatible.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-145">Specifies that providers run in compatible mode.</span></span>

</dd> <dt>

<span data-ttu-id="ad7f1-146"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="ad7f1-146"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="ad7f1-147">Especifica que los proveedores se ejecuten en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-147">Specifies that providers run in secure mode.</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="ad7f1-148">En la lista siguiente se enumeran los posibles valores del registro y los modos de ejecución asociados para un proveedor.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-148">The following list lists the possible registry settings and the associated running modes for a provider.</span></span>



| <span data-ttu-id="ad7f1-149">Aparece en SecuredHostProviders</span><span class="sxs-lookup"><span data-stu-id="ad7f1-149">Listed under SecuredHostProviders</span></span> | <span data-ttu-id="ad7f1-150">Aparece en CompatibleHostProviders</span><span class="sxs-lookup"><span data-stu-id="ad7f1-150">Listed under CompatibleHostProviders</span></span> | <span data-ttu-id="ad7f1-151">Configuración de DefaultSecuredHost</span><span class="sxs-lookup"><span data-stu-id="ad7f1-151">DefaultSecuredHost Setting</span></span> | <span data-ttu-id="ad7f1-152">Mode</span><span class="sxs-lookup"><span data-stu-id="ad7f1-152">Mode</span></span>       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| <span data-ttu-id="ad7f1-153">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-153">No</span></span>                                | <span data-ttu-id="ad7f1-154">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-154">No</span></span>                                   | <span data-ttu-id="ad7f1-155">0</span><span class="sxs-lookup"><span data-stu-id="ad7f1-155">0</span></span>                          | <span data-ttu-id="ad7f1-156">Compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-156">Compatible</span></span> |
| <span data-ttu-id="ad7f1-157">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-157">No</span></span>                                | <span data-ttu-id="ad7f1-158">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-158">Yes</span></span>                                  | <span data-ttu-id="ad7f1-159">0</span><span class="sxs-lookup"><span data-stu-id="ad7f1-159">0</span></span>                          | <span data-ttu-id="ad7f1-160">Compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-160">Compatible</span></span> |
| <span data-ttu-id="ad7f1-161">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-161">Yes</span></span>                               | <span data-ttu-id="ad7f1-162">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-162">No</span></span>                                   | <span data-ttu-id="ad7f1-163">0</span><span class="sxs-lookup"><span data-stu-id="ad7f1-163">0</span></span>                          | <span data-ttu-id="ad7f1-164">Seguridad</span><span class="sxs-lookup"><span data-stu-id="ad7f1-164">Secure</span></span>     |
| <span data-ttu-id="ad7f1-165">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-165">Yes</span></span>                               | <span data-ttu-id="ad7f1-166">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-166">Yes</span></span>                                  | <span data-ttu-id="ad7f1-167">0</span><span class="sxs-lookup"><span data-stu-id="ad7f1-167">0</span></span>                          | <span data-ttu-id="ad7f1-168">Seguridad</span><span class="sxs-lookup"><span data-stu-id="ad7f1-168">Secure</span></span>     |
| <span data-ttu-id="ad7f1-169">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-169">No</span></span>                                | <span data-ttu-id="ad7f1-170">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-170">No</span></span>                                   | <span data-ttu-id="ad7f1-171">1</span><span class="sxs-lookup"><span data-stu-id="ad7f1-171">1</span></span>                          | <span data-ttu-id="ad7f1-172">Seguridad</span><span class="sxs-lookup"><span data-stu-id="ad7f1-172">Secure</span></span>     |
| <span data-ttu-id="ad7f1-173">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-173">No</span></span>                                | <span data-ttu-id="ad7f1-174">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-174">Yes</span></span>                                  | <span data-ttu-id="ad7f1-175">1</span><span class="sxs-lookup"><span data-stu-id="ad7f1-175">1</span></span>                          | <span data-ttu-id="ad7f1-176">Compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-176">Compatible</span></span> |
| <span data-ttu-id="ad7f1-177">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-177">Yes</span></span>                               | <span data-ttu-id="ad7f1-178">No</span><span class="sxs-lookup"><span data-stu-id="ad7f1-178">No</span></span>                                   | <span data-ttu-id="ad7f1-179">1</span><span class="sxs-lookup"><span data-stu-id="ad7f1-179">1</span></span>                          | <span data-ttu-id="ad7f1-180">Seguridad</span><span class="sxs-lookup"><span data-stu-id="ad7f1-180">Secure</span></span>     |
| <span data-ttu-id="ad7f1-181">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-181">Yes</span></span>                               | <span data-ttu-id="ad7f1-182">Sí</span><span class="sxs-lookup"><span data-stu-id="ad7f1-182">Yes</span></span>                                  | <span data-ttu-id="ad7f1-183">1</span><span class="sxs-lookup"><span data-stu-id="ad7f1-183">1</span></span>                          | <span data-ttu-id="ad7f1-184">Seguridad</span><span class="sxs-lookup"><span data-stu-id="ad7f1-184">Secure</span></span>     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a><span data-ttu-id="ad7f1-185">Configuración de un proveedor para que se ejecute en modo seguro o compatible</span><span class="sxs-lookup"><span data-stu-id="ad7f1-185">Configuring a Provider to Run in Secure or Compatible Mode</span></span>

<span data-ttu-id="ad7f1-186">Las claves del registro se pueden modificar mediante el Consola de administración de directivas de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-186">The registry keys can be modified using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="ad7f1-187">Para obtener más información, vea [consola de administración de directivas de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-187">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="ad7f1-188">En los procedimientos siguientes se muestra cómo administrar la configuración de modo seguro y compatible mediante preferencias de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-188">The following procedures illustrate how to manage secure and compatible mode settings by using group policy preferences.</span></span> <span data-ttu-id="ad7f1-189">Para obtener más información sobre las preferencias de directiva de grupo, consulte la [información general sobre las preferencias de directiva de grupo](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-189">For more information about group policy preferences, see the [Group Policy Preferences Overview](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span></span>

<span data-ttu-id="ad7f1-190">**Para agregar un proveedor al modo seguro o compatible mediante el uso de directiva de grupo**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-190">**To add a provider to either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="ad7f1-191">Abra GPMC.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-191">Open the GPMC.</span></span>
2.  <span data-ttu-id="ad7f1-192">Cree un objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="ad7f1-192">Create a Group Policy Object (GPO).</span></span>
3.  <span data-ttu-id="ad7f1-193">Edite el GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-193">Edit the GPO.</span></span>
4.  <span data-ttu-id="ad7f1-194">Vaya a preferencias/configuración de Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-194">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="ad7f1-195">Haga clic con el botón derecho y seleccione **nuevo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-195">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="ad7f1-196">Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-196">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="ad7f1-197">Seleccione el comando **crear** .</span><span class="sxs-lookup"><span data-stu-id="ad7f1-197">Select the **Create** command.</span></span>
7.  <span data-ttu-id="ad7f1-198">Seleccione la siguiente ruta de acceso de clave del registro:</span><span class="sxs-lookup"><span data-stu-id="ad7f1-198">Select the following registry key path:</span></span>

    <span data-ttu-id="ad7f1-199">**Modo seguro: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-199">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="ad7f1-200">**Modo compatible: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-200">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="ad7f1-201">En el campo **nombre** , escriba el nombre del proveedor que desea agregar a esta clave.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-201">In the **name** field, enter the name of the provider you want to add to this key.</span></span> <span data-ttu-id="ad7f1-202">El nombre del proveedor debe tener el formato siguiente: <namespace> : <\_ \_ RELPATH>.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-202">The provider name must be in the following format: <namespace>:<\_\_RELPATH>.</span></span> <span data-ttu-id="ad7f1-203">Por ejemplo, la raíz \\ cimv2: \_ \_ win32provider. Name = "DataProvider".</span><span class="sxs-lookup"><span data-stu-id="ad7f1-203">For example, root\\cimv2:\_\_win32provider.name="MyProvider".</span></span>
9.  <span data-ttu-id="ad7f1-204">En el campo de **datos** , escriba 0.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-204">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="ad7f1-205">Haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-205">Click OK.</span></span>

<span data-ttu-id="ad7f1-206">**Para quitar un proveedor del modo seguro o compatible mediante directiva de grupo**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-206">**To remove a provider from either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="ad7f1-207">Abra GPMC.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-207">Open the GPMC.</span></span>
2.  <span data-ttu-id="ad7f1-208">Cree un GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-208">Create a GPO.</span></span>
3.  <span data-ttu-id="ad7f1-209">Edite el GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-209">Edit the GPO.</span></span>
4.  <span data-ttu-id="ad7f1-210">Vaya a preferencias/configuración de Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-210">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="ad7f1-211">Haga clic con el botón derecho y seleccione **nuevo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-211">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="ad7f1-212">Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-212">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="ad7f1-213">Seleccione el comando **quitar** .</span><span class="sxs-lookup"><span data-stu-id="ad7f1-213">Select the **Remove** command.</span></span>
7.  <span data-ttu-id="ad7f1-214">Seleccione la siguiente ruta de acceso de clave del registro:</span><span class="sxs-lookup"><span data-stu-id="ad7f1-214">Select the following registry key path:</span></span>

    <span data-ttu-id="ad7f1-215">**Modo seguro: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-215">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="ad7f1-216">**Modo compatible: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-216">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="ad7f1-217">En el campo **nombre** , escriba el nombre del proveedor que desea quitar de esta clave.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-217">In the **name** field, enter the name of the provider you want to remove from this key.</span></span>
9.  <span data-ttu-id="ad7f1-218">En el campo de **datos** , escriba 0.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-218">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="ad7f1-219">Haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-219">Click OK.</span></span>

<span data-ttu-id="ad7f1-220">En el procedimiento siguiente se proporcionan detalles sobre cómo modificar el comportamiento de los proveedores que no se enumeran en las claves **SecuredHostProviders** o **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="ad7f1-220">The following procedure provides details about how to modify the behavior of providers that are not listed in either the **SecuredHostProviders** or **CompatibleHostProviders** keys.</span></span>

<span data-ttu-id="ad7f1-221">**Para cambiar el valor predeterminado de la clave DefaultSecuredHost mediante directiva de grupo**</span><span class="sxs-lookup"><span data-stu-id="ad7f1-221">**To change the default value of the DefaultSecuredHost key by using Group Policy**</span></span>

1.  <span data-ttu-id="ad7f1-222">Abra GPMC.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-222">Open the GPMC.</span></span>
2.  <span data-ttu-id="ad7f1-223">Cree un GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-223">Create a GPO.</span></span>
3.  <span data-ttu-id="ad7f1-224">Edite el GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-224">Edit the GPO.</span></span>
4.  <span data-ttu-id="ad7f1-225">Vaya a preferencias/configuración de Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-225">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="ad7f1-226">Haga clic con el botón derecho y seleccione **nuevo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-226">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="ad7f1-227">Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-227">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="ad7f1-228">Seleccione el comando de **actualización** .</span><span class="sxs-lookup"><span data-stu-id="ad7f1-228">Select the **Update** command.</span></span>
7.  <span data-ttu-id="ad7f1-229">Seleccione la siguiente ruta de acceso de clave del registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-229">Select the following registry key path: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**.</span></span>
8.  <span data-ttu-id="ad7f1-230">En el campo **nombre** , escriba **DefaultSecuredHost**.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-230">In the **name** field, enter **DefaultSecuredHost**.</span></span>
9.  <span data-ttu-id="ad7f1-231">En el campo de **datos** , escriba 0 para el modo compatible o 1 para el modo seguro.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-231">In the **data** field, enter 0 for compatible mode or 1 for secure mode.</span></span>
10. <span data-ttu-id="ad7f1-232">Haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="ad7f1-232">Click OK.</span></span>

 

 
