---
description: Asociación entre una instancia de CIM \_ VirtualSystemSettingData y la instancia de \_ VIRTUALSYSTEMSETTINGDATA de CIM que representa la instantánea más reciente en la que se basa este objeto.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: CIM_ParentChildSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718823"
---
# <a name="cim_parentchildsettingdata-class"></a><span data-ttu-id="1a0a3-103">\_Clase ParentChildSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="1a0a3-103">CIM\_ParentChildSettingData class</span></span>

<span data-ttu-id="1a0a3-104">Asociación entre una instancia de [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) y la instancia de **\_ VirtualSystemSettingData de CIM** que representa la instantánea más reciente en la que se basa este objeto.</span><span class="sxs-lookup"><span data-stu-id="1a0a3-104">An association between an instance of [**CIM\_VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) and the **CIM\_VirtualSystemSettingData** instance which represents the most recent snapshot upon which this object is based.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a0a3-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="1a0a3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1a0a3-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1a0a3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1a0a3-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1a0a3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0a3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a0a3-108">Syntax</span></span>

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a><span data-ttu-id="1a0a3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a0a3-109">Members</span></span>

<span data-ttu-id="1a0a3-110">La clase **CIM \_ ParentChildSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a0a3-110">The **CIM\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1a0a3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a0a3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a0a3-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a0a3-112">Properties</span></span>

<span data-ttu-id="1a0a3-113">La clase **CIM \_ ParentChildSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a0a3-113">The **CIM\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a0a3-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a0a3-115">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-115">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="1a0a3-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a0a3-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a0a3-117">Referencia al objeto independiente de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="1a0a3-117">Reference to the independent object in this association.</span></span>

<span data-ttu-id="1a0a3-118">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="1a0a3-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="1a0a3-119">**Elemento secundario**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-119">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a0a3-120">Tipo de datos: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-120">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="1a0a3-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a0a3-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a0a3-122">Los datos de configuración del sistema virtual que representa el elemento secundario del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1a0a3-122">The setting data for the virtual system which represents the child of the Parent.</span></span>

</dd> <dt>

<span data-ttu-id="1a0a3-123">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a0a3-124">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-124">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="1a0a3-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a0a3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a0a3-126">Referencia al objeto que depende de la propiedad **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="1a0a3-126">Reference to the object that is dependent on the **Antecedent** property.</span></span>

<span data-ttu-id="1a0a3-127">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="1a0a3-127">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="1a0a3-128">**Parent**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-128">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a0a3-129">Tipo de datos: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-129">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="1a0a3-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a0a3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a0a3-131">Los datos de configuración de instantáneas en los que se basan los datos de configuración secundarios.</span><span class="sxs-lookup"><span data-stu-id="1a0a3-131">The snapshot setting data upon which the Child setting data is based.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a0a3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a0a3-132">Requirements</span></span>



| <span data-ttu-id="1a0a3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a0a3-133">Requirement</span></span> | <span data-ttu-id="1a0a3-134">Value</span><span class="sxs-lookup"><span data-stu-id="1a0a3-134">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="1a0a3-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a0a3-135">Namespace</span></span><br/> | <span data-ttu-id="1a0a3-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a0a3-136">Root\\CIMV2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a0a3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a0a3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a0a3-138">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

