---
description: Permite cambiar el nombre del grupo.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659325"
---
# <a name="rename-method-of-the-win32_group-class"></a><span data-ttu-id="b8eed-103">Cambiar el nombre del método de la clase de grupo de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="b8eed-103">Rename method of the Win32\_Group class</span></span>

<span data-ttu-id="b8eed-104">El método **Rename** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) permite cambiar el nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="b8eed-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows the group name to be changed.</span></span>

<span data-ttu-id="b8eed-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b8eed-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b8eed-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b8eed-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8eed-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8eed-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="b8eed-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8eed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8eed-109">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b8eed-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-110">Nombre de la cuenta de usuario de Windows en el dominio especificado por la propiedad de **dominio** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="b8eed-110">Name of the Windows user account on the domain specified by the **Domain** property of this class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8eed-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8eed-111">Return value</span></span>

<span data-ttu-id="b8eed-112">El método **Rename** puede devolver los códigos de error que se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="b8eed-112">The **Rename** method can return the error codes listed in the following list.</span></span> <span data-ttu-id="b8eed-113">En el caso de valores enteros distintos de los enumerados, consulte los [ \_ códigos de retorno de WMI](/windows/desktop/WmiSdk/wmi-return-codes).</span><span class="sxs-lookup"><span data-stu-id="b8eed-113">For integer values other than those listed, refer to [WMI\_Return Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b8eed-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="b8eed-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-115">0</span><span class="sxs-lookup"><span data-stu-id="b8eed-115">0</span></span>

<span data-ttu-id="b8eed-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b8eed-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-117">**No se encontró la instancia**</span><span class="sxs-lookup"><span data-stu-id="b8eed-117">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-118">1</span><span class="sxs-lookup"><span data-stu-id="b8eed-118">1</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-119">**Instancia requerida**</span><span class="sxs-lookup"><span data-stu-id="b8eed-119">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-120">2</span><span class="sxs-lookup"><span data-stu-id="b8eed-120">2</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-121">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="b8eed-121">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-122">3</span><span class="sxs-lookup"><span data-stu-id="b8eed-122">3</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-123">**Grupo no encontrado**</span><span class="sxs-lookup"><span data-stu-id="b8eed-123">**Group not found**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-124">4</span><span class="sxs-lookup"><span data-stu-id="b8eed-124">4</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-125">**No se encontró el dominio**</span><span class="sxs-lookup"><span data-stu-id="b8eed-125">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-126">5</span><span class="sxs-lookup"><span data-stu-id="b8eed-126">5</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-127">**La operación solo se permite en el controlador de dominio principal del dominio**</span><span class="sxs-lookup"><span data-stu-id="b8eed-127">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-128">6</span><span class="sxs-lookup"><span data-stu-id="b8eed-128">6</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-129">**No se permite la operación en grupos especiales especificados; usuario, administrador, local o invitado.**</span><span class="sxs-lookup"><span data-stu-id="b8eed-129">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-130">7</span><span class="sxs-lookup"><span data-stu-id="b8eed-130">7</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-131">**Otro error de API**</span><span class="sxs-lookup"><span data-stu-id="b8eed-131">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-132">8</span><span class="sxs-lookup"><span data-stu-id="b8eed-132">8</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-133">**Error interno**</span><span class="sxs-lookup"><span data-stu-id="b8eed-133">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="b8eed-134">9</span><span class="sxs-lookup"><span data-stu-id="b8eed-134">9</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8eed-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8eed-135">Requirements</span></span>



| <span data-ttu-id="b8eed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8eed-136">Requirement</span></span> | <span data-ttu-id="b8eed-137">Value</span><span class="sxs-lookup"><span data-stu-id="b8eed-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8eed-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8eed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b8eed-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8eed-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8eed-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8eed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b8eed-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8eed-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8eed-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8eed-142">Namespace</span></span><br/>                | <span data-ttu-id="b8eed-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b8eed-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8eed-144">MOF</span><span class="sxs-lookup"><span data-stu-id="b8eed-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8eed-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8eed-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8eed-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8eed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8eed-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8eed-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8eed-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8eed-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8eed-149">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8eed-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b8eed-150">**\_Grupo Win32**</span><span class="sxs-lookup"><span data-stu-id="b8eed-150">**Win32\_Group**</span></span>](win32-group.md)
</dt> <dt>

[<span data-ttu-id="b8eed-151">**Win32 \_ LogicalFileSecuritySetting**</span><span class="sxs-lookup"><span data-stu-id="b8eed-151">**Win32\_LogicalFileSecuritySetting**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

