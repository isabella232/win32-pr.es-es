---
description: Actualiza el descriptor de seguridad de acceso de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de una clase de Win32 \_ SecurityDescriptor.
ms.assetid: 71b708ba-5eb7-400e-bee2-37ca93966c3f
ms.tgt_platform: multiple
title: Método SetAccessSecurityDescriptor de la clase Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c0975475c5f20682ee77125b66ed703fbb4b9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907499"
---
# <a name="setaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="3e23b-103">Método SetAccessSecurityDescriptor de la \_ clase DCOMApplicationSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="3e23b-103">SetAccessSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="3e23b-104">El método **SetAccessSecurityDescriptor** actualiza el descriptor de seguridad de acceso de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de una clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="3e23b-104">The **SetAccessSecurityDescriptor** method updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="3e23b-105">Este descriptor de seguridad controla quién tiene permiso para obtener acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e23b-105">This security descriptor controls who is allowed to access the application.</span></span> <span data-ttu-id="3e23b-106">La cuenta que ejecuta el script o la aplicación que llama a este método debe tener los privilegios **SeSecurityPrivilege** y **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="3e23b-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="3e23b-107">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="3e23b-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e23b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e23b-108">Syntax</span></span>


```mof
uint32 SetAccessSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="3e23b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e23b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e23b-110">*Descriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e23b-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e23b-111">Descriptor de seguridad que se va a establecer para la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="3e23b-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e23b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e23b-112">Return value</span></span>

<span data-ttu-id="3e23b-113">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3e23b-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="3e23b-114">Para obtener más información, vea [códigos de retorno de WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3e23b-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="3e23b-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="3e23b-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3e23b-116">0</span><span class="sxs-lookup"><span data-stu-id="3e23b-116">0</span></span>

<span data-ttu-id="3e23b-117">Completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e23b-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="3e23b-118">**2**</span><span class="sxs-lookup"><span data-stu-id="3e23b-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3e23b-119">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="3e23b-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="3e23b-120">**8**</span><span class="sxs-lookup"><span data-stu-id="3e23b-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3e23b-121">Error desconocido</span><span class="sxs-lookup"><span data-stu-id="3e23b-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="3e23b-122">**9**</span><span class="sxs-lookup"><span data-stu-id="3e23b-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3e23b-123">El usuario no tiene los privilegios adecuados para ejecutar el método</span><span class="sxs-lookup"><span data-stu-id="3e23b-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="3e23b-124">**21**</span><span class="sxs-lookup"><span data-stu-id="3e23b-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3e23b-125">Un parámetro especificado en la llamada al método no es válido</span><span class="sxs-lookup"><span data-stu-id="3e23b-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="3e23b-126">**Otros**</span><span class="sxs-lookup"><span data-stu-id="3e23b-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3e23b-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="3e23b-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e23b-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e23b-128">Remarks</span></span>

<span data-ttu-id="3e23b-129">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="3e23b-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="3e23b-130">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="3e23b-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="3e23b-131">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="3e23b-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="3e23b-132">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="3e23b-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="3e23b-133">Puede actualizar la DACL y la SACL en la instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o la SACL.</span><span class="sxs-lookup"><span data-stu-id="3e23b-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="3e23b-134">Los valores siguientes en el [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualizan la DACL, la SACL o ambas.</span><span class="sxs-lookup"><span data-stu-id="3e23b-134">The following values in the [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="3e23b-135">**DACL de SE \_ \_ presente**</span><span class="sxs-lookup"><span data-stu-id="3e23b-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="3e23b-136">Indica que se debe actualizar la DACL.</span><span class="sxs-lookup"><span data-stu-id="3e23b-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="3e23b-137">Si no se establece, WMI conserva el valor original de la DACL.</span><span class="sxs-lookup"><span data-stu-id="3e23b-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="3e23b-138">**la \_ SACL de se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="3e23b-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="3e23b-139">Indica que se debe actualizar la SACL.</span><span class="sxs-lookup"><span data-stu-id="3e23b-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="3e23b-140">Si no se establece, WMI conserva el valor original de la SACL.</span><span class="sxs-lookup"><span data-stu-id="3e23b-140">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="3e23b-141">Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="3e23b-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="3e23b-142">En el caso de scripting, el nombre del privilegio es **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="3e23b-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="3e23b-143">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="3e23b-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="3e23b-144">Si el administrador de confianza del grupo y las propiedades del administrador del propietario no son **nulos**, se actualizan.</span><span class="sxs-lookup"><span data-stu-id="3e23b-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="3e23b-145">De lo contrario, WMI conserva los valores originales.</span><span class="sxs-lookup"><span data-stu-id="3e23b-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="3e23b-146">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="3e23b-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="3e23b-147">Cuando una nueva SACL es **null** en una llamada a este método, la SACL del descriptor de seguridad del objeto protegible de destino permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="3e23b-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e23b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e23b-148">Requirements</span></span>



| <span data-ttu-id="3e23b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e23b-149">Requirement</span></span> | <span data-ttu-id="3e23b-150">Value</span><span class="sxs-lookup"><span data-stu-id="3e23b-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e23b-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e23b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3e23b-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e23b-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e23b-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e23b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3e23b-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e23b-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e23b-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e23b-155">Namespace</span></span><br/>                | <span data-ttu-id="3e23b-156">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3e23b-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e23b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3e23b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e23b-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e23b-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e23b-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e23b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e23b-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e23b-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e23b-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e23b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e23b-162">**Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="3e23b-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="3e23b-163">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="3e23b-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="3e23b-164">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="3e23b-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="3e23b-165">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="3e23b-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

