---
description: Cambia el nombre de un nombre de cuenta de usuario.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153369"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a><span data-ttu-id="ecec5-103">Cambiar el nombre del método de la \_ clase Win32 cuentadeusuario</span><span class="sxs-lookup"><span data-stu-id="ecec5-103">Rename method of the Win32\_UserAccount class</span></span>

<span data-ttu-id="ecec5-104">El método **Rename** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cambia el nombre de un nombre de cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="ecec5-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a user account name.</span></span>

<span data-ttu-id="ecec5-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ecec5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ecec5-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ecec5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecec5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecec5-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="ecec5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecec5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecec5-109">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ecec5-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-110">Nuevo nombre de cuenta.</span><span class="sxs-lookup"><span data-stu-id="ecec5-110">New account name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecec5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecec5-111">Return value</span></span>

<span data-ttu-id="ecec5-112">Devuelve uno de los valores enumerados en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="ecec5-112">Returns one of the values listed in the following list.</span></span> <span data-ttu-id="ecec5-113">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ecec5-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ecec5-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ecec5-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ecec5-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="ecec5-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-116">0</span><span class="sxs-lookup"><span data-stu-id="ecec5-116">0</span></span>

<span data-ttu-id="ecec5-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="ecec5-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-118">**No se encontró la instancia**</span><span class="sxs-lookup"><span data-stu-id="ecec5-118">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-119">1</span><span class="sxs-lookup"><span data-stu-id="ecec5-119">1</span></span>

<span data-ttu-id="ecec5-120">No se encuentra la instancia.</span><span class="sxs-lookup"><span data-stu-id="ecec5-120">Instance not found.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-121">**Instancia requerida**</span><span class="sxs-lookup"><span data-stu-id="ecec5-121">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-122">2</span><span class="sxs-lookup"><span data-stu-id="ecec5-122">2</span></span>

<span data-ttu-id="ecec5-123">Instancia requerida.</span><span class="sxs-lookup"><span data-stu-id="ecec5-123">Instance required.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-124">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="ecec5-124">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-125">3</span><span class="sxs-lookup"><span data-stu-id="ecec5-125">3</span></span>

<span data-ttu-id="ecec5-126">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="ecec5-126">Invalid parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-127">**Usuario no encontrado**</span><span class="sxs-lookup"><span data-stu-id="ecec5-127">**User not found**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-128">4</span><span class="sxs-lookup"><span data-stu-id="ecec5-128">4</span></span>

<span data-ttu-id="ecec5-129">Usuario no encontrado.</span><span class="sxs-lookup"><span data-stu-id="ecec5-129">User not found.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-130">**No se encontró el dominio**</span><span class="sxs-lookup"><span data-stu-id="ecec5-130">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-131">5</span><span class="sxs-lookup"><span data-stu-id="ecec5-131">5</span></span>

<span data-ttu-id="ecec5-132">No se encontró el dominio.</span><span class="sxs-lookup"><span data-stu-id="ecec5-132">Domain not found.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-133">**La operación solo se permite en el controlador de dominio principal del dominio**</span><span class="sxs-lookup"><span data-stu-id="ecec5-133">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-134">6</span><span class="sxs-lookup"><span data-stu-id="ecec5-134">6</span></span>

<span data-ttu-id="ecec5-135">La operación solo se permite en el controlador de dominio principal del dominio.</span><span class="sxs-lookup"><span data-stu-id="ecec5-135">Operation is allowed only on the primary domain controller of the domain.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-136">**La operación no se permite en la última cuenta administrativa.**</span><span class="sxs-lookup"><span data-stu-id="ecec5-136">**Operation is not allowed on the last administrative account.**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-137">7</span><span class="sxs-lookup"><span data-stu-id="ecec5-137">7</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-138">**No se permite la operación en grupos especiales especificados; usuario, administrador, local o invitado.**</span><span class="sxs-lookup"><span data-stu-id="ecec5-138">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-139">8</span><span class="sxs-lookup"><span data-stu-id="ecec5-139">8</span></span>

<span data-ttu-id="ecec5-140">No se permite la operación en grupos especiales especificados: usuario, administrador, local o invitado.</span><span class="sxs-lookup"><span data-stu-id="ecec5-140">Operation is not allowed on specified special groups: user, admin, local, or guest.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-141">**Otro error de API**</span><span class="sxs-lookup"><span data-stu-id="ecec5-141">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-142">9</span><span class="sxs-lookup"><span data-stu-id="ecec5-142">9</span></span>

<span data-ttu-id="ecec5-143">Otro error de la API.</span><span class="sxs-lookup"><span data-stu-id="ecec5-143">Other API error.</span></span>

</dd> <dt>

<span data-ttu-id="ecec5-144">**Error interno**</span><span class="sxs-lookup"><span data-stu-id="ecec5-144">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="ecec5-145">10</span><span class="sxs-lookup"><span data-stu-id="ecec5-145">10</span></span>

<span data-ttu-id="ecec5-146">Error interno.</span><span class="sxs-lookup"><span data-stu-id="ecec5-146">Internal error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecec5-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecec5-147">Remarks</span></span>

<span data-ttu-id="ecec5-148">Esta funcionalidad se implementa como un método para proporcionar un contexto independiente para el nuevo nombre que se puede distinguir del valor de la propiedad clave para el nombre que está asociado a la instancia que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="ecec5-148">This functionality is implemented as a method to provide a separate context for the new name that is distinguishable from the key property value for Name that is associated with the instance to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecec5-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecec5-149">Requirements</span></span>



| <span data-ttu-id="ecec5-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecec5-150">Requirement</span></span> | <span data-ttu-id="ecec5-151">Value</span><span class="sxs-lookup"><span data-stu-id="ecec5-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecec5-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecec5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ecec5-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecec5-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ecec5-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecec5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ecec5-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecec5-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecec5-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ecec5-156">Namespace</span></span><br/>                | <span data-ttu-id="ecec5-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ecec5-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ecec5-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ecec5-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecec5-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecec5-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecec5-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ecec5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecec5-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecec5-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecec5-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecec5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecec5-163">**Cuentadeusuario de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ecec5-163">**Win32\_UserAccount**</span></span>](win32-useraccount.md)
</dt> <dt>

<span data-ttu-id="ecec5-164">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ecec5-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

