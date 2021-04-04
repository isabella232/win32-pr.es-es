---
title: Valores de registro del Protocolo de autenticación
description: El software de instalación de la DLL EAP puede crear los siguientes valores del registro bajo eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104077162"
---
# <a name="authentication-protocol-registry-values"></a><span data-ttu-id="eb5e8-119">Valores de registro del Protocolo de autenticación</span><span class="sxs-lookup"><span data-stu-id="eb5e8-119">Authentication Protocol Registry Values</span></span>

<span data-ttu-id="eb5e8-120">El software de instalación de la DLL EAP puede crear los siguientes valores del registro bajo **&lt; eaptypeid &gt;**.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-120">The setup software for the EAP DLL may create the following registry values below **&lt;eaptypeid&gt;**.</span></span> <span data-ttu-id="eb5e8-121">Estos valores del registro se definen en el archivo de encabezado Raseapif. h.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-121">These registry values are defined in the Raseapif.h header file.</span></span> <span data-ttu-id="eb5e8-122">Los valores **RAS_EAP_VALUENAME_PATH** y **RAS_EAP_VALUENAME_FRIENDLY_NAME** son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-122">The **RAS_EAP_VALUENAME_PATH** and **RAS_EAP_VALUENAME_FRIENDLY_NAME** values are required.</span></span> <span data-ttu-id="eb5e8-123">El software de instalación también puede crear otras claves y valores.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-123">The setup software may create other keys and values as well.</span></span> <span data-ttu-id="eb5e8-124">Estos podrían ser usados por el propio protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-124">These could be used by the authentication protocol itself.</span></span> <span data-ttu-id="eb5e8-125">Para obtener más información y un ejemplo de la configuración del registro, consulte [ejemplo de valores del registro](registry-values-example.md).</span><span class="sxs-lookup"><span data-stu-id="eb5e8-125">For more information and an example of registry configuration, see [Registry Values Example](registry-values-example.md).</span></span>

