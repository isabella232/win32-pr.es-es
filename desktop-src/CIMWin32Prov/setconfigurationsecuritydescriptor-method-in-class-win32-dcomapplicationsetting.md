---
description: Actualiza el descriptor de seguridad de configuración de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de una clase de Win32 \_ SecurityDescriptor.
ms.assetid: e0fe3d2f-7641-4cae-972d-888e800548de
ms.tgt_platform: multiple
title: Método SetConfigurationSecurityDescriptor de la clase Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8556e49d2e87e12763e3f0699bcff1f786ac1e72
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907018"
---
# <a name="setconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="d05c7-103">Método SetConfigurationSecurityDescriptor de la \_ clase DCOMApplicationSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="d05c7-103">SetConfigurationSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="d05c7-104">El método **SetConfigurationSecurityDescriptor** actualiza el descriptor de seguridad de configuración de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de una clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="d05c7-104">The **SetConfigurationSecurityDescriptor** method updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="d05c7-105">Este descriptor de seguridad controla quién tiene permiso para configurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d05c7-105">This security descriptor controls who is allowed to configure the application.</span></span> <span data-ttu-id="d05c7-106">La cuenta que ejecuta el script o la aplicación que llama a este método debe tener los privilegios **SeSecurityPrivilege** y **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="d05c7-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="d05c7-107">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="d05c7-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="d05c7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d05c7-108">Syntax</span></span>


```mof
uint32 SetConfigurationSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="d05c7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d05c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d05c7-110">*Descriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d05c7-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d05c7-111">Descriptor de seguridad que se va a establecer para la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="d05c7-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d05c7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d05c7-112">Return value</span></span>

<span data-ttu-id="d05c7-113">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="d05c7-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="d05c7-114">Para obtener más información, vea [códigos de retorno de WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d05c7-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="d05c7-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="d05c7-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d05c7-116">0</span><span class="sxs-lookup"><span data-stu-id="d05c7-116">0</span></span>

<span data-ttu-id="d05c7-117">Completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d05c7-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="d05c7-118">**2**</span><span class="sxs-lookup"><span data-stu-id="d05c7-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d05c7-119">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="d05c7-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="d05c7-120">**8**</span><span class="sxs-lookup"><span data-stu-id="d05c7-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d05c7-121">Error desconocido</span><span class="sxs-lookup"><span data-stu-id="d05c7-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="d05c7-122">**9**</span><span class="sxs-lookup"><span data-stu-id="d05c7-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d05c7-123">El usuario no tiene los privilegios adecuados para ejecutar el método</span><span class="sxs-lookup"><span data-stu-id="d05c7-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="d05c7-124">**21**</span><span class="sxs-lookup"><span data-stu-id="d05c7-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d05c7-125">Un parámetro especificado en la llamada al método no es válido</span><span class="sxs-lookup"><span data-stu-id="d05c7-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="d05c7-126">**Otros**</span><span class="sxs-lookup"><span data-stu-id="d05c7-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d05c7-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="d05c7-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d05c7-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d05c7-128">Remarks</span></span>

<span data-ttu-id="d05c7-129">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d05c7-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d05c7-130">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="d05c7-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="d05c7-131">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="d05c7-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="d05c7-132">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="d05c7-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="d05c7-133">Puede actualizar la DACL y la SACL en la instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o la SACL.</span><span class="sxs-lookup"><span data-stu-id="d05c7-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="d05c7-134">Los valores siguientes en el [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualizan la DACL, la SACL o ambas.</span><span class="sxs-lookup"><span data-stu-id="d05c7-134">The following values in the [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="d05c7-135">**DACL de SE \_ \_ presente**</span><span class="sxs-lookup"><span data-stu-id="d05c7-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="d05c7-136">Indica que se debe actualizar la DACL.</span><span class="sxs-lookup"><span data-stu-id="d05c7-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="d05c7-137">Si no se establece, WMI conserva el valor original de la DACL.</span><span class="sxs-lookup"><span data-stu-id="d05c7-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="d05c7-138">**la \_ SACL de se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="d05c7-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="d05c7-139">Indica que se debe actualizar la SACL.</span><span class="sxs-lookup"><span data-stu-id="d05c7-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="d05c7-140">Si no se establece, WMI conserva el valor original de la SACL.</span><span class="sxs-lookup"><span data-stu-id="d05c7-140">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="d05c7-141">Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="d05c7-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="d05c7-142">En el caso de scripting, el nombre del privilegio es **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="d05c7-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="d05c7-143">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="d05c7-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="d05c7-144">Si el administrador de confianza del grupo y las propiedades del administrador del propietario no son **nulos**, se actualizan.</span><span class="sxs-lookup"><span data-stu-id="d05c7-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="d05c7-145">De lo contrario, WMI conserva los valores originales.</span><span class="sxs-lookup"><span data-stu-id="d05c7-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="d05c7-146">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="d05c7-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="d05c7-147">Cuando una nueva SACL es **null** en una llamada a este método, la SACL del descriptor de seguridad del objeto protegible de destino permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d05c7-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="d05c7-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d05c7-148">Requirements</span></span>



| <span data-ttu-id="d05c7-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="d05c7-149">Requirement</span></span> | <span data-ttu-id="d05c7-150">Value</span><span class="sxs-lookup"><span data-stu-id="d05c7-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d05c7-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d05c7-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d05c7-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d05c7-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d05c7-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d05c7-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d05c7-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d05c7-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d05c7-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d05c7-155">Namespace</span></span><br/>                | <span data-ttu-id="d05c7-156">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d05c7-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d05c7-157">MOF</span><span class="sxs-lookup"><span data-stu-id="d05c7-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d05c7-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d05c7-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d05c7-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d05c7-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d05c7-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d05c7-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d05c7-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="d05c7-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d05c7-162">**Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="d05c7-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="d05c7-163">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="d05c7-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="d05c7-164">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="d05c7-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="d05c7-165">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="d05c7-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

