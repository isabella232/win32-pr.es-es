---
description: La \_ clase BootOSFromFS de CIM asocia el sistema operativo y los sistemas de archivos desde los que se carga el sistema operativo.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: CIM_BootOSFromFS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 993ee7a66ef9f8b0cbb47285e38b78e4fd4dd61b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000672"
---
# <a name="cim_bootosfromfs-class"></a><span data-ttu-id="984b1-103">\_Clase BootOSFromFS de CIM</span><span class="sxs-lookup"><span data-stu-id="984b1-103">CIM\_BootOSFromFS class</span></span>

<span data-ttu-id="984b1-104">La **clase \_ BootOSFromFS de CIM** asocia el sistema operativo y los sistemas de archivos desde los que se carga el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="984b1-104">The **CIM\_BootOSFromFS** class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="984b1-105">La asociación es de varios a varios; un sistema operativo distribuido puede depender de varios sistemas de archivos para que se carguen correctamente y por completo.</span><span class="sxs-lookup"><span data-stu-id="984b1-105">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="984b1-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="984b1-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="984b1-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="984b1-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="984b1-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="984b1-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="984b1-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="984b1-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="984b1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="984b1-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="984b1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="984b1-111">Members</span></span>

<span data-ttu-id="984b1-112">La clase **CIM \_ BootOSFromFS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="984b1-112">The **CIM\_BootOSFromFS** class has these types of members:</span></span>

-   [<span data-ttu-id="984b1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="984b1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="984b1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="984b1-114">Properties</span></span>

<span data-ttu-id="984b1-115">La clase **CIM \_ BootOSFromFS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="984b1-115">The **CIM\_BootOSFromFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="984b1-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="984b1-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984b1-117">Tipo de datos **: \_ sistema de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="984b1-117">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="984b1-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="984b1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="984b1-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="984b1-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="984b1-120">El sistema de archivos desde el que se carga el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="984b1-120">The file system from which the operating system is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="984b1-121">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="984b1-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984b1-122">Tipo de datos: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="984b1-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="984b1-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="984b1-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="984b1-124">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="984b1-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="984b1-125">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="984b1-125">The operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="984b1-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="984b1-126">Remarks</span></span>

<span data-ttu-id="984b1-127">La clase **CIM \_ BootOSFromFS** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="984b1-127">The **CIM\_BootOSFromFS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="984b1-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="984b1-128">WMI does not implement this class.</span></span>

<span data-ttu-id="984b1-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="984b1-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="984b1-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="984b1-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="984b1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="984b1-131">Requirements</span></span>



| <span data-ttu-id="984b1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="984b1-132">Requirement</span></span> | <span data-ttu-id="984b1-133">Value</span><span class="sxs-lookup"><span data-stu-id="984b1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="984b1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="984b1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="984b1-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="984b1-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="984b1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="984b1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="984b1-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="984b1-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="984b1-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="984b1-138">Namespace</span></span><br/>                | <span data-ttu-id="984b1-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="984b1-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="984b1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="984b1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="984b1-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="984b1-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="984b1-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="984b1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="984b1-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="984b1-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="984b1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="984b1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984b1-145">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="984b1-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

