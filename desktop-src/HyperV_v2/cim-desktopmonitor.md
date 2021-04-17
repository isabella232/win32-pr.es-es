---
description: Representa un monitor de escritorio de CRT.
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: CIM_DesktopMonitor (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666697"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a><span data-ttu-id="687a3-103">CIM_DesktopMonitor (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="687a3-103">CIM_DesktopMonitor class (Hyper-V management)</span></span>

<span data-ttu-id="687a3-104">Representa un monitor de escritorio de CRT.</span><span class="sxs-lookup"><span data-stu-id="687a3-104">Represents a CRT desktop monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="687a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="687a3-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="687a3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="687a3-106">Members</span></span>

<span data-ttu-id="687a3-107">La clase **CIM \_ DesktopMonitor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="687a3-107">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="687a3-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="687a3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="687a3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="687a3-109">Properties</span></span>

<span data-ttu-id="687a3-110">La clase **CIM \_ DesktopMonitor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="687a3-110">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="687a3-111">**Ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="687a3-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a3-112">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="687a3-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="687a3-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687a3-114">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahercios"), **punitivo** ("hercios \* 10 ^ 6")</span><span class="sxs-lookup"><span data-stu-id="687a3-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="687a3-115">Ancho de banda de la pantalla, en MHertz.</span><span class="sxs-lookup"><span data-stu-id="687a3-115">The bandwidth of the display, in MHertz.</span></span> <span data-ttu-id="687a3-116">"0" indica desconocido.</span><span class="sxs-lookup"><span data-stu-id="687a3-116">"0" indicates unknown.</span></span>

</dd> <dt>

<span data-ttu-id="687a3-117">**TipoDePresentación**</span><span class="sxs-lookup"><span data-stu-id="687a3-117">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a3-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a3-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a3-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a3-120">Tipo de tipo de presentación del monitor de CRT.</span><span class="sxs-lookup"><span data-stu-id="687a3-120">The type of display type of the CRT monitor.</span></span> <span data-ttu-id="687a3-121">Por ejemplo, color Multiscan o monocromo.</span><span class="sxs-lookup"><span data-stu-id="687a3-121">For example, multiscan color, or monochrome.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="687a3-122">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="687a3-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="687a3-123">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="687a3-123">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="687a3-124">**Color de Multiscan** (2)</span><span class="sxs-lookup"><span data-stu-id="687a3-124">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="687a3-125">**Monocromo Multiscan** (3)</span><span class="sxs-lookup"><span data-stu-id="687a3-125">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="687a3-126">**Color de frecuencia fijo** (4)</span><span class="sxs-lookup"><span data-stu-id="687a3-126">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="687a3-127">**Monocromática de frecuencia fija** (5)</span><span class="sxs-lookup"><span data-stu-id="687a3-127">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="687a3-128">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="687a3-128">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a3-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="687a3-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="687a3-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a3-131">Alto lógico de la pantalla, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="687a3-131">The logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="687a3-132">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="687a3-132">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a3-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="687a3-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="687a3-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a3-135">Ancho lógico de la pantalla, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="687a3-135">The logical width of the display, in screen coordinates.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="687a3-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="687a3-136">Requirements</span></span>



| <span data-ttu-id="687a3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="687a3-137">Requirement</span></span> | <span data-ttu-id="687a3-138">Value</span><span class="sxs-lookup"><span data-stu-id="687a3-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="687a3-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="687a3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="687a3-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="687a3-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="687a3-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="687a3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="687a3-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="687a3-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="687a3-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="687a3-143">Namespace</span></span><br/>                | <span data-ttu-id="687a3-144">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="687a3-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="687a3-145">MOF</span><span class="sxs-lookup"><span data-stu-id="687a3-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="687a3-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="687a3-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="687a3-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="687a3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687a3-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="687a3-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="687a3-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="687a3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687a3-150">**Presentación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="687a3-150">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

