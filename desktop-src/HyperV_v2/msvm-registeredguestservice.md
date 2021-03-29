---
description: Representa una asociación entre una instancia de MSVM \_ GuestServiceInterfaceComponent y una instancia de MSVM \_ GuestService, que representa un servicio que se ejecuta en el invitado.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Msvm_RegisteredGuestService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814214"
---
# <a name="msvm_registeredguestservice-class"></a><span data-ttu-id="022a2-103">MSVM \_ RegisteredGuestService (clase)</span><span class="sxs-lookup"><span data-stu-id="022a2-103">Msvm\_RegisteredGuestService class</span></span>

<span data-ttu-id="022a2-104">Representa una asociación entre una instancia de [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) y una instancia de [**MSVM \_ GuestService**](msvm-guestservice.md), que representa un servicio que se ejecuta en el invitado.</span><span class="sxs-lookup"><span data-stu-id="022a2-104">Represents an association between an instance of [**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) and an instance of [**Msvm\_GuestService**](msvm-guestservice.md), which represents a service running in the guest.</span></span> <span data-ttu-id="022a2-105">Esta clase se deriva de la clase de [**\_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="022a2-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="022a2-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="022a2-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="022a2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="022a2-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="022a2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="022a2-108">Members</span></span>

<span data-ttu-id="022a2-109">La clase **MSVM \_ RegisteredGuestService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="022a2-109">The **Msvm\_RegisteredGuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="022a2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="022a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="022a2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="022a2-111">Properties</span></span>

<span data-ttu-id="022a2-112">La clase **MSVM \_ RegisteredGuestService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="022a2-112">The **Msvm\_RegisteredGuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="022a2-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="022a2-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022a2-114">Tipo de datos: **[ **MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="022a2-114">Data type: **[**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="022a2-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="022a2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="022a2-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. antecedente")</span><span class="sxs-lookup"><span data-stu-id="022a2-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="022a2-117">Referencia al componente de la interfaz de servicio de invitado en esta asociación.</span><span class="sxs-lookup"><span data-stu-id="022a2-117">Reference to the guest service interface component in this association.</span></span>

</dd> <dt>

<span data-ttu-id="022a2-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="022a2-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022a2-119">Tipo de datos: **[ **MSVM \_ GuestService**](msvm-guestservice.md)**</span><span class="sxs-lookup"><span data-stu-id="022a2-119">Data type: **[**Msvm\_GuestService**](msvm-guestservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="022a2-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="022a2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="022a2-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Dependent")</span><span class="sxs-lookup"><span data-stu-id="022a2-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="022a2-122">Referencia al servicio invitado registrado que depende de la propiedad **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="022a2-122">Reference to the registered guest service that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="022a2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="022a2-123">Requirements</span></span>



| <span data-ttu-id="022a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="022a2-124">Requirement</span></span> | <span data-ttu-id="022a2-125">Value</span><span class="sxs-lookup"><span data-stu-id="022a2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="022a2-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="022a2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="022a2-127">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="022a2-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="022a2-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="022a2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="022a2-129">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="022a2-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="022a2-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="022a2-130">Namespace</span></span><br/>                | <span data-ttu-id="022a2-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="022a2-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="022a2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="022a2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="022a2-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="022a2-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="022a2-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="022a2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="022a2-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="022a2-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="022a2-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="022a2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022a2-137">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="022a2-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="022a2-138">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="022a2-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

