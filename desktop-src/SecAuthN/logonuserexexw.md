---
description: La función LogonUserExExW intenta iniciar una sesión de usuario en el equipo local.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Función LogonUserExExW (Winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083155"
---
# <a name="logonuserexexw-function"></a><span data-ttu-id="a728a-103">LogonUserExExW función)</span><span class="sxs-lookup"><span data-stu-id="a728a-103">LogonUserExExW function</span></span>

<span data-ttu-id="a728a-104">La función **LogonUserExExW** intenta iniciar una sesión de usuario en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="a728a-104">The **LogonUserExExW** function attempts to log a user on to the local computer.</span></span> <span data-ttu-id="a728a-105">El equipo local es el equipo desde el que se llamó a **LogonUserExExW** .</span><span class="sxs-lookup"><span data-stu-id="a728a-105">The local computer is the computer from which **LogonUserExExW** was called.</span></span> <span data-ttu-id="a728a-106">No se puede usar **LogonUserExExW** para iniciar sesión en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="a728a-106">You cannot use **LogonUserExExW** to log on to a remote computer.</span></span> <span data-ttu-id="a728a-107">Especifique el usuario mediante un nombre de usuario y un dominio y [*autentique*](../secgloss/a-gly.md) al usuario mediante una contraseña de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="a728a-107">Specify the user by using a user name and domain and [*authenticate*](../secgloss/a-gly.md) the user by using a plaintext password.</span></span> <span data-ttu-id="a728a-108">Si la función se ejecuta correctamente, recibe un identificador de un token que representa al usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-108">If the function succeeds, it receives a handle to a token that represents the logged-on user.</span></span> <span data-ttu-id="a728a-109">Después, puede usar este identificador de token para suplantar al usuario especificado o, en la mayoría de los casos, crear un [*proceso*](../secgloss/p-gly.md) que se ejecute en el contexto del usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="a728a-109">You can then use this token handle to impersonate the specified user or, in most cases, to create a [*process*](../secgloss/p-gly.md) that runs in the context of the specified user.</span></span>

<span data-ttu-id="a728a-110">Esta función es similar a la función [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , salvo que toma el parámetro adicional, *pTokenGroups*, que es un conjunto de uno o varios [*identificadores de seguridad*](../secgloss/s-gly.md) (SID) que se agregan al token que se devuelve al autor de la llamada cuando el inicio de sesión se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a728a-110">This function is similar to the [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) function, except that it takes the additional parameter, *pTokenGroups*, which is a set of one or more [*security identifiers*](../secgloss/s-gly.md) (SIDs) that are added to the token returned to the caller when the logon is successful.</span></span>

<span data-ttu-id="a728a-111">Esta función no se declara en un encabezado público y no tiene asociada ninguna biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="a728a-111">This function is not declared in a public header and has no associated import library.</span></span> <span data-ttu-id="a728a-112">Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a728a-112">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="a728a-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a728a-113">Syntax</span></span>


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a><span data-ttu-id="a728a-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a728a-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a728a-115">*lpszUsername* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a728a-115">*lpszUsername* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-116">Puntero a una cadena terminada en null que especifica el nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="a728a-116">A pointer to a null-terminated string that specifies the name of the user.</span></span> <span data-ttu-id="a728a-117">Es el nombre de la cuenta de usuario en la que se va a iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-117">This is the name of the user account to log on to.</span></span> <span data-ttu-id="a728a-118">Si usa el formato de [*nombre principal de usuario*](../secgloss/u-gly.md) (UPN), el parámetro *LpszDomain* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a728a-118">If you use the [*user principal name*](../secgloss/u-gly.md) (UPN) format, the *lpszDomain* parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a728a-119">*lpszDomain* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-119">*lpszDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-120">Un puntero a una cadena terminada en null que especifica el nombre del dominio o servidor cuya base de datos de cuenta contiene la cuenta *lpszUsername* .</span><span class="sxs-lookup"><span data-stu-id="a728a-120">A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the *lpszUsername* account.</span></span> <span data-ttu-id="a728a-121">Si este parámetro es **null**, el nombre de usuario debe especificarse en formato UPN.</span><span class="sxs-lookup"><span data-stu-id="a728a-121">If this parameter is **NULL**, the user name must be specified in UPN format.</span></span> <span data-ttu-id="a728a-122">Si este parámetro es ".", la función valida la cuenta usando solo la base de datos de la cuenta local.</span><span class="sxs-lookup"><span data-stu-id="a728a-122">If this parameter is ".", the function validates the account by using only the local account database.</span></span>

</dd> <dt>

<span data-ttu-id="a728a-123">*lpszPassword* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-123">*lpszPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-124">Puntero a una cadena terminada en null que especifica la contraseña de texto no cifrado para la cuenta de usuario especificada por *lpszUsername*.</span><span class="sxs-lookup"><span data-stu-id="a728a-124">A pointer to a null-terminated string that specifies the plaintext password for the user account specified by *lpszUsername*.</span></span> <span data-ttu-id="a728a-125">Cuando haya terminado de usar la contraseña, borre la contraseña de la memoria mediante una llamada a la función [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a728a-125">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="a728a-126">Para obtener más información sobre cómo proteger las contraseñas, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="a728a-126">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="a728a-127">*dwLogonType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a728a-127">*dwLogonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-128">Tipo de operación de inicio de sesión que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="a728a-128">The type of logon operation to perform.</span></span> <span data-ttu-id="a728a-129">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a728a-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a728a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a728a-130">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="a728a-131">Significado</span><span class="sxs-lookup"><span data-stu-id="a728a-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <span data-ttu-id="a728a-132"><dt>**LOGON32 \_ Inicio de sesión \_ interactivo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-132"><dt>**LOGON32\_LOGON\_INTERACTIVE**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="a728a-133">Este tipo de inicio de sesión está destinado a usuarios que van a usar el equipo de forma interactiva, como un usuario que inicia sesión en un servidor de [*terminal*](../secgloss/t-gly.md) Server, un shell remoto o un proceso similar.</span><span class="sxs-lookup"><span data-stu-id="a728a-133">This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a [*terminal*](../secgloss/t-gly.md) server, remote shell, or similar process.</span></span> <span data-ttu-id="a728a-134">Este tipo de inicio de sesión tiene el gasto adicional de almacenar en caché la información de inicio de sesión para las operaciones desconectadas. por lo tanto, no es apropiado para algunas aplicaciones cliente/servidor, como un servidor de correo.</span><span class="sxs-lookup"><span data-stu-id="a728a-134">This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.</span></span><br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <span data-ttu-id="a728a-135"><dt>**LOGON32 \_ \_Red de inicio de sesión**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-135"><dt>**LOGON32\_LOGON\_NETWORK**</dt> <dt>3</dt></span></span> </dl>                                | <span data-ttu-id="a728a-136">Este tipo de inicio de sesión está diseñado para servidores de alto rendimiento para autenticar contraseñas de texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="a728a-136">This logon type is intended for high performance servers to authenticate plaintext passwords.</span></span> <span data-ttu-id="a728a-137">La función **LogonUserExExW** no almacena en caché las credenciales para este tipo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-137">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <span data-ttu-id="a728a-138"><dt>**LOGON32 \_ \_Lote de inicio de sesión**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-138"><dt>**LOGON32\_LOGON\_BATCH**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="a728a-139">Este tipo de inicio de sesión está pensado para los servidores de batch, donde los procesos se pueden ejecutar en nombre de un usuario sin su intervención directa.</span><span class="sxs-lookup"><span data-stu-id="a728a-139">This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.</span></span> <span data-ttu-id="a728a-140">Este tipo también es para servidores de mayor rendimiento que procesan muchos intentos de autenticación de texto simple a la vez, como servidores web o de correo.</span><span class="sxs-lookup"><span data-stu-id="a728a-140">This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="a728a-141">La función **LogonUserExExW** no almacena en caché las credenciales para este tipo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-141">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <span data-ttu-id="a728a-142"><dt>**LOGON32 \_ \_Servicio de inicio de sesión**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-142"><dt>**LOGON32\_LOGON\_SERVICE**</dt> <dt>5</dt></span></span> </dl>                                | <span data-ttu-id="a728a-143">Indica un inicio de sesión de tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="a728a-143">Indicates a service-type logon.</span></span> <span data-ttu-id="a728a-144">La cuenta proporcionada debe tener habilitado el privilegio de servicio.</span><span class="sxs-lookup"><span data-stu-id="a728a-144">The account provided must have the service privilege enabled.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <span data-ttu-id="a728a-145"><dt>**LOGON32 \_ \_Desbloqueo de inicio de sesión**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-145"><dt>**LOGON32\_LOGON\_UNLOCK**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="a728a-146">Este tipo de inicio de sesión es para los archivos dll de [*Gina*](../secgloss/g-gly.md) que inician sesión en los usuarios que van a usar el equipo de forma interactiva.</span><span class="sxs-lookup"><span data-stu-id="a728a-146">This logon type is for [*GINA*](../secgloss/g-gly.md) DLLs that log on users who will be interactively using the computer.</span></span> <span data-ttu-id="a728a-147">Este tipo de inicio de sesión puede generar un registro de auditoría único que muestra Cuándo se desbloqueó la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a728a-147">This logon type can generate a unique audit record that shows when the workstation was unlocked.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <span data-ttu-id="a728a-148"><dt>**LOGON32 \_ Red de inicio de sesión \_ \_ ClearText**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-148"><dt>**LOGON32\_LOGON\_NETWORK\_CLEARTEXT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="a728a-149">Este tipo de inicio de sesión conserva el nombre y la contraseña en el [*paquete de autenticación*](../secgloss/a-gly.md), lo que permite que el servidor realice conexiones a otros servidores de red durante la suplantación del cliente.</span><span class="sxs-lookup"><span data-stu-id="a728a-149">This logon type preserves the name and password in the [*authentication package*](../secgloss/a-gly.md), which allows the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="a728a-150">Un servidor puede aceptar credenciales de texto simple de un cliente, llamar a **LogonUserExExW**, comprobar que el usuario puede tener acceso al sistema a través de la red y seguir comunicándose con otros servidores.</span><span class="sxs-lookup"><span data-stu-id="a728a-150">A server can accept plaintext credentials from a client, call **LogonUserExExW**, verify that the user can access the system across the network, and still communicate with other servers.</span></span> <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <span data-ttu-id="a728a-151"><dt>**LOGON32 \_ \_ \_ Credenciales nuevas de inicio de sesión**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-151"><dt>**LOGON32\_LOGON\_NEW\_CREDENTIALS**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="a728a-152">Este tipo de inicio de sesión permite que el autor de la llamada Clone su token actual y especifique nuevas credenciales para las conexiones salientes.</span><span class="sxs-lookup"><span data-stu-id="a728a-152">This logon type allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="a728a-153">La nueva sesión de inicio de sesión tiene el mismo identificador local, pero usa credenciales diferentes para otras conexiones de red.</span><span class="sxs-lookup"><span data-stu-id="a728a-153">The new logon session has the same local identifier but uses different credentials for other network connections.</span></span><br/> <span data-ttu-id="a728a-154">Este tipo de inicio de sesión solo es compatible con el proveedor de inicio de sesión **\_ \_ WINNT50 del proveedor LOGON32** .</span><span class="sxs-lookup"><span data-stu-id="a728a-154">This logon type is supported only by the **LOGON32\_PROVIDER\_WINNT50** logon provider.</span></span><br/>                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="a728a-155">*dwLogonProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a728a-155">*dwLogonProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-156">Proveedor de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-156">The logon provider.</span></span> <span data-ttu-id="a728a-157">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a728a-157">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a728a-158">Valor</span><span class="sxs-lookup"><span data-stu-id="a728a-158">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="a728a-159">Significado</span><span class="sxs-lookup"><span data-stu-id="a728a-159">Meaning</span></span>                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <span data-ttu-id="a728a-160"><dt>**\_Valor predeterminado del proveedor LOGON32 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-160"><dt>**LOGON32\_PROVIDER\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="a728a-161">Use el proveedor de inicio de sesión estándar para el sistema.</span><span class="sxs-lookup"><span data-stu-id="a728a-161">Use the standard logon provider for the system.</span></span> <span data-ttu-id="a728a-162">El [*proveedor de seguridad*](../secgloss/s-gly.md) predeterminado es NTLM.</span><span class="sxs-lookup"><span data-stu-id="a728a-162">The default [*security provider*](../secgloss/s-gly.md) is NTLM.</span></span><br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <span data-ttu-id="a728a-163"><dt>**Proveedor de LOGON32 \_ \_ WINNT50**</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-163"><dt>**LOGON32\_PROVIDER\_WINNT50**</dt></span></span> </dl> | <span data-ttu-id="a728a-164">Use el proveedor de inicio de sesión Negotiate.</span><span class="sxs-lookup"><span data-stu-id="a728a-164">Use the negotiate logon provider.</span></span> <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <span data-ttu-id="a728a-165"><dt>**Proveedor de LOGON32 \_ \_ WINNT40**</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-165"><dt>**LOGON32\_PROVIDER\_WINNT40**</dt></span></span> </dl> | <span data-ttu-id="a728a-166">Use el proveedor de inicio de sesión de NTLM.</span><span class="sxs-lookup"><span data-stu-id="a728a-166">Use the NTLM logon provider.</span></span><br/>                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="a728a-167">*pTokenGroups* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-167">*pTokenGroups* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-168">Un puntero a una estructura de [**\_ grupos de tokens**](/windows/win32/api/winnt/ns-winnt-token_groups) que especifica una lista de SID de grupo que se agregan al token que esta función recibe cuando el inicio de sesión se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a728a-168">A pointer to a [**TOKEN\_GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) structure that specifies a list of group SIDs that are added to the token that this function receives upon successful logon.</span></span> <span data-ttu-id="a728a-169">Cualquier SID agregado al token también afecta a la expansión de grupos.</span><span class="sxs-lookup"><span data-stu-id="a728a-169">Any SIDs added to the token also effect group expansion.</span></span> <span data-ttu-id="a728a-170">Por ejemplo, si los SID agregados son miembros de grupos locales, esos grupos también se agregan al token de acceso recibido.</span><span class="sxs-lookup"><span data-stu-id="a728a-170">For example, if the added SIDs are members of local groups, those groups are also added to the received access token.</span></span>

<span data-ttu-id="a728a-171">Si este parámetro no es **null**, el autor de la llamada de esta función debe tener concedidos y habilitados los privilegios de **\_ \_ privilegio** de la TCB.</span><span class="sxs-lookup"><span data-stu-id="a728a-171">If this parameter is not **NULL**, the caller of this function must have the **SE\_TCB\_PRIVILEGE** privilege granted and enabled.</span></span>

</dd> <dt>

<span data-ttu-id="a728a-172">*phToken* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-172">*phToken* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-173">Un puntero a una variable de identificador que recibe un identificador a un token que representa el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="a728a-173">A pointer to a handle variable that receives a handle to a token that represents the specified user.</span></span>

<span data-ttu-id="a728a-174">Puede usar el identificador devuelto en las llamadas a la función [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .</span><span class="sxs-lookup"><span data-stu-id="a728a-174">You can use the returned handle in calls to the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="a728a-175">En la mayoría de los casos, el identificador devuelto es un [*token primario*](../secgloss/p-gly.md) que puede usar en las llamadas a la función [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="a728a-175">In most cases, the returned handle is a [*primary token*](../secgloss/p-gly.md) that you can use in calls to the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="a728a-176">Sin embargo, si especifica la marca de red de inicio de sesión de LOGON32 \_ \_ , **LogonUserExExW** devuelve un [*token de suplantación*](../secgloss/i-gly.md) que no se puede usar en **CreateProcessAsUser** a menos que llame a [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para convertir el token de suplantación en un token primario.</span><span class="sxs-lookup"><span data-stu-id="a728a-176">However, if you specify the LOGON32\_LOGON\_NETWORK flag, **LogonUserExExW** returns an [*impersonation token*](../secgloss/i-gly.md) that you cannot use in **CreateProcessAsUser** unless you call [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) to convert the impersonation token to a primary token.</span></span>

<span data-ttu-id="a728a-177">Cuando ya no necesite este identificador, ciérrelo llamando a la función [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="a728a-177">When you no longer need this handle, close it by calling the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

</dd> <dt>

<span data-ttu-id="a728a-178">*ppLogonSid* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-178">*ppLogonSid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-179">Un puntero a un puntero a un SID que recibe el SID del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-179">A pointer to a pointer to a SID that receives the SID of the user logged on.</span></span>

<span data-ttu-id="a728a-180">Cuando haya terminado de usar el SID, liberelo llamando a la función [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="a728a-180">When you have finished using the SID, free it by calling the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function.</span></span>

</dd> <dt>

<span data-ttu-id="a728a-181">*ppProfileBuffer* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-181">*ppProfileBuffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-182">Un puntero a un puntero que recibe la dirección de un búfer que contiene el perfil del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-182">A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.</span></span>

</dd> <dt>

<span data-ttu-id="a728a-183">*pdwProfileLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-183">*pdwProfileLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-184">Un puntero a un **valor DWORD** que recibe la longitud del búfer de perfil.</span><span class="sxs-lookup"><span data-stu-id="a728a-184">A pointer to a **DWORD** that receives the length of the profile buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a728a-185">*pQuotaLimits* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a728a-185">*pQuotaLimits* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a728a-186">Puntero a una estructura [**de \_ límites de cuota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) que recibe información acerca de las cuotas del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="a728a-186">A pointer to a [**QUOTA\_LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) structure that receives information about the quotas for the logged on user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a728a-187">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a728a-187">Return value</span></span>

<span data-ttu-id="a728a-188">Si la función se ejecuta correctamente, la función devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a728a-188">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="a728a-189">Si se produce un error en la función, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a728a-189">If the function fails, it returns zero.</span></span> <span data-ttu-id="a728a-190">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a728a-190">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a728a-191">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a728a-191">Remarks</span></span>

<span data-ttu-id="a728a-192">El tipo de inicio de sesión de **\_ \_ red de LOGON32 Logon** es más rápido, pero tiene las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="a728a-192">The **LOGON32\_LOGON\_NETWORK** logon type is fastest, but it has the following limitations:</span></span>

-   <span data-ttu-id="a728a-193">La función devuelve un [*token de suplantación*](../secgloss/i-gly.md), no un token primario.</span><span class="sxs-lookup"><span data-stu-id="a728a-193">The function returns an [*impersonation token*](../secgloss/i-gly.md), not a primary token.</span></span> <span data-ttu-id="a728a-194">Este token no se puede usar directamente en la función [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="a728a-194">You cannot use this token directly in the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="a728a-195">Sin embargo, puede llamar a la función [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para convertir el token en un token primario y, a continuación, usarlo en **CreateProcessAsUser**.</span><span class="sxs-lookup"><span data-stu-id="a728a-195">However, you can call the [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) function to convert the token to a primary token, and then use it in **CreateProcessAsUser**.</span></span>
-   <span data-ttu-id="a728a-196">Si convierte el token en un token principal y lo usa en [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar un proceso, el nuevo proceso no puede tener acceso a otros recursos de red, como servidores o impresoras remotos, a través del redirector.</span><span class="sxs-lookup"><span data-stu-id="a728a-196">If you convert the token to a primary token and use it in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector.</span></span> <span data-ttu-id="a728a-197">Una excepción es que si no se controla el acceso al recurso de red, el nuevo proceso podrá tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="a728a-197">An exception is that if the network resource is not access controlled, then the new process will be able to access it.</span></span>

<span data-ttu-id="a728a-198">La cuenta especificada por *lpszUsername* debe tener los derechos de cuenta necesarios.</span><span class="sxs-lookup"><span data-stu-id="a728a-198">The account specified by *lpszUsername* must have the necessary account rights.</span></span> <span data-ttu-id="a728a-199">Por ejemplo, para iniciar la sesión de un usuario con el indicador **\_ \_ interactivo de inicio de sesión de LOGON32** , el usuario (o un grupo al que pertenezca el usuario) debe tener el derecho de cuenta de **\_ \_ \_ nombre de inicio de sesión** de es interactivo.</span><span class="sxs-lookup"><span data-stu-id="a728a-199">For example, to log on a user with the **LOGON32\_LOGON\_INTERACTIVE** flag, the user (or a group to which the user belongs) must have the **SE\_INTERACTIVE\_LOGON\_NAME** account right.</span></span> <span data-ttu-id="a728a-200">Para obtener una lista de los derechos de cuenta que afectan a las distintas operaciones de inicio de sesión, consulte [derechos de acceso a objetos de cuenta](../secmgmt/account-object-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="a728a-200">For a list of the account rights that affect the various logon operations, see [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span></span>

<span data-ttu-id="a728a-201">Se considera que un usuario ha iniciado sesión si existe al menos un token.</span><span class="sxs-lookup"><span data-stu-id="a728a-201">A user is considered logged on if at least one token exists.</span></span> <span data-ttu-id="a728a-202">Si llama a [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) y, a continuación, cierra el token, el usuario seguirá iniciando sesión hasta que finalice el proceso (y todos los procesos secundarios).</span><span class="sxs-lookup"><span data-stu-id="a728a-202">If you call [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) and then close the token, the user is still logged on until the process (and all child processes) have ended.</span></span>

<span data-ttu-id="a728a-203">Si se proporciona el parámetro opcional *pTokenGroups* , LSA no agregará el SID local ni el SID de inicio de sesión automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a728a-203">If the optional *pTokenGroups* parameter is supplied, LSA will not add either the local SID or the logon SID automatically.</span></span>

## <a name="requirements"></a><span data-ttu-id="a728a-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a728a-204">Requirements</span></span>



| <span data-ttu-id="a728a-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="a728a-205">Requirement</span></span> | <span data-ttu-id="a728a-206">Value</span><span class="sxs-lookup"><span data-stu-id="a728a-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a728a-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a728a-207">Minimum supported client</span></span><br/> | <span data-ttu-id="a728a-208">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a728a-208">Windows Vista \[desktop apps only\]</span></span><br/>                                                                        |
| <span data-ttu-id="a728a-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a728a-209">Minimum supported server</span></span><br/> | <span data-ttu-id="a728a-210">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a728a-210">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="a728a-211">Versión</span><span class="sxs-lookup"><span data-stu-id="a728a-211">Version</span></span><br/>                  | <span data-ttu-id="a728a-212">LogonUserExExW también está disponible en Windows Server 2003 o Windows XPwith la versión de distribución general.</span><span class="sxs-lookup"><span data-stu-id="a728a-212">LogonUserExExW is also available onWindows Server 2003 or Windows XPwith the General Distribution Release.</span></span><br/> |
| <span data-ttu-id="a728a-213">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a728a-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="a728a-214"><dt>Winbasep. h</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-214"><dt>Winbasep.h</dt></span></span> </dl>                                 |
| <span data-ttu-id="a728a-215">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a728a-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a728a-216"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a728a-216"><dt>Advapi32.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a728a-217">Vea también</span><span class="sxs-lookup"><span data-stu-id="a728a-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a728a-218">Access Control cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="a728a-218">Client/Server Access Control</span></span>](../secauthz/client-server-access-control.md)
</dt> <dt>

[<span data-ttu-id="a728a-219">Funciones de Access Control cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="a728a-219">Client/Server Access Control Functions</span></span>](../secauthz/authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="a728a-220">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="a728a-220">**CloseHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[<span data-ttu-id="a728a-221">**CreateProcessAsUser ha**</span><span class="sxs-lookup"><span data-stu-id="a728a-221">**CreateProcessAsUser**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[<span data-ttu-id="a728a-222">**DuplicateTokenEx**</span><span class="sxs-lookup"><span data-stu-id="a728a-222">**DuplicateTokenEx**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[<span data-ttu-id="a728a-223">**ImpersonateLoggedOnUser**</span><span class="sxs-lookup"><span data-stu-id="a728a-223">**ImpersonateLoggedOnUser**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[<span data-ttu-id="a728a-224">**LogonUserEx**</span><span class="sxs-lookup"><span data-stu-id="a728a-224">**LogonUserEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[<span data-ttu-id="a728a-225">**límites de cuota \_**</span><span class="sxs-lookup"><span data-stu-id="a728a-225">**QUOTA\_LIMITS**</span></span>](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
