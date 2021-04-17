---
description: Devuelve el descriptor de seguridad que controla el acceso a la impresora.
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659475"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="f9770-103">Método GetSecurityDescriptor de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="f9770-103">GetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="f9770-104">El método **GetSecurityDescriptor** devuelve el descriptor de seguridad que controla el acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="f9770-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="f9770-105">El descriptor se devuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="f9770-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="f9770-106">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="f9770-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="f9770-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f9770-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f9770-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f9770-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9770-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9770-109">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="f9770-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9770-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9770-111">*Descriptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9770-111">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9770-112">Descriptor de seguridad asociado a la impresora.</span><span class="sxs-lookup"><span data-stu-id="f9770-112">The security descriptor associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9770-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9770-113">Return value</span></span>

<span data-ttu-id="f9770-114">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f9770-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="f9770-115">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f9770-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f9770-116">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f9770-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f9770-117">**0**</span><span class="sxs-lookup"><span data-stu-id="f9770-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f9770-118">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="f9770-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="f9770-119">**2**</span><span class="sxs-lookup"><span data-stu-id="f9770-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f9770-120">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="f9770-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f9770-121">**8**</span><span class="sxs-lookup"><span data-stu-id="f9770-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f9770-122">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="f9770-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f9770-123">**9**</span><span class="sxs-lookup"><span data-stu-id="f9770-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f9770-124">El usuario no tiene los privilegios adecuados para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="f9770-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="f9770-125">**21**</span><span class="sxs-lookup"><span data-stu-id="f9770-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f9770-126">Un parámetro especificado en la llamada al método no es válido.</span><span class="sxs-lookup"><span data-stu-id="f9770-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9770-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9770-127">Remarks</span></span>

<span data-ttu-id="f9770-128">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="f9770-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="f9770-129">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="f9770-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="f9770-130">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="f9770-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="f9770-131">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="f9770-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="f9770-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f9770-132">Examples</span></span>

<span data-ttu-id="f9770-133">En el siguiente ejemplo de código de VBScript se enumeran las impresoras conectadas al equipo local y se obtiene el descriptor de seguridad de cada impresora.</span><span class="sxs-lookup"><span data-stu-id="f9770-133">The following VBScript code example lists the printers attached to the local computer and gets the security descriptor for each printer.</span></span> <span data-ttu-id="f9770-134">A continuación, se extraen las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de la lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) para determinar qué usuarios tienen acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="f9770-134">Then the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACE) in the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) are extracted to determine which users have access to the printer.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="requirements"></a><span data-ttu-id="f9770-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9770-135">Requirements</span></span>



| <span data-ttu-id="f9770-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9770-136">Requirement</span></span> | <span data-ttu-id="f9770-137">Value</span><span class="sxs-lookup"><span data-stu-id="f9770-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9770-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9770-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f9770-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9770-139">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="f9770-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9770-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f9770-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9770-141">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="f9770-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9770-142">Namespace</span></span><br/>                | <span data-ttu-id="f9770-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f9770-143">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="f9770-144">MOF</span><span class="sxs-lookup"><span data-stu-id="f9770-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9770-145"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9770-145"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9770-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9770-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9770-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9770-147"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f9770-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9770-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9770-149">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="f9770-149">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="f9770-150">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="f9770-150">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="f9770-151">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="f9770-151">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="f9770-152">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="f9770-152">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

