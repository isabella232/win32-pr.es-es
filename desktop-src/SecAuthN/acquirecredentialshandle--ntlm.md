---
description: Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa NTLM.
ms.assetid: 8a51ca50-0e05-4f1e-9dfc-c5d0118f65ed
title: Función AcquireCredentialsHandle (NTLM) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 233bfd57c6e3a7471d7c26204157cd1451d7884f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278268"
---
# <a name="acquirecredentialshandle-ntlm-function"></a><span data-ttu-id="85cd8-103">Función AcquireCredentialsHandle (NTLM)</span><span class="sxs-lookup"><span data-stu-id="85cd8-103">AcquireCredentialsHandle (NTLM) function</span></span>

<span data-ttu-id="85cd8-104">La función **AcquireCredentialsHandle (NTLM)** adquiere un identificador a las credenciales preexistentes de una [*entidad de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85cd8-104">The **AcquireCredentialsHandle (NTLM)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="85cd8-105">Este identificador es necesario para las funciones [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) y [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="85cd8-105">This handle is required by the [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) and [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) functions.</span></span> <span data-ttu-id="85cd8-106">Pueden ser *credenciales* preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.</span><span class="sxs-lookup"><span data-stu-id="85cd8-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="85cd8-107">No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="85cd8-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85cd8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85cd8-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="85cd8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85cd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85cd8-110">*pszPrincipal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-111">Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.</span><span class="sxs-lookup"><span data-stu-id="85cd8-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="85cd8-112">Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="85cd8-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="85cd8-113">Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo [*contexto de seguridad*](../secgloss/s-gly.md) se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="85cd8-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="85cd8-114">*pszPackage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-115">Puntero a una cadena terminada en null que especifica el nombre del [*paquete de seguridad*](../secgloss/s-gly.md) con el que se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="85cd8-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="85cd8-116">Se trata de un nombre de [*paquete de seguridad*](../secgloss/s-gly.md) devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="85cd8-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="85cd8-117">Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) con *ULATTRIBUTE* establecido en SECPKG \_ ATTR \_ Package \_ info para devolver información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) en uso.</span><span class="sxs-lookup"><span data-stu-id="85cd8-117">After a context is established, [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="85cd8-118">*fCredentialUse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-119">Marca que indica cómo se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="85cd8-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="85cd8-120">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="85cd8-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="85cd8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="85cd8-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="85cd8-122">Significado</span><span class="sxs-lookup"><span data-stu-id="85cd8-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="85cd8-123"><dt>**SECPKG \_ CRED \_ both**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="85cd8-124">Validar una credencial entrante o usar una credencial local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="85cd8-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="85cd8-125">Esta marca habilita ambos marcadores.</span><span class="sxs-lookup"><span data-stu-id="85cd8-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="85cd8-126"><dt>**SECPKG \_ de \_ entrada de cred**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="85cd8-127">Validar una credencial de servidor entrante.</span><span class="sxs-lookup"><span data-stu-id="85cd8-127">Validate an incoming server credential.</span></span> <span data-ttu-id="85cd8-128">Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) o [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="85cd8-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) or [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) is called.</span></span> <span data-ttu-id="85cd8-129">Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la \_ \_ autoridad de \_ autenticación \_ .</span><span class="sxs-lookup"><span data-stu-id="85cd8-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="85cd8-130">La validación es específica del paquete.</span><span class="sxs-lookup"><span data-stu-id="85cd8-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="85cd8-131"><dt>**SECPKG \_ CRED \_ saliente**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="85cd8-132">Permitir una credencial de cliente local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="85cd8-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="85cd8-133">*pvLogonID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-134">Un puntero a un [*identificador local único*](../secgloss/l-gly.md) (LUID) que identifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="85cd8-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="85cd8-135">Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red.</span><span class="sxs-lookup"><span data-stu-id="85cd8-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="85cd8-136">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="85cd8-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85cd8-137">*pAuthData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-138">Puntero a datos específicos del paquete.</span><span class="sxs-lookup"><span data-stu-id="85cd8-138">A pointer to package-specific data.</span></span> <span data-ttu-id="85cd8-139">Este parámetro puede ser **null**, lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="85cd8-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="85cd8-140">Para usar las credenciales proporcionadas, pase una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que incluya esas credenciales en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="85cd8-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="85cd8-141">El tiempo de ejecución de RPC pasa todo lo que se proporcionó en [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="85cd8-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="85cd8-142">Al usar el paquete NTLM, las longitudes máximas de caracteres para el nombre de usuario, la contraseña y el dominio son 256, 256 y 15, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="85cd8-142">When using the NTLM package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="85cd8-143">*pGetKeyFn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-143">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-144">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="85cd8-144">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85cd8-145">*pvGetKeyArgument* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-145">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-146">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="85cd8-146">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85cd8-147">*phCredential* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-147">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-148">Puntero a una estructura [CredHandle](sspi-handles.md) para recibir el identificador de la credencial.</span><span class="sxs-lookup"><span data-stu-id="85cd8-148">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="85cd8-149">*ptsExpiry* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-149">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-150">Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas.</span><span class="sxs-lookup"><span data-stu-id="85cd8-150">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="85cd8-151">El valor devuelto en esta estructura de **marca** de tiempo depende de la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85cd8-151">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="85cd8-152">El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.</span><span class="sxs-lookup"><span data-stu-id="85cd8-152">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85cd8-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85cd8-153">Return value</span></span>

<span data-ttu-id="85cd8-154">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85cd8-154">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="85cd8-155">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="85cd8-155">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="85cd8-156">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="85cd8-156">Return code</span></span>                                                                                                 | <span data-ttu-id="85cd8-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="85cd8-157">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85cd8-158"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-158"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="85cd8-159">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="85cd8-159">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="85cd8-160"><dt>**s \_ E \_ interno \_ error**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-160"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="85cd8-161">Error que no se ha asignado a un código de error SSPI.</span><span class="sxs-lookup"><span data-stu-id="85cd8-161">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="85cd8-162"><dt>**s \_ E \_ sin \_ credenciales**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-162"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="85cd8-163">No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85cd8-163">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="85cd8-164"><dt>**s \_ E \_ no \_ propietario**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-164"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="85cd8-165">El autor de la llamada de la función no tiene las credenciales necesarias.</span><span class="sxs-lookup"><span data-stu-id="85cd8-165">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="85cd8-166"><dt>**s \_ E \_ SECPKG \_ no \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-166"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="85cd8-167">El [*paquete de seguridad*](../secgloss/s-gly.md) solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="85cd8-167">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="85cd8-168"><dt>**s \_ E \_ credenciales desconocidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-168"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="85cd8-169">No se reconocieron las credenciales proporcionadas al paquete.</span><span class="sxs-lookup"><span data-stu-id="85cd8-169">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="85cd8-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85cd8-170">Remarks</span></span>

<span data-ttu-id="85cd8-171">La función **AcquireCredentialsHandle (NTLM)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa una [*delegación restringida*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="85cd8-171">The **AcquireCredentialsHandle (NTLM)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="85cd8-172">Puede ser el identificador de las credenciales preexistentes o la función puede crear un nuevo conjunto de credenciales y devolverlo.</span><span class="sxs-lookup"><span data-stu-id="85cd8-172">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="85cd8-173">Este identificador se puede utilizar en llamadas posteriores a las funciones [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) y [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="85cd8-173">This handle can be used in subsequent calls to the [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) and [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) functions.</span></span>

<span data-ttu-id="85cd8-174">En general, **AcquireCredentialsHandle (NTLM)** no permite a un proceso obtener un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="85cd8-174">In general, **AcquireCredentialsHandle (NTLM)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="85cd8-175">Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/s-gly.md) ' TCB name ' tiene la opción de especificar el [*identificador de inicio de sesión*](../secgloss/l-gly.md) (LUID) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85cd8-175">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="85cd8-176">Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="85cd8-176">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="85cd8-177">Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="85cd8-177">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="85cd8-178">Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="85cd8-178">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="85cd8-179">En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:</span><span class="sxs-lookup"><span data-stu-id="85cd8-179">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="85cd8-180">Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="85cd8-180">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="85cd8-181">Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.</span><span class="sxs-lookup"><span data-stu-id="85cd8-181">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="85cd8-182">Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="85cd8-182">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="85cd8-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85cd8-183">Requirements</span></span>



| <span data-ttu-id="85cd8-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="85cd8-184">Requirement</span></span> | <span data-ttu-id="85cd8-185">Value</span><span class="sxs-lookup"><span data-stu-id="85cd8-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85cd8-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85cd8-186">Minimum supported client</span></span><br/> | <span data-ttu-id="85cd8-187">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="85cd8-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85cd8-188">Minimum supported server</span></span><br/> | <span data-ttu-id="85cd8-189">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="85cd8-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85cd8-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="85cd8-191"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="85cd8-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85cd8-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="85cd8-193"><dt>SECUR32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="85cd8-194">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85cd8-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85cd8-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-195"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="85cd8-196">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="85cd8-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="85cd8-197">**AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="85cd8-197">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="85cd8-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="85cd8-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85cd8-199">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="85cd8-199">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="85cd8-200">**AcceptSecurityContext (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="85cd8-200">**AcceptSecurityContext (NTLM)**</span></span>](acceptsecuritycontext--ntlm.md)
</dt> <dt>

[<span data-ttu-id="85cd8-201">**InitializeSecurityContext (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="85cd8-201">**InitializeSecurityContext (NTLM)**</span></span>](initializesecuritycontext--ntlm.md)
</dt> <dt>

[<span data-ttu-id="85cd8-202">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="85cd8-202">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
