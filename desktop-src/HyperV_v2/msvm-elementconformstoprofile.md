---
description: Define los perfiles registrados a los que se ajusta el sistema al que se hace referencia.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile clase
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
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843286"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="b5483-103">Clase \_ ElementConformsToProfile de Msvm</span><span class="sxs-lookup"><span data-stu-id="b5483-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="b5483-104">Define los perfiles registrados a los que se ajusta el sistema al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="b5483-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="b5483-105">Esta asociación puede aplicarse a cualquier elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="b5483-105">This association may apply to any managed element.</span></span> <span data-ttu-id="b5483-106">El uso típico lo aplicará a una instancia de nivel superior, como un sistema, un espacio de nombres o un servicio.</span><span class="sxs-lookup"><span data-stu-id="b5483-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="b5483-107">Cuando se aplica a una instancia de nivel superior, todas las partes constituyentes deben comportarse correctamente en apoyo de la conformidad del elemento administrado con el perfil registrado con nombre.</span><span class="sxs-lookup"><span data-stu-id="b5483-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="b5483-108">La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b5483-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5483-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5483-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="b5483-110">Members</span><span class="sxs-lookup"><span data-stu-id="b5483-110">Members</span></span>

<span data-ttu-id="b5483-111">La **clase \_ ElementConformsToProfile de Msvm** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b5483-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="b5483-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5483-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5483-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5483-113">Properties</span></span>

<span data-ttu-id="b5483-114">La **clase \_ ElementConformsToProfile de Msvm** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b5483-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5483-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="b5483-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5483-116">Tipo de datos: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="b5483-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b5483-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b5483-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5483-118">Calificadores: [ **Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5483-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5483-119">Referencia a una instancia de la clase [**\_ RegisteredProfile de Msvm**](msvm-registeredprofile.md) que representa el perfil registrado al que se ajusta el sistema.</span><span class="sxs-lookup"><span data-stu-id="b5483-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="b5483-120">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="b5483-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5483-121">Tipo de datos: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="b5483-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b5483-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b5483-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5483-123">Calificadores: [ **Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5483-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5483-124">Referencia a una instancia de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa el sistema que se ajusta al perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="b5483-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5483-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5483-125">Requirements</span></span>



| <span data-ttu-id="b5483-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5483-126">Requirement</span></span> | <span data-ttu-id="b5483-127">Value</span><span class="sxs-lookup"><span data-stu-id="b5483-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5483-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5483-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5483-129">Windows 8.1 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="b5483-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b5483-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5483-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5483-131">Solo aplicaciones de escritorio de Windows Server 2012 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="b5483-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5483-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5483-132">Namespace</span></span><br/>                | <span data-ttu-id="b5483-133">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="b5483-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5483-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b5483-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5483-135"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5483-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5483-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5483-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5483-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5483-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

