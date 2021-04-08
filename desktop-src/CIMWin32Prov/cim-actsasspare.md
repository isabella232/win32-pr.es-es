---
description: La \_ Asociación ActsAsSpare de CIM indica qué elementos pueden ser repuestos o reemplazar otros elementos agregados. Una reserva puede funcionar en &\# 0034; modo de espera activa&\# 0034; tal y como se especifica en cada elemento.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: CIM_ActsAsSpare (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000699"
---
# <a name="cim_actsasspare-class"></a><span data-ttu-id="5737f-104">\_Clase ActsAsSpare de CIM</span><span class="sxs-lookup"><span data-stu-id="5737f-104">CIM\_ActsAsSpare class</span></span>

<span data-ttu-id="5737f-105">La **Asociación \_ ActsAsSpare de CIM** indica qué elementos pueden ser repuestos o reemplazar otros elementos agregados.</span><span class="sxs-lookup"><span data-stu-id="5737f-105">The **CIM\_ActsAsSpare** association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="5737f-106">Una reserva puede funcionar en modo de "espera activa" como se especifica en cada elemento.</span><span class="sxs-lookup"><span data-stu-id="5737f-106">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5737f-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5737f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5737f-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5737f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5737f-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5737f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5737f-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5737f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5737f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5737f-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a><span data-ttu-id="5737f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5737f-112">Members</span></span>

<span data-ttu-id="5737f-113">La clase **CIM \_ ActsAsSpare** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5737f-113">The **CIM\_ActsAsSpare** class has these types of members:</span></span>

-   [<span data-ttu-id="5737f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5737f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5737f-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5737f-115">Properties</span></span>

<span data-ttu-id="5737f-116">La clase **CIM \_ ActsAsSpare** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5737f-116">The **CIM\_ActsAsSpare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5737f-117">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="5737f-117">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5737f-118">Tipo de datos: **CIM \_ SpareGroup**</span><span class="sxs-lookup"><span data-stu-id="5737f-118">Data type: **CIM\_SpareGroup**</span></span>
</dt> <dt>

<span data-ttu-id="5737f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5737f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5737f-120">Referencia a la propiedad de **Grupo** que representa la clase [**\_ SpareGroup de CIM**](cim-sparegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="5737f-120">Reference to the **Group** property that represents the [**CIM\_SpareGroup**](cim-sparegroup.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="5737f-121">**HotStandby**</span><span class="sxs-lookup"><span data-stu-id="5737f-121">**HotStandby**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5737f-122">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5737f-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5737f-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5737f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5737f-124">Si es **true**, la reserva funciona como una espera activa.</span><span class="sxs-lookup"><span data-stu-id="5737f-124">If **TRUE**, the spare is operating as a hot standby.</span></span>

</dd> <dt>

<span data-ttu-id="5737f-125">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="5737f-125">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5737f-126">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="5737f-126">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="5737f-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5737f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5737f-128">Referencia a un elemento del sistema administrado que actúa como repuesto y que participa en el grupo de reserva.</span><span class="sxs-lookup"><span data-stu-id="5737f-128">Reference to a managed system element acting as a spare and participating in the spare group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5737f-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5737f-129">Remarks</span></span>

<span data-ttu-id="5737f-130">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5737f-130">WMI does not implement this class.</span></span>

<span data-ttu-id="5737f-131">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5737f-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5737f-132">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5737f-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5737f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5737f-133">Requirements</span></span>



| <span data-ttu-id="5737f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5737f-134">Requirement</span></span> | <span data-ttu-id="5737f-135">Value</span><span class="sxs-lookup"><span data-stu-id="5737f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5737f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5737f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5737f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5737f-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5737f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5737f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5737f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5737f-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5737f-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5737f-140">Namespace</span></span><br/>                | <span data-ttu-id="5737f-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5737f-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5737f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5737f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5737f-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5737f-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5737f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5737f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5737f-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5737f-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5737f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="5737f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5737f-147">Clases CIM</span><span class="sxs-lookup"><span data-stu-id="5737f-147">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

