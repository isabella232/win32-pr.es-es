---
description: Representa una entrada de control de acceso (ACE).
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: __ACE (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498070"
---
# <a name="__ace-class"></a><span data-ttu-id="e2d96-103">\_\_ACE (clase)</span><span class="sxs-lookup"><span data-stu-id="e2d96-103">\_\_ACE class</span></span>

<span data-ttu-id="e2d96-104">La clase **\_ \_ ACE** Abstract System representa una entrada de control de acceso ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span><span class="sxs-lookup"><span data-stu-id="e2d96-104">The **\_\_ACE** abstract system class represents an access control entry ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span></span>

<span data-ttu-id="e2d96-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e2d96-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e2d96-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e2d96-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d96-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2d96-107">Syntax</span></span>

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a><span data-ttu-id="e2d96-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2d96-108">Members</span></span>

<span data-ttu-id="e2d96-109">La clase **\_ \_ ACE** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e2d96-109">The **\_\_ACE** class has these types of members:</span></span>

-   [<span data-ttu-id="e2d96-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2d96-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2d96-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2d96-111">Properties</span></span>

<span data-ttu-id="e2d96-112">La clase **\_ \_ ACE** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2d96-112">The **\_\_ACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2d96-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="e2d96-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d96-114">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2d96-114">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="e2d96-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e2d96-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2d96-116">Marcas de bits que representan derechos que se conceden o deniegan al administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="e2d96-116">Bit flags representing rights that are granted or denied to the trustee.</span></span> <span data-ttu-id="e2d96-117">Para obtener más información y una descripción de las marcas, consulte propiedad **AccessMask** en la clase [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="e2d96-117">For more information and a description of the flags, see **AccessMask** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="e2d96-118">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="e2d96-118">**AceFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d96-119">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2d96-119">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="e2d96-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e2d96-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2d96-121">Marcas de bits que especifican la herencia de la ACE.</span><span class="sxs-lookup"><span data-stu-id="e2d96-121">Bit flags specifying the inheritance of the ACE.</span></span> <span data-ttu-id="e2d96-122">Para obtener más información y una descripción de las marcas, consulte la propiedad **AceFlags** en la clase [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="e2d96-122">For more information and a description of the flags, see **AceFlags** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="e2d96-123">**AceType**</span><span class="sxs-lookup"><span data-stu-id="e2d96-123">**AceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d96-124">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2d96-124">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="e2d96-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e2d96-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2d96-126">Tipo de entrada ACE que representa esta instancia.</span><span class="sxs-lookup"><span data-stu-id="e2d96-126">The type of ACE entry that this instance represents.</span></span>

</dd> <dt>

<span data-ttu-id="e2d96-127">**GuidInheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="e2d96-127">**GuidInheritedObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d96-128">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2d96-128">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="e2d96-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e2d96-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2d96-130">GUID del objeto primario del objeto al que se aplican los derechos de acceso en la propiedad **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="e2d96-130">The GUID of the parent of the object to which the access rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="e2d96-131">**GuidObjectType**</span><span class="sxs-lookup"><span data-stu-id="e2d96-131">**GuidObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d96-132">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2d96-132">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="e2d96-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e2d96-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2d96-134">GUID que indica el tipo de objeto al que se aplican los derechos de la propiedad **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="e2d96-134">The GUID that indicates the type of object to which the rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="e2d96-135">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="e2d96-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d96-136">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2d96-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2d96-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d96-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d96-138">La hora, en el formato de [ \_ fecha y](cim-datetime.md) hora de CIM, cuando se creó el descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e2d96-138">The time, in the [CIM\_DATETIME](cim-datetime.md) format, when the security descriptor was created.</span></span>

</dd> <dt>

<span data-ttu-id="e2d96-139">**Confianza**</span><span class="sxs-lookup"><span data-stu-id="e2d96-139">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d96-140">Tipo de datos: **[ **\_ \_ Administrador de confianza**](--trustee.md)**</span><span class="sxs-lookup"><span data-stu-id="e2d96-140">Data type: **[**\_\_Trustee**](--trustee.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e2d96-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e2d96-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2d96-142">Administrador de confianza de la entrada ACE representada por esta instancia de la clase **\_ \_ ACE** .</span><span class="sxs-lookup"><span data-stu-id="e2d96-142">The trustee of the ACE entry represented by this instance of the **\_\_ACE** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2d96-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2d96-143">Remarks</span></span>

<span data-ttu-id="e2d96-144">Esta clase proporciona las propiedades que hereda la clase [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , que es miembro de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="e2d96-144">This class provides the properties that are inherited by the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="e2d96-145">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e2d96-145">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="e2d96-146">Para obtener más información sobre las ACE, vea [componentes de Access Control](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="e2d96-146">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d96-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d96-147">Requirements</span></span>



| <span data-ttu-id="e2d96-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d96-148">Requirement</span></span> | <span data-ttu-id="e2d96-149">Value</span><span class="sxs-lookup"><span data-stu-id="e2d96-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e2d96-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2d96-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d96-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2d96-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e2d96-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2d96-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d96-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2d96-153">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e2d96-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2d96-154">Namespace</span></span><br/>                | <span data-ttu-id="e2d96-155">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="e2d96-155">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e2d96-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2d96-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d96-157">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="e2d96-157">**\_\_SecurityRelatedClass**</span></span>](--securityrelatedclass.md)
</dt> <dt>

[<span data-ttu-id="e2d96-158">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="e2d96-158">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e2d96-159">**ACE de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="e2d96-159">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="e2d96-160">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="e2d96-160">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

