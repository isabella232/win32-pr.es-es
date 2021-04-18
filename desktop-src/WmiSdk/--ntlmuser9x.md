---
description: Controla el acceso remoto a versiones no admitidas de Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: __NTLMUser9X (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707105"
---
# <a name="__ntlmuser9x-class"></a><span data-ttu-id="7770a-103">\_\_Clase NTLMUser9X</span><span class="sxs-lookup"><span data-stu-id="7770a-103">\_\_NTLMUser9X class</span></span>

<span data-ttu-id="7770a-104">La clase del sistema **\_ \_ NTLMUser9X** controla el acceso remoto a versiones no admitidas de Windows.</span><span class="sxs-lookup"><span data-stu-id="7770a-104">The **\_\_NTLMUser9X** system class controls remote access to unsupported versions of Windows.</span></span> <span data-ttu-id="7770a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7770a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7770a-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7770a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7770a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7770a-107">Syntax</span></span>

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="7770a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7770a-108">Members</span></span>

<span data-ttu-id="7770a-109">La clase **\_ \_ NTLMUser9X** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7770a-109">The **\_\_NTLMUser9X** class has these types of members:</span></span>

-   [<span data-ttu-id="7770a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7770a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7770a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7770a-111">Properties</span></span>

<span data-ttu-id="7770a-112">La clase **\_ \_ NTLMUser9X** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7770a-112">The **\_\_NTLMUser9X** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7770a-113">**Autoridad**</span><span class="sxs-lookup"><span data-stu-id="7770a-113">**Authority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7770a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7770a-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7770a-116">Dominio al que se aplica un nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="7770a-116">Domain to which a user name applies.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-117">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="7770a-117">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-118">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7770a-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7770a-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7770a-120">Marcadores de herencia.</span><span class="sxs-lookup"><span data-stu-id="7770a-120">Inheritance flags.</span></span>

<dt>

<span data-ttu-id="7770a-121">0</span><span class="sxs-lookup"><span data-stu-id="7770a-121">0</span></span>
</dt> <dd>

<span data-ttu-id="7770a-122">Sin herencias.</span><span class="sxs-lookup"><span data-stu-id="7770a-122">No inheritance.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-123">2</span><span class="sxs-lookup"><span data-stu-id="7770a-123">2</span></span>
</dt> <dd>

<span data-ttu-id="7770a-124">Aplicar a los espacios de nombres secundarios, además del actual.</span><span class="sxs-lookup"><span data-stu-id="7770a-124">Apply to child namespaces, in addition to the current one.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7770a-125">**Máscara**</span><span class="sxs-lookup"><span data-stu-id="7770a-125">**Mask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7770a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7770a-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7770a-128">Máscara de máscara que especifica los derechos de acceso al espacio de nombres en el repositorio de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7770a-128">Bitmask that specifies access rights to the namespace in the Windows Management Instrumentation (WMI) repository.</span></span> <span data-ttu-id="7770a-129">Para los valores de bit, consulte [**constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7770a-129">For bit values, see [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-130">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7770a-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7770a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7770a-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7770a-133">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="7770a-133">User name.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-134">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7770a-134">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7770a-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7770a-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7770a-137">Acceso permitido.</span><span class="sxs-lookup"><span data-stu-id="7770a-137">Access allowed.</span></span>

<dt>

<span data-ttu-id="7770a-138">0</span><span class="sxs-lookup"><span data-stu-id="7770a-138">0</span></span>
</dt> <dd>

<span data-ttu-id="7770a-139">Acceso permitido.</span><span class="sxs-lookup"><span data-stu-id="7770a-139">Access allowed.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-140">2</span><span class="sxs-lookup"><span data-stu-id="7770a-140">2</span></span>
</dt> <dd>

<span data-ttu-id="7770a-141">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="7770a-141">Access denied.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7770a-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7770a-142">Remarks</span></span>

<span data-ttu-id="7770a-143">La clase **\_ \_ NTLMUser9X** se usa como parámetro de entrada para los métodos [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) y [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .</span><span class="sxs-lookup"><span data-stu-id="7770a-143">The **\_\_NTLMUser9X** class is used as an input parameter for the [**\_\_SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) and [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="7770a-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7770a-144">Requirements</span></span>



| <span data-ttu-id="7770a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="7770a-145">Requirement</span></span> | <span data-ttu-id="7770a-146">Value</span><span class="sxs-lookup"><span data-stu-id="7770a-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7770a-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7770a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7770a-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7770a-148">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7770a-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7770a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7770a-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7770a-150">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7770a-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7770a-151">Namespace</span></span><br/>                | <span data-ttu-id="7770a-152">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="7770a-152">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7770a-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="7770a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7770a-154">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="7770a-154">**\_\_SecurityRelatedClass**</span></span>](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[<span data-ttu-id="7770a-155">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="7770a-155">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7770a-156">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="7770a-156">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

