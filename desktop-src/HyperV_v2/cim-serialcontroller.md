---
description: Describe las capacidades y la administración de un controlador serie.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: CIM_SerialController (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686902"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a><span data-ttu-id="723b1-103">CIM_SerialController (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="723b1-103">CIM_SerialController class (Hyper-V management)</span></span>

<span data-ttu-id="723b1-104">Describe las capacidades y la administración de un controlador serie.</span><span class="sxs-lookup"><span data-stu-id="723b1-104">Describes the capabilities and management of a serial controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="723b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="723b1-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a><span data-ttu-id="723b1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="723b1-106">Members</span></span>

<span data-ttu-id="723b1-107">La clase **CIM \_ SerialController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="723b1-107">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="723b1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="723b1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="723b1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="723b1-109">Properties</span></span>

<span data-ttu-id="723b1-110">La clase **CIM \_ SerialController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="723b1-110">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="723b1-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="723b1-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="723b1-112">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="723b1-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="723b1-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="723b1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="723b1-114">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puertos serie DMTF \| 004,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="723b1-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="723b1-115">Compatibilidad de nivel de chip para el controlador serie.</span><span class="sxs-lookup"><span data-stu-id="723b1-115">The chip level compatibility for the serial controller.</span></span> <span data-ttu-id="723b1-116">Esta propiedad describe el almacenamiento en búfer y otras capacidades del controlador serie que podrían ser inherentes en el hardware del chip.</span><span class="sxs-lookup"><span data-stu-id="723b1-116">This property describes the buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="723b1-117">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="723b1-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="723b1-118">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="723b1-118">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="723b1-119">**XT/at compatible** (3)</span><span class="sxs-lookup"><span data-stu-id="723b1-119">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="723b1-120">**compatible con 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="723b1-120">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="723b1-121">**16550 compatible** (5)</span><span class="sxs-lookup"><span data-stu-id="723b1-121">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="723b1-122">**compatible con 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="723b1-122">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="723b1-123">**compatible con 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="723b1-123">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="723b1-124">**compatible con 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="723b1-124">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="723b1-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="723b1-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="723b1-126">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="723b1-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="723b1-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="723b1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="723b1-128">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="723b1-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="723b1-129">Una matriz que contiene explicaciones más detalladas de las características del controlador serie en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="723b1-129">An array that contains more detailed explanations for serial controller features in the **Capabilities** array.</span></span> <span data-ttu-id="723b1-130">Los elementos de la matriz **CapabilityDescriptions** se correlacionan con los de la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="723b1-130">The items in the **CapabilityDescriptions** array correlate to those in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="723b1-131">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="723b1-131">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="723b1-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="723b1-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="723b1-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="723b1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="723b1-134">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puertos serie DMTF \| 004,6 "), **punitivo** (" bit por segundo ")</span><span class="sxs-lookup"><span data-stu-id="723b1-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="723b1-135">La velocidad máxima en baudios en, en bits por segundo, que es compatible con el controlador serie.</span><span class="sxs-lookup"><span data-stu-id="723b1-135">The maximum baud rate in, bits per second, that is supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="723b1-136">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="723b1-136">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="723b1-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="723b1-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="723b1-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="723b1-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="723b1-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puertos serie DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="723b1-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="723b1-140">La seguridad operativa del controlador.</span><span class="sxs-lookup"><span data-stu-id="723b1-140">The operational security for the controller.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="723b1-141">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="723b1-141">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="723b1-142">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="723b1-142">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="723b1-143">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="723b1-143">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="723b1-144">**Interfaz externa bloqueada** (4)</span><span class="sxs-lookup"><span data-stu-id="723b1-144">**External Interface Locked Out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="723b1-145">**Interfaz externa habilitada** (5)</span><span class="sxs-lookup"><span data-stu-id="723b1-145">**External Interface Enabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="723b1-146">**Omisión de arranque** (6)</span><span class="sxs-lookup"><span data-stu-id="723b1-146">**Boot Bypass** (6)</span></span>


<span data-ttu-id="723b1-147"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="723b1-147"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="723b1-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="723b1-148">Requirements</span></span>



| <span data-ttu-id="723b1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="723b1-149">Requirement</span></span> | <span data-ttu-id="723b1-150">Value</span><span class="sxs-lookup"><span data-stu-id="723b1-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723b1-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="723b1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="723b1-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="723b1-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="723b1-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="723b1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="723b1-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="723b1-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="723b1-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="723b1-155">Namespace</span></span><br/>                | <span data-ttu-id="723b1-156">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="723b1-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="723b1-157">MOF</span><span class="sxs-lookup"><span data-stu-id="723b1-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="723b1-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="723b1-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="723b1-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="723b1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="723b1-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="723b1-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="723b1-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="723b1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723b1-162">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="723b1-162">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

