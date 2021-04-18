---
description: Establece el parámetro Rights como un mapa de bits con cada bit correspondiente a un derecho de acceso.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Método GetCallerAccessRights de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706845"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a><span data-ttu-id="d2a29-103">Método GetCallerAccessRights de la \_ \_ clase SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="d2a29-103">GetCallerAccessRights method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="d2a29-104">El método **\_ \_ SystemSecurity:: GetCallerAccessRights** establece el parámetro *Rights* como un mapa de bits con cada bit correspondiente a un derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="d2a29-104">The **\_\_SystemSecurity::GetCallerAccessRights** method sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span> <span data-ttu-id="d2a29-105">Cualquier cliente puede llamar a este método para determinar qué derechos tiene el cliente.</span><span class="sxs-lookup"><span data-stu-id="d2a29-105">Any client can call this to determine which rights the client has.</span></span> <span data-ttu-id="d2a29-106">Este método es útil para los clientes que habilitan o deshabilitan características de.</span><span class="sxs-lookup"><span data-stu-id="d2a29-106">This method is useful for clients that enable or disable features.</span></span> <span data-ttu-id="d2a29-107">Por ejemplo, una aplicación GUI podría deshabilitar un botón si el usuario que ha iniciado sesión actualmente no tiene derechos de ejecución del método.</span><span class="sxs-lookup"><span data-stu-id="d2a29-107">For example, a GUI application might disable a button if the currently logged-on user does not have method execution rights.</span></span>

<span data-ttu-id="d2a29-108">Cualquier cliente habilitado tiene derecho a llamar a **GetCallerAccessRights**, incluso si ese cliente no tiene derechos de ejecución de método general.</span><span class="sxs-lookup"><span data-stu-id="d2a29-108">Any enabled client has the right to call **GetCallerAccessRights**, even if that client does not have general method execution rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a29-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2a29-109">Syntax</span></span>


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a><span data-ttu-id="d2a29-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2a29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a29-111">*derechos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d2a29-111">*rights* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a29-112">Derechos de acceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="d2a29-112">Access rights of the client.</span></span> <span data-ttu-id="d2a29-113">Para obtener más información, vea [**\_ \_ SystemSecurity**](--systemsecurity.md) y las [constantes de seguridad WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d2a29-113">For more information, see [**\_\_SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span></span>

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span data-ttu-id="d2a29-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ HABILITAR** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d2a29-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-115">Habilita la cuenta y concede al usuario permisos de lectura.</span><span class="sxs-lookup"><span data-stu-id="d2a29-115">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="d2a29-116">Este es el derecho de acceso predeterminado para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d2a29-116">This is the default access right for all users.</span></span>

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span data-ttu-id="d2a29-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ MÉTODO \_ Execute** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="d2a29-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-118">Permite la ejecución de métodos.</span><span class="sxs-lookup"><span data-stu-id="d2a29-118">Allows the execution of methods.</span></span>

> [!Note]  
> <span data-ttu-id="d2a29-119">Los proveedores pueden realizar comprobaciones de acceso adicionales.</span><span class="sxs-lookup"><span data-stu-id="d2a29-119">Providers may perform additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span data-ttu-id="d2a29-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ Rellenado completo de \_ escritura \_** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="d2a29-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-121">Permite que el llamador, el contexto de seguridad o el usuario escriba en clases e instancias excepto en las clases del sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a29-121">Allows the caller, security context, or user to write to classes and instances except for system classes.</span></span>

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span data-ttu-id="d2a29-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Rep. de escritura parcial** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="d2a29-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-123">Permite que el autor de la llamada, el contexto de seguridad o el usuario escriban instancias de proveedor, pero no clases estáticas o instancias estáticas en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="d2a29-123">Allows the caller, security context, or user to write provider instances but not static classes or static instances to the repository.</span></span>

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span data-ttu-id="d2a29-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Proveedor de escritura** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d2a29-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-125">Permite que el autor de la llamada, el contexto de seguridad o el usuario escriban clases e instancias en los proveedores.</span><span class="sxs-lookup"><span data-stu-id="d2a29-125">Allows the caller, security context, or user to write classes and instances to providers.</span></span>

> [!Note]  
> <span data-ttu-id="d2a29-126">Los proveedores de suplantación pueden realizar comprobaciones de acceso adicionales.</span><span class="sxs-lookup"><span data-stu-id="d2a29-126">Impersonating providers may do additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span data-ttu-id="d2a29-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Acceso remoto** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d2a29-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-128">Permite que una cuenta de usuario realice de forma remota las operaciones permitidas por los permisos establecidos por otros bits.</span><span class="sxs-lookup"><span data-stu-id="d2a29-128">Allows a user account to remotely perform any operations allowed by the permissions set by other bits.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="d2a29-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d2a29-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-130">Permite el acceso de lectura a los descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d2a29-130">Allows read access to the security descriptors.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="d2a29-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="d2a29-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="d2a29-132">Permite el acceso de escritura a las listas de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="d2a29-132">Allows write access to discretionary access control lists (DACL).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a29-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2a29-133">Return value</span></span>

<span data-ttu-id="d2a29-134">Este método devuelve un **valor HRESULT** que indica el estado de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="d2a29-134">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="d2a29-135">En la lista siguiente se muestran los valores devueltos que son significativos para [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span><span class="sxs-lookup"><span data-stu-id="d2a29-135">The following list lists the return values that are of significance to [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span></span> <span data-ttu-id="d2a29-136">En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2a29-136">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="d2a29-137">Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2a29-137">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="d2a29-138">**WBEM \_ E \_ método \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="d2a29-138">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="d2a29-139">Este método no se admite en las versiones compatibles de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2a29-139">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2a29-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2a29-140">Requirements</span></span>



| <span data-ttu-id="d2a29-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a29-141">Requirement</span></span> | <span data-ttu-id="d2a29-142">Value</span><span class="sxs-lookup"><span data-stu-id="d2a29-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d2a29-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a29-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a29-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2a29-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d2a29-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a29-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a29-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2a29-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d2a29-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2a29-147">Namespace</span></span><br/>                | <span data-ttu-id="d2a29-148">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="d2a29-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d2a29-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2a29-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a29-150">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d2a29-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d2a29-151">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="d2a29-151">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="d2a29-152">**\_\_SystemSecurity:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="d2a29-152">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="d2a29-153">**\_\_SystemSecurity:: establecido**</span><span class="sxs-lookup"><span data-stu-id="d2a29-153">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="d2a29-154">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="d2a29-154">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="d2a29-155">**ACE de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d2a29-155">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="d2a29-156">**SecurityDescriptor de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d2a29-156">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="d2a29-157">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="d2a29-157">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

<span data-ttu-id="d2a29-158">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="d2a29-158">WMI Security Constants</span></span>
</dt> </dl>

 

