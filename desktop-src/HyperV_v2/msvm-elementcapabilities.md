---
description: Representa la asociación entre los elementos administrados y sus capacidades.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Msvm_ElementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687845"
---
# <a name="msvm_elementcapabilities-class"></a><span data-ttu-id="2a400-103">MSVM \_ ElementCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="2a400-103">Msvm\_ElementCapabilities class</span></span>

<span data-ttu-id="2a400-104">Representa la asociación entre los elementos administrados y sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="2a400-104">Represents the association between managed elements and their capabilities.</span></span>

<span data-ttu-id="2a400-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2a400-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a400-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a400-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="2a400-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a400-107">Members</span></span>

<span data-ttu-id="2a400-108">La clase **MSVM \_ ElementCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2a400-108">The **Msvm\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="2a400-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a400-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a400-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a400-110">Properties</span></span>

<span data-ttu-id="2a400-111">La clase **MSVM \_ ElementCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2a400-111">The **Msvm\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a400-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2a400-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a400-113">Tipo de datos: **[ **\_ capacidades de CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="2a400-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="2a400-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a400-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a400-115">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="2a400-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2a400-116">Objeto Capabilities asociado al elemento.</span><span class="sxs-lookup"><span data-stu-id="2a400-116">The capabilities object associated with the element.</span></span> <span data-ttu-id="2a400-117">Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="2a400-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="2a400-118">**Características**</span><span class="sxs-lookup"><span data-stu-id="2a400-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a400-119">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a400-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a400-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a400-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a400-121">Proporciona información descriptiva acerca de las capacidades de.</span><span class="sxs-lookup"><span data-stu-id="2a400-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="2a400-122">Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="2a400-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="2a400-123">Value</span><span class="sxs-lookup"><span data-stu-id="2a400-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="2a400-124">Significado</span><span class="sxs-lookup"><span data-stu-id="2a400-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="2a400-125"><dt>**Valor predeterminado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2a400-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="2a400-126">Las capacidades asociadas representan las funciones predeterminadas del elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="2a400-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="2a400-127"><dt>**Actual**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a400-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="2a400-128">Las capacidades asociadas representan las capacidades actuales del elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="2a400-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a400-129">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="2a400-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a400-130">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="2a400-130">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="2a400-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a400-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a400-132">Calificadores: **clave**, **mín** . (1)</span><span class="sxs-lookup"><span data-stu-id="2a400-132">Qualifiers: **Key**, **Min** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="2a400-133">Elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="2a400-133">The managed element.</span></span> <span data-ttu-id="2a400-134">Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="2a400-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a400-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a400-135">Remarks</span></span>

<span data-ttu-id="2a400-136">El acceso a la clase **MSVM \_ ElementCapabilities** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="2a400-136">Access to the **Msvm\_ElementCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2a400-137">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2a400-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a400-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a400-138">Requirements</span></span>



| <span data-ttu-id="2a400-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a400-139">Requirement</span></span> | <span data-ttu-id="2a400-140">Value</span><span class="sxs-lookup"><span data-stu-id="2a400-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a400-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a400-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2a400-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a400-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a400-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a400-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2a400-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a400-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a400-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a400-145">Namespace</span></span><br/>                | <span data-ttu-id="2a400-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2a400-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a400-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2a400-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a400-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a400-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a400-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a400-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a400-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a400-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a400-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a400-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a400-152">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="2a400-152">**CIM\_ElementCapabilities**</span></span>](cim-elementcapabilities.md)
</dt> <dt>

[<span data-ttu-id="2a400-153">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="2a400-153">**CIM\_ElementCapabilities**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[<span data-ttu-id="2a400-154">**MSVM \_ ElementCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="2a400-154">**Msvm\_ElementCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

