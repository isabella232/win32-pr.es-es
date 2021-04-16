---
description: Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa Kerberos.
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: Función AcquireCredentialsHandle (Kerberos) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 05a4dd885712e89b812896684f73d60df610e41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720662"
---
# <a name="acquirecredentialshandle-kerberos-function"></a><span data-ttu-id="d90b3-103">Función AcquireCredentialsHandle (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="d90b3-103">AcquireCredentialsHandle (Kerberos) function</span></span>

<span data-ttu-id="d90b3-104">La función **AcquireCredentialsHandle (Kerberos)** adquiere un identificador a las credenciales preexistentes de una [*entidad de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d90b3-104">The **AcquireCredentialsHandle (Kerberos)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d90b3-105">Este identificador es necesario para las funciones [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) y [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="d90b3-105">This handle is required by the [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) and [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) functions.</span></span> <span data-ttu-id="d90b3-106">Pueden ser *credenciales* preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.</span><span class="sxs-lookup"><span data-stu-id="d90b3-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="d90b3-107">No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="d90b3-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d90b3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d90b3-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d90b3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d90b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d90b3-110">*pszPrincipal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-111">Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.</span><span class="sxs-lookup"><span data-stu-id="d90b3-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="d90b3-112">Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d90b3-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="d90b3-113">Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo [*contexto de seguridad*](../secgloss/s-gly.md) se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d90b3-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="d90b3-114">*pszPackage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-115">Puntero a una cadena terminada en null que especifica el nombre del [*paquete de seguridad*](../secgloss/s-gly.md) con el que se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="d90b3-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="d90b3-116">Se trata de un nombre de [*paquete de seguridad*](../secgloss/s-gly.md) devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="d90b3-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="d90b3-117">Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) con *ULATTRIBUTE* establecido en SECPKG \_ ATTR \_ Package \_ info para devolver información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) en uso.</span><span class="sxs-lookup"><span data-stu-id="d90b3-117">After a context is established, [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="d90b3-118">*fCredentialUse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-119">Marca que indica cómo se utilizarán estas credenciales.</span><span class="sxs-lookup"><span data-stu-id="d90b3-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="d90b3-120">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d90b3-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d90b3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d90b3-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="d90b3-122">Significado</span><span class="sxs-lookup"><span data-stu-id="d90b3-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="d90b3-123"><dt>**SECPKG \_ CRED \_ both**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="d90b3-124">Validar una credencial entrante o usar una credencial local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="d90b3-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="d90b3-125">Esta marca habilita ambos marcadores.</span><span class="sxs-lookup"><span data-stu-id="d90b3-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="d90b3-126"><dt>**SECPKG \_ de \_ entrada de cred**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="d90b3-127">Validar una credencial de servidor entrante.</span><span class="sxs-lookup"><span data-stu-id="d90b3-127">Validate an incoming server credential.</span></span> <span data-ttu-id="d90b3-128">Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) o [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="d90b3-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) or [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) is called.</span></span> <span data-ttu-id="d90b3-129">Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la \_ \_ autoridad de \_ autenticación \_ .</span><span class="sxs-lookup"><span data-stu-id="d90b3-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="d90b3-130">La validación es específica del paquete.</span><span class="sxs-lookup"><span data-stu-id="d90b3-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="d90b3-131"><dt>**SECPKG \_ CRED \_ saliente**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="d90b3-132">Permitir una credencial de cliente local para preparar un token saliente.</span><span class="sxs-lookup"><span data-stu-id="d90b3-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="d90b3-133">*pvLogonID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-134">Un puntero a un [*identificador local único*](../secgloss/l-gly.md) (LUID) que identifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="d90b3-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="d90b3-135">Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red.</span><span class="sxs-lookup"><span data-stu-id="d90b3-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="d90b3-136">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d90b3-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d90b3-137">*pAuthData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-138">Puntero a datos específicos del paquete.</span><span class="sxs-lookup"><span data-stu-id="d90b3-138">A pointer to package-specific data.</span></span> <span data-ttu-id="d90b3-139">Este parámetro puede ser **null**, lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d90b3-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="d90b3-140">Para usar las credenciales proporcionadas, pase una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que incluya esas credenciales en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="d90b3-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="d90b3-141">El tiempo de ejecución de RPC pasa todo lo que se proporcionó en [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="d90b3-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

</dd> <dt>

