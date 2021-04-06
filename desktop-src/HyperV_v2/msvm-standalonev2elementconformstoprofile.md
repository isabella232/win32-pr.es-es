---
description: Define los perfiles registrados a los que se ajusta el sistema independiente al que se hace referencia.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Msvm_StandaloneV2ElementConformsToProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001490"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a><span data-ttu-id="6b7a5-103">MSVM \_ StandaloneV2ElementConformsToProfile (clase)</span><span class="sxs-lookup"><span data-stu-id="6b7a5-103">Msvm\_StandaloneV2ElementConformsToProfile class</span></span>

<span data-ttu-id="6b7a5-104">Define los perfiles registrados a los que se ajusta el sistema independiente al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="6b7a5-104">Defines the registered profiles to which the referenced standalone system conforms.</span></span>

<span data-ttu-id="6b7a5-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6b7a5-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7a5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b7a5-106">Syntax</span></span>

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="6b7a5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b7a5-107">Members</span></span>

<span data-ttu-id="6b7a5-108">La clase **MSVM \_ StandaloneV2ElementConformsToProfile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6b7a5-108">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="6b7a5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b7a5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b7a5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b7a5-110">Properties</span></span>

<span data-ttu-id="6b7a5-111">La clase **MSVM \_ StandaloneV2ElementConformsToProfile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6b7a5-111">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b7a5-112">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="6b7a5-112">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b7a5-113">Tipo de datos: **MSVM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="6b7a5-113">Data type: **Msvm\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="6b7a5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b7a5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b7a5-115">Calificadores: [ **invalidación**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b7a5-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b7a5-116">Perfil registrado al que se ajusta el sistema independiente.</span><span class="sxs-lookup"><span data-stu-id="6b7a5-116">The registered profile to which the standalone system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="6b7a5-117">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6b7a5-117">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b7a5-118">Tipo de datos: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6b7a5-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6b7a5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b7a5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b7a5-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers), **msft \_ targetNamespace** (" \\ \\ virtualización de raíz \\ \\ V2")</span><span class="sxs-lookup"><span data-stu-id="6b7a5-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT\_TargetNamespace** ("root\\\\virtualization\\\\v2")</span></span>
</dt> </dl>

<span data-ttu-id="6b7a5-121">Sistema independiente que se ajusta al perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="6b7a5-121">The standalone system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b7a5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b7a5-122">Requirements</span></span>



| <span data-ttu-id="6b7a5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b7a5-123">Requirement</span></span> | <span data-ttu-id="6b7a5-124">Value</span><span class="sxs-lookup"><span data-stu-id="6b7a5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7a5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b7a5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6b7a5-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b7a5-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6b7a5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b7a5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6b7a5-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6b7a5-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6b7a5-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b7a5-129">Namespace</span></span><br/>                | <span data-ttu-id="6b7a5-130">\\Interoperabilidad raíz</span><span class="sxs-lookup"><span data-stu-id="6b7a5-130">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="6b7a5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6b7a5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b7a5-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b7a5-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b7a5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b7a5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b7a5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b7a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7a5-136">**MSVM \_ ElementConformsToProfile**</span><span class="sxs-lookup"><span data-stu-id="6b7a5-136">**Msvm\_ElementConformsToProfile**</span></span>](msvm-elementconformstoprofile.md)
</dt> </dl>

 

