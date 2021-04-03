---
description: Asocia una unidad de almacenamiento con el medio insertado en la unidad.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Msvm_MediaPresent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914210"
---
# <a name="msvm_mediapresent-class"></a><span data-ttu-id="4dc2e-103">MSVM \_ MediaPresent (clase)</span><span class="sxs-lookup"><span data-stu-id="4dc2e-103">Msvm\_MediaPresent class</span></span>

<span data-ttu-id="4dc2e-104">Asocia una unidad de almacenamiento con el medio insertado en la unidad.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-104">Associates a storage drive with the media inserted into the drive.</span></span> <span data-ttu-id="4dc2e-105">Esta asociación se utiliza para todos los objetos de unidad de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-105">This association is used for all storage drive objects.</span></span>

<span data-ttu-id="4dc2e-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dc2e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dc2e-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="4dc2e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4dc2e-108">Members</span></span>

<span data-ttu-id="4dc2e-109">La clase **MSVM \_ MediaPresent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4dc2e-109">The **Msvm\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="4dc2e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4dc2e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dc2e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4dc2e-111">Properties</span></span>

<span data-ttu-id="4dc2e-112">La clase **MSVM \_ MediaPresent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-112">The **Msvm\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dc2e-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dc2e-114">Tipo de datos: **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-114">Data type: **[**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span></span>
</dt> <dt>

<span data-ttu-id="4dc2e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4dc2e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dc2e-116">Referencia al dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-116">The reference to the media access device.</span></span> <span data-ttu-id="4dc2e-117">Esta propiedad se hereda de [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="4dc2e-117">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="4dc2e-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dc2e-119">Tipo de datos: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-119">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="4dc2e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4dc2e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dc2e-121">Referencia a la extensión de almacenamiento a la que se tiene acceso con el dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-121">The reference to the storage extent accessed with the media access device.</span></span> <span data-ttu-id="4dc2e-122">Esta propiedad se hereda de [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="4dc2e-122">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="4dc2e-123">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-123">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dc2e-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4dc2e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4dc2e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dc2e-126">Indica si la extensión de almacenamiento a la que se tiene acceso es fija y no se puede expulsar.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-126">Indicates whether the accessed storage extent is fixed and cannot be ejected.</span></span> <span data-ttu-id="4dc2e-127">El valor es **true** para los discos duros y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-127">The value is **True** for hard disks and **False** otherwise.</span></span> <span data-ttu-id="4dc2e-128">Esta propiedad se hereda de [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="4dc2e-128">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dc2e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dc2e-129">Remarks</span></span>

<span data-ttu-id="4dc2e-130">El acceso a la clase **MSVM \_ MediaPresent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="4dc2e-130">Access to the **Msvm\_MediaPresent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4dc2e-131">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4dc2e-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc2e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dc2e-132">Requirements</span></span>



| <span data-ttu-id="4dc2e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dc2e-133">Requirement</span></span> | <span data-ttu-id="4dc2e-134">Value</span><span class="sxs-lookup"><span data-stu-id="4dc2e-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc2e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dc2e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc2e-136">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4dc2e-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4dc2e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dc2e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc2e-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4dc2e-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4dc2e-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4dc2e-139">Namespace</span></span><br/>                | <span data-ttu-id="4dc2e-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4dc2e-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4dc2e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4dc2e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4dc2e-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4dc2e-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4dc2e-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4dc2e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dc2e-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4dc2e-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4dc2e-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dc2e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc2e-146">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-146">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

[<span data-ttu-id="4dc2e-147">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4dc2e-147">**CIM\_MediaPresent**</span></span>](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[<span data-ttu-id="4dc2e-148">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="4dc2e-148">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

