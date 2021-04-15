---
description: La \_ \_ clase de sistema abstracta de administrador de confianza representa un administrador de confianza. Se puede usar un nombre o un SID (matriz de bytes).
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547182"
---
# <a name="__trustee-class"></a><span data-ttu-id="c06c7-104">\_\_Trustee (clase)</span><span class="sxs-lookup"><span data-stu-id="c06c7-104">\_\_Trustee class</span></span>

<span data-ttu-id="c06c7-105">La clase de sistema abstracta de [**\_ \_ Administrador de confianza**](--securitydescriptor.md) representa un administrador de [*confianza*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="c06c7-105">The [**\_\_Trustee**](--securitydescriptor.md) abstract system class represents a [*trustee*](/windows/desktop/SecGloss/t-gly).</span></span> <span data-ttu-id="c06c7-106">Se puede usar un nombre o un SID (matriz de bytes).</span><span class="sxs-lookup"><span data-stu-id="c06c7-106">Either a name or an SID (byte array) can be used.</span></span>

<span data-ttu-id="c06c7-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c06c7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c06c7-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c06c7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06c7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c06c7-109">Syntax</span></span>

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c06c7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c06c7-110">Members</span></span>

<span data-ttu-id="c06c7-111">La clase **\_ \_ Trustee** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c06c7-111">The **\_\_Trustee** class has these types of members:</span></span>

-   [<span data-ttu-id="c06c7-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c06c7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c06c7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c06c7-113">Properties</span></span>

<span data-ttu-id="c06c7-114">La clase **\_ \_ Trustee** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c06c7-114">The **\_\_Trustee** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c06c7-115">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="c06c7-115">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c06c7-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c06c7-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c06c7-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c06c7-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c06c7-118">Parte del dominio de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c06c7-118">Domain portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="c06c7-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c06c7-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c06c7-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c06c7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c06c7-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c06c7-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c06c7-122">Parte del nombre de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c06c7-122">Name portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="c06c7-123">**SID**</span><span class="sxs-lookup"><span data-stu-id="c06c7-123">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c06c7-124">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="c06c7-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c06c7-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c06c7-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c06c7-126">El SID del administrador de confianza en el formato de la matriz de bytes binaria.</span><span class="sxs-lookup"><span data-stu-id="c06c7-126">The SID of the trustee in the binary byte array form.</span></span>

</dd> <dt>

<span data-ttu-id="c06c7-127">**SidLength**</span><span class="sxs-lookup"><span data-stu-id="c06c7-127">**SidLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c06c7-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c06c7-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c06c7-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c06c7-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c06c7-130">Longitud del SID en bytes.</span><span class="sxs-lookup"><span data-stu-id="c06c7-130">The length of the SID in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c06c7-131">**SidString**</span><span class="sxs-lookup"><span data-stu-id="c06c7-131">**SidString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c06c7-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c06c7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c06c7-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c06c7-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c06c7-134">SID del administrador de confianza en el formato de cadena, por ejemplo, "S-1-1-0".</span><span class="sxs-lookup"><span data-stu-id="c06c7-134">The SID of the trustee in the string format, for example, "S-1-1-0".</span></span>

</dd> <dt>

<span data-ttu-id="c06c7-135">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="c06c7-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c06c7-136">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c06c7-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c06c7-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c06c7-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c06c7-138">Hora en el formato de [ \_ fecha y](cim-datetime.md) hora de CIM cuando se creó el descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c06c7-138">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c06c7-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c06c7-139">Remarks</span></span>

<span data-ttu-id="c06c7-140">Esta clase proporciona propiedades heredadas por la clase [**de \_ Administrador de confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , que es miembro de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="c06c7-140">This class provides properties that are inherited by the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="c06c7-141">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c06c7-141">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="c06c7-142">Para obtener más información sobre las ACE, vea [componentes de Access Control](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="c06c7-142">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="c06c7-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c06c7-143">Requirements</span></span>



| <span data-ttu-id="c06c7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c06c7-144">Requirement</span></span> | <span data-ttu-id="c06c7-145">Value</span><span class="sxs-lookup"><span data-stu-id="c06c7-145">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c06c7-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c06c7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c06c7-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c06c7-147">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c06c7-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c06c7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c06c7-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c06c7-149">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c06c7-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c06c7-150">Namespace</span></span><br/>                | <span data-ttu-id="c06c7-151">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="c06c7-151">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c06c7-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="c06c7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06c7-153">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="c06c7-153">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c06c7-154">**Administrador de confianza de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="c06c7-154">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[<span data-ttu-id="c06c7-155">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="c06c7-155">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

