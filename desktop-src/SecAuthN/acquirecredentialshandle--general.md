---
description: Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad.
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: AcquireCredentialsHandle (general) (función) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720663"
---
# <a name="acquirecredentialshandle-general-function"></a><span data-ttu-id="a18fe-103">AcquireCredentialsHandle (general), función</span><span class="sxs-lookup"><span data-stu-id="a18fe-103">AcquireCredentialsHandle (General) function</span></span>

<span data-ttu-id="a18fe-104">La función **AcquireCredentialsHandle (general)** adquiere un identificador a las credenciales preexistentes de una [*entidad de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a18fe-104">The **AcquireCredentialsHandle (General)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="a18fe-105">Este identificador es necesario para las funciones [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) y [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="a18fe-105">This handle is required by the [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) and [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) functions.</span></span> <span data-ttu-id="a18fe-106">Pueden ser credenciales preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.</span><span class="sxs-lookup"><span data-stu-id="a18fe-106">These can be either preexisting credentials, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="a18fe-107">No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="a18fe-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

<span data-ttu-id="a18fe-108">Para obtener información sobre el uso de esta función con un [*proveedor de compatibilidad de seguridad*](../secgloss/s-gly.md) (SSP) específico, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a18fe-108">For information about using this function with a specific [*security support provider*](../secgloss/s-gly.md) (SSP), see the following topics.</span></span>



| <span data-ttu-id="a18fe-109">Tema</span><span class="sxs-lookup"><span data-stu-id="a18fe-109">Topic</span></span>                                                                                           | <span data-ttu-id="a18fe-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a18fe-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a18fe-111">**AcquireCredentialsHandle (CredSSP)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-111">**AcquireCredentialsHandle (CredSSP)**</span></span>](acquirecredentialshandle--credssp.md)<br/>     | <span data-ttu-id="a18fe-112">Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa el proveedor de compatibilidad para seguridad de credenciales (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="a18fe-112">Acquires a handle to preexisting credentials of a security principal that is using Credential Security Support Provider (CredSSP).</span></span><br/> |
| [<span data-ttu-id="a18fe-113">**AcquireCredentialsHandle (Resumen)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-113">**AcquireCredentialsHandle (Digest)**</span></span>](acquirecredentialshandle--digest.md)<br/>       | <span data-ttu-id="a18fe-114">Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa la síntesis.</span><span class="sxs-lookup"><span data-stu-id="a18fe-114">Acquires a handle to preexisting credentials of a security principal that is using Digest.</span></span><br/>                                         |
| [<span data-ttu-id="a18fe-115">**AcquireCredentialsHandle (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-115">**AcquireCredentialsHandle (Kerberos)**</span></span>](acquirecredentialshandle--kerberos.md)<br/>   | <span data-ttu-id="a18fe-116">Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a18fe-116">Acquires a handle to preexisting credentials of a security principal that is using Kerberos.</span></span><br/>                                       |
| [<span data-ttu-id="a18fe-117">**AcquireCredentialsHandle (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-117">**AcquireCredentialsHandle (Negotiate)**</span></span>](acquirecredentialshandle--negotiate.md)<br/> | <span data-ttu-id="a18fe-118">Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que utiliza Negotiate.</span><span class="sxs-lookup"><span data-stu-id="a18fe-118">Acquires a handle to preexisting credentials of a security principal that is using Negotiate.</span></span><br/>                                      |
| [<span data-ttu-id="a18fe-119">**AcquireCredentialsHandle (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-119">**AcquireCredentialsHandle (NTLM)**</span></span>](acquirecredentialshandle--ntlm.md)<br/>           | <span data-ttu-id="a18fe-120">Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa NTLM.</span><span class="sxs-lookup"><span data-stu-id="a18fe-120">Acquires a handle to preexisting credentials of a security principal that is using NTLM.</span></span><br/>                                           |
| [<span data-ttu-id="a18fe-121">**AcquireCredentialsHandle (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-121">**AcquireCredentialsHandle (Schannel)**</span></span>](acquirecredentialshandle--schannel.md)<br/>   | <span data-ttu-id="a18fe-122">Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa Schannel.</span><span class="sxs-lookup"><span data-stu-id="a18fe-122">Acquires a handle to preexisting credentials of a security principal that is using Schannel.</span></span><br/>                                       |



 

## <a name="syntax"></a><span data-ttu-id="a18fe-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a18fe-123">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="a18fe-124">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a18fe-124">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a18fe-125">*pszPrincipal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-125">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-126">Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.</span><span class="sxs-lookup"><span data-stu-id="a18fe-126">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="a18fe-127">Cuando se usa el SSP de síntesis, este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="a18fe-127">When using the Digest SSP, this parameter is optional.</span></span>

<span data-ttu-id="a18fe-128">Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="a18fe-128">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="a18fe-129">Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a18fe-129">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="a18fe-130">Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo [*contexto de seguridad*](../secgloss/s-gly.md) se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a18fe-130">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="a18fe-131">*pszPackage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-131">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-132">Puntero a una cadena terminada en null que especifica el nombre del [*paquete de seguridad*](../secgloss/s-gly.md) con el que se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="a18fe-132">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="a18fe-133">Se trata de un nombre de [*paquete de seguridad*](../secgloss/s-gly.md) devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="a18fe-133">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="a18fe-134">Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (general)**](querycontextattributes--general.md) con *ULATTRIBUTE* establecido en SECPKG \_ ATTR \_ Package \_ info para devolver información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) en uso.</span><span class="sxs-lookup"><span data-stu-id="a18fe-134">After a context is established, [**QueryContextAttributes (General)**](querycontextattributes--general.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="a18fe-135">Al usar el SSP de síntesis, establezca este parámetro en WDIGEST \_ Sp \_ Name.</span><span class="sxs-lookup"><span data-stu-id="a18fe-135">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

<span data-ttu-id="a18fe-136">Al usar Schannel SSP, establezca este parámetro en UNISP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="a18fe-136">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="a18fe-137">*fCredentialUse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-137">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-138">Marca que indica cómo se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="a18fe-138">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="a18fe-139">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a18fe-139">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a18fe-140">Valor</span><span class="sxs-lookup"><span data-stu-id="a18fe-140">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="a18fe-141">Significado</span><span class="sxs-lookup"><span data-stu-id="a18fe-141">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="a18fe-142"><dt>**SECPKG \_ CRED \_ AUTOlogon- \_ Restricted**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-142"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="a18fe-143">La seguridad no usa credenciales de inicio de sesión predeterminadas o credenciales del [Administrador de credenciales](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="a18fe-143">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="a18fe-144">Este valor solo es compatible con la [*delegación restringida*](../secgloss/s-gly.md)Negotiate.</span><span class="sxs-lookup"><span data-stu-id="a18fe-144">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="a18fe-145">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="a18fe-145">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="a18fe-146"><dt>**SECPKG \_ CRED \_ both**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-146"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="a18fe-147">Validar una credencial entrante o usar una credencial local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="a18fe-147">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="a18fe-148">Esta marca habilita ambos marcadores.</span><span class="sxs-lookup"><span data-stu-id="a18fe-148">This flag enables both other flags.</span></span> <span data-ttu-id="a18fe-149">Esta marca no es válida con el SSP de Schannel y Digest.</span><span class="sxs-lookup"><span data-stu-id="a18fe-149">This flag is not valid with the Digest and Schannel SSPs.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="a18fe-150"><dt>**SECPKG \_ de \_ entrada de cred**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-150"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="a18fe-151">Validar una credencial de servidor entrante.</span><span class="sxs-lookup"><span data-stu-id="a18fe-151">Validate an incoming server credential.</span></span> <span data-ttu-id="a18fe-152">Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) o [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="a18fe-152">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) or [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) is called.</span></span> <span data-ttu-id="a18fe-153">Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la \_ \_ autoridad de \_ autenticación \_ .</span><span class="sxs-lookup"><span data-stu-id="a18fe-153">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="a18fe-154">La validación es específica del paquete.</span><span class="sxs-lookup"><span data-stu-id="a18fe-154">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="a18fe-155"><dt>**SECPKG \_ CRED \_ saliente**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-155"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="a18fe-156">Permitir una credencial de cliente local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="a18fe-156">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="a18fe-157"><dt>**SECPKG \_ La \_ Directiva de proceso CRED \_ \_ solo**</dt> es <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-157"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="a18fe-158">La función procesa la Directiva de servidor y devuelve las **\_ \_ \_ credenciales sec e no**, lo que indica que la aplicación debe solicitar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="a18fe-158">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="a18fe-159">Este valor solo es compatible con la [*delegación restringida*](../secgloss/s-gly.md)Negotiate.</span><span class="sxs-lookup"><span data-stu-id="a18fe-159">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="a18fe-160">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="a18fe-160">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="a18fe-161">*pvLogonID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-161">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-162">Un puntero a un [*identificador local único*](../secgloss/l-gly.md) (LUID) que identifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="a18fe-162">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="a18fe-163">Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red.</span><span class="sxs-lookup"><span data-stu-id="a18fe-163">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="a18fe-164">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a18fe-164">This parameter can be **NULL**.</span></span>

<span data-ttu-id="a18fe-165">Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="a18fe-165">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a18fe-166">*pAuthData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-166">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-167">Puntero a datos específicos del paquete.</span><span class="sxs-lookup"><span data-stu-id="a18fe-167">A pointer to package-specific data.</span></span> <span data-ttu-id="a18fe-168">Este parámetro puede ser **null**, lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a18fe-168">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="a18fe-169">Para usar las credenciales proporcionadas, pase una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que incluya esas credenciales en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="a18fe-169">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="a18fe-170">El tiempo de ejecución de RPC pasa todo lo que se proporcionó en [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="a18fe-170">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="a18fe-171">Cuando se usa el SSP de síntesis, este parámetro es un puntero a una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que contiene la información de autenticación que se va a usar para buscar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="a18fe-171">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

<span data-ttu-id="a18fe-172">Al usar el SSP de Schannel, especifique una estructura de [**\_ CRED de Schannel**](/windows/win32/api/schannel/ns-schannel-schannel_cred) que indique el protocolo que se va a usar y los valores para varias características de canal personalizables.</span><span class="sxs-lookup"><span data-stu-id="a18fe-172">When using the Schannel SSP, specify an [**SCHANNEL\_CRED**](/windows/win32/api/schannel/ns-schannel-schannel_cred) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

<span data-ttu-id="a18fe-173">Al usar los paquetes NTLM o Negotiate, las longitudes máximas de caracteres para el nombre de usuario, la contraseña y el dominio son 256, 256 y 15, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a18fe-173">When using the NTLM or Negotiate packages, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="a18fe-174">*pGetKeyFn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-174">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-175">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="a18fe-175">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a18fe-176">*pvGetKeyArgument* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-176">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-177">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="a18fe-177">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a18fe-178">*phCredential* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-178">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-179">Puntero a una estructura [CredHandle](sspi-handles.md) para recibir el identificador de la credencial.</span><span class="sxs-lookup"><span data-stu-id="a18fe-179">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="a18fe-180">*ptsExpiry* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-180">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a18fe-181">Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas.</span><span class="sxs-lookup"><span data-stu-id="a18fe-181">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="a18fe-182">El valor devuelto en esta estructura de **marca** de tiempo depende de la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a18fe-182">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="a18fe-183">El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.</span><span class="sxs-lookup"><span data-stu-id="a18fe-183">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="a18fe-184">Este parámetro se establece en un tiempo máximo constante.</span><span class="sxs-lookup"><span data-stu-id="a18fe-184">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="a18fe-185">No hay ningún tiempo de expiración para las credenciales o el [*contexto de seguridad*](../secgloss/s-gly.md)implícita o cuando se usa el SSP de síntesis.</span><span class="sxs-lookup"><span data-stu-id="a18fe-185">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

<span data-ttu-id="a18fe-186">Cuando se usa Schannel SSP, este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="a18fe-186">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="a18fe-187">Cuando la credencial que se va a usar para la autenticación es un certificado, este parámetro recibe la hora de expiración de ese certificado.</span><span class="sxs-lookup"><span data-stu-id="a18fe-187">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="a18fe-188">Si no se ha proporcionado ningún certificado, se devuelve un valor de tiempo máximo.</span><span class="sxs-lookup"><span data-stu-id="a18fe-188">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a18fe-189">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a18fe-189">Return value</span></span>

<span data-ttu-id="a18fe-190">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a18fe-190">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="a18fe-191">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a18fe-191">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="a18fe-192">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a18fe-192">Return code</span></span>                                                                                                 | <span data-ttu-id="a18fe-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="a18fe-193">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a18fe-194"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-194"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="a18fe-195">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="a18fe-195">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="a18fe-196"><dt>**s \_ E \_ interno \_ error**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-196"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="a18fe-197">Error que no se ha asignado a un código de error SSPI.</span><span class="sxs-lookup"><span data-stu-id="a18fe-197">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="a18fe-198"><dt>**s \_ E \_ sin \_ credenciales**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-198"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="a18fe-199">No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a18fe-199">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="a18fe-200"><dt>**s \_ E \_ no \_ propietario**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-200"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="a18fe-201">El autor de la llamada de la función no tiene las credenciales necesarias.</span><span class="sxs-lookup"><span data-stu-id="a18fe-201">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="a18fe-202"><dt>**s \_ E \_ SECPKG \_ no \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-202"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="a18fe-203">El [*paquete de seguridad*](../secgloss/s-gly.md) solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="a18fe-203">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="a18fe-204"><dt>**s \_ E \_ credenciales desconocidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-204"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="a18fe-205">No se reconocieron las credenciales proporcionadas al paquete.</span><span class="sxs-lookup"><span data-stu-id="a18fe-205">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="a18fe-206">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a18fe-206">Remarks</span></span>

<span data-ttu-id="a18fe-207">La función **AcquireCredentialsHandle (general)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa una [*delegación restringida*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="a18fe-207">The **AcquireCredentialsHandle (General)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="a18fe-208">Puede ser el identificador de las credenciales preexistentes o la función puede crear un nuevo conjunto de credenciales y devolverlo.</span><span class="sxs-lookup"><span data-stu-id="a18fe-208">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="a18fe-209">Este identificador se puede utilizar en llamadas posteriores a las funciones [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) y [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="a18fe-209">This handle can be used in subsequent calls to the [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) and [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) functions.</span></span>

<span data-ttu-id="a18fe-210">En general, **AcquireCredentialsHandle (general)** no permite a un proceso obtener un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="a18fe-210">In general, **AcquireCredentialsHandle (General)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="a18fe-211">Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/s-gly.md) ' TCB name ' tiene la opción de especificar el [*identificador de inicio de sesión*](../secgloss/l-gly.md) (LUID) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a18fe-211">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="a18fe-212">Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="a18fe-212">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="a18fe-213">Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="a18fe-213">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="a18fe-214">Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a18fe-214">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="a18fe-215">En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:</span><span class="sxs-lookup"><span data-stu-id="a18fe-215">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="a18fe-216">Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a18fe-216">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="a18fe-217">Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.</span><span class="sxs-lookup"><span data-stu-id="a18fe-217">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="a18fe-218">Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="a18fe-218">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a18fe-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a18fe-219">Requirements</span></span>



| <span data-ttu-id="a18fe-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="a18fe-220">Requirement</span></span> | <span data-ttu-id="a18fe-221">Value</span><span class="sxs-lookup"><span data-stu-id="a18fe-221">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a18fe-222">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a18fe-222">Minimum supported client</span></span><br/> | <span data-ttu-id="a18fe-223">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-223">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a18fe-224">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a18fe-224">Minimum supported server</span></span><br/> | <span data-ttu-id="a18fe-225">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a18fe-225">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a18fe-226">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a18fe-226">Header</span></span><br/>                   | <dl> <span data-ttu-id="a18fe-227"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-227"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="a18fe-228">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a18fe-228">Library</span></span><br/>                  | <dl> <span data-ttu-id="a18fe-229"><dt>SECUR32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-229"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="a18fe-230">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a18fe-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a18fe-231"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a18fe-231"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="a18fe-232">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a18fe-232">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a18fe-233">**AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a18fe-233">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a18fe-234">Vea también</span><span class="sxs-lookup"><span data-stu-id="a18fe-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18fe-235">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="a18fe-235">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="a18fe-236">**AcceptSecurityContext (general)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-236">**AcceptSecurityContext (General)**</span></span>](acceptsecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="a18fe-237">**InitializeSecurityContext (general)**</span><span class="sxs-lookup"><span data-stu-id="a18fe-237">**InitializeSecurityContext (General)**</span></span>](initializesecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="a18fe-238">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="a18fe-238">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
