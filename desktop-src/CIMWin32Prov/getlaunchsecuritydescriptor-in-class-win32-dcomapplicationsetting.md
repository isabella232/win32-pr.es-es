---
description: Obtiene el descriptor de seguridad que controla quién tiene permiso para iniciar una aplicación DCOM.
ms.assetid: ba02807f-aa2a-4b1c-9692-2803d93cd2ee
ms.tgt_platform: multiple
title: Método GetLaunchSecurityDescriptor de la clase Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6d434c0cc9a4d236350f3dd4d15cf9d8c8e5ad4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274919"
---
# <a name="getlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="fae3f-103">Método GetLaunchSecurityDescriptor de la \_ clase DCOMApplicationSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="fae3f-103">GetLaunchSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="fae3f-104">El método WMI **GetLaunchSecurityDescriptor** obtiene el descriptor de seguridad que controla quién tiene permiso para iniciar una aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="fae3f-104">The **GetLaunchSecurityDescriptor** WMI method gets the security descriptor that controls who is allowed to start a DCOM application.</span></span> <span data-ttu-id="fae3f-105">El descriptor de seguridad es una instancia de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="fae3f-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="fae3f-106">La cuenta que ejecuta el script o la aplicación que llama a este método debe tener los privilegios **SeSecurityPrivilege** y **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="fae3f-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="fae3f-107">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="fae3f-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="fae3f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fae3f-108">Syntax</span></span>


```mof
uint32 GetLaunchSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="fae3f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fae3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae3f-110">*Descriptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fae3f-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fae3f-111">Descriptor de seguridad que se va a establecer que controla quién puede iniciar la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="fae3f-111">The security descriptor to set that controls who can start the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae3f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fae3f-112">Return value</span></span>

<span data-ttu-id="fae3f-113">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="fae3f-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="fae3f-114">Para obtener más información, vea [códigos de retorno de WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fae3f-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="fae3f-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="fae3f-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="fae3f-116">0</span><span class="sxs-lookup"><span data-stu-id="fae3f-116">0</span></span>

<span data-ttu-id="fae3f-117">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="fae3f-117">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="fae3f-118">**2**</span><span class="sxs-lookup"><span data-stu-id="fae3f-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fae3f-119">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="fae3f-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="fae3f-120">**8**</span><span class="sxs-lookup"><span data-stu-id="fae3f-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fae3f-121">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="fae3f-121">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="fae3f-122">**9**</span><span class="sxs-lookup"><span data-stu-id="fae3f-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fae3f-123">El usuario no tiene los privilegios adecuados para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="fae3f-123">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="fae3f-124">**21**</span><span class="sxs-lookup"><span data-stu-id="fae3f-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fae3f-125">Un parámetro especificado en la llamada al método no es válido.</span><span class="sxs-lookup"><span data-stu-id="fae3f-125">A parameter specified in the method call is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fae3f-126">**Otros**</span><span class="sxs-lookup"><span data-stu-id="fae3f-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fae3f-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="fae3f-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fae3f-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fae3f-128">Remarks</span></span>

<span data-ttu-id="fae3f-129">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="fae3f-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="fae3f-130">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="fae3f-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="fae3f-131">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="fae3f-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="fae3f-132">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="fae3f-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="fae3f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fae3f-133">Requirements</span></span>



| <span data-ttu-id="fae3f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae3f-134">Requirement</span></span> | <span data-ttu-id="fae3f-135">Value</span><span class="sxs-lookup"><span data-stu-id="fae3f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fae3f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae3f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fae3f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fae3f-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fae3f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae3f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fae3f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fae3f-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fae3f-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fae3f-140">Namespace</span></span><br/>                | <span data-ttu-id="fae3f-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fae3f-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fae3f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fae3f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fae3f-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fae3f-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fae3f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fae3f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae3f-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae3f-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fae3f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="fae3f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae3f-147">**Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="fae3f-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="fae3f-148">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="fae3f-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="fae3f-149">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="fae3f-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="fae3f-150">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="fae3f-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

