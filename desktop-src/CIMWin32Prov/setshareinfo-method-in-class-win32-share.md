---
description: SetShareInfo&\# 8194; El método de clase WMI establece los parámetros de un recurso compartido.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Método SetShareInfo de la clase Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275101"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a><span data-ttu-id="9ade0-103">Método SetShareInfo de la \_ clase de recursos compartidos de Win32</span><span class="sxs-lookup"><span data-stu-id="9ade0-103">SetShareInfo method of the Win32\_Share class</span></span>

<span data-ttu-id="9ade0-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** establece los parámetros de un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="9ade0-104">The **SetShareInfo** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the parameters of a shared resource.</span></span>

<span data-ttu-id="9ade0-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9ade0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9ade0-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9ade0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ade0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ade0-107">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="9ade0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ade0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ade0-109">*MaximumAllowed* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9ade0-109">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ade0-110">Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="9ade0-110">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

<span data-ttu-id="9ade0-111">Ejemplo: 10.</span><span class="sxs-lookup"><span data-stu-id="9ade0-111">Example: 10.</span></span> <span data-ttu-id="9ade0-112">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="9ade0-112">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="9ade0-113">*Descripción* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9ade0-113">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ade0-114">Comentario opcional para describir el recurso que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="9ade0-114">Optional comment to describe the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="9ade0-115">*Acceso a* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9ade0-115">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ade0-116">Descriptor de seguridad para permisos de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="9ade0-116">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="9ade0-117">Un descriptor de seguridad contiene información sobre el permiso, el propietario y las capacidades de acceso del recurso.</span><span class="sxs-lookup"><span data-stu-id="9ade0-117">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="9ade0-118">Para obtener más información, [**vea \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="9ade0-118">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ade0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ade0-119">Return value</span></span>

<span data-ttu-id="9ade0-120">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="9ade0-120">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9ade0-121">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="9ade0-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-122">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="9ade0-122">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-123">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="9ade0-123">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-124">**Nombre no válido** (9)</span><span class="sxs-lookup"><span data-stu-id="9ade0-124">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-125">**Nivel no válido** (10)</span><span class="sxs-lookup"><span data-stu-id="9ade0-125">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-126">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="9ade0-126">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-127">**Recurso compartido duplicado** (22)</span><span class="sxs-lookup"><span data-stu-id="9ade0-127">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-128">**Ruta de acceso redirigida** (23)</span><span class="sxs-lookup"><span data-stu-id="9ade0-128">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-129">**Dispositivo o directorio desconocido** (24)</span><span class="sxs-lookup"><span data-stu-id="9ade0-129">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-130">**No se encontró el nombre de red** (25)</span><span class="sxs-lookup"><span data-stu-id="9ade0-130">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="9ade0-131">**Otro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="9ade0-131">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9ade0-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ade0-132">Remarks</span></span>

<span data-ttu-id="9ade0-133">El método **SetShareInfo** es un método de objeto dinámico y se usa en una aparición de esta clase.</span><span class="sxs-lookup"><span data-stu-id="9ade0-133">**SetShareInfo** method is a dynamic object method and is used on an occurrence of this class.</span></span>

<span data-ttu-id="9ade0-134">Solo los miembros del grupo local Administradores o operadores de cuenta, o los que tengan la pertenencia a un grupo de operador de servidor o de comunicación pueden ejecutar correctamente **SetShareInfo**.</span><span class="sxs-lookup"><span data-stu-id="9ade0-134">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **SetShareInfo**.</span></span> <span data-ttu-id="9ade0-135">El operador Print solo puede establecer colas de impresora.</span><span class="sxs-lookup"><span data-stu-id="9ade0-135">The print operator can only set printer queues.</span></span> <span data-ttu-id="9ade0-136">El operador de comunicación solo puede establecer colas de dispositivos de comunicación.</span><span class="sxs-lookup"><span data-stu-id="9ade0-136">The Communication operator can only set communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="9ade0-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9ade0-137">Examples</span></span>

<span data-ttu-id="9ade0-138">El siguiente ejemplo de PowerShell actualiza el nombre del recurso compartido **newShare** .</span><span class="sxs-lookup"><span data-stu-id="9ade0-138">The following PowerShell sample updates the name of the **newShare** share.</span></span>


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a><span data-ttu-id="9ade0-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ade0-139">Requirements</span></span>



| <span data-ttu-id="9ade0-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ade0-140">Requirement</span></span> | <span data-ttu-id="9ade0-141">Value</span><span class="sxs-lookup"><span data-stu-id="9ade0-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ade0-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ade0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9ade0-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ade0-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ade0-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ade0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9ade0-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ade0-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ade0-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ade0-146">Namespace</span></span><br/>                | <span data-ttu-id="9ade0-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9ade0-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ade0-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9ade0-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ade0-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ade0-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ade0-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ade0-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ade0-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ade0-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ade0-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ade0-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ade0-153">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ade0-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9ade0-154">**\_Recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="9ade0-154">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

