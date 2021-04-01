---
description: Quita un equipo de un dominio o un grupo de trabajo.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Método UnjoinDomainOrWorkgroup de la clase Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907466"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="c84e0-103">Método UnjoinDomainOrWorkgroup de la clase de Win32 \_ ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="c84e0-103">UnjoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="c84e0-104">El método **UnjoinDomainOrWorkgroup** quita un equipo de un dominio o un grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c84e0-104">The **UnjoinDomainOrWorkgroup** method removes a computer system from a domain or workgroup.</span></span>

<span data-ttu-id="c84e0-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c84e0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c84e0-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c84e0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c84e0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c84e0-107">Syntax</span></span>


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="c84e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c84e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c84e0-109">*Contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c84e0-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84e0-110">Si el parámetro *username* especifica un nombre de cuenta, el parámetro *password* debe apuntar a la contraseña que se va a usar al conectarse al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="c84e0-110">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="c84e0-111">De lo contrario, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c84e0-111">Otherwise, this parameter must be **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="c84e0-112">La *contraseña* debe usar un nivel de autenticación alto, no menor que la **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, al conectarse a WinMgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en el puntero [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="c84e0-112">*Password* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="c84e0-113">Si es local a WinMgmt, esto no es un problema.</span><span class="sxs-lookup"><span data-stu-id="c84e0-113">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="c84e0-114">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c84e0-114">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84e0-115">Puntero a una cadena de caracteres terminada en null que especifica el nombre de la cuenta que se va a usar al conectarse al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="c84e0-115">Pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="c84e0-116">Debe especificar un dominio y una cuenta de usuario, por ejemplo, "dominio \\ usuario" o " user@domain ".</span><span class="sxs-lookup"><span data-stu-id="c84e0-116">Must specify a domain and user account, for example, "domain\\user" or "user@domain".</span></span> <span data-ttu-id="c84e0-117">Si este parámetro es **null**, se utiliza el contexto del llamador.</span><span class="sxs-lookup"><span data-stu-id="c84e0-117">If this parameter is **NULL**, the caller context is used.</span></span>

> [!Note]  
> <span data-ttu-id="c84e0-118">El *nombre de usuario* debe usar un nivel de autenticación alto, no menor que la **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, al conectarse a WinMgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en el puntero [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="c84e0-118">*UserName* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="c84e0-119">Si es local a WinMgmt, esto no es un problema.</span><span class="sxs-lookup"><span data-stu-id="c84e0-119">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="c84e0-120">*FUnjoinOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c84e0-120">*FUnjoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84e0-121">Conjunto de marcadores de bits que definen las opciones de unjoin.</span><span class="sxs-lookup"><span data-stu-id="c84e0-121">Set of bit flags defining the unjoin options.</span></span>

<dt>



 <span data-ttu-id="c84e0-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="c84e0-122">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c84e0-123">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c84e0-123">Default.</span></span> <span data-ttu-id="c84e0-124">No hay opciones.</span><span class="sxs-lookup"><span data-stu-id="c84e0-124">No options.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span data-ttu-id="c84e0-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ \_Eliminación** de cuenta (4)</span><span class="sxs-lookup"><span data-stu-id="c84e0-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP\_ACCT\_DELETE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c84e0-126">Deshabilite la cuenta de Active Directory después de la operación de desunión, pero no elimine la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c84e0-126">Disable the Active Directory account after the unjoin operation, but do not delete the account.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c84e0-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c84e0-127">Return value</span></span>

<span data-ttu-id="c84e0-128">El método **UnjoinDomainOrWorkgroup** devuelve 0 (cero) si se realiza correctamente o no hay opciones implicadas.</span><span class="sxs-lookup"><span data-stu-id="c84e0-128">The **UnjoinDomainOrWorkgroup** method returns 0 (zero) on success or when no options are involved.</span></span> <span data-ttu-id="c84e0-129">Cualquier otro valor indica un error.</span><span class="sxs-lookup"><span data-stu-id="c84e0-129">Any other value indicates an error.</span></span> <span data-ttu-id="c84e0-130">Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c84e0-130">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c84e0-131">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c84e0-131">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c84e0-132">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="c84e0-132">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c84e0-133">**Otro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="c84e0-133">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c84e0-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c84e0-134">Remarks</span></span>

<span data-ttu-id="c84e0-135">Después de llamar a este método, reinicie el equipo afectado para aplicar los cambios.</span><span class="sxs-lookup"><span data-stu-id="c84e0-135">After calling this method, restart the affected computer to apply the changes.</span></span>

## <a name="examples"></a><span data-ttu-id="c84e0-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c84e0-136">Examples</span></span>

<span data-ttu-id="c84e0-137">[Desasociar un equipo de un dominio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) El ejemplo de VBScript Desune el equipo local de su dominio actual y deshabilita la cuenta de equipo.</span><span class="sxs-lookup"><span data-stu-id="c84e0-137">[The Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript sample unjoins the local computer from its current domain and disables the computer account.</span></span>

<span data-ttu-id="c84e0-138">El ejemplo de [script separar un equipo de un dominio con VBS](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) quita la Unión de un equipo especificado de un dominio.</span><span class="sxs-lookup"><span data-stu-id="c84e0-138">The [Unjoin a Computer from a Domain using VBS script](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) sample unjoins a specified computer from a domain.</span></span> <span data-ttu-id="c84e0-139">.</span><span class="sxs-lookup"><span data-stu-id="c84e0-139">.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84e0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84e0-140">Requirements</span></span>



| <span data-ttu-id="c84e0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84e0-141">Requirement</span></span> | <span data-ttu-id="c84e0-142">Value</span><span class="sxs-lookup"><span data-stu-id="c84e0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c84e0-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84e0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c84e0-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c84e0-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c84e0-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84e0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c84e0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c84e0-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c84e0-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c84e0-147">Namespace</span></span><br/>                | <span data-ttu-id="c84e0-148">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c84e0-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c84e0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c84e0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c84e0-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c84e0-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c84e0-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c84e0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84e0-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84e0-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c84e0-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="c84e0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84e0-154">**ComputerSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="c84e0-154">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="c84e0-155">**Método JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="c84e0-155">**JoinDomainOrWorkgroup method**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

