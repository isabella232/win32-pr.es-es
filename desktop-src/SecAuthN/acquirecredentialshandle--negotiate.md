---
description: Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que utiliza Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: Función AcquireCredentialsHandle (Negotiate) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720661"
---
# <a name="acquirecredentialshandle-negotiate-function"></a><span data-ttu-id="86c23-103">AcquireCredentialsHandle (Negotiate) (función)</span><span class="sxs-lookup"><span data-stu-id="86c23-103">AcquireCredentialsHandle (Negotiate) function</span></span>

<span data-ttu-id="86c23-104">La función **AcquireCredentialsHandle (Negotiate)** adquiere un identificador a las credenciales preexistentes de una [*entidad de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="86c23-104">The **AcquireCredentialsHandle (Negotiate)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="86c23-105">Este identificador es necesario para las funciones [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) y [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="86c23-105">This handle is required by the [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) and [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) functions.</span></span> <span data-ttu-id="86c23-106">Pueden ser *credenciales* preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.</span><span class="sxs-lookup"><span data-stu-id="86c23-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="86c23-107">No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="86c23-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="86c23-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86c23-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="86c23-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86c23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c23-110">*pszPrincipal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86c23-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-111">Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.</span><span class="sxs-lookup"><span data-stu-id="86c23-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="86c23-112">Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="86c23-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="86c23-113">Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo [*contexto de seguridad*](../secgloss/s-gly.md) se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="86c23-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="86c23-114">*pszPackage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86c23-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-115">Puntero a una cadena terminada en null que especifica el nombre del [*paquete de seguridad*](../secgloss/s-gly.md) con el que se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="86c23-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="86c23-116">Se trata de un nombre de [*paquete de seguridad*](../secgloss/s-gly.md) devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="86c23-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="86c23-117">Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) con *ULATTRIBUTE* establecido en SECPKG \_ ATTR \_ Package \_ info para devolver información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) en uso.</span><span class="sxs-lookup"><span data-stu-id="86c23-117">After a context is established, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="86c23-118">Para llamar correctamente a esta función mediante el SSP Negotiate, establezca este parámetro en "Negotiate".</span><span class="sxs-lookup"><span data-stu-id="86c23-118">To successfully call this function using the Negotiate SSP, set this parameter to "Negotiate".</span></span>

</dd> <dt>

