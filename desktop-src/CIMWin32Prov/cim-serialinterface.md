---
description: La \_ clase CIM SerialInterface representa una \_ relación CONTROLLEDBY de CIM que indica a qué dispositivos se tiene acceso a través del controlador serie y las características del acceso.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: CIM_SerialInterface (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907178"
---
# <a name="cim_serialinterface-class"></a><span data-ttu-id="fcc4a-103">\_Clase SerialInterface de CIM</span><span class="sxs-lookup"><span data-stu-id="fcc4a-103">CIM\_SerialInterface class</span></span>

<span data-ttu-id="fcc4a-104">La clase **CIM \_ SerialInterface** representa una relación [**\_ ControlledBy de CIM**](cim-controlledby.md) que indica a qué dispositivos se tiene acceso a través del controlador serie y las características del acceso.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-104">The **CIM\_SerialInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcc4a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fcc4a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fcc4a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fcc4a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc4a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcc4a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a><span data-ttu-id="fcc4a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fcc4a-110">Members</span></span>

<span data-ttu-id="fcc4a-111">La clase **CIM \_ SerialInterface** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fcc4a-111">The **CIM\_SerialInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="fcc4a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fcc4a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcc4a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fcc4a-113">Properties</span></span>

<span data-ttu-id="fcc4a-114">La clase **CIM \_ SerialInterface** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-114">The **CIM\_SerialInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcc4a-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-118">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="fcc4a-119">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="fcc4a-120">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fcc4a-121">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="fcc4a-122">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="fcc4a-123">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fcc4a-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-125">Tipo de datos: **CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-125">Data type: **CIM\_SerialController**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-127">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="fcc4a-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-128">[**\_ SerialController CIM**](cim-serialcontroller.md) que describe el controlador serie.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-128">A [**CIM\_SerialController**](cim-serialcontroller.md) that describes the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="fcc4a-129">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-130">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-132">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="fcc4a-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-133">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="fcc4a-134">**FlowControlInfo**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-134">**FlowControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-137">Indica el control de flujo para los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-137">Indicates the flow control for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fcc4a-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fcc4a-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="fcc4a-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (2)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span data-ttu-id="fcc4a-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XOnXOff** (3)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span data-ttu-id="fcc4a-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span data-ttu-id="fcc4a-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XOnXOff y RTS/CTS** (5)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Both XonXoff and RTS/CTS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fcc4a-144">XonXoff y RTS/CTS</span><span class="sxs-lookup"><span data-stu-id="fcc4a-144">XonXoff and RTS/CTS</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fcc4a-145">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-145">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-148">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="fcc4a-148">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-149">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-149">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="fcc4a-150">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-150">Data width is specified in bits.</span></span> <span data-ttu-id="fcc4a-151">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-151">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="fcc4a-152">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcc4a-153">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-153">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-154">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-156">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="fcc4a-156">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-157">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-157">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="fcc4a-158">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-158">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="fcc4a-159">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-159">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="fcc4a-160">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fcc4a-161">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-161">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcc4a-162">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-162">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-165">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-165">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="fcc4a-166">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-166">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="fcc4a-167">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-167">All internal device state information and data are lost.</span></span>

<span data-ttu-id="fcc4a-168">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-168">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcc4a-169">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-169">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-172">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-172">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="fcc4a-173">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-173">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="fcc4a-174">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-174">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="fcc4a-175">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-175">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcc4a-176">**NumberOfStopBits**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-176">**NumberOfStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-177">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-179">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="fcc4a-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-180">Número de bits de parada que se van a transmitir.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-180">Number of stop bits to transmit.</span></span>

</dd> <dt>

<span data-ttu-id="fcc4a-181">**ParityInfo**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-181">**ParityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcc4a-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcc4a-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fcc4a-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcc4a-184">Información sobre la configuración de paridad para los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-184">Information about the parity setting for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fcc4a-185">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-185">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="fcc4a-186">**Ninguno** (1)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-186">**None** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="fcc4a-187">**Par** (2)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-187">**Even** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="fcc4a-188">**Impar** (3)</span><span class="sxs-lookup"><span data-stu-id="fcc4a-188">**Odd** (3)</span></span>


<span data-ttu-id="fcc4a-189"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fcc4a-189"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="fcc4a-190">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcc4a-190">Remarks</span></span>

<span data-ttu-id="fcc4a-191">La clase **CIM \_ SerialInterface** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4a-191">The **CIM\_SerialInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="fcc4a-192">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-192">WMI does not implement this class.</span></span>

<span data-ttu-id="fcc4a-193">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-193">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fcc4a-194">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="fcc4a-194">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc4a-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc4a-195">Requirements</span></span>



| <span data-ttu-id="fcc4a-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc4a-196">Requirement</span></span> | <span data-ttu-id="fcc4a-197">Value</span><span class="sxs-lookup"><span data-stu-id="fcc4a-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc4a-198">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcc4a-198">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc4a-199">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcc4a-199">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fcc4a-200">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcc4a-200">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc4a-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcc4a-201">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fcc4a-202">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fcc4a-202">Namespace</span></span><br/>                | <span data-ttu-id="fcc4a-203">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fcc4a-203">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fcc4a-204">MOF</span><span class="sxs-lookup"><span data-stu-id="fcc4a-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcc4a-205"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcc4a-205"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcc4a-206">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fcc4a-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcc4a-207"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcc4a-207"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc4a-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcc4a-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc4a-209">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="fcc4a-209">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