[<span data-ttu-id="eb5e8-126">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="eb5e8-126">RAS_EAP_VALUENAME_PATH</span></span>](#ras_eap_valuename_path)

[<span data-ttu-id="eb5e8-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="eb5e8-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>](#ras_eap_valuename_friendly_name)

[<span data-ttu-id="eb5e8-128">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="eb5e8-128">RAS_EAP_VALUENAME_CONFIGUI</span></span>](#ras_eap_valuename_configui)

[<span data-ttu-id="eb5e8-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="eb5e8-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>](#ras_eap_valuename_default_data)

[<span data-ttu-id="eb5e8-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="eb5e8-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>](#ras_eap_valuename_require_configui)

[<span data-ttu-id="eb5e8-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="eb5e8-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>](#ras_eap_valuename_config_clsid)

[<span data-ttu-id="eb5e8-132">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="eb5e8-132">RAS_EAP_VALUENAME_IDENTITY</span></span>](#ras_eap_valuename_identity)

<span data-ttu-id="eb5e8-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Configur</span><span class="sxs-lookup"><span data-stu-id="eb5e8-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)I</span></span>

[<span data-ttu-id="eb5e8-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="eb5e8-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>](#ras_eap_valuename_invoke_namedlg)

[<span data-ttu-id="eb5e8-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="eb5e8-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>](#ras_eap_valuename_invoke_pwddlg)

[<span data-ttu-id="eb5e8-136">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="eb5e8-136">RAS_EAP_VALUENAME_ENCRYPTION</span></span>](#ras_eap_valuename_encryption)

[<span data-ttu-id="eb5e8-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="eb5e8-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>](#ras_eap_valuename_standalone_supported)

[<span data-ttu-id="eb5e8-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="eb5e8-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>](#ras_eap_valuename_roles_supported)

[<span data-ttu-id="eb5e8-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="eb5e8-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>](#ras_eap_valuename_per_policy_config)

[<span data-ttu-id="eb5e8-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>](#ras_eap_valuename_istunnel_method)

[<span data-ttu-id="eb5e8-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="eb5e8-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a><span data-ttu-id="eb5e8-142">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="eb5e8-142">RAS_EAP_VALUENAME_PATH</span></span>

| <span data-ttu-id="eb5e8-143">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-143">Constant value</span></span> | <span data-ttu-id="eb5e8-144">Path</span><span class="sxs-lookup"><span data-stu-id="eb5e8-144">Path</span></span>                               |
|----------------|------------------------------------|
| <span data-ttu-id="eb5e8-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-145">Type</span></span>           | <span data-ttu-id="eb5e8-146"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="eb5e8-146">REG_EXPAND_SZ</span></span>                    |
| <span data-ttu-id="eb5e8-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-147">Description</span></span>    | <span data-ttu-id="eb5e8-148">Especifica la ruta de acceso al archivo DLL de EAP.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-148">Specifies the path to the EAP DLL.</span></span> |

## <a name="ras_eap_valuename_friendly_name"></a><span data-ttu-id="eb5e8-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="eb5e8-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>

| <span data-ttu-id="eb5e8-150">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-150">Constant value</span></span> | <span data-ttu-id="eb5e8-151">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="eb5e8-151">FriendlyName</span></span>                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-152">Type</span></span>           | <span data-ttu-id="eb5e8-153">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="eb5e8-153">REG_SZ</span></span>                                                                                                                                                           |
| <span data-ttu-id="eb5e8-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-154">Description</span></span>    | <span data-ttu-id="eb5e8-155">Especifica un nombre descriptivo para el protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-155">Specifies a friendly name for the authentication protocol.</span></span> <span data-ttu-id="eb5e8-156">Este nombre aparece en la interfaz de usuario de la aplicación EAP para implementaciones de acceso telefónico e inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-156">This name appears in the EAP application user interface for both dial-up and wireless implementations.</span></span> |

## <a name="ras_eap_valuename_configui"></a><span data-ttu-id="eb5e8-157">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="eb5e8-157">RAS_EAP_VALUENAME_CONFIGUI</span></span>

| <span data-ttu-id="eb5e8-158">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-158">Constant value</span></span> | <span data-ttu-id="eb5e8-159">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="eb5e8-159">ConfigUIPath</span></span>                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-160">Type</span></span>           | <span data-ttu-id="eb5e8-161"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="eb5e8-161">REG_EXPAND_SZ</span></span>                                                                                                                   |
| <span data-ttu-id="eb5e8-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-162">Description</span></span>    | <span data-ttu-id="eb5e8-163">Especifica la ruta de acceso al archivo DLL que implementa la interfaz de usuario de configuración en el cliente, ya que esta interfaz de usuario es solo para el cliente.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-163">Specifies the path to the DLL that implements the configuration user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_default_data"></a><span data-ttu-id="eb5e8-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="eb5e8-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>

| <span data-ttu-id="eb5e8-165">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-165">Constant value</span></span> | <span data-ttu-id="eb5e8-166">ConfigData</span><span class="sxs-lookup"><span data-stu-id="eb5e8-166">ConfigData</span></span>                                                            |
|----------------|-----------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-167">Type</span></span>           | <span data-ttu-id="eb5e8-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="eb5e8-168">REG_BINARY</span></span>                                                           |
| <span data-ttu-id="eb5e8-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-169">Description</span></span>    | <span data-ttu-id="eb5e8-170">Especifica los datos de configuración predeterminados para el protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-170">Specifies default configuration data for the authentication protocol.</span></span> |

## <a name="ras_eap_valuename_require_configui"></a><span data-ttu-id="eb5e8-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="eb5e8-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>

| <span data-ttu-id="eb5e8-172">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-172">Constant value</span></span> | <span data-ttu-id="eb5e8-173">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="eb5e8-173">RequireConfigUI</span></span>                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-174">Type</span></span>           | <span data-ttu-id="eb5e8-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-175">REG_DWORD</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="eb5e8-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-176">Description</span></span>    | <span data-ttu-id="eb5e8-177">Especifica si el usuario debe proporcionar datos de configuración en la interfaz de usuario de la aplicación cliente EAP.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-177">Specifies whether the user must provide configuration data in the EAP client application user interface.</span></span> <span data-ttu-id="eb5e8-178">Si este valor es 1, no se permite que el usuario salga de la interfaz de usuario de la aplicación cliente EAP sin proporcionar datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-178">If this value is 1, the user is not allowed to exit the EAP client application UI without providing configuration data.</span></span> <span data-ttu-id="eb5e8-179">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-179">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_config_clsid"></a><span data-ttu-id="eb5e8-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="eb5e8-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>

| <span data-ttu-id="eb5e8-181">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-181">Constant value</span></span> | <span data-ttu-id="eb5e8-182">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="eb5e8-182">ConfigCLSID</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="eb5e8-183">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-183">Type</span></span>           | <span data-ttu-id="eb5e8-184">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="eb5e8-184">REG_SZ</span></span>                                                       |
| <span data-ttu-id="eb5e8-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-185">Description</span></span>    | <span data-ttu-id="eb5e8-186">Especifica el ID. de clase de la interfaz de usuario de configuración en el servidor.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-186">Specifies the class ID of the configuration UI on the server.</span></span> |

## <a name="ras_eap_valuename_identity"></a><span data-ttu-id="eb5e8-187">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="eb5e8-187">RAS_EAP_VALUENAME_IDENTITY</span></span>

| <span data-ttu-id="eb5e8-188">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-188">Constant value</span></span> | <span data-ttu-id="eb5e8-189">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="eb5e8-189">IdentityPath</span></span>                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-190">Type</span></span>           | <span data-ttu-id="eb5e8-191"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="eb5e8-191">REG_EXPAND_SZ</span></span>                                                                                                                        |
| <span data-ttu-id="eb5e8-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-192">Description</span></span>    | <span data-ttu-id="eb5e8-193">Especifica la ruta de acceso al archivo DLL que implementa funciones para obtener la identidad del usuario en el cliente, ya que esta interfaz de usuario es solo para el cliente.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-193">Specifies the path to the DLL that implements functions to obtain the user identity on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_interactiveui"></a><span data-ttu-id="eb5e8-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span><span class="sxs-lookup"><span data-stu-id="eb5e8-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span></span>

| <span data-ttu-id="eb5e8-195">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-195">Constant value</span></span> | <span data-ttu-id="eb5e8-196">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="eb5e8-196">InteractiveUIPath</span></span>                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-197">Type</span></span>           | <span data-ttu-id="eb5e8-198"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="eb5e8-198">REG_EXPAND_SZ</span></span>                                                                                                                 |
| <span data-ttu-id="eb5e8-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-199">Description</span></span>    | <span data-ttu-id="eb5e8-200">Especifica la ruta de acceso al archivo DLL que implementa la interfaz de usuario interactiva en el cliente, ya que esta interfaz de usuario es solo para el cliente.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-200">Specifies the path to the DLL that implements the interactive user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_invoke_namedlg"></a><span data-ttu-id="eb5e8-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="eb5e8-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>

| <span data-ttu-id="eb5e8-202">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-202">Constant value</span></span> | <span data-ttu-id="eb5e8-203">InvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="eb5e8-203">InvokeUsernameDialog</span></span>                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-204">Type</span></span>           | <span data-ttu-id="eb5e8-205">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-205">REG_DWORD</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="eb5e8-206">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-206">Description</span></span>    | <span data-ttu-id="eb5e8-207">Especifica si RAS debe mostrar el cuadro de diálogo de nombre de usuario estándar de Windows NT/Windows 2000 (valor 1) o invocar [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valor 0).</span><span class="sxs-lookup"><span data-stu-id="eb5e8-207">Specifies whether RAS should display the standard Windows NT/Windows 2000 user name dialog (value of 1) or invoke [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (value of 0).</span></span> <span data-ttu-id="eb5e8-208">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-208">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_invoke_pwddlg"></a><span data-ttu-id="eb5e8-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="eb5e8-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>

| <span data-ttu-id="eb5e8-210">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-210">Constant value</span></span> | <span data-ttu-id="eb5e8-211">InvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="eb5e8-211">InvokePasswordDialog</span></span>                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-212">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-212">Type</span></span>           | <span data-ttu-id="eb5e8-213">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-213">REG_DWORD</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="eb5e8-214">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-214">Description</span></span>    | <span data-ttu-id="eb5e8-215">Especifica si RAS debe mostrar el cuadro de diálogo de contraseña estándar de Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-215">Specifies whether RAS should display the standard Windows NT/Windows 2000 password dialog.</span></span> <span data-ttu-id="eb5e8-216">Si este valor existe y es 0, RAS no mostrará el cuadro de diálogo de contraseña.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-216">If this value exists and is 0, RAS will not display the password dialog.</span></span> <span data-ttu-id="eb5e8-217">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-217">The default value is 1.</span></span> |


## <a name="ras_eap_valuename_encryption"></a><span data-ttu-id="eb5e8-218">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="eb5e8-218">RAS_EAP_VALUENAME_ENCRYPTION</span></span>

| <span data-ttu-id="eb5e8-219">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-219">Constant value</span></span> | <span data-ttu-id="eb5e8-220">MPPEEncryptionSupported</span><span class="sxs-lookup"><span data-stu-id="eb5e8-220">MPPEEncryptionSupported</span></span>                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-221">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-221">Type</span></span>           | <span data-ttu-id="eb5e8-222">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-222">REG_DWORD</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="eb5e8-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-223">Description</span></span>    | <span data-ttu-id="eb5e8-224">Si este valor es 1, el protocolo de autenticación puede generar claves para el estilo de cifrado punto a punto de Microsoft (MPPE) del cifrado.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-224">If this value is 1, the authentication protocol can generate keys for the Microsoft Point-to-Point Encryption (MPPE) style of encryption.</span></span> <span data-ttu-id="eb5e8-225">Los valores posibles son 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-225">Possible values are 0 or 1.</span></span> <span data-ttu-id="eb5e8-226">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-226">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_standalone_supported"></a><span data-ttu-id="eb5e8-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="eb5e8-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>

| <span data-ttu-id="eb5e8-228">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-228">Constant value</span></span> | <span data-ttu-id="eb5e8-229">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="eb5e8-229">StandaloneSupported</span></span>                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-230">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-230">Type</span></span>           | <span data-ttu-id="eb5e8-231">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-231">REG_DWORD</span></span>                                                                                                                                                                     |
| <span data-ttu-id="eb5e8-232">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-232">Description</span></span>    | <span data-ttu-id="eb5e8-233">Especifica si este protocolo de autenticación se admite en un servidor de Windows 2000 independiente.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-233">Specifies whether this authentication protocol is supported on a standalone Windows 2000 Server.</span></span> <span data-ttu-id="eb5e8-234">Un valor de 0 indica que no se admite EAP.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-234">A value of 0 indicates that the EAP is not supported.</span></span> <span data-ttu-id="eb5e8-235">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-235">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_roles_supported"></a><span data-ttu-id="eb5e8-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="eb5e8-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>

| <span data-ttu-id="eb5e8-237">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-237">Constant Value</span></span> | <span data-ttu-id="eb5e8-238">RolesSupported</span><span class="sxs-lookup"><span data-stu-id="eb5e8-238">RolesSupported</span></span>                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5e8-239">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-239">Type</span></span>           | <span data-ttu-id="eb5e8-240">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-240">REG_DWORD</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="eb5e8-241">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-241">Description</span></span>    | <span data-ttu-id="eb5e8-242">Especifica los distintos roles que admite el EAP.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-242">Specifies the various roles the EAP supports.</span></span> <span data-ttu-id="eb5e8-243">Indica si se puede usar en un servidor o en un cliente, si es compatible con conexiones RAS (VPN) o PEAP.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-243">This indicates whether it can be used on a server or a client, whether it is supported for RAS connections (VPN) or PEAP.</span></span> <span data-ttu-id="eb5e8-244">El comportamiento predeterminado es mostrar el método EAP en PEAP y en EAP.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-244">The default behavior is to show the EAP method in PEAP and in EAP.</span></span> |

## <a name="ras_eap_valuename_per_policy_config"></a><span data-ttu-id="eb5e8-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="eb5e8-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>

| <span data-ttu-id="eb5e8-246">Valor constante</span><span class="sxs-lookup"><span data-stu-id="eb5e8-246">Constant Value</span></span> | <span data-ttu-id="eb5e8-247">PerPolicyConfig</span><span class="sxs-lookup"><span data-stu-id="eb5e8-247">PerPolicyConfig</span></span> |
|----------------|-----------------|
| <span data-ttu-id="eb5e8-248">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb5e8-248">Type</span></span>           | <span data-ttu-id="eb5e8-249">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-249">REG_DWORD</span></span>      |
| <span data-ttu-id="eb5e8-250">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb5e8-250">Description</span></span>    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a><span data-ttu-id="eb5e8-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="eb5e8-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>

<span data-ttu-id="eb5e8-252">Este valor del registro no está en uso.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-252">This registry value is not in use.</span></span>

## <a name="ras_eap_valuename_filter_innermethods"></a><span data-ttu-id="eb5e8-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="eb5e8-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>

<span data-ttu-id="eb5e8-254">Este valor del registro no está en uso.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-254">This registry value is not in use.</span></span>

