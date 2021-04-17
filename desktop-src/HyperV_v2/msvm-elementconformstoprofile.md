---
description: Define los perfiles registrados a los que se ajusta el sistema al que se hace referencia.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b0afdc7dd9d55a036de0695f9a88a95d2b01308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687948"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="61096-103">MSVM \_ ElementConformsToProfile (clase)</span><span class="sxs-lookup"><span data-stu-id="61096-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="61096-104">Define los perfiles registrados a los que se ajusta el sistema al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="61096-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="61096-105">Esta asociación se puede aplicar a cualquier elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="61096-105">This association may apply to any managed element.</span></span> <span data-ttu-id="61096-106">El uso típico lo aplicará a una instancia de nivel superior, como un sistema, un espacio de nombres o un servicio.</span><span class="sxs-lookup"><span data-stu-id="61096-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="61096-107">Cuando se aplica a una instancia de nivel superior, todas las partes constituyentes deben comportarse de forma adecuada para admitir la conformidad del elemento administrado con el perfil registrado con nombre.</span><span class="sxs-lookup"><span data-stu-id="61096-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="61096-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="61096-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61096-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61096-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="61096-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="61096-110">Members</span></span>

<span data-ttu-id="61096-111">La clase **MSVM \_ ElementConformsToProfile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="61096-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="61096-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61096-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61096-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61096-113">Properties</span></span>

<span data-ttu-id="61096-114">La clase **MSVM \_ ElementConformsToProfile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="61096-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61096-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="61096-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61096-116">Tipo de datos: **[ **MSVM \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="61096-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="61096-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61096-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61096-118">Calificadores: [ **invalidación**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="61096-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="61096-119">Referencia a una instancia de la clase [**MSVM \_ RegisteredProfile**](msvm-registeredprofile.md) que representa el perfil registrado al que se ajusta el sistema.</span><span class="sxs-lookup"><span data-stu-id="61096-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="61096-120">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="61096-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61096-121">Tipo de datos: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="61096-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="61096-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61096-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61096-123">Calificadores: [ **invalidación**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="61096-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="61096-124">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema que se ajusta al perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="61096-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61096-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61096-125">Requirements</span></span>



| <span data-ttu-id="61096-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="61096-126">Requirement</span></span> | <span data-ttu-id="61096-127">Value</span><span class="sxs-lookup"><span data-stu-id="61096-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61096-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61096-128">Minimum supported client</span></span><br/> | <span data-ttu-id="61096-129">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="61096-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="61096-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61096-130">Minimum supported server</span></span><br/> | <span data-ttu-id="61096-131">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="61096-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="61096-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61096-132">Namespace</span></span><br/>                | <span data-ttu-id="61096-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="61096-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61096-134">MOF</span><span class="sxs-lookup"><span data-stu-id="61096-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61096-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61096-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61096-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61096-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61096-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61096-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

