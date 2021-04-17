---
description: Representa una asociación en la que un elemento administrado se ajusta al estándar de un perfil registrado.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: CIM_ElementConformsToProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666692"
---
# <a name="cim_elementconformstoprofile-class"></a><span data-ttu-id="dd965-103">\_Clase ElementConformsToProfile de CIM</span><span class="sxs-lookup"><span data-stu-id="dd965-103">CIM\_ElementConformsToProfile class</span></span>

<span data-ttu-id="dd965-104">Representa una asociación en la que un elemento administrado se ajusta al estándar de un perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="dd965-104">Represents an association in which a managed element conforms to the standard of a registered profile.</span></span> <span data-ttu-id="dd965-105">Esta asociación se aplica normalmente a una instancia de nivel superior, como un sistema, un espacio de nombres o un servicio.</span><span class="sxs-lookup"><span data-stu-id="dd965-105">This association usually applies to a higher level instance, such as a system, namespace, or service.</span></span> <span data-ttu-id="dd965-106">Cuando se aplica a una instancia de nivel superior, todas las partes constituyentes deben comportarse de forma adecuada para admitir la conformidad del ManagedElement con el RegisteredProfile con nombre.</span><span class="sxs-lookup"><span data-stu-id="dd965-106">When applied to a higher level instance, all constituent parts MUST behave appropriately in support of the ManagedElement's conformance to the named RegisteredProfile.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd965-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd965-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="dd965-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd965-108">Members</span></span>

<span data-ttu-id="dd965-109">La clase **CIM \_ ElementConformsToProfile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dd965-109">The **CIM\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="dd965-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd965-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd965-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd965-111">Properties</span></span>

<span data-ttu-id="dd965-112">La clase **CIM \_ ElementConformsToProfile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd965-112">The **CIM\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd965-113">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="dd965-113">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd965-114">Tipo de datos: **CIM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="dd965-114">Data type: **CIM\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="dd965-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd965-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd965-116">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd965-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd965-117">Perfil registrado al que se ajusta el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="dd965-117">The registered profile to which the managed element conforms.</span></span>

</dd> <dt>

<span data-ttu-id="dd965-118">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="dd965-118">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd965-119">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="dd965-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="dd965-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd965-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd965-121">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd965-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd965-122">Elemento administrado que se ajusta al perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="dd965-122">The managed element that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd965-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd965-123">Requirements</span></span>



| <span data-ttu-id="dd965-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd965-124">Requirement</span></span> | <span data-ttu-id="dd965-125">Value</span><span class="sxs-lookup"><span data-stu-id="dd965-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd965-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd965-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dd965-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dd965-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dd965-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd965-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dd965-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dd965-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dd965-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd965-130">Namespace</span></span><br/>                | <span data-ttu-id="dd965-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dd965-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd965-132">MOF</span><span class="sxs-lookup"><span data-stu-id="dd965-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd965-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd965-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd965-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd965-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd965-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd965-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

