---
description: Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa Schannel.
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: Función AcquireCredentialsHandle (Schannel) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5b7de49e76cf5b09611790a12826f1a13fc38e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720660"
---
# <a name="acquirecredentialshandle-schannel-function"></a><span data-ttu-id="bc02a-103">AcquireCredentialsHandle (Schannel) (función)</span><span class="sxs-lookup"><span data-stu-id="bc02a-103">AcquireCredentialsHandle (Schannel) function</span></span>

<span data-ttu-id="bc02a-104">La función **AcquireCredentialsHandle (Schannel)** adquiere un identificador a las credenciales preexistentes de una [*entidad de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bc02a-104">The **AcquireCredentialsHandle (Schannel)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="bc02a-105">Este identificador es necesario para las funciones [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) y [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="bc02a-105">This handle is required by the [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) and [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) functions.</span></span> <span data-ttu-id="bc02a-106">Pueden ser *credenciales* preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.</span><span class="sxs-lookup"><span data-stu-id="bc02a-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="bc02a-107">No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="bc02a-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bc02a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc02a-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="bc02a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc02a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc02a-110">*pszPrincipal* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-110">*pszPrincipal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-111">Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.</span><span class="sxs-lookup"><span data-stu-id="bc02a-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="bc02a-112">Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="bc02a-112">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="bc02a-113">Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="bc02a-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="bc02a-114">Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo [*contexto de seguridad*](../secgloss/s-gly.md) se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="bc02a-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="bc02a-115">*pszPackage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-116">Puntero a una cadena terminada en null que especifica el nombre del [*paquete de seguridad*](../secgloss/s-gly.md) con el que se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="bc02a-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="bc02a-117">Se trata de un nombre de [*paquete de seguridad*](../secgloss/s-gly.md) devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="bc02a-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="bc02a-118">Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) con *ULATTRIBUTE* establecido en SECPKG \_ ATTR \_ Package \_ info para devolver información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) en uso.</span><span class="sxs-lookup"><span data-stu-id="bc02a-118">After a context is established, [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="bc02a-119">Al usar Schannel SSP, establezca este parámetro en UNISP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="bc02a-119">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="bc02a-120">*fCredentialUse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-121">Marca que indica cómo se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="bc02a-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="bc02a-122">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bc02a-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="bc02a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bc02a-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="bc02a-124">Significado</span><span class="sxs-lookup"><span data-stu-id="bc02a-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="bc02a-125"><dt>**SECPKG \_ de \_ entrada de cred**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="bc02a-126">Validar una credencial de servidor entrante.</span><span class="sxs-lookup"><span data-stu-id="bc02a-126">Validate an incoming server credential.</span></span> <span data-ttu-id="bc02a-127">Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) o [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="bc02a-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) or [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) is called.</span></span> <span data-ttu-id="bc02a-128">Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la \_ \_ autoridad de \_ autenticación \_ .</span><span class="sxs-lookup"><span data-stu-id="bc02a-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="bc02a-129">La validación es específica del paquete.</span><span class="sxs-lookup"><span data-stu-id="bc02a-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="bc02a-130"><dt>**SECPKG \_ CRED \_ saliente**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="bc02a-131">Permitir una credencial de cliente local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="bc02a-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="bc02a-132">*pvLogonID* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-132">*pvLogonID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-133">Un puntero a un [*identificador local único*](../secgloss/l-gly.md) (LUID) que identifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="bc02a-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="bc02a-134">Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red.</span><span class="sxs-lookup"><span data-stu-id="bc02a-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="bc02a-135">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bc02a-135">This parameter can be **NULL**.</span></span>

