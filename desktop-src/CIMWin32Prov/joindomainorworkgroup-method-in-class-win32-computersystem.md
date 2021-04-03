---
description: Une un equipo a un dominio o grupo de trabajo.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Método JoinDomainOrWorkgroup de la clase Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907429"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="d4e79-103">Método JoinDomainOrWorkgroup de la clase de Win32 \_ ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="d4e79-103">JoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="d4e79-104">El método **JoinDomainOrWorkgroup** une un equipo a un dominio o grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d4e79-104">The **JoinDomainOrWorkgroup** method joins a computer system to a domain or workgroup.</span></span>

<span data-ttu-id="d4e79-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d4e79-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d4e79-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d4e79-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e79-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4e79-107">Syntax</span></span>


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="d4e79-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4e79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e79-109">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d4e79-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-110">Especifica el dominio o grupo de trabajo al que se va a unir.</span><span class="sxs-lookup"><span data-stu-id="d4e79-110">Specifies the domain or workgroup to join.</span></span> <span data-ttu-id="d4e79-111">No puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d4e79-111">Cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-112">*Contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d4e79-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-113">Si el parámetro *username* especifica un nombre de cuenta, el parámetro *password* debe apuntar a la contraseña que se va a usar al conectarse al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-113">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="d4e79-114">De lo contrario, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d4e79-114">Otherwise, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-115">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4e79-115">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-116">Puntero a una cadena de caracteres terminada en **null** que especifica el nombre de la cuenta que se va a usar al conectarse al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-116">Pointer to a constant **null**-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="d4e79-117">Debe especificar un nombre NetBIOS de dominio y una cuenta de usuario, por ejemplo, usuario de dominio \\ .</span><span class="sxs-lookup"><span data-stu-id="d4e79-117">Must specify a domain NetBIOS name and user account, for example, Domain\\user.</span></span> <span data-ttu-id="d4e79-118">Si este parámetro es **null**, se utiliza la información del llamador.</span><span class="sxs-lookup"><span data-stu-id="d4e79-118">If this parameter is **NULL**, the caller information is used.</span></span>

<span data-ttu-id="d4e79-119">También puede usar el nombre principal de usuario (UPPED) en el formulario user@domain .</span><span class="sxs-lookup"><span data-stu-id="d4e79-119">You can also use the user principal name (UPPED) in the form user@domain.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-120">*AccountOU* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4e79-120">*AccountOU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-121">Especifica el puntero a una cadena de caracteres terminada en **null** que contiene el nombre de formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) de la unidad organizativa (OU) de la cuenta de equipo.</span><span class="sxs-lookup"><span data-stu-id="d4e79-121">Specifies the pointer to a constant **null**-terminated character string that contains the [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) format name of the organizational unit (OU) for the computer account.</span></span> <span data-ttu-id="d4e79-122">Si especifica este parámetro, la cadena debe contener una ruta de acceso completa; de lo contrario, *acento* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d4e79-122">If you specify this parameter, the string must contain a full path, otherwise *Accent* must be **NULL**.</span></span>

<span data-ttu-id="d4e79-123">Ejemplo: "OU = testOU; DC = dominio; DC = dominio; DC = com "</span><span class="sxs-lookup"><span data-stu-id="d4e79-123">Example: "OU=testOU; DC=domain; DC=Domain; DC=com"</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-124">*FJoinOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4e79-124">*FJoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-125">Conjunto de marcadores de bits que definen las opciones de combinación.</span><span class="sxs-lookup"><span data-stu-id="d4e79-125">Set of bit flags that define the join options.</span></span>

