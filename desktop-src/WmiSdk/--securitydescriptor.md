---
description: Representa un descriptor de seguridad.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277128"
---
# <a name="__securitydescriptor-class"></a><span data-ttu-id="4d754-103">\_\_SecurityDescriptor (clase)</span><span class="sxs-lookup"><span data-stu-id="4d754-103">\_\_SecurityDescriptor class</span></span>

<span data-ttu-id="4d754-104">La clase del sistema de Resumen de **\_ \_ SecurityDescriptor** representa un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="4d754-104">The **\_\_SecurityDescriptor** abstract system class represents a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="4d754-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4d754-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4d754-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4d754-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d754-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d754-107">Syntax</span></span>

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="4d754-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d754-108">Members</span></span>

<span data-ttu-id="4d754-109">La clase **\_ \_ SecurityDescriptor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d754-109">The **\_\_SecurityDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="4d754-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d754-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d754-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d754-111">Properties</span></span>

<span data-ttu-id="4d754-112">La clase **\_ \_ SecurityDescriptor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4d754-112">The **\_\_SecurityDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d754-113">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="4d754-113">**ControlFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d754-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d754-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d754-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d754-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d754-116">Marcas de bits que proporcionan información sobre el contenido y el formato del descriptor.</span><span class="sxs-lookup"><span data-stu-id="4d754-116">Bit flags that provide information about the descriptor's contents and format.</span></span> <span data-ttu-id="4d754-117">Vea la propiedad **ControlFlags** de la [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) para obtener una descripción de las marcas.</span><span class="sxs-lookup"><span data-stu-id="4d754-117">See the **ControlFlags** property in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class for a description of the flags.</span></span>

</dd> <dt>

<span data-ttu-id="4d754-118">**DACL**</span><span class="sxs-lookup"><span data-stu-id="4d754-118">**DACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d754-119">Tipo de datos: matriz **[**\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="4d754-119">Data type: **[**\_\_ACE**](--ace.md)** array</span></span>
</dt> <dt>

<span data-ttu-id="4d754-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d754-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d754-121">Matriz de entradas [**\_ \_ ACE**](--ace.md) que especifican el acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="4d754-121">An array of [**\_\_ACE**](--ace.md) entries that specify access to the object.</span></span>

</dd> <dt>

<span data-ttu-id="4d754-122">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="4d754-122">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d754-123">Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="4d754-123">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4d754-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d754-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d754-125">ACE que identifica el administrador de confianza que representa el grupo del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d754-125">ACE that identifies the trustee representing the group of the object.</span></span>

</dd> <dt>

<span data-ttu-id="4d754-126">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="4d754-126">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d754-127">Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="4d754-127">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4d754-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d754-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d754-129">ACE que identifica el administrador de confianza que representa el propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d754-129">ACE that identifies the trustee representing the owner of the object.</span></span>

</dd> <dt>

<span data-ttu-id="4d754-130">**SACL**</span><span class="sxs-lookup"><span data-stu-id="4d754-130">**SACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d754-131">Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="4d754-131">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4d754-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d754-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d754-133">Matriz de entradas [**\_ \_ ACE**](--ace.md) que identifica los usuarios y los grupos para los que se recopila información de auditoría.</span><span class="sxs-lookup"><span data-stu-id="4d754-133">An array of [**\_\_ACE**](--ace.md) entries that identifies users and groups for which auditing information is gathered.</span></span>

</dd> <dt>

<span data-ttu-id="4d754-134">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="4d754-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d754-135">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d754-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d754-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d754-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d754-137">Hora en el formato de [ \_ fecha y](cim-datetime.md) hora de CIM cuando se creó el descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4d754-137">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d754-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d754-138">Remarks</span></span>

<span data-ttu-id="4d754-139">Esta clase proporciona propiedades heredadas por el [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="4d754-139">This class provides properties inherited by [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="4d754-140">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4d754-140">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="4d754-141">Para obtener más información sobre las ACE, vea [componentes de Access Control](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="4d754-141">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d754-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d754-142">Requirements</span></span>



| <span data-ttu-id="4d754-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d754-143">Requirement</span></span> | <span data-ttu-id="4d754-144">Value</span><span class="sxs-lookup"><span data-stu-id="4d754-144">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4d754-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d754-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4d754-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d754-146">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4d754-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d754-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4d754-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d754-148">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4d754-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d754-149">Namespace</span></span><br/>                | <span data-ttu-id="4d754-150">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="4d754-150">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4d754-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d754-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d754-152">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="4d754-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4d754-153">**SecurityDescriptor de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="4d754-153">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="4d754-154">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="4d754-154">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