<span data-ttu-id="bc02a-136">Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="bc02a-136">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc02a-137">*pAuthData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-137">*pAuthData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-138">Puntero a datos específicos del paquete.</span><span class="sxs-lookup"><span data-stu-id="bc02a-138">A pointer to package-specific data.</span></span> <span data-ttu-id="bc02a-139">Este parámetro puede ser **null**, lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bc02a-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="bc02a-140">Para usar las credenciales proporcionadas, pase una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que incluya esas credenciales en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="bc02a-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="bc02a-141">El tiempo de ejecución de RPC pasa todo lo que se proporcionó en [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="bc02a-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="bc02a-142">Al usar el SSP de Schannel, especifique una estructura de [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) que indique el protocolo que se va a usar y los valores para varias características de canal personalizables.</span><span class="sxs-lookup"><span data-stu-id="bc02a-142">When using the Schannel SSP, specify an [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

</dd> <dt>

<span data-ttu-id="bc02a-143">*pGetKeyFn* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-143">*pGetKeyFn* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-144">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="bc02a-144">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc02a-145">*pvGetKeyArgument* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-145">*pvGetKeyArgument* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-146">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="bc02a-146">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc02a-147">*phCredential* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-147">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-148">Puntero a una estructura [CredHandle](sspi-handles.md) para recibir el identificador de la credencial.</span><span class="sxs-lookup"><span data-stu-id="bc02a-148">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="bc02a-149">*ptsExpiry* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-149">*ptsExpiry* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc02a-150">Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas.</span><span class="sxs-lookup"><span data-stu-id="bc02a-150">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="bc02a-151">El valor devuelto en esta estructura de **marca** de tiempo depende de la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bc02a-151">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="bc02a-152">El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.</span><span class="sxs-lookup"><span data-stu-id="bc02a-152">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="bc02a-153">Cuando se usa Schannel SSP, este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="bc02a-153">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="bc02a-154">Cuando la credencial que se va a usar para la autenticación es un certificado, este parámetro recibe la hora de expiración de ese certificado.</span><span class="sxs-lookup"><span data-stu-id="bc02a-154">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="bc02a-155">Si no se ha proporcionado ningún certificado, se devuelve un valor de tiempo máximo.</span><span class="sxs-lookup"><span data-stu-id="bc02a-155">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc02a-156">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc02a-156">Return value</span></span>

<span data-ttu-id="bc02a-157">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc02a-157">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="bc02a-158">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="bc02a-158">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="bc02a-159">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bc02a-159">Return code</span></span>                                                                                                 | <span data-ttu-id="bc02a-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc02a-160">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc02a-161"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-161"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="bc02a-162">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="bc02a-162">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="bc02a-163"><dt>**s \_ E \_ interno \_ error**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-163"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="bc02a-164">Error que no se ha asignado a un código de error SSPI.</span><span class="sxs-lookup"><span data-stu-id="bc02a-164">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="bc02a-165"><dt>**s \_ E \_ sin \_ credenciales**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-165"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="bc02a-166">No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bc02a-166">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="bc02a-167"><dt>**s \_ E \_ no \_ propietario**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-167"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="bc02a-168">El autor de la llamada de la función no tiene las credenciales necesarias.</span><span class="sxs-lookup"><span data-stu-id="bc02a-168">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="bc02a-169"><dt>**s \_ E \_ SECPKG \_ no \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-169"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="bc02a-170">El [*paquete de seguridad*](../secgloss/s-gly.md) solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="bc02a-170">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="bc02a-171"><dt>**s \_ E \_ credenciales desconocidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-171"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="bc02a-172">No se reconocieron las credenciales proporcionadas al paquete.</span><span class="sxs-lookup"><span data-stu-id="bc02a-172">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="bc02a-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc02a-173">Remarks</span></span>

<span data-ttu-id="bc02a-174">La función **AcquireCredentialsHandle (Schannel)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa una [*delegación restringida*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="bc02a-174">The **AcquireCredentialsHandle (Schannel)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="bc02a-175">Puede ser el identificador de las credenciales preexistentes o la función puede crear un nuevo conjunto de credenciales y devolverlo.</span><span class="sxs-lookup"><span data-stu-id="bc02a-175">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="bc02a-176">Este identificador se puede utilizar en llamadas posteriores a las funciones [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) y [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="bc02a-176">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) and [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) functions.</span></span>

<span data-ttu-id="bc02a-177">En general, **AcquireCredentialsHandle (Schannel)** no permite a un proceso obtener un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="bc02a-177">In general, **AcquireCredentialsHandle (Schannel)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="bc02a-178">Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/s-gly.md) ' TCB name ' tiene la opción de especificar el [*identificador de inicio de sesión*](../secgloss/l-gly.md) (LUID) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de la sesión.</span><span class="sxs-lookup"><span data-stu-id="bc02a-178">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="bc02a-179">Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="bc02a-179">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="bc02a-180">Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="bc02a-180">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="bc02a-181">Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bc02a-181">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="bc02a-182">En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:</span><span class="sxs-lookup"><span data-stu-id="bc02a-182">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="bc02a-183">Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bc02a-183">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="bc02a-184">Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.</span><span class="sxs-lookup"><span data-stu-id="bc02a-184">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="bc02a-185">Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="bc02a-185">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc02a-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc02a-186">Requirements</span></span>



| <span data-ttu-id="bc02a-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc02a-187">Requirement</span></span> | <span data-ttu-id="bc02a-188">Value</span><span class="sxs-lookup"><span data-stu-id="bc02a-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc02a-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc02a-189">Minimum supported client</span></span><br/> | <span data-ttu-id="bc02a-190">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-190">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bc02a-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc02a-191">Minimum supported server</span></span><br/> | <span data-ttu-id="bc02a-192">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc02a-192">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="bc02a-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc02a-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc02a-194"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-194"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="bc02a-195">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc02a-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc02a-196"><dt>SECUR32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-196"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="bc02a-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc02a-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc02a-198"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc02a-198"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="bc02a-199">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="bc02a-199">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc02a-200">**AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bc02a-200">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bc02a-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc02a-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc02a-202">**AcceptSecurityContext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="bc02a-202">**AcceptSecurityContext (Schannel)**</span></span>](acceptsecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="bc02a-203">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="bc02a-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[<span data-ttu-id="bc02a-204">**InitializeSecurityContext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="bc02a-204">**InitializeSecurityContext (Schannel)**</span></span>](initializesecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="bc02a-205">**SCH_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="bc02a-205">**SCH_CREDENTIALS**</span></span>](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[<span data-ttu-id="bc02a-206">**Funciones SSPI**</span><span class="sxs-lookup"><span data-stu-id="bc02a-206">**SSPI Functions**</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 