<span data-ttu-id="d90b3-142">*pGetKeyFn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-143">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="d90b3-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d90b3-144">*pvGetKeyArgument* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-145">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="d90b3-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d90b3-146">*phCredential* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-147">Puntero a una estructura [CredHandle](sspi-handles.md) para recibir el identificador de la credencial.</span><span class="sxs-lookup"><span data-stu-id="d90b3-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="d90b3-148">*ptsExpiry* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b3-149">Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas.</span><span class="sxs-lookup"><span data-stu-id="d90b3-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="d90b3-150">El valor devuelto en esta estructura de **marca** de tiempo depende de la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d90b3-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d90b3-151">El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.</span><span class="sxs-lookup"><span data-stu-id="d90b3-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d90b3-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d90b3-152">Return value</span></span>

<span data-ttu-id="d90b3-153">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d90b3-153">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="d90b3-154">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="d90b3-154">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="d90b3-155">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d90b3-155">Return code</span></span>                                                                                                 | <span data-ttu-id="d90b3-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="d90b3-156">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d90b3-157"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-157"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="d90b3-158">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="d90b3-158">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="d90b3-159"><dt>**s \_ E \_ interno \_ error**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-159"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="d90b3-160">Error que no se ha asignado a un código de error SSPI.</span><span class="sxs-lookup"><span data-stu-id="d90b3-160">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="d90b3-161"><dt>**s \_ E \_ sin \_ credenciales**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-161"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="d90b3-162">No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d90b3-162">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="d90b3-163"><dt>**s \_ E \_ no \_ propietario**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-163"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="d90b3-164">El autor de la llamada de la función no tiene las credenciales necesarias.</span><span class="sxs-lookup"><span data-stu-id="d90b3-164">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="d90b3-165"><dt>**s \_ E \_ SECPKG \_ no \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-165"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="d90b3-166">El [*paquete de seguridad*](../secgloss/s-gly.md) solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="d90b3-166">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="d90b3-167"><dt>**s \_ E \_ credenciales desconocidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-167"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="d90b3-168">No se reconocieron las credenciales proporcionadas al paquete.</span><span class="sxs-lookup"><span data-stu-id="d90b3-168">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d90b3-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d90b3-169">Remarks</span></span>

<span data-ttu-id="d90b3-170">La función **AcquireCredentialsHandle (Kerberos)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa una [*delegación restringida*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="d90b3-170">The **AcquireCredentialsHandle (Kerberos)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d90b3-171">Puede ser el identificador de las credenciales preexistentes o la función puede crear un nuevo conjunto de credenciales y devolverlo.</span><span class="sxs-lookup"><span data-stu-id="d90b3-171">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="d90b3-172">Este identificador se puede utilizar en llamadas posteriores a las funciones [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) y [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="d90b3-172">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) and [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) functions.</span></span>

<span data-ttu-id="d90b3-173">En general, **AcquireCredentialsHandle (Kerberos)** no permite a un proceso obtener un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="d90b3-173">In general, **AcquireCredentialsHandle (Kerberos)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="d90b3-174">Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/s-gly.md) ' TCB name ' tiene la opción de especificar el [*identificador de inicio de sesión*](../secgloss/l-gly.md) (LUID) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d90b3-174">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="d90b3-175">Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="d90b3-175">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="d90b3-176">Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="d90b3-176">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="d90b3-177">Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d90b3-177">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="d90b3-178">En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:</span><span class="sxs-lookup"><span data-stu-id="d90b3-178">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="d90b3-179">Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d90b3-179">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="d90b3-180">Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.</span><span class="sxs-lookup"><span data-stu-id="d90b3-180">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="d90b3-181">Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="d90b3-181">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d90b3-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d90b3-182">Requirements</span></span>



| <span data-ttu-id="d90b3-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="d90b3-183">Requirement</span></span> | <span data-ttu-id="d90b3-184">Value</span><span class="sxs-lookup"><span data-stu-id="d90b3-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d90b3-185">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d90b3-185">Minimum supported client</span></span><br/> | <span data-ttu-id="d90b3-186">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-186">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d90b3-187">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d90b3-187">Minimum supported server</span></span><br/> | <span data-ttu-id="d90b3-188">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d90b3-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d90b3-189">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d90b3-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="d90b3-190"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-190"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="d90b3-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d90b3-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="d90b3-192"><dt>SECUR32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-192"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="d90b3-193">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d90b3-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d90b3-194"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d90b3-194"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="d90b3-195">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d90b3-195">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d90b3-196">**AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d90b3-196">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d90b3-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="d90b3-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90b3-198">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="d90b3-198">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="d90b3-199">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="d90b3-199">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="d90b3-200">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="d90b3-200">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="d90b3-201">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="d90b3-201">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
