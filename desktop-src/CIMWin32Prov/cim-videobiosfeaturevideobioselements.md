---
description: La \_ clase VideoBIOSFeatureVideoBIOSElements de CIM asocia una característica de BIOS de vídeo y sus elementos de BIOS de vídeo agregados.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeatureVideoBIOSElements (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153047"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a><span data-ttu-id="63e7e-103">\_Clase VideoBIOSFeatureVideoBIOSElements de CIM</span><span class="sxs-lookup"><span data-stu-id="63e7e-103">CIM\_VideoBIOSFeatureVideoBIOSElements class</span></span>

<span data-ttu-id="63e7e-104">La **clase \_ VideoBIOSFeatureVideoBIOSElements de CIM** asocia una característica de BIOS de vídeo y sus elementos de BIOS de vídeo agregados.</span><span class="sxs-lookup"><span data-stu-id="63e7e-104">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63e7e-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="63e7e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="63e7e-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="63e7e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="63e7e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="63e7e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="63e7e-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="63e7e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e7e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63e7e-109">Syntax</span></span>

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="63e7e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="63e7e-110">Members</span></span>

<span data-ttu-id="63e7e-111">La clase **CIM \_ VideoBIOSFeatureVideoBIOSElements** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="63e7e-111">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="63e7e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63e7e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63e7e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63e7e-113">Properties</span></span>

<span data-ttu-id="63e7e-114">La clase **CIM \_ VideoBIOSFeatureVideoBIOSElements** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="63e7e-114">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63e7e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="63e7e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e7e-116">Tipo de datos: **CIM \_ VideoBIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="63e7e-116">Data type: **CIM\_VideoBIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="63e7e-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63e7e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e7e-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="63e7e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="63e7e-119">Un [**\_ VideoBIOSFeature de CIM**](cim-videobiosfeature.md) que describe la característica BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="63e7e-119">A [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) that describes the video BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="63e7e-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="63e7e-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e7e-121">Tipo de datos: **CIM \_ VideoBIOSElement**</span><span class="sxs-lookup"><span data-stu-id="63e7e-121">Data type: **CIM\_VideoBIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="63e7e-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63e7e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e7e-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="63e7e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="63e7e-124">Un [**\_ VideoBIOSElement de CIM**](cim-videobioselement.md) que describe el elemento de BIOS de vídeo que implementa las funciones descritas en la característica BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="63e7e-124">A [**CIM\_VideoBIOSElement**](cim-videobioselement.md) that describes the video BIOS element that implements the capabilities described by video BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63e7e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63e7e-125">Remarks</span></span>

<span data-ttu-id="63e7e-126">La clase **CIM \_ VideoBIOSFeatureVideoBIOSElements** se deriva de [**\_ SoftwareFeatureSoftwareElements de CIM**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="63e7e-126">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="63e7e-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="63e7e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="63e7e-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="63e7e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="63e7e-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="63e7e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e7e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e7e-130">Requirements</span></span>



| <span data-ttu-id="63e7e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e7e-131">Requirement</span></span> | <span data-ttu-id="63e7e-132">Value</span><span class="sxs-lookup"><span data-stu-id="63e7e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63e7e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e7e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="63e7e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63e7e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63e7e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e7e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="63e7e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63e7e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63e7e-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="63e7e-137">Namespace</span></span><br/>                | <span data-ttu-id="63e7e-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="63e7e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63e7e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="63e7e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63e7e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63e7e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63e7e-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63e7e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e7e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e7e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e7e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="63e7e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e7e-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="63e7e-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

