---
description: Representa un dispositivo que se usa para señalar a las regiones de una pantalla.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: CIM_PointingDevice (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156948"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a><span data-ttu-id="29f49-103">CIM_PointingDevice (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="29f49-103">CIM_PointingDevice class (Hyper-V management)</span></span>

<span data-ttu-id="29f49-104">Representa un dispositivo que se usa para señalar a las regiones de una pantalla.</span><span class="sxs-lookup"><span data-stu-id="29f49-104">Represents a device used to point to regions of a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="29f49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29f49-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a><span data-ttu-id="29f49-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="29f49-106">Members</span></span>

<span data-ttu-id="29f49-107">La clase **CIM \_ PointingDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="29f49-107">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="29f49-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29f49-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29f49-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29f49-109">Properties</span></span>

<span data-ttu-id="29f49-110">La clase **CIM \_ PointingDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="29f49-110">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29f49-111">**Situación**</span><span class="sxs-lookup"><span data-stu-id="29f49-111">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29f49-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29f49-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="29f49-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29f49-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29f49-114">Indica si el dispositivo señalador está configurado para la operación de mano a la derecha o a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="29f49-114">Indicates whether the pointing device is configured for right or left handed operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="29f49-115">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="29f49-115">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="29f49-116">**No aplicable** (1)</span><span class="sxs-lookup"><span data-stu-id="29f49-116">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="29f49-117">**Operación de mano derecha** (2)</span><span class="sxs-lookup"><span data-stu-id="29f49-117">**Right Handed Operation** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="29f49-118">**Operación de mano izquierda** (3)</span><span class="sxs-lookup"><span data-stu-id="29f49-118">**Left Handed Operation** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="29f49-119">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="29f49-119">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29f49-120">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="29f49-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="29f49-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29f49-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29f49-122">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo señalador DMTF \| 003,4 ")</span><span class="sxs-lookup"><span data-stu-id="29f49-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.4")</span></span>
</dt> </dl>

<span data-ttu-id="29f49-123">Número de botones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29f49-123">The number of buttons on the device.</span></span> <span data-ttu-id="29f49-124">Si el dispositivo señalador no tiene botones, este valor debe establecerse en "0".</span><span class="sxs-lookup"><span data-stu-id="29f49-124">If the pointing device has no buttons, this value should be set to "0".</span></span>

</dd> <dt>

<span data-ttu-id="29f49-125">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="29f49-125">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29f49-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29f49-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="29f49-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29f49-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29f49-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo señalador DMTF \| 003,1 ")</span><span class="sxs-lookup"><span data-stu-id="29f49-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.1")</span></span>
</dt> </dl>

<span data-ttu-id="29f49-129">Tipo del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="29f49-129">The type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="29f49-130">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="29f49-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="29f49-131">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="29f49-131">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="29f49-132">**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="29f49-132">**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="29f49-133">**Bola de seguimiento** (4)</span><span class="sxs-lookup"><span data-stu-id="29f49-133">**Track Ball** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="29f49-134">**Punto de seguimiento** (5)</span><span class="sxs-lookup"><span data-stu-id="29f49-134">**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="29f49-135">**Punto de deslizamiento** (6)</span><span class="sxs-lookup"><span data-stu-id="29f49-135">**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="29f49-136">**Teclado táctil** (7)</span><span class="sxs-lookup"><span data-stu-id="29f49-136">**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="29f49-137">**Pantalla táctil** (8)</span><span class="sxs-lookup"><span data-stu-id="29f49-137">**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="29f49-138">**Mouse-sensor óptico** (9)</span><span class="sxs-lookup"><span data-stu-id="29f49-138">**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="29f49-139">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="29f49-139">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29f49-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29f49-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29f49-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29f49-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29f49-142">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuentos por pulgada"), **punitivo** ("recuento/pulgada")</span><span class="sxs-lookup"><span data-stu-id="29f49-142">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Counts per Inch"), **PUnit** ("count / inch")</span></span>
</dt> </dl>

<span data-ttu-id="29f49-143">La resolución de seguimiento del dispositivo señalador, en recuentos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="29f49-143">The tracking resolution of the pointing device, in counts per inch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29f49-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29f49-144">Requirements</span></span>



| <span data-ttu-id="29f49-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="29f49-145">Requirement</span></span> | <span data-ttu-id="29f49-146">Value</span><span class="sxs-lookup"><span data-stu-id="29f49-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29f49-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29f49-147">Minimum supported client</span></span><br/> | <span data-ttu-id="29f49-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29f49-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="29f49-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29f49-149">Minimum supported server</span></span><br/> | <span data-ttu-id="29f49-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29f49-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="29f49-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29f49-151">Namespace</span></span><br/>                | <span data-ttu-id="29f49-152">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="29f49-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="29f49-153">MOF</span><span class="sxs-lookup"><span data-stu-id="29f49-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29f49-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29f49-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29f49-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29f49-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29f49-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29f49-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29f49-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="29f49-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f49-158">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="29f49-158">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

