---
description: La \_ clase MonitorSetting de CIM asocia la resolución del monitor con el monitor de escritorio al que se aplica.
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: CIM_MonitorSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc947f4bb484ec5392204747e583fbf80bbf88cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907328"
---
# <a name="cim_monitorsetting-class"></a><span data-ttu-id="68272-103">\_Clase MonitorSetting de CIM</span><span class="sxs-lookup"><span data-stu-id="68272-103">CIM\_MonitorSetting class</span></span>

<span data-ttu-id="68272-104">La **clase \_ MonitorSetting de CIM** asocia la resolución del monitor con el monitor de escritorio al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="68272-104">The **CIM\_MonitorSetting** class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68272-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="68272-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="68272-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="68272-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="68272-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="68272-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="68272-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="68272-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68272-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68272-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a><span data-ttu-id="68272-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="68272-110">Members</span></span>

<span data-ttu-id="68272-111">La clase **CIM \_ MonitorSetting** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="68272-111">The **CIM\_MonitorSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="68272-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68272-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68272-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68272-113">Properties</span></span>

<span data-ttu-id="68272-114">La clase **CIM \_ MonitorSetting** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="68272-114">The **CIM\_MonitorSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68272-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="68272-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68272-116">Tipo de datos: **CIM \_ DesktopMonitor**</span><span class="sxs-lookup"><span data-stu-id="68272-116">Data type: **CIM\_DesktopMonitor**</span></span>
</dt> <dt>

<span data-ttu-id="68272-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68272-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68272-118">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento")</span><span class="sxs-lookup"><span data-stu-id="68272-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="68272-119">Un [**\_ DesktopMonitor de CIM**](cim-desktopmonitor.md) que describe el monitor de escritorio.</span><span class="sxs-lookup"><span data-stu-id="68272-119">A [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) describing the desktop monitor.</span></span>

</dd> <dt>

<span data-ttu-id="68272-120">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="68272-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68272-121">Tipo de datos: **CIM \_ MonitorResolution**</span><span class="sxs-lookup"><span data-stu-id="68272-121">Data type: **CIM\_MonitorResolution**</span></span>
</dt> <dt>

<span data-ttu-id="68272-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68272-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68272-123">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuración")</span><span class="sxs-lookup"><span data-stu-id="68272-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="68272-124">Un [**\_ MonitorResolution de CIM**](cim-monitorresolution.md) que describe la resolución del monitor asociada con el monitor de escritorio.</span><span class="sxs-lookup"><span data-stu-id="68272-124">A [**CIM\_MonitorResolution**](cim-monitorresolution.md) describing the monitor resolution associated with the desktop monitor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68272-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68272-125">Remarks</span></span>

<span data-ttu-id="68272-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="68272-126">WMI does not implement this class.</span></span>

<span data-ttu-id="68272-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="68272-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="68272-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="68272-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="68272-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68272-129">Requirements</span></span>



| <span data-ttu-id="68272-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="68272-130">Requirement</span></span> | <span data-ttu-id="68272-131">Value</span><span class="sxs-lookup"><span data-stu-id="68272-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68272-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68272-132">Minimum supported client</span></span><br/> | <span data-ttu-id="68272-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68272-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68272-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68272-134">Minimum supported server</span></span><br/> | <span data-ttu-id="68272-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68272-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68272-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68272-136">Namespace</span></span><br/>                | <span data-ttu-id="68272-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68272-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68272-138">MOF</span><span class="sxs-lookup"><span data-stu-id="68272-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68272-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68272-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68272-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68272-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68272-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68272-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68272-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="68272-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68272-143">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="68272-143">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

