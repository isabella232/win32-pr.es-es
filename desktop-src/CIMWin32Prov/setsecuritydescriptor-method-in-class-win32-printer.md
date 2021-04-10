---
description: Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275104"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="56526-103">Método SetSecurityDescriptor de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="56526-103">SetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="56526-104">El método **SetSecurityDescriptor** escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="56526-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="56526-105">El descriptor de seguridad es una instancia de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="56526-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="56526-106">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="56526-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="56526-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="56526-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="56526-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="56526-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="56526-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56526-109">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="56526-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56526-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56526-111">*Descriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56526-111">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56526-112">Descriptor de seguridad asociado a la impresora.</span><span class="sxs-lookup"><span data-stu-id="56526-112">The security descriptor that is associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56526-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56526-113">Return value</span></span>

<span data-ttu-id="56526-114">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="56526-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="56526-115">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="56526-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="56526-116">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="56526-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="56526-117">**0**</span><span class="sxs-lookup"><span data-stu-id="56526-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="56526-118">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="56526-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="56526-119">**2**</span><span class="sxs-lookup"><span data-stu-id="56526-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="56526-120">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="56526-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="56526-121">**8**</span><span class="sxs-lookup"><span data-stu-id="56526-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="56526-122">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="56526-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="56526-123">**9**</span><span class="sxs-lookup"><span data-stu-id="56526-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="56526-124">El usuario no tiene los privilegios adecuados para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="56526-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="56526-125">**21**</span><span class="sxs-lookup"><span data-stu-id="56526-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="56526-126">Un parámetro especificado en la llamada al método no es válido.</span><span class="sxs-lookup"><span data-stu-id="56526-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56526-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56526-127">Remarks</span></span>

<span data-ttu-id="56526-128">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="56526-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="56526-129">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="56526-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="56526-130">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="56526-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="56526-131">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="56526-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="56526-132">Puede actualizar la DACL y la SACL en la instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o la SACL.</span><span class="sxs-lookup"><span data-stu-id="56526-132">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you can also update only the DACL or only the SACL.</span></span>

<span data-ttu-id="56526-133">Los valores siguientes en [**el \_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualiza la DACL, la SACL o ambas.</span><span class="sxs-lookup"><span data-stu-id="56526-133">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="56526-134">**DACL de SE \_ \_ presente**</span><span class="sxs-lookup"><span data-stu-id="56526-134">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="56526-135">Indica que se debe actualizar la DACL.</span><span class="sxs-lookup"><span data-stu-id="56526-135">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="56526-136">Si no se establece, WMI conserva el valor original de la DACL.</span><span class="sxs-lookup"><span data-stu-id="56526-136">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="56526-137">**la \_ SACL de se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="56526-137">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="56526-138">Indica que se debe actualizar la SACL.</span><span class="sxs-lookup"><span data-stu-id="56526-138">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="56526-139">Si no se establece, WMI conserva el valor original de la SACL.</span><span class="sxs-lookup"><span data-stu-id="56526-139">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="56526-140">Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="56526-140">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="56526-141">En el caso de scripting, el nombre del privilegio es **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="56526-141">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="56526-142">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="56526-142">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="56526-143">Si el administrador de confianza del grupo y las propiedades del administrador del propietario no son **nulos**, se actualizan.</span><span class="sxs-lookup"><span data-stu-id="56526-143">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="56526-144">De lo contrario, WMI conserva los valores originales.</span><span class="sxs-lookup"><span data-stu-id="56526-144">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="56526-145">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="56526-145">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="56526-146">Cuando una nueva SACL es **null** en una llamada a este método, la SACL del descriptor de seguridad del objeto protegible de destino permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="56526-146">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="examples"></a><span data-ttu-id="56526-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56526-147">Examples</span></span>

<span data-ttu-id="56526-148">El ejemplo de PowerShell [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) reemplaza los permisos (ACL) de una impresora a otra.</span><span class="sxs-lookup"><span data-stu-id="56526-148">The [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell sample Replace the permissions (ACL) from one printer to another.</span></span>

<span data-ttu-id="56526-149">En el ejemplo de código de PowerShell siguiente se describe cómo establecer el descriptor de seguridad para una impresora.</span><span class="sxs-lookup"><span data-stu-id="56526-149">The following PowerShell code sample describes how to set the security descriptor for a printer.</span></span>


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a><span data-ttu-id="56526-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56526-150">Requirements</span></span>



| <span data-ttu-id="56526-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="56526-151">Requirement</span></span> | <span data-ttu-id="56526-152">Value</span><span class="sxs-lookup"><span data-stu-id="56526-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56526-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56526-153">Minimum supported client</span></span><br/> | <span data-ttu-id="56526-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56526-154">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="56526-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56526-155">Minimum supported server</span></span><br/> | <span data-ttu-id="56526-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56526-156">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="56526-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56526-157">Namespace</span></span><br/>                | <span data-ttu-id="56526-158">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="56526-158">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="56526-159">MOF</span><span class="sxs-lookup"><span data-stu-id="56526-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56526-160"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56526-160"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="56526-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56526-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56526-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56526-162"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="56526-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="56526-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56526-164">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="56526-164">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="56526-165">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="56526-165">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="56526-166">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="56526-166">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="56526-167">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="56526-167">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

