---
description: Escribe una versión actualizada del descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se representa mediante una instancia de \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706653"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="a69f7-104">Método SetSecurityDescriptor de la \_ \_ clase SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="a69f7-104">SetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="a69f7-105">El método [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) escribe una versión actualizada del descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado.</span><span class="sxs-lookup"><span data-stu-id="a69f7-105">The [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) method writes an updated version of the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="a69f7-106">El descriptor de seguridad se representa mediante una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="a69f7-106">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="a69f7-107">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a69f7-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a69f7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a69f7-108">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="a69f7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a69f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a69f7-110">*Descriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a69f7-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a69f7-111">Descriptor de seguridad asociado al espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="a69f7-111">The security descriptor associated with the WMI Namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a69f7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a69f7-112">Return value</span></span>

<span data-ttu-id="a69f7-113">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a69f7-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="a69f7-114">Para obtener más información, vea [códigos de retorno de WMI](wmi-return-codes.md) o [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a69f7-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="a69f7-115">**0**</span><span class="sxs-lookup"><span data-stu-id="a69f7-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a69f7-116">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="a69f7-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="a69f7-117">**2**</span><span class="sxs-lookup"><span data-stu-id="a69f7-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a69f7-118">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="a69f7-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a69f7-119">**8**</span><span class="sxs-lookup"><span data-stu-id="a69f7-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a69f7-120">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="a69f7-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a69f7-121">**9**</span><span class="sxs-lookup"><span data-stu-id="a69f7-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a69f7-122">El usuario no tiene los privilegios adecuados para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="a69f7-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="a69f7-123">**21**</span><span class="sxs-lookup"><span data-stu-id="a69f7-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a69f7-124">Un parámetro especificado en la llamada al método no es válido.</span><span class="sxs-lookup"><span data-stu-id="a69f7-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a69f7-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a69f7-125">Remarks</span></span>

<span data-ttu-id="a69f7-126">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de Access Control del sistema*](/windows/desktop/SecGloss/a-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="a69f7-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL).</span></span> <span data-ttu-id="a69f7-127">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="a69f7-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="a69f7-128">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="a69f7-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="a69f7-129">Para obtener más información, vea [**constantes de privilegios**](privilege-constants.md) y [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a69f7-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="a69f7-130">Puede actualizar la DACL y la SACL en la instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o la SACL.</span><span class="sxs-lookup"><span data-stu-id="a69f7-130">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="a69f7-131">Los valores siguientes en [**el \_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualizan la DACL o la SACL, o ambas.</span><span class="sxs-lookup"><span data-stu-id="a69f7-131">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL or the SACL or both are updated.</span></span>

-   <span data-ttu-id="a69f7-132">**DACL de SE \_ \_ presente**</span><span class="sxs-lookup"><span data-stu-id="a69f7-132">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="a69f7-133">Indica que se debe actualizar la DACL.</span><span class="sxs-lookup"><span data-stu-id="a69f7-133">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="a69f7-134">Si no se establece, WMI conserva el valor original de la DACL.</span><span class="sxs-lookup"><span data-stu-id="a69f7-134">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="a69f7-135">**la \_ SACL de se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="a69f7-135">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="a69f7-136">Indica que se debe actualizar la SACL.</span><span class="sxs-lookup"><span data-stu-id="a69f7-136">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="a69f7-137">Si no se establece, WMI conserva el valor original de la SACL.</span><span class="sxs-lookup"><span data-stu-id="a69f7-137">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="a69f7-138">Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="a69f7-138">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="a69f7-139">En el caso de scripting, el nombre del privilegio es **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="a69f7-139">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="a69f7-140">Para obtener más información, vea [**constantes de privilegios**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a69f7-140">For more information, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="a69f7-141">Si el administrador de confianza del grupo y las propiedades del administrador del propietario no son **nulos**, se actualizan.</span><span class="sxs-lookup"><span data-stu-id="a69f7-141">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="a69f7-142">De lo contrario, WMI conserva los valores originales.</span><span class="sxs-lookup"><span data-stu-id="a69f7-142">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="a69f7-143">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a69f7-143">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span>

<span data-ttu-id="a69f7-144">Cuando una nueva SACL es **null** en una llamada a este método, la SACL del descriptor de seguridad del objeto protegible de destino permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="a69f7-144">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="a69f7-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a69f7-145">Requirements</span></span>



| <span data-ttu-id="a69f7-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a69f7-146">Requirement</span></span> | <span data-ttu-id="a69f7-147">Value</span><span class="sxs-lookup"><span data-stu-id="a69f7-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a69f7-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a69f7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a69f7-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a69f7-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a69f7-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a69f7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a69f7-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a69f7-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a69f7-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a69f7-152">Namespace</span></span><br/>                | <span data-ttu-id="a69f7-153">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="a69f7-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a69f7-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="a69f7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a69f7-155">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="a69f7-155">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="a69f7-156">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="a69f7-156">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

