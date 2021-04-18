---
description: Recupera la contraseña de la cuenta de servicio.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Función GetServiceAccountPassword (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688026"
---
# <a name="getserviceaccountpassword-function"></a><span data-ttu-id="06a5b-103">GetServiceAccountPassword función)</span><span class="sxs-lookup"><span data-stu-id="06a5b-103">GetServiceAccountPassword function</span></span>

<span data-ttu-id="06a5b-104">Recupera la contraseña de la cuenta de servicio, disponible para los [*proveedores de compatibilidad para seguridad*](/windows/desktop/SecGloss/s-gly) (SSP), como Kerberos SSP.</span><span class="sxs-lookup"><span data-stu-id="06a5b-104">Retrieves the service account password, available to [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), such as Kerberos SSP.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a5b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06a5b-105">Syntax</span></span>


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a><span data-ttu-id="06a5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06a5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a5b-107">*AccountName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-107">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a5b-108">Nombre de cuenta terminada en NULL de la cuenta de la cuenta de servicio administrada de grupo (gMSA).</span><span class="sxs-lookup"><span data-stu-id="06a5b-108">Null-terminated account name of the Group Managed Service Account (gMSA) account.</span></span> <span data-ttu-id="06a5b-109">El nombre de usuario puede ser uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="06a5b-109">The user name can be one of the following forms:</span></span>

-   <span data-ttu-id="06a5b-110">Nombre de cuenta SAM del gMSA.</span><span class="sxs-lookup"><span data-stu-id="06a5b-110">SAM account name of the gMSA.</span></span>
-   <span data-ttu-id="06a5b-111">Nombre de usuario en un nombre de dominio completo (FQDN), como *domainname \* **\\** _username_ o **www.** _dominio_* de _. com \\_ \* _nombre_.</span><span class="sxs-lookup"><span data-stu-id="06a5b-111">User name in a fully qualified domain name (FQDN), such as *DomainName\***\\**_UserName_ or **www.**_domain_*_.com\\_\*_name_.</span></span> <span data-ttu-id="06a5b-112">El nombre de usuario debe ser un nombre de SAM únicamente.</span><span class="sxs-lookup"><span data-stu-id="06a5b-112">The user name must be a SAM name only.</span></span> <span data-ttu-id="06a5b-113">El nombre de dominio puede ser un nombre DNS o un nombre NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="06a5b-113">The domain name can be a DNS name or a NetBIOS name.</span></span>
-   <span data-ttu-id="06a5b-114">Nombre principal de usuario (UPN) implícito para la cuenta de gMSA, por ejemplo, *SomeName \* **@** _Domain_*_. com_\*, donde, según la definición de un UPN implícito, el *dominio \* \* *. com** es el nombre DNS real del dominio.</span><span class="sxs-lookup"><span data-stu-id="06a5b-114">Implicit user principal name (UPN) for the gMSA account, for example, *SomeName\***@**_Domain_*_.com_\* where, according to the definition of an implicit UPN, the *Domain\*\*\*.com*\* is the actual domain DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="06a5b-115">*Dominio* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-115">*DomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06a5b-116">Nombre de dominio opcional terminado en NULL.</span><span class="sxs-lookup"><span data-stu-id="06a5b-116">Optional null-terminated domain name.</span></span> <span data-ttu-id="06a5b-117">Esto solo es válido si el parámetro *AccountName* es un nombre de cuenta SAM.</span><span class="sxs-lookup"><span data-stu-id="06a5b-117">This is valid only if the *AccountName* parameter is a SAM account name.</span></span> <span data-ttu-id="06a5b-118">El nombre de dominio solo puede ser un nombre NetBIOS o un nombre de dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="06a5b-118">The domain name can only be a NetBIOS name or a fully qualified domain name (FQDN).</span></span>

</dd> <dt>

<span data-ttu-id="06a5b-119">*CredFetch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-119">*CredFetch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a5b-120">Un valor de la enumeración [**CRED \_ Fetch**](cred-fetch.md) que especifica cómo recuperar la credencial.</span><span class="sxs-lookup"><span data-stu-id="06a5b-120">A value of the [**CRED\_FETCH**](cred-fetch.md) enumeration that specifies how to retrieve the credential.</span></span>



| <span data-ttu-id="06a5b-121">Value</span><span class="sxs-lookup"><span data-stu-id="06a5b-121">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="06a5b-122">Significado</span><span class="sxs-lookup"><span data-stu-id="06a5b-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <span data-ttu-id="06a5b-123"><dt>**CredFetchDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="06a5b-123"><dt>**CredFetchDefault**</dt></span></span> </dl> | <span data-ttu-id="06a5b-124">El sistema operativo primero intenta recuperar la contraseña de la memoria caché local si no es hora de capturar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="06a5b-124">The operating system first attempts to retrieve the password from the local cache if it is not time to fetch the password.</span></span> <span data-ttu-id="06a5b-125">Si es el momento de capturar la contraseña, el sistema operativo se pone en contacto con el controlador de dominio; de lo contrario, devuelve cualquier contraseña almacenada en caché con un valor de estado correcto.</span><span class="sxs-lookup"><span data-stu-id="06a5b-125">If it is time to fetch the password, then the operating system contacts the domain controller, otherwise, return any cached passwords with a status value of success.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <span data-ttu-id="06a5b-126"><dt>**CredFetchDPAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="06a5b-126"><dt>**CredFetchDPAPI**</dt></span></span> </dl>         | <span data-ttu-id="06a5b-127">Devuelve la credencial DPAPI local al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="06a5b-127">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="06a5b-128">Los SSP generalmente no requieren el uso de este valor.</span><span class="sxs-lookup"><span data-stu-id="06a5b-128">SSPs generally would not require use of this value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <span data-ttu-id="06a5b-129"><dt>**CredFetchForced**</dt></span><span class="sxs-lookup"><span data-stu-id="06a5b-129"><dt>**CredFetchForced**</dt></span></span> </dl>     | <span data-ttu-id="06a5b-130">Obliga al sistema operativo a intentar leer la contraseña del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="06a5b-130">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="06a5b-131">Durante el tiempo de sustitución de contraseña, la contraseña puede haber cambiado en el controlador de dominio y en otros hosts miembros, pero el host miembro gMSA reconoce la contraseña como todavía válida.</span><span class="sxs-lookup"><span data-stu-id="06a5b-131">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="06a5b-132">Esto puede ocurrir debido a problemas de sesgo del reloj entre distintos controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="06a5b-132">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="06a5b-133">Cuando se especifica este valor, el sistema operativo determina si puede haber un posible cambio de contraseña debido al sesgo del reloj y, en caso afirmativo, recupera la contraseña.</span><span class="sxs-lookup"><span data-stu-id="06a5b-133">When this value is specified, the operating system determines if there could be a possible password change due to clock skew and if so, retrieves the password.</span></span> <span data-ttu-id="06a5b-134">De lo contrario, se devuelve la credencial almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="06a5b-134">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="06a5b-135">Si no hay ninguna credencial almacenada en caché, el sistema operativo intenta obtener una del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="06a5b-135">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06a5b-136">*FileTimeExpiry* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-136">*FileTimeExpiry* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06a5b-137">En la entrada, si este valor no es NULL y no es un **FILETIME** de cero, *FileTimeExpiry* contiene la hora de expiración de las credenciales de la cuenta de servicio que conoce el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="06a5b-137">On input, if this value is nonnull and is not a zero **FILETIME**, *FileTimeExpiry* contains the expiry time of the service account credentials as known to the caller.</span></span> <span data-ttu-id="06a5b-138">Si el parámetro *FileTimeExpiry* es el mismo que el de una de las credenciales actuales, se produce un error en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="06a5b-138">If the *FileTimeExpiry* parameter is the same as one of the current credentials, this call fails.</span></span> <span data-ttu-id="06a5b-139">En la salida, el parámetro *FileTimeExpiry* contiene la hora de expiración de la credencial que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="06a5b-139">On output, the *FileTimeExpiry* parameter contains the expiry time of the credential being returned.</span></span>

</dd> <dt>

<span data-ttu-id="06a5b-140">*CurrentPassword* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-140">*CurrentPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06a5b-141">La contraseña actual de gMSA.</span><span class="sxs-lookup"><span data-stu-id="06a5b-141">The current password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="06a5b-142">*PreviousPassword* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-142">*PreviousPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06a5b-143">La contraseña anterior de gMSA.</span><span class="sxs-lookup"><span data-stu-id="06a5b-143">The previous password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="06a5b-144">*FileTimeCurrPwdValidForOutbound* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-144">*FileTimeCurrPwdValidForOutbound* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06a5b-145">Denota el tiempo después del cual la contraseña actual es válida para las solicitudes salientes.</span><span class="sxs-lookup"><span data-stu-id="06a5b-145">Denotes the time after which the current password is valid for outbound requests.</span></span> <span data-ttu-id="06a5b-146">El autor de la llamada debe comparar la hora actual con este valor y usar la contraseña actual devuelta solo si la hora actual es mayor o igual que el valor devuelto por este parámetro.</span><span class="sxs-lookup"><span data-stu-id="06a5b-146">The caller should compare the current time with this value and use the current password returned only if the current time is greater than or equal to the value returned by this parameter.</span></span> <span data-ttu-id="06a5b-147">El uso de este parámetro está diseñado para llamadores que no tienen reintentos en la lógica de salida, por ejemplo, NTLM.</span><span class="sxs-lookup"><span data-stu-id="06a5b-147">The use of this parameter is designed for callers that do not have retry in the outbound logic, for example, NTLM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a5b-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06a5b-148">Return value</span></span>

<span data-ttu-id="06a5b-149">Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success.</span><span class="sxs-lookup"><span data-stu-id="06a5b-149">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="06a5b-150">Si se produce un error en la función, el valor devuelto es un código NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="06a5b-150">If the function fails, the return value is an NTSTATUS code.</span></span> <span data-ttu-id="06a5b-151">Para obtener más información, vea [valores devueltos de la función de directiva LSA](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="06a5b-151">For more information, see [LSA Policy Function Return Values](management-return-values.md).</span></span>

<span data-ttu-id="06a5b-152">Puede usar la función [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) para convertir el código NTSTATUS en un código de error de Windows.</span><span class="sxs-lookup"><span data-stu-id="06a5b-152">You can use the [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) function to convert the NTSTATUS code to a Windows error code.</span></span>

<span data-ttu-id="06a5b-153">Cuando haya terminado de usar los búferes devueltos en los parámetros *CurrentPassword* y *PreviousPassword* , liberelos mediante una llamada a la función [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .</span><span class="sxs-lookup"><span data-stu-id="06a5b-153">When you have finished using the buffers returned in the *CurrentPassword* and *PreviousPassword* parameters, free them by calling the [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a5b-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06a5b-154">Remarks</span></span>

<span data-ttu-id="06a5b-155">Se puede llamar a la función **GetServiceAccountPassword** en los escenarios siguientes:</span><span class="sxs-lookup"><span data-stu-id="06a5b-155">The **GetServiceAccountPassword** function can be called in the following scenarios:</span></span>

-   <span data-ttu-id="06a5b-156">En las funciones de inicio de sesión de los proveedores de compatibilidad para seguridad (SSP), el SSP debe detectar que la contraseña de la cuenta de servicio \_ \_ se utiliza para iniciar sesión en la entidad y debe comprobar que el autor de la llamada tiene privilegios TCB o es un servicio de red.</span><span class="sxs-lookup"><span data-stu-id="06a5b-156">From the logon functions of Security Support Providers (SSP), the SSP should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used to log on to the entity and should check that the caller has TCB privilege or is a network service.</span></span> <span data-ttu-id="06a5b-157">Después, el SSP debe permitir que el proceso de inicio de sesión continúe obteniendo la credencial más reciente mediante una llamada a la función **GetServiceAccountPassword** con el valor **CredFetchDefault** en la enumeración de [**\_ recopilación de credenciales**](cred-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="06a5b-157">Then the SSP should allow the log on process to proceed by getting the latest credential by calling the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration.</span></span>

-   <span data-ttu-id="06a5b-158">Desde SSP en sus llamadas [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) y [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="06a5b-158">From SSPs in their [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) and [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) calls.</span></span> <span data-ttu-id="06a5b-159">Los SSP deben detectar que la \_ \_ contraseña de la cuenta de servicio se utiliza para estas llamadas y, si la llamada es para las credenciales no principales, el SSP debe asegurarse de que el autor de la llamada tenga privilegios TCB o sea un servicio de red.</span><span class="sxs-lookup"><span data-stu-id="06a5b-159">SSPs should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used for these calls, and if the call is for nonprimary credentials, then the SSP should ensure that the caller has either TCB privilege or is a network service.</span></span> <span data-ttu-id="06a5b-160">A continuación, el SSP debe llamar a la función **GetServiceAccountPassword** con el valor **CredFetchDefault** en la enumeración de [**\_ recopilación de credenciales**](cred-fetch.md) y continuar con la llamada.</span><span class="sxs-lookup"><span data-stu-id="06a5b-160">Then the SSP should call the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration and proceed with the call.</span></span> <span data-ttu-id="06a5b-161">Si se produce un error en las llamadas a **InitializeSecurityContext** y **ACCEPTSECURITYCONTEXT** , el SSP debe usar el *FileTimeExpiry* recuperado de la llamada anterior a **GetServiceAccountPassword** y usarlo como entrada para llamar a **GetServiceAccountPassword** de nuevo con el valor **CredFetchForced** en la enumeración de **\_ recopilación de credenciales** .</span><span class="sxs-lookup"><span data-stu-id="06a5b-161">If the **InitializeSecurityContext** and **AcceptSecurityContext** calls fail, then the SSP should use the *FileTimeExpiry* retrieved from the previous call to **GetServiceAccountPassword** and use it as input to calling **GetServiceAccountPassword** again using the **CredFetchForced** value in the **CRED\_FETCH** enumeration.</span></span> <span data-ttu-id="06a5b-162">Si hay disponible una nueva credencial de gMSA, la segunda llamada se realizará correctamente con nuevas credenciales y el SSP debe volver a intentarlo con las nuevas credenciales.</span><span class="sxs-lookup"><span data-stu-id="06a5b-162">If a new gMSA credential is available, the second call will succeed with new credentials, and the SSP should then retry with the new credentials.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a5b-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06a5b-163">Requirements</span></span>



| <span data-ttu-id="06a5b-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="06a5b-164">Requirement</span></span> | <span data-ttu-id="06a5b-165">Value</span><span class="sxs-lookup"><span data-stu-id="06a5b-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06a5b-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06a5b-166">Minimum supported client</span></span><br/> | <span data-ttu-id="06a5b-167">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-167">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="06a5b-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06a5b-168">Minimum supported server</span></span><br/> | <span data-ttu-id="06a5b-169">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="06a5b-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="06a5b-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06a5b-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="06a5b-171"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="06a5b-171"><dt>Secpkg.h</dt></span></span> </dl> |



 