<span data-ttu-id="86c23-119">*fCredentialUse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86c23-119">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-120">Marca que indica cómo se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="86c23-120">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="86c23-121">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="86c23-121">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="86c23-122">Valor</span><span class="sxs-lookup"><span data-stu-id="86c23-122">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="86c23-123">Significado</span><span class="sxs-lookup"><span data-stu-id="86c23-123">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="86c23-124"><dt>**SECPKG \_ CRED \_ AUTOlogon- \_ Restricted**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-124"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="86c23-125">La seguridad no usa credenciales de inicio de sesión predeterminadas o credenciales del [Administrador de credenciales](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="86c23-125">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="86c23-126">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="86c23-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="86c23-127"><dt>**SECPKG \_ CRED \_ both**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-127"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="86c23-128">Validar una credencial entrante o usar una credencial local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="86c23-128">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="86c23-129">Esta marca habilita ambos marcadores.</span><span class="sxs-lookup"><span data-stu-id="86c23-129">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="86c23-130"><dt>**SECPKG \_ de \_ entrada de cred**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-130"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="86c23-131">Validar una credencial de servidor entrante.</span><span class="sxs-lookup"><span data-stu-id="86c23-131">Validate an incoming server credential.</span></span> <span data-ttu-id="86c23-132">Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) o [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="86c23-132">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) or [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) is called.</span></span> <span data-ttu-id="86c23-133">Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la \_ \_ autoridad de \_ autenticación \_ .</span><span class="sxs-lookup"><span data-stu-id="86c23-133">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="86c23-134">La validación es específica del paquete.</span><span class="sxs-lookup"><span data-stu-id="86c23-134">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="86c23-135"><dt>**SECPKG \_ CRED \_ saliente**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-135"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="86c23-136">Permitir una credencial de cliente local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="86c23-136">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="86c23-137"><dt>**SECPKG \_ La \_ Directiva de proceso CRED \_ \_ solo**</dt> es <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-137"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="86c23-138">La función procesa la Directiva de servidor y devuelve las **\_ \_ \_ credenciales sec e no**, lo que indica que la aplicación debe solicitar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="86c23-138">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="86c23-139">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="86c23-139">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="86c23-140">*pvLogonID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86c23-140">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-141">Un puntero a un [*identificador local único*](../secgloss/l-gly.md) (LUID) que identifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="86c23-141">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="86c23-142">Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red.</span><span class="sxs-lookup"><span data-stu-id="86c23-142">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="86c23-143">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="86c23-143">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="86c23-144">*pAuthData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86c23-144">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-145">Puntero a datos específicos del paquete.</span><span class="sxs-lookup"><span data-stu-id="86c23-145">A pointer to package-specific data.</span></span> <span data-ttu-id="86c23-146">Este parámetro puede ser **null**, lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="86c23-146">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="86c23-147">Para usar las credenciales proporcionadas, pase una estructura **opaca de identidad de autenticación de PSEC \_ WinNT \_ \_ \_** devuelta desde una llamada anterior a la función [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .</span><span class="sxs-lookup"><span data-stu-id="86c23-147">To use supplied credentials, pass a **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** structure returned from a previous call to the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function.</span></span>

<span data-ttu-id="86c23-148">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admiten el tipo **opaco de identidad de autenticación de PSEC \_ WinNT \_ \_ \_** y la función [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .</span><span class="sxs-lookup"><span data-stu-id="86c23-148">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** The **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** type and the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function are not supported.</span></span> <span data-ttu-id="86c23-149">Para usar las credenciales proporcionadas, pase un puntero a una [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC o a una estructura de [**autenticación de \_ WinNT de la \_ \_ identidad \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) que incluye esas credenciales.</span><span class="sxs-lookup"><span data-stu-id="86c23-149">To use supplied credentials, pass a pointer to either a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) or [**SEC\_WINNT\_AUTH\_IDENTITY\_EX**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) structure that includes those credentials.</span></span>

<span data-ttu-id="86c23-150">El tiempo de ejecución de RPC pasa todo lo que se proporcionó en [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="86c23-150">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="86c23-151">Al usar el paquete Negotiate, las longitudes máximas de caracteres para el nombre de usuario, la contraseña y el dominio son 256, 256 y 15, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="86c23-151">When using the Negotiate package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="86c23-152">*pGetKeyFn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86c23-152">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-153">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="86c23-153">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="86c23-154">*pvGetKeyArgument* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86c23-154">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-155">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="86c23-155">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="86c23-156">*phCredential* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86c23-156">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-157">Puntero a una estructura [CredHandle](sspi-handles.md) para recibir el identificador de la credencial.</span><span class="sxs-lookup"><span data-stu-id="86c23-157">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="86c23-158">*ptsExpiry* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86c23-158">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c23-159">Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas.</span><span class="sxs-lookup"><span data-stu-id="86c23-159">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="86c23-160">El valor devuelto en esta estructura de **marca** de tiempo depende de la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="86c23-160">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="86c23-161">El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.</span><span class="sxs-lookup"><span data-stu-id="86c23-161">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c23-162">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86c23-162">Return value</span></span>

<span data-ttu-id="86c23-163">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86c23-163">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="86c23-164">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="86c23-164">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="86c23-165">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="86c23-165">Return code</span></span>                                                                                                 | <span data-ttu-id="86c23-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c23-166">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86c23-167"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-167"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="86c23-168">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="86c23-168">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="86c23-169"><dt>**s \_ E \_ interno \_ error**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-169"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="86c23-170">Error que no se ha asignado a un código de error SSPI.</span><span class="sxs-lookup"><span data-stu-id="86c23-170">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="86c23-171"><dt>**s \_ E \_ sin \_ credenciales**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-171"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="86c23-172">No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="86c23-172">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="86c23-173"><dt>**s \_ E \_ no \_ propietario**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-173"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="86c23-174">El autor de la llamada de la función no tiene las credenciales necesarias.</span><span class="sxs-lookup"><span data-stu-id="86c23-174">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="86c23-175"><dt>**s \_ E \_ SECPKG \_ no \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-175"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="86c23-176">El [*paquete de seguridad*](../secgloss/s-gly.md) solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="86c23-176">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="86c23-177"><dt>**s \_ E \_ credenciales desconocidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-177"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="86c23-178">No se reconocieron las credenciales proporcionadas al paquete.</span><span class="sxs-lookup"><span data-stu-id="86c23-178">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="86c23-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86c23-179">Remarks</span></span>

<span data-ttu-id="86c23-180">La función **AcquireCredentialsHandle (Negotiate)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa una [*delegación restringida*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="86c23-180">The **AcquireCredentialsHandle (Negotiate)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="86c23-181">Puede ser el identificador de las credenciales preexistentes o la función puede crear un nuevo conjunto de credenciales y devolverlo.</span><span class="sxs-lookup"><span data-stu-id="86c23-181">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="86c23-182">Este identificador se puede utilizar en llamadas posteriores a las funciones [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) y [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="86c23-182">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) and [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) functions.</span></span>

<span data-ttu-id="86c23-183">En general, **AcquireCredentialsHandle (Negotiate)** no permite a un proceso obtener un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="86c23-183">In general, **AcquireCredentialsHandle (Negotiate)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="86c23-184">Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/s-gly.md) ' TCB name ' tiene la opción de especificar el [*identificador de inicio de sesión*](../secgloss/l-gly.md) (LUID) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de la sesión.</span><span class="sxs-lookup"><span data-stu-id="86c23-184">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="86c23-185">Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="86c23-185">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="86c23-186">Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="86c23-186">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="86c23-187">Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="86c23-187">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="86c23-188">En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:</span><span class="sxs-lookup"><span data-stu-id="86c23-188">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="86c23-189">Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="86c23-189">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="86c23-190">Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.</span><span class="sxs-lookup"><span data-stu-id="86c23-190">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="86c23-191">Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="86c23-191">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c23-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86c23-192">Requirements</span></span>



| <span data-ttu-id="86c23-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c23-193">Requirement</span></span> | <span data-ttu-id="86c23-194">Value</span><span class="sxs-lookup"><span data-stu-id="86c23-194">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c23-195">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86c23-195">Minimum supported client</span></span><br/> | <span data-ttu-id="86c23-196">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="86c23-196">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="86c23-197">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86c23-197">Minimum supported server</span></span><br/> | <span data-ttu-id="86c23-198">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="86c23-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="86c23-199">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86c23-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c23-200"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-200"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="86c23-201">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86c23-201">Library</span></span><br/>                  | <dl> <span data-ttu-id="86c23-202"><dt>SECUR32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-202"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="86c23-203">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86c23-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c23-204"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c23-204"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="86c23-205">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="86c23-205">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="86c23-206">**AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="86c23-206">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="86c23-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="86c23-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c23-208">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="86c23-208">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="86c23-209">**AcceptSecurityContext (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="86c23-209">**AcceptSecurityContext (Negotiate)**</span></span>](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="86c23-210">**InitializeSecurityContext (negociar)**</span><span class="sxs-lookup"><span data-stu-id="86c23-210">**InitializeSecurityContext (Negotiate)**</span></span>](initializesecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="86c23-211">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="86c23-211">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