<dt>



 <span data-ttu-id="d4e79-126"> (0)</span><span class="sxs-lookup"><span data-stu-id="d4e79-126">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d4e79-127">Default.</span></span> <span data-ttu-id="d4e79-128">No hay opciones de combinación.</span><span class="sxs-lookup"><span data-stu-id="d4e79-128">No join options.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span data-ttu-id="d4e79-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP \_ UNIRSE a \_ dominio** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d4e79-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP\_JOIN\_DOMAIN** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-130">Une el equipo a un dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-130">Joins the computer to a domain.</span></span> <span data-ttu-id="d4e79-131">Si no se especifica este valor, une el equipo a un grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d4e79-131">If this value is not specified, joins the computer to a workgroup.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span data-ttu-id="d4e79-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP \_ \_Creación de cuentas** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d4e79-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP\_ACCT\_CREATE** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-133">Crea la cuenta en el dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-133">Creates the account on the domain.</span></span>

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span data-ttu-id="d4e79-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP \_ \_Actualización de Win9x** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="d4e79-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP\_WIN9X\_UPGRADE** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-135">La operación de Unión se está produciendo como parte de una actualización.</span><span class="sxs-lookup"><span data-stu-id="d4e79-135">The join operation is occurring as part of an upgrade.</span></span>

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span data-ttu-id="d4e79-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP \_ Unión al dominio \_ \_ si está \_ Unido** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="d4e79-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP\_DOMAIN\_JOIN\_IF\_JOINED** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-137">Permite una combinación con un nuevo dominio, incluso si el equipo ya está unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-137">Allows a join to a new domain even if the computer is already joined to a domain.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span data-ttu-id="d4e79-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP \_ Unión no \_ segura** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="d4e79-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP\_JOIN\_UNSECURE** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-139">realiza una unión no segura.</span><span class="sxs-lookup"><span data-stu-id="d4e79-139">Performs an unsecured join.</span></span>

<span data-ttu-id="d4e79-140">Esta opción solicita una Unión de dominio a una cuenta creada previamente sin autenticarse con las credenciales de usuario de dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-140">This option requests a domain join to a pre-created account without authenticating with domain user credentials.</span></span> <span data-ttu-id="d4e79-141">Esta opción se puede usar junto con la opción de la **\_ máquina pwd de NETSETUP \_ \_ pasada** .</span><span class="sxs-lookup"><span data-stu-id="d4e79-141">This option can be used in conjunction with **NETSETUP\_MACHINE\_PWD\_PASSED** option.</span></span> <span data-ttu-id="d4e79-142">En este caso, *password* es la contraseña de la cuenta de equipo creada previamente.</span><span class="sxs-lookup"><span data-stu-id="d4e79-142">In this case, *Password* is the password of the pre-created machine account.</span></span>

<span data-ttu-id="d4e79-143">Antes de Windows Vista con SP1 y Windows Server 2008, una Unión no segura no se autenticaba en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-143">Prior to Windows Vista with SP1 and Windows Server 2008, an unsecure join did not authenticate to the domain controller.</span></span> <span data-ttu-id="d4e79-144">Toda la comunicación se realizó mediante una sesión nula (sin autenticar).</span><span class="sxs-lookup"><span data-stu-id="d4e79-144">All communication was performed using a null (unauthenticated) session.</span></span> <span data-ttu-id="d4e79-145">A partir de Windows Vista con SP1 y Windows Server 2008, se usan el nombre y la contraseña de la cuenta de equipo para autenticarse en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-145">Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller.</span></span>

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span data-ttu-id="d4e79-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP \_ \_ \_ Se pasó la pwd del equipo** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="d4e79-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP\_MACHINE\_PWD\_PASSED** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-147">Indica que el parámetro de *contraseña* especifica una contraseña de cuenta de equipo local en lugar de una contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="d4e79-147">Indicates that the *Password* parameter specifies a local machine account password rather than a user password.</span></span> <span data-ttu-id="d4e79-148">Esta marca solo es válida para las combinaciones no seguras, que debe indicar estableciendo también la \_ \_ marca NETSETUP unsecure.</span><span class="sxs-lookup"><span data-stu-id="d4e79-148">This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP\_JOIN\_UNSECURE flag.</span></span>

<span data-ttu-id="d4e79-149">Si establece esta marca, después de que la operación de Unión se realice correctamente, la contraseña del equipo se establecerá en el valor de *contraseña*, si ese valor es una contraseña de equipo válida.</span><span class="sxs-lookup"><span data-stu-id="d4e79-149">If you set this flag, then after the join operation succeeds, the machine password will be set to the value of *Password*, if that value is a valid machine password.</span></span>

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span data-ttu-id="d4e79-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP \_ APLAZAr el \_ \_ conjunto de SPN** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="d4e79-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP\_DEFER\_SPN\_SET** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-151">Indica que el nombre de entidad de seguridad de servicio (SPN) y las propiedades de DnsHostName en el objeto de equipo no deben actualizarse en este momento.</span><span class="sxs-lookup"><span data-stu-id="d4e79-151">Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time.</span></span>

