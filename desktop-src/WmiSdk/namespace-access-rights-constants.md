---
description: 'WMI tiene constantes de seguridad usadas para la comprobación de acceso del espacio de nombres de \_ \_ SystemSecurity:: GetCallerAccessRights.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Constantes de derechos de acceso de espacio de nombres (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104081976"
---
# <a name="namespace-access-rights-constants"></a><span data-ttu-id="dbb0d-103">Constantes de derechos de acceso de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dbb0d-103">Namespace Access Rights Constants</span></span>

<span data-ttu-id="dbb0d-104">WMI tiene constantes de seguridad usadas para la comprobación de acceso del espacio de nombres de [**\_ \_ SystemSecurity:: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span><span class="sxs-lookup"><span data-stu-id="dbb0d-104">WMI has security constants used for namespace access checking by [**\_\_SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span></span> <span data-ttu-id="dbb0d-105">Para obtener información de seguridad acerca de las listas de control de acceso (ACL, DACL o SACL), consulte [listas de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [**derechos de acceso estándar**](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="dbb0d-105">For security information about access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [**Standard Access Rights**](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="dbb0d-106">Estas constantes se definen en la enumeración de **\_ \_ marcas de seguridad WBEM** .</span><span class="sxs-lookup"><span data-stu-id="dbb0d-106">These constants are defined in the **WBEM\_SECURITY\_FLAGS** enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="dbb0d-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**\_Habilitar WBEM**</span><span class="sxs-lookup"><span data-stu-id="dbb0d-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb0d-108">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="dbb0d-108">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="dbb0d-109">Habilita la cuenta y concede al usuario permisos de lectura.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-109">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="dbb0d-110">Este es un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso habilitar cuenta en la pestaña seguridad del [*control WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="dbb0d-110">This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="dbb0d-111">Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="dbb0d-111">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbb0d-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_ejecución del método WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="dbb0d-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb0d-113">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="dbb0d-113">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="dbb0d-114">Permite la ejecución de métodos.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-114">Allows the execution of methods.</span></span> <span data-ttu-id="dbb0d-115">Los proveedores pueden realizar comprobaciones de acceso adicionales.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-115">Providers can perform additional access checks.</span></span> <span data-ttu-id="dbb0d-116">Este es un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso ejecutar métodos en la pestaña seguridad del control WMI.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-116">This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbb0d-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_rellenado completo de WBEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dbb0d-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb0d-118">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="dbb0d-118">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="dbb0d-119">Permite que una cuenta de usuario escriba en las clases del repositorio WMI, así como en las instancias.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-119">Allows a user account to write to classes in the WMI repository as well as instances.</span></span> <span data-ttu-id="dbb0d-120">Un usuario no puede escribir en las clases del sistema.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-120">A user cannot write to system classes.</span></span> <span data-ttu-id="dbb0d-121">Solo los miembros del grupo administradores tienen este permiso.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-121">Only members of the Administrators group have this permission.</span></span> <span data-ttu-id="dbb0d-122">**WBEM \_ El \_ \_ representante de escritura completo** corresponde al permiso de escritura completo en la pestaña seguridad del control WMI.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-122">**WBEM\_FULL\_WRITE\_REP** corresponds to the Full Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbb0d-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_representación parcial de la \_ escritura de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="dbb0d-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb0d-124">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="dbb0d-124">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="dbb0d-125">Permite escribir datos solo en instancias, no en clases.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-125">Allows you to write data to instances only, not classes.</span></span> <span data-ttu-id="dbb0d-126">Un usuario no puede escribir clases en el [*repositorio WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="dbb0d-126">A user cannot write classes to the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="dbb0d-127">Solo los miembros del grupo administradores tienen este derecho.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-127">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="dbb0d-128">**WBEM \_ La \_ \_ representación de escritura parcial** corresponde al permiso de escritura parcial en la pestaña seguridad del control WMI.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-128">**WBEM\_PARTIAL\_WRITE\_REP** corresponds to the Partial Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbb0d-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_proveedor de escritura WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="dbb0d-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb0d-130">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="dbb0d-130">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="dbb0d-131">Permite escribir clases e instancias en los proveedores.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-131">Allows writing classes and instances to providers.</span></span> <span data-ttu-id="dbb0d-132">Tenga en cuenta que los proveedores pueden realizar comprobaciones de acceso adicionales al suplantar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-132">Note that providers can do additional access checks when impersonating a user.</span></span> <span data-ttu-id="dbb0d-133">Este es un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso de escritura de proveedor en la pestaña seguridad del control WMI.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-133">This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbb0d-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_acceso remoto de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="dbb0d-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb0d-135">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="dbb0d-135">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="dbb0d-136">Permite que una cuenta de usuario realice de forma remota las operaciones permitidas por los permisos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-136">Allows a user account to remotely perform any operations allowed by the permissions described above.</span></span> <span data-ttu-id="dbb0d-137">Solo los miembros del grupo administradores tienen este derecho.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-137">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="dbb0d-138">**WBEM \_ El \_ acceso remoto** corresponde al permiso Remote enable en la pestaña seguridad del control WMI.</span><span class="sxs-lookup"><span data-stu-id="dbb0d-138">**WBEM\_REMOTE\_ACCESS** corresponds to the Remote Enable permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbb0d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbb0d-139">Requirements</span></span>



| <span data-ttu-id="dbb0d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb0d-140">Requirement</span></span> | <span data-ttu-id="dbb0d-141">Value</span><span class="sxs-lookup"><span data-stu-id="dbb0d-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb0d-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbb0d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb0d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbb0d-143">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="dbb0d-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbb0d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb0d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbb0d-145">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="dbb0d-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbb0d-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb0d-147"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbb0d-147"><dt>Wbemcli.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb0d-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbb0d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb0d-149">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="dbb0d-149">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="dbb0d-150">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="dbb0d-150">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="dbb0d-151">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="dbb0d-151">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="dbb0d-152">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="dbb0d-152">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="dbb0d-153">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="dbb0d-153">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

