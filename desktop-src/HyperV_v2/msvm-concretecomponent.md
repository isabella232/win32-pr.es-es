---
description: Asociación genérica que se usa para establecer parte de las relaciones entre los elementos administrados.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Msvm_ConcreteComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667827"
---
# <a name="msvm_concretecomponent-class"></a><span data-ttu-id="6ccea-103">MSVM \_ ConcreteComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="6ccea-103">Msvm\_ConcreteComponent class</span></span>

<span data-ttu-id="6ccea-104">Asociación genérica que se usa para establecer relaciones entre elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="6ccea-104">A generic association used to establish 'part of' relationships between managed elements.</span></span> <span data-ttu-id="6ccea-105">[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) se define como una subclase concreta de la clase [**del \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component) abstracto, que se utilizará en lugar de muchas subclases concretas de componente que no agregan ninguna semántica (es decir, subclases que no aclaran el tipo de composición, actualizan cardinalidades o agregan o quitan calificadores).</span><span class="sxs-lookup"><span data-stu-id="6ccea-105">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) is defined as a concrete subclass of the abstract [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component) class, to be used in place of many specific subclasses of component that add no semantics (that is subclasses that do not clarify the type of composition, update cardinalities, or add or remove qualifiers.)</span></span>

<span data-ttu-id="6ccea-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6ccea-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ccea-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6ccea-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ccea-108">Members</span></span>

<span data-ttu-id="6ccea-109">La clase **MSVM \_ ConcreteComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6ccea-109">The **Msvm\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="6ccea-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ccea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ccea-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ccea-111">Properties</span></span>

<span data-ttu-id="6ccea-112">La clase **MSVM \_ ConcreteComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6ccea-112">The **Msvm\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ccea-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6ccea-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ccea-114">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="6ccea-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="6ccea-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ccea-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ccea-116">Elemento primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="6ccea-116">The parent element in the association.</span></span> <span data-ttu-id="6ccea-117">Esta propiedad se hereda de [**\_ ConcreteComponent CIM**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ccea-117">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6ccea-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6ccea-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ccea-119">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="6ccea-119">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="6ccea-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ccea-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ccea-121">Elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="6ccea-121">The child element in the association.</span></span> <span data-ttu-id="6ccea-122">Esta propiedad se hereda de [**\_ ConcreteComponent CIM**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ccea-122">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ccea-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ccea-123">Remarks</span></span>

<span data-ttu-id="6ccea-124">El acceso a la clase **MSVM \_ ConcreteComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="6ccea-124">Access to the **Msvm\_ConcreteComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6ccea-125">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6ccea-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccea-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ccea-126">Requirements</span></span>



| <span data-ttu-id="6ccea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ccea-127">Requirement</span></span> | <span data-ttu-id="6ccea-128">Value</span><span class="sxs-lookup"><span data-stu-id="6ccea-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccea-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ccea-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccea-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ccea-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ccea-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ccea-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccea-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ccea-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ccea-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ccea-133">Namespace</span></span><br/>                | <span data-ttu-id="6ccea-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6ccea-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ccea-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6ccea-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ccea-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ccea-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ccea-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ccea-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ccea-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ccea-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ccea-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ccea-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccea-140">**\_CONCRETECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6ccea-140">**CIM\_ConcreteComponent**</span></span>](cim-concretecomponent.md)
</dt> <dt>

<span data-ttu-id="6ccea-141">[**\_CONCRETECOMPONENT CIM**](/previous-versions//cc150665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ccea-141">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6ccea-142">Clases de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="6ccea-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