<span data-ttu-id="d4e79-152">Normalmente, estas propiedades se actualizan durante la operación de combinación.</span><span class="sxs-lookup"><span data-stu-id="d4e79-152">Typically, these properties are updated during the join operation.</span></span> <span data-ttu-id="d4e79-153">En su lugar, estas propiedades se deben actualizar durante una llamada subsiguiente al método [**Rename**](rename-method-in-class-win32-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e79-153">Instead, these properties should be updated during a subsequent call to the [**Rename**](rename-method-in-class-win32-computersystem.md) method.</span></span> <span data-ttu-id="d4e79-154">Estas propiedades siempre se actualizan durante la operación de cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="d4e79-154">These properties are always updated during the rename operation.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span data-ttu-id="d4e79-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP \_ Unirse a una \_ \_ cuenta de controlador de dominio** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="d4e79-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP\_JOIN\_DC\_ACCOUNT** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-156">Permitir la Unión al dominio si la cuenta existente es un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-156">Allow the domain join if existing account is a domain controller.</span></span>

> [!Note]  
> <span data-ttu-id="d4e79-157">Esta marca es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4e79-157">This flag is supported on Windows Vista and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span data-ttu-id="d4e79-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP \_ \_DC ambiguo** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="d4e79-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP\_AMBIGUOUS\_DC** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-159">Al unirse al dominio, no intente establecer el controlador de dominio preferido en el registro.</span><span class="sxs-lookup"><span data-stu-id="d4e79-159">When joining the domain don't try to set the preferred domain controller in the registry.</span></span>

> [!Note]  
> <span data-ttu-id="d4e79-160">Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4e79-160">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span data-ttu-id="d4e79-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP \_ NO \_ hay \_ caché de Netlogon** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="d4e79-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP\_NO\_NETLOGON\_CACHE** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-162">Al unirse al dominio, no cree la memoria caché de netlogon.</span><span class="sxs-lookup"><span data-stu-id="d4e79-162">When joining the domain don't create the Netlogon cache.</span></span>

> [!Note]  
> <span data-ttu-id="d4e79-163">Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4e79-163">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span data-ttu-id="d4e79-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP \_ No \_ controlar \_ servicios** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="d4e79-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP\_DONT\_CONTROL\_SERVICES** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-165">Al unirse al dominio, no fuerce el inicio del servicio NetLogon.</span><span class="sxs-lookup"><span data-stu-id="d4e79-165">When joining the domain don't force Netlogon service to start.</span></span>

> [!Note]  
> <span data-ttu-id="d4e79-166">Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4e79-166">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span data-ttu-id="d4e79-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP \_ ESTABLECER \_ \_ el nombre** de la máquina (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="d4e79-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP\_SET\_MACHINE\_NAME** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-168">Al unirse al dominio solo para la combinación sin conexión, establezca el nombre de host y el nombre de NetBIOS del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="d4e79-168">When joining the domain for offline join only, set target machine hostname and NetBIOS name.</span></span>

> [!Note]  
> <span data-ttu-id="d4e79-169">Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4e79-169">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span data-ttu-id="d4e79-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP \_ FORZAr el \_ \_ conjunto de SPN** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="d4e79-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP\_FORCE\_SPN\_SET** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-171">Al unirse al dominio, invalide otras opciones durante la Unión al dominio y establezca el nombre de la entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="d4e79-171">When joining the domain, override other settings during domain join and set the service principal name (SPN).</span></span>

> [!Note]  
> <span data-ttu-id="d4e79-172">Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4e79-172">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span data-ttu-id="d4e79-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP \_ NO \_ \_ reutilización de cuentas** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="d4e79-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP\_NO\_ACCT\_REUSE** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-174">Al unirse al dominio, no vuelva a usar una cuenta existente.</span><span class="sxs-lookup"><span data-stu-id="d4e79-174">When joining the domain, do not reuse an existing account.</span></span>

> [!Note]  
> <span data-ttu-id="d4e79-175">Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4e79-175">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span data-ttu-id="d4e79-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP \_ OMITIr \_ \_ marcas no admitidas** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="d4e79-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP\_IGNORE\_UNSUPPORTED\_FLAGS** (0x10000000)</span></span>


</dt> <dd>

<span data-ttu-id="d4e79-177">Si se establece este bit, se omitirán las marcas no reconocidas por la función **JoinDomainOrWorkgroup** y [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) se comportará como si no se hubieran establecido las marcas.</span><span class="sxs-lookup"><span data-stu-id="d4e79-177">If this bit is set, unrecognized flags will be ignored by the **JoinDomainOrWorkgroup** function and [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) will behave as if the flags were not set.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e79-178">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4e79-178">Return value</span></span>

<span data-ttu-id="d4e79-179">Devuelve un [código de error del sistema](/windows/desktop/Debug/system-error-codes), que puede incluir uno de los siguientes valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="d4e79-179">Returns a [system error code](/windows/desktop/Debug/system-error-codes), which may include one of the following numeric values.</span></span> <span data-ttu-id="d4e79-180">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="d4e79-180">Any other number indicates an error.</span></span> <span data-ttu-id="d4e79-181">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d4e79-181">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="d4e79-182">**Success**</span><span class="sxs-lookup"><span data-stu-id="d4e79-182">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-183">0</span><span class="sxs-lookup"><span data-stu-id="d4e79-183">0</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-184">**5**</span><span class="sxs-lookup"><span data-stu-id="d4e79-184">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-185">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d4e79-185">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-186">**87**</span><span class="sxs-lookup"><span data-stu-id="d4e79-186">**87**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-187">El parámetro no es correcto.</span><span class="sxs-lookup"><span data-stu-id="d4e79-187">The parameter is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-188">**110**</span><span class="sxs-lookup"><span data-stu-id="d4e79-188">**110**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-189">el sistema no puede abrir el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d4e79-189">he system cannot open the specified object.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-190">**1323**</span><span class="sxs-lookup"><span data-stu-id="d4e79-190">**1323**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-191">No se puede actualizar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="d4e79-191">Unable to update the password.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-192">**1326**</span><span class="sxs-lookup"><span data-stu-id="d4e79-192">**1326**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-193">Error de inicio de sesión: nombre de usuario desconocido o contraseña incorrecta.</span><span class="sxs-lookup"><span data-stu-id="d4e79-193">Logon failure: unknown username or bad password.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-194">**1355**</span><span class="sxs-lookup"><span data-stu-id="d4e79-194">**1355**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-195">El dominio especificado no existe o no se pudo establecer contacto con él.</span><span class="sxs-lookup"><span data-stu-id="d4e79-195">The specified domain either does not exist or could not be contacted.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-196">**2224**</span><span class="sxs-lookup"><span data-stu-id="d4e79-196">**2224**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-197">La cuenta ya existe.</span><span class="sxs-lookup"><span data-stu-id="d4e79-197">The account already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-198">**2691**</span><span class="sxs-lookup"><span data-stu-id="d4e79-198">**2691**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-199">El equipo ya está unido al dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-199">The machine is already joined to the domain.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-200">**2692**</span><span class="sxs-lookup"><span data-stu-id="d4e79-200">**2692**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-201">El equipo no está unido actualmente a un dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-201">The machine is not currently joined to a domain.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-202">**se \_ \_ requiere la \_ conexión cifrada WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="d4e79-202">**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-203">0x80041087</span><span class="sxs-lookup"><span data-stu-id="d4e79-203">0x80041087</span></span>

<span data-ttu-id="d4e79-204">Se especifican la *contraseña* y el *nombre de usuario* , pero el nivel de autenticación no es **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="d4e79-204">*Password* and *UserName* are specified but the authentication level is not **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="d4e79-205">Por Visual Basic, se devuelve **wbemErrEncryptedConnectionRequired** .</span><span class="sxs-lookup"><span data-stu-id="d4e79-205">For Visual Basic, **wbemErrEncryptedConnectionRequired** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="d4e79-206">**Otros**</span><span class="sxs-lookup"><span data-stu-id="d4e79-206">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d4e79-207">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="d4e79-207">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4e79-208">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4e79-208">Remarks</span></span>

<span data-ttu-id="d4e79-209">Al mover un equipo de un dominio a un grupo de trabajo, debe quitar el equipo del dominio (con una llamada a [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) antes de llamar a este método para unirse a un grupo de trabajo (con una llamada a **JoinDomainOrWorkgroup**).</span><span class="sxs-lookup"><span data-stu-id="d4e79-209">When moving a computer from a domain to a workgroup, you must remove the computer from the domain (with a call to [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) before calling this method to join a workgroup (with a call to **JoinDomainOrWorkgroup**).</span></span> <span data-ttu-id="d4e79-210">Después de llamar a este método, reinicie el equipo afectado para aplicar los cambios.</span><span class="sxs-lookup"><span data-stu-id="d4e79-210">After calling this method, restart the affected computer to apply the changes.</span></span>

<span data-ttu-id="d4e79-211">El *nombre de usuario* y la *contraseña* pueden dejarse en **blanco.**</span><span class="sxs-lookup"><span data-stu-id="d4e79-211">*UserName* and *Password* can be left **null**.</span></span> <span data-ttu-id="d4e79-212">Sin embargo, la autenticación de la conexión a WMI debe ser 6 en el script o **WbemAuthenticationLevelPktPrivacy** en Visual Basic y otros idiomas que pueden usar la biblioteca de [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) .</span><span class="sxs-lookup"><span data-stu-id="d4e79-212">However, the authentication of the connection to WMI must be 6 in script or **WbemAuthenticationLevelPktPrivacy** in Visual Basic and other languages that can use the [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) library.</span></span> <span data-ttu-id="d4e79-213">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="d4e79-213">For more information, see [Setting the Default Process Security Level Using VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span></span>

<span data-ttu-id="d4e79-214">En C++, establezca la autenticación de **nivel de autenticación RPC \_ C de \_ \_ nivel \_ \_** de autenticación en [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), para todo el proceso o en [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), para una conexión al proxy [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="d4e79-214">In C++, set the authentication at **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** either in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), for the entire process, or in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), for a connection to the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="d4e79-215">Para obtener más información, vea [establecer la autenticación con C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) y [establecer la seguridad en IWbemServices y en otros servidores proxy](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span><span class="sxs-lookup"><span data-stu-id="d4e79-215">For more information, see [Setting Authentication Using C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) and [Setting the Security on IWbemServices and Other Proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span></span>

## <a name="examples"></a><span data-ttu-id="d4e79-216">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4e79-216">Examples</span></span>

<span data-ttu-id="d4e79-217">El ejemplo [unir un equipo a un dominio](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) de PowerShell une un equipo a un dominio.</span><span class="sxs-lookup"><span data-stu-id="d4e79-217">The [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell example joins a computer to a domain.</span></span>

<span data-ttu-id="d4e79-218">El siguiente ejemplo de código de VBScript une un equipo a un dominio y crea la cuenta del equipo en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4e79-218">The following VBScript code example joins a computer to a domain and creates the computer's account in Active Directory.</span></span>


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a><span data-ttu-id="d4e79-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4e79-219">Requirements</span></span>



| <span data-ttu-id="d4e79-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4e79-220">Requirement</span></span> | <span data-ttu-id="d4e79-221">Value</span><span class="sxs-lookup"><span data-stu-id="d4e79-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e79-222">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4e79-222">Minimum supported client</span></span><br/> | <span data-ttu-id="d4e79-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4e79-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4e79-224">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4e79-224">Minimum supported server</span></span><br/> | <span data-ttu-id="d4e79-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4e79-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4e79-226">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4e79-226">Namespace</span></span><br/>                | <span data-ttu-id="d4e79-227">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d4e79-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d4e79-228">MOF</span><span class="sxs-lookup"><span data-stu-id="d4e79-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4e79-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4e79-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4e79-230">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4e79-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4e79-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4e79-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e79-232">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4e79-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e79-233">**ComputerSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d4e79-233">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="d4e79-234">**Método UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="d4e79-234">**UnjoinDomainOrWorkgroup method**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

