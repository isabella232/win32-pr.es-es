---
description: Representa una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: CIM_MediaPresent (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670057"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a><span data-ttu-id="75839-103">CIM_MediaPresent (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="75839-103">CIM_MediaPresent class (Hyper-V management)</span></span>

<span data-ttu-id="75839-104">Representa una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="75839-104">Represents a relationship in which a storage extent must be accessed through a media access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="75839-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75839-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="75839-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="75839-106">Members</span></span>

<span data-ttu-id="75839-107">La clase **CIM \_ MediaPresent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="75839-107">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="75839-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75839-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75839-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75839-109">Properties</span></span>

<span data-ttu-id="75839-110">La clase **CIM \_ MediaPresent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="75839-110">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75839-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="75839-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75839-112">Tipo de datos: **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="75839-112">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="75839-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="75839-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75839-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="75839-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="75839-115">El dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="75839-115">The media access device.</span></span>

</dd> <dt>

<span data-ttu-id="75839-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="75839-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75839-117">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="75839-117">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="75839-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="75839-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75839-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="75839-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="75839-120">La extensión de almacenamiento a la que se tiene acceso cuando se usa el dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="75839-120">The storage extent that is accessed when using the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="75839-121">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="75839-121">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75839-122">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="75839-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="75839-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="75839-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75839-124">**true** si la extensión de almacenamiento es fija en el dispositivo de acceso a medios y no se puede expulsar; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="75839-124">**true** if the storage extent is fixed in the media access device and can not be ejected; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75839-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75839-125">Requirements</span></span>



| <span data-ttu-id="75839-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="75839-126">Requirement</span></span> | <span data-ttu-id="75839-127">Value</span><span class="sxs-lookup"><span data-stu-id="75839-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75839-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75839-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75839-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="75839-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="75839-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75839-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75839-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75839-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="75839-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75839-132">Namespace</span></span><br/>                | <span data-ttu-id="75839-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="75839-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="75839-134">MOF</span><span class="sxs-lookup"><span data-stu-id="75839-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75839-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75839-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75839-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75839-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75839-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75839-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75839-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="75839-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75839-139">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="75839-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

