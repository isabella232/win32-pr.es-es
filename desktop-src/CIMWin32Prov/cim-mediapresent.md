---
description: La \_ Asociación MediaPresent de CIM describe una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: CIM_MediaPresent (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914158"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a><span data-ttu-id="f4abc-103">CIM_MediaPresent (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f4abc-103">CIM_MediaPresent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f4abc-104">La **Asociación \_ MediaPresent de CIM** describe una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="f4abc-104">The **CIM\_MediaPresent** association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4abc-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f4abc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f4abc-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f4abc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f4abc-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f4abc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f4abc-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f4abc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4abc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4abc-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f4abc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4abc-110">Members</span></span>

<span data-ttu-id="f4abc-111">La clase **CIM \_ MediaPresent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f4abc-111">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="f4abc-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4abc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4abc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4abc-113">Properties</span></span>

<span data-ttu-id="f4abc-114">La clase **CIM \_ MediaPresent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f4abc-114">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4abc-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f4abc-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4abc-116">Tipo de datos: **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="f4abc-116">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f4abc-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4abc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4abc-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="f4abc-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f4abc-119">Un [**\_ MediaAccessDevice de CIM**](cim-mediaaccessdevice.md) que describe el dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="f4abc-119">A [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) that describes the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="f4abc-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f4abc-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4abc-121">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="f4abc-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="f4abc-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4abc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4abc-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="f4abc-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f4abc-124">Un [**\_ StorageExtent de CIM**](cim-storageextent.md) que describe la extensión de almacenamiento a la que se tiene acceso mediante el dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="f4abc-124">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent accessed using the media access device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4abc-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4abc-125">Remarks</span></span>

<span data-ttu-id="f4abc-126">La clase **CIM \_ MediaPresent** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f4abc-126">The **CIM\_MediaPresent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f4abc-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f4abc-127">WMI does not implement this class.</span></span> <span data-ttu-id="f4abc-128">Para las clases derivadas de **CIM \_ MediaPresent**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f4abc-128">For classes derived from **CIM\_MediaPresent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f4abc-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f4abc-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f4abc-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f4abc-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4abc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4abc-131">Requirements</span></span>



| <span data-ttu-id="f4abc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4abc-132">Requirement</span></span> | <span data-ttu-id="f4abc-133">Value</span><span class="sxs-lookup"><span data-stu-id="f4abc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4abc-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4abc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f4abc-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4abc-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4abc-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4abc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f4abc-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4abc-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4abc-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4abc-138">Namespace</span></span><br/>                | <span data-ttu-id="f4abc-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f4abc-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4abc-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f4abc-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4abc-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4abc-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4abc-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4abc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4abc-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4abc-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4abc-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4abc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4abc-145">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f4abc-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

