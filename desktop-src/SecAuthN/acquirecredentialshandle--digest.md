---
description: Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa la síntesis.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: Función AcquireCredentialsHandle (digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278269"
---
# <a name="acquirecredentialshandle-digest-function"></a><span data-ttu-id="1cc79-103">AcquireCredentialsHandle (síntesis) (función)</span><span class="sxs-lookup"><span data-stu-id="1cc79-103">AcquireCredentialsHandle (Digest) function</span></span>

<span data-ttu-id="1cc79-104">La función **AcquireCredentialsHandle (síntesis)** adquiere un identificador a las credenciales preexistentes de una [*entidad de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1cc79-104">The **AcquireCredentialsHandle (Digest)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1cc79-105">Este identificador es necesario para las funciones [**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md) y [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc79-105">This handle is required by the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span> <span data-ttu-id="1cc79-106">Pueden ser *credenciales* preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.</span><span class="sxs-lookup"><span data-stu-id="1cc79-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="1cc79-107">No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1cc79-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1cc79-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cc79-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1cc79-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cc79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc79-110">*pszPrincipal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-111">Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.</span><span class="sxs-lookup"><span data-stu-id="1cc79-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="1cc79-112">Cuando se usa el SSP de síntesis, este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="1cc79-112">When using the Digest SSP, this parameter is optional.</span></span>

> [!Note]  
> <span data-ttu-id="1cc79-113">Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1cc79-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="1cc79-114">Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo [*contexto de seguridad*](../secgloss/s-gly.md) se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="1cc79-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="1cc79-115">*pszPackage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-116">Puntero a una cadena terminada en null que especifica el nombre del [*paquete de seguridad*](../secgloss/s-gly.md) con el que se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="1cc79-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="1cc79-117">Se trata de un nombre de [*paquete de seguridad*](../secgloss/s-gly.md) devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="1cc79-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="1cc79-118">Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) con *ULATTRIBUTE* establecido en SECPKG \_ ATTR \_ Package \_ info para devolver información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) en uso.</span><span class="sxs-lookup"><span data-stu-id="1cc79-118">After a context is established, [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="1cc79-119">Al usar el SSP de síntesis, establezca este parámetro en WDIGEST \_ Sp \_ Name.</span><span class="sxs-lookup"><span data-stu-id="1cc79-119">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="1cc79-120">*fCredentialUse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-121">Marca que indica cómo se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="1cc79-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="1cc79-122">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1cc79-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1cc79-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1cc79-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="1cc79-124">Significado</span><span class="sxs-lookup"><span data-stu-id="1cc79-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="1cc79-125"><dt>**SECPKG \_ de \_ entrada de cred**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="1cc79-126">Validar una credencial de servidor entrante.</span><span class="sxs-lookup"><span data-stu-id="1cc79-126">Validate an incoming server credential.</span></span> <span data-ttu-id="1cc79-127">Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) o [**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc79-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) or [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) is called.</span></span> <span data-ttu-id="1cc79-128">Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la \_ \_ autoridad de \_ autenticación \_ .</span><span class="sxs-lookup"><span data-stu-id="1cc79-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="1cc79-129">La validación es específica del paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc79-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="1cc79-130"><dt>**SECPKG \_ CRED \_ saliente**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="1cc79-131">Permitir una credencial de cliente local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="1cc79-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="1cc79-132">*pvLogonID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-132">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-133">Un puntero a un [*identificador local único*](../secgloss/l-gly.md) (LUID) que identifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="1cc79-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="1cc79-134">Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red.</span><span class="sxs-lookup"><span data-stu-id="1cc79-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="1cc79-135">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1cc79-135">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cc79-136">*pAuthData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-136">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-137">Puntero a datos específicos del paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc79-137">A pointer to package-specific data.</span></span> <span data-ttu-id="1cc79-138">Este parámetro puede ser **null**, lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc79-138">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="1cc79-139">Para usar las credenciales proporcionadas, pase una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que incluya esas credenciales en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="1cc79-139">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="1cc79-140">El tiempo de ejecución de RPC pasa todo lo que se proporcionó en [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="1cc79-140">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="1cc79-141">Cuando se usa el SSP de síntesis, este parámetro es un puntero a una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que contiene la información de autenticación que se va a usar para buscar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="1cc79-141">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

</dd> <dt>

<span data-ttu-id="1cc79-142">*pGetKeyFn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-143">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="1cc79-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cc79-144">*pvGetKeyArgument* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-145">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="1cc79-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cc79-146">*phCredential* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-147">Puntero a una estructura [CredHandle](sspi-handles.md) para recibir el identificador de la credencial.</span><span class="sxs-lookup"><span data-stu-id="1cc79-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="1cc79-148">*ptsExpiry* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc79-149">Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas.</span><span class="sxs-lookup"><span data-stu-id="1cc79-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="1cc79-150">El valor devuelto en esta estructura de **marca** de tiempo depende de la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1cc79-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1cc79-151">El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.</span><span class="sxs-lookup"><span data-stu-id="1cc79-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="1cc79-152">Este parámetro se establece en un tiempo máximo constante.</span><span class="sxs-lookup"><span data-stu-id="1cc79-152">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="1cc79-153">No hay ningún tiempo de expiración para las credenciales o el [*contexto de seguridad*](../secgloss/s-gly.md)implícita o cuando se usa el SSP de síntesis.</span><span class="sxs-lookup"><span data-stu-id="1cc79-153">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc79-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cc79-154">Return value</span></span>

<span data-ttu-id="1cc79-155">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1cc79-155">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="1cc79-156">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1cc79-156">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="1cc79-157">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1cc79-157">Return code</span></span>                                                                                                 | <span data-ttu-id="1cc79-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cc79-158">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cc79-159"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-159"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="1cc79-160">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="1cc79-160">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="1cc79-161"><dt>**s \_ E \_ interno \_ error**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-161"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="1cc79-162">Error que no se ha asignado a un código de error SSPI.</span><span class="sxs-lookup"><span data-stu-id="1cc79-162">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="1cc79-163"><dt>**s \_ E \_ sin \_ credenciales**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-163"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="1cc79-164">No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1cc79-164">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="1cc79-165"><dt>**s \_ E \_ no \_ propietario**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-165"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="1cc79-166">El autor de la llamada de la función no tiene las credenciales necesarias.</span><span class="sxs-lookup"><span data-stu-id="1cc79-166">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="1cc79-167"><dt>**s \_ E \_ SECPKG \_ no \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-167"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="1cc79-168">El [*paquete de seguridad*](../secgloss/s-gly.md) solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="1cc79-168">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="1cc79-169"><dt>**s \_ E \_ credenciales desconocidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-169"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="1cc79-170">No se reconocieron las credenciales proporcionadas al paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc79-170">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1cc79-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cc79-171">Remarks</span></span>

<span data-ttu-id="1cc79-172">La función **AcquireCredentialsHandle (síntesis)** devuelve un identificador para las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa una [*delegación restringida*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="1cc79-172">The **AcquireCredentialsHandle (Digest)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1cc79-173">Puede ser el identificador de las credenciales preexistentes o la función puede crear un nuevo conjunto de credenciales y devolverlo.</span><span class="sxs-lookup"><span data-stu-id="1cc79-173">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="1cc79-174">Este identificador se puede utilizar en llamadas posteriores a las funciones [**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md) y [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc79-174">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span>

<span data-ttu-id="1cc79-175">En general, **AcquireCredentialsHandle (digest)** no permite a un proceso obtener un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="1cc79-175">In general, **AcquireCredentialsHandle (Digest)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="1cc79-176">Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/s-gly.md) ' TCB name ' tiene la opción de especificar el [*identificador de inicio de sesión*](../secgloss/l-gly.md) (LUID) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1cc79-176">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="1cc79-177">Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="1cc79-177">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="1cc79-178">Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="1cc79-178">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="1cc79-179">Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1cc79-179">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="1cc79-180">En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:</span><span class="sxs-lookup"><span data-stu-id="1cc79-180">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="1cc79-181">Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc79-181">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="1cc79-182">Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.</span><span class="sxs-lookup"><span data-stu-id="1cc79-182">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="1cc79-183">Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="1cc79-183">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc79-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc79-184">Requirements</span></span>



| <span data-ttu-id="1cc79-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc79-185">Requirement</span></span> | <span data-ttu-id="1cc79-186">Value</span><span class="sxs-lookup"><span data-stu-id="1cc79-186">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc79-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cc79-187">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc79-188">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-188">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1cc79-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cc79-189">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc79-190">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cc79-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1cc79-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cc79-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc79-192"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-192"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="1cc79-193">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cc79-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cc79-194"><dt>SECUR32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-194"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="1cc79-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1cc79-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cc79-196"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc79-196"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="1cc79-197">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1cc79-197">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1cc79-198">**AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1cc79-198">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1cc79-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cc79-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc79-200">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="1cc79-200">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="1cc79-201">**AcceptSecurityContext (Resumen)**</span><span class="sxs-lookup"><span data-stu-id="1cc79-201">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="1cc79-202">**InitializeSecurityContext (Resumen)**</span><span class="sxs-lookup"><span data-stu-id="1cc79-202">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="1cc79-203">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="1cc79-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
