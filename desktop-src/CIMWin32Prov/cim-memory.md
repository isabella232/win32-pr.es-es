---
description: La \_ clase de memoria CIM representa las capacidades y la administración de los dispositivos lógicos relacionados con la memoria.
ms.assetid: ddc72aad-5687-4bc1-b402-e27b27eca9be
ms.tgt_platform: multiple
title: CIM_Memory (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Caption
- CIM_Memory.Description
- CIM_Memory.InstallDate
- CIM_Memory.Name
- CIM_Memory.Status
- CIM_Memory.Availability
- CIM_Memory.ConfigManagerErrorCode
- CIM_Memory.ConfigManagerUserConfig
- CIM_Memory.CreationClassName
- CIM_Memory.DeviceID
- CIM_Memory.PowerManagementCapabilities
- CIM_Memory.ErrorCleared
- CIM_Memory.ErrorDescription
- CIM_Memory.LastErrorCode
- CIM_Memory.PNPDeviceID
- CIM_Memory.PowerManagementSupported
- CIM_Memory.StatusInfo
- CIM_Memory.SystemCreationClassName
- CIM_Memory.SystemName
- CIM_Memory.Access
- CIM_Memory.BlockSize
- CIM_Memory.NumberOfBlocks
- CIM_Memory.Purpose
- CIM_Memory.ErrorMethodology
- CIM_Memory.AdditionalErrorData
- CIM_Memory.CorrectableError
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorAddress
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorInfo
- CIM_Memory.ErrorResolution
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorTransferSize
- CIM_Memory.OtherErrorDescription
- CIM_Memory.StartingAddress
- CIM_Memory.SystemLevelAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35fbb8467337da1ceab044a42533a6ca8628cf63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153276"
---
# <a name="cim_memory-class-cimwin32-wmi-providers"></a><span data-ttu-id="19714-103">CIM_Memory (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="19714-103">CIM_Memory class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="19714-104">La clase de **\_ memoria CIM** representa las capacidades y la administración de los dispositivos lógicos relacionados con la memoria.</span><span class="sxs-lookup"><span data-stu-id="19714-104">The **CIM\_Memory** class represents the capabilities and management of memory-related logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19714-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="19714-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="19714-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="19714-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="19714-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="19714-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="19714-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="19714-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19714-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19714-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B64-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
};
```

## <a name="members"></a><span data-ttu-id="19714-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="19714-110">Members</span></span>

<span data-ttu-id="19714-111">La clase de **\_ memoria CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="19714-111">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="19714-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="19714-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="19714-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19714-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="19714-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="19714-114">Methods</span></span>

<span data-ttu-id="19714-115">La clase de **\_ memoria CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="19714-115">The **CIM\_Memory** class has these methods.</span></span>



| <span data-ttu-id="19714-116">Método</span><span class="sxs-lookup"><span data-stu-id="19714-116">Method</span></span>                                                            | <span data-ttu-id="19714-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="19714-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19714-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="19714-118">**Reset**</span></span>](reset-method-in-class-cim-memory.md)                 | <span data-ttu-id="19714-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="19714-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="19714-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="19714-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="19714-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="19714-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-memory.md) | <span data-ttu-id="19714-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="19714-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="19714-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="19714-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="19714-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19714-124">Properties</span></span>

<span data-ttu-id="19714-125">La clase de **\_ memoria CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="19714-125">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19714-126">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="19714-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19714-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19714-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-129">Describe las propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="19714-129">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="19714-130">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="19714-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-131">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="19714-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="19714-132">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="19714-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="19714-133">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="19714-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="19714-134">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="19714-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="19714-135">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="19714-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="19714-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-137">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="19714-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="19714-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,18 "," MIF. \|Matriz de memoria física DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="19714-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19714-140">Matriz de octetos que contienen información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="19714-140">Array of octets that hold additional error information.</span></span> <span data-ttu-id="19714-141">Un ejemplo es el síndrome de comprobación y corrección de errores (ECC) o el retorno de los bits de comprobación si se usa una metodología de error basada en CRC.</span><span class="sxs-lookup"><span data-stu-id="19714-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="19714-142">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, se puede determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="19714-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="19714-143">Este tipo de datos (síndrome ECC, datos de bit de comprobación o de bits de paridad u otra información proporcionada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="19714-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="19714-144">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="19714-145">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="19714-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-146">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19714-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19714-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="19714-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="19714-149">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19714-149">Availability and status of the device.</span></span>

<span data-ttu-id="19714-150">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="19714-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="19714-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="19714-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="19714-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="19714-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="19714-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="19714-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="19714-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="19714-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="19714-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="19714-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="19714-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="19714-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="19714-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="19714-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="19714-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="19714-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="19714-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="19714-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="19714-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="19714-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="19714-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="19714-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="19714-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="19714-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="19714-164">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="19714-164">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="19714-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="19714-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="19714-166">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="19714-166">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="19714-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="19714-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="19714-168">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="19714-168">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="19714-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="19714-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="19714-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="19714-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="19714-171">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="19714-171">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="19714-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="19714-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="19714-173">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="19714-173">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="19714-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="19714-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="19714-175">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="19714-175">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="19714-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="19714-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="19714-177">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="19714-177">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="19714-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="19714-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="19714-179">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="19714-179">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-180">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="19714-180">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-181">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19714-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19714-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-183">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="19714-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="19714-184">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="19714-184">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="19714-185">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="19714-185">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="19714-186">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="19714-186">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="19714-187">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="19714-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="19714-188">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="19714-188">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="19714-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-192">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="19714-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="19714-193">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="19714-193">A short textual description of the object.</span></span>

<span data-ttu-id="19714-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19714-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="19714-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-196">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19714-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19714-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-198">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="19714-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="19714-199">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="19714-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="19714-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="19714-201">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="19714-201">**This device is working properly.**</span></span> <span data-ttu-id="19714-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="19714-202">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="19714-203">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="19714-203">**This device is not configured correctly.**</span></span> <span data-ttu-id="19714-204">(1)</span><span class="sxs-lookup"><span data-stu-id="19714-204">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="19714-205">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-205">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="19714-206">(2)</span><span class="sxs-lookup"><span data-stu-id="19714-206">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="19714-207">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="19714-207">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="19714-208">(3)</span><span class="sxs-lookup"><span data-stu-id="19714-208">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="19714-209">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="19714-209">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="19714-210">(4)</span><span class="sxs-lookup"><span data-stu-id="19714-210">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="19714-211">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="19714-211">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="19714-212">(5)</span><span class="sxs-lookup"><span data-stu-id="19714-212">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="19714-213">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="19714-213">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="19714-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="19714-214">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="19714-215">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="19714-215">**Cannot filter.**</span></span> <span data-ttu-id="19714-216">(7)</span><span class="sxs-lookup"><span data-stu-id="19714-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="19714-217">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-217">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="19714-218">(8)</span><span class="sxs-lookup"><span data-stu-id="19714-218">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="19714-219">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="19714-219">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="19714-220">(9)</span><span class="sxs-lookup"><span data-stu-id="19714-220">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="19714-221">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="19714-221">**This device cannot start.**</span></span> <span data-ttu-id="19714-222">(10)</span><span class="sxs-lookup"><span data-stu-id="19714-222">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="19714-223">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-223">**This device failed.**</span></span> <span data-ttu-id="19714-224">(11)</span><span class="sxs-lookup"><span data-stu-id="19714-224">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="19714-225">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="19714-225">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="19714-226">(12)</span><span class="sxs-lookup"><span data-stu-id="19714-226">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="19714-227">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-227">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="19714-228">(13)</span><span class="sxs-lookup"><span data-stu-id="19714-228">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="19714-229">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="19714-229">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="19714-230">(14)</span><span class="sxs-lookup"><span data-stu-id="19714-230">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="19714-231">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="19714-231">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="19714-232">(15)</span><span class="sxs-lookup"><span data-stu-id="19714-232">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="19714-233">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-233">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="19714-234">(16)</span><span class="sxs-lookup"><span data-stu-id="19714-234">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="19714-235">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="19714-235">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="19714-236">(17)</span><span class="sxs-lookup"><span data-stu-id="19714-236">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="19714-237">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-237">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="19714-238">(18)</span><span class="sxs-lookup"><span data-stu-id="19714-238">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="19714-239">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="19714-239">**Failure using the VxD loader.**</span></span> <span data-ttu-id="19714-240">(19)</span><span class="sxs-lookup"><span data-stu-id="19714-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="19714-241">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="19714-241">**Your registry might be corrupted.**</span></span> <span data-ttu-id="19714-242">(20)</span><span class="sxs-lookup"><span data-stu-id="19714-242">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="19714-243">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-243">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="19714-244">(21)</span><span class="sxs-lookup"><span data-stu-id="19714-244">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="19714-245">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="19714-245">**This device is disabled.**</span></span> <span data-ttu-id="19714-246">(22)</span><span class="sxs-lookup"><span data-stu-id="19714-246">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="19714-247">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="19714-247">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="19714-248">(23)</span><span class="sxs-lookup"><span data-stu-id="19714-248">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="19714-249">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="19714-249">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="19714-250">(24)</span><span class="sxs-lookup"><span data-stu-id="19714-250">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="19714-251">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-251">**Windows is still setting up this device.**</span></span> <span data-ttu-id="19714-252">(25)</span><span class="sxs-lookup"><span data-stu-id="19714-252">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="19714-253">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-253">**Windows is still setting up this device.**</span></span> <span data-ttu-id="19714-254">(26)</span><span class="sxs-lookup"><span data-stu-id="19714-254">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="19714-255">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="19714-255">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="19714-256">(27)</span><span class="sxs-lookup"><span data-stu-id="19714-256">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="19714-257">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="19714-257">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="19714-258">(28)</span><span class="sxs-lookup"><span data-stu-id="19714-258">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="19714-259">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="19714-259">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="19714-260">(29)</span><span class="sxs-lookup"><span data-stu-id="19714-260">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="19714-261">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="19714-261">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="19714-262">(30)</span><span class="sxs-lookup"><span data-stu-id="19714-262">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="19714-263">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="19714-263">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="19714-264">31</span><span class="sxs-lookup"><span data-stu-id="19714-264">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-265">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="19714-265">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-266">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19714-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19714-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-268">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="19714-268">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="19714-269">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="19714-269">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="19714-270">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-271">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="19714-271">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-272">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19714-272">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19714-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-274">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="19714-274">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="19714-275">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="19714-275">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="19714-276">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-276">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="19714-277">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="19714-277">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-280">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="19714-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="19714-281">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="19714-281">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="19714-282">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="19714-282">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="19714-283">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-284">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19714-284">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-287">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="19714-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="19714-288">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="19714-288">A textual description of the object.</span></span>

<span data-ttu-id="19714-289">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19714-289">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-290">**ID**</span><span class="sxs-lookup"><span data-stu-id="19714-290">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-291">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-293">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="19714-293">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="19714-294">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="19714-294">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="19714-295">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-296">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="19714-296">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-297">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19714-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19714-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-299">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,4 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="19714-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="19714-300">Dirección final a la que hace referencia una aplicación o un sistema operativo y asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="19714-300">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="19714-301">La dirección final se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="19714-301">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="19714-302">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="19714-302">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="19714-303">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="19714-303">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-304">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19714-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19714-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-306">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,15 "," MIF. \|Matriz de memoria física DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="19714-306">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="19714-307">Operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="19714-307">Memory access operation that caused the last error.</span></span> <span data-ttu-id="19714-308">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="19714-308">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="19714-309">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-309">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="19714-310">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="19714-310">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-311">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="19714-311">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="19714-312">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="19714-312">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="19714-313">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="19714-313">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="19714-314">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="19714-314">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-315">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="19714-315">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-316">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19714-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19714-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-318">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,19 "," MIF. \|Dispositivo de memoria DMTF \| 002,20 "," MIF. \|Matriz de memoria física DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="19714-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="19714-319">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="19714-319">Address of the last memory error.</span></span> <span data-ttu-id="19714-320">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="19714-320">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="19714-321">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-321">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="19714-322">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="19714-322">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="19714-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="19714-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-324">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19714-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19714-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-326">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="19714-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="19714-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-328">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="19714-328">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-329">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="19714-329">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="19714-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-331">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,17 "," MIF. \|Matriz de memoria física DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="19714-331">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19714-332">Datos capturados durante el último acceso erróneo a la memoria.</span><span class="sxs-lookup"><span data-stu-id="19714-332">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="19714-333">Los datos ocupan los primeros *n* octetos de la matriz que son necesarios para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="19714-333">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="19714-334">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-334">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="19714-335">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="19714-335">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-336">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19714-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19714-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-338">Orden de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="19714-338">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="19714-339">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-339">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="19714-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="19714-341">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="19714-341">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="19714-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="19714-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="19714-343">Byte menos significativo primero.</span><span class="sxs-lookup"><span data-stu-id="19714-343">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="19714-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="19714-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19714-345">Byte más significativo en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="19714-345">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-346">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="19714-346">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-349">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="19714-349">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="19714-350">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-351">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="19714-351">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-352">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19714-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19714-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-354">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ memoria de CIM**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="19714-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="19714-355">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="19714-355">Type of error that occurred most recently.</span></span> <span data-ttu-id="19714-356">Los valores 12 a 14 no están definidos en el esquema CIM porque DMI mezcla la semántica del tipo de error y si es corregible.</span><span class="sxs-lookup"><span data-stu-id="19714-356">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="19714-357">El hecho de que se corrija un error se indica en la propiedad **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="19714-357">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="19714-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="19714-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="19714-359">Otros.</span><span class="sxs-lookup"><span data-stu-id="19714-359">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="19714-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19714-361">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="19714-361">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="19714-362"><span id="OK"></span><span id="ok"></span>**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="19714-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="19714-363">Aceptar.</span><span class="sxs-lookup"><span data-stu-id="19714-363">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="19714-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="19714-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="19714-365">Lectura incorrecta.</span><span class="sxs-lookup"><span data-stu-id="19714-365">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="19714-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="19714-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="19714-367">Error de paridad.</span><span class="sxs-lookup"><span data-stu-id="19714-367">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="19714-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="19714-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="19714-369">Error de un bit.</span><span class="sxs-lookup"><span data-stu-id="19714-369">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="19714-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="19714-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="19714-371">Error de doble bit.</span><span class="sxs-lookup"><span data-stu-id="19714-371">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="19714-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="19714-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="19714-373">Error de bits múltiple.</span><span class="sxs-lookup"><span data-stu-id="19714-373">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="19714-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="19714-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="19714-375">Error de recorte.</span><span class="sxs-lookup"><span data-stu-id="19714-375">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="19714-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="19714-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="19714-377">Error de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="19714-377">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="19714-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="19714-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="19714-379">Error de CRC.</span><span class="sxs-lookup"><span data-stu-id="19714-379">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="19714-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span><span class="sxs-lookup"><span data-stu-id="19714-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="19714-381">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="19714-381">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="19714-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (13)</span><span class="sxs-lookup"><span data-stu-id="19714-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="19714-383">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="19714-383">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="19714-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span><span class="sxs-lookup"><span data-stu-id="19714-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="19714-385">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="19714-385">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-386">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="19714-386">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-389">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="19714-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="19714-390">Indica si se utilizan algoritmos de paridad o CRC, ECC u otros mecanismos.</span><span class="sxs-lookup"><span data-stu-id="19714-390">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="19714-391">También se pueden proporcionar detalles sobre el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="19714-391">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="19714-392">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="19714-392">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-393">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19714-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19714-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-395">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,21 "," MIF. \|Matriz de memoria física DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="19714-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="19714-396">Especifica el intervalo, en bytes, en el que se puede resolver el último error.</span><span class="sxs-lookup"><span data-stu-id="19714-396">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="19714-397">Por ejemplo, si las direcciones de error se resuelven en el bit 11 (es decir, en una página típica), los errores pueden resolverse en límites de 4 KB y esta propiedad se establece en 4000.</span><span class="sxs-lookup"><span data-stu-id="19714-397">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="19714-398">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-398">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="19714-399">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="19714-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="19714-400">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="19714-400">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-401">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="19714-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="19714-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-403">Fecha y hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="19714-403">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="19714-404">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="19714-404">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="19714-405">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-405">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="19714-406">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="19714-406">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-407">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19714-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19714-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-409">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,16 "," MIF. \|Matriz de memoria física DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="19714-409">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="19714-410">Tamaño de la transferencia de datos, en bits, que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="19714-410">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="19714-411">Un valor de 0 indica que no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="19714-411">A value of 0 indicates no error.</span></span> <span data-ttu-id="19714-412">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="19714-412">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="19714-413">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="19714-413">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-414">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="19714-414">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="19714-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-416">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="19714-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="19714-417">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="19714-417">Indicates when the object was installed.</span></span> <span data-ttu-id="19714-418">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="19714-418">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="19714-419">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19714-419">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-420">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="19714-420">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-421">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19714-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19714-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-423">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="19714-423">Last error code reported by the logical device.</span></span>

<span data-ttu-id="19714-424">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-425">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="19714-425">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-426">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-427">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-428">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="19714-428">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="19714-429">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="19714-429">Label by which the object is known.</span></span> <span data-ttu-id="19714-430">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="19714-430">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="19714-431">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19714-431">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-432">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="19714-432">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-433">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19714-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19714-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-435">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="19714-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="19714-436">Número de bloques consecutivos, cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="19714-436">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="19714-437">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="19714-437">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="19714-438">Si el valor de **blocksize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="19714-438">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="19714-439">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="19714-439">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="19714-440">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="19714-440">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-441">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="19714-441">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-444">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ memoria de CIM**.**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="19714-444">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="19714-445">Cadena de forma libre que proporciona información si la propiedad de **ErrorType** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="19714-445">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="19714-446">Si no se establece en 1, esta cadena no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-446">If it is not set to 1, then this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="19714-447">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="19714-447">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-450">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="19714-450">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="19714-451">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="19714-451">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="19714-452">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="19714-452">Example: "\*PNP030b"</span></span>

<span data-ttu-id="19714-453">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-454">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="19714-454">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-455">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19714-455">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19714-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-457">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="19714-457">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="19714-458">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="19714-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="19714-460">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="19714-460">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="19714-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="19714-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="19714-462">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19714-462">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="19714-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="19714-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19714-464">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="19714-464">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="19714-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="19714-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="19714-466">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="19714-466">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="19714-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="19714-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="19714-468">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="19714-468">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="19714-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="19714-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="19714-470">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="19714-470">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="19714-471">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="19714-471">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="19714-472">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="19714-472">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="19714-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="19714-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="19714-474">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="19714-474">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="19714-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="19714-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="19714-476">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="19714-476">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-477">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="19714-477">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-478">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19714-478">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19714-479">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-480">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="19714-480">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="19714-481">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="19714-481">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="19714-482">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="19714-482">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="19714-483">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="19714-483">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="19714-484">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-485">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="19714-485">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-486">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-486">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-488">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="19714-488">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="19714-489">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="19714-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-490">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="19714-490">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-491">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19714-491">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19714-492">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-493">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,3 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="19714-493">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="19714-494">Dirección inicial, a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria, para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="19714-494">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="19714-495">La dirección de inicio se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="19714-495">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="19714-496">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="19714-496">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="19714-497">**Estado**</span><span class="sxs-lookup"><span data-stu-id="19714-497">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-498">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-500">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="19714-500">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="19714-501">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="19714-501">String that indicates the current status of the object.</span></span> <span data-ttu-id="19714-502">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="19714-502">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="19714-503">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="19714-503">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="19714-504">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="19714-504">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="19714-505">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="19714-505">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="19714-506">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="19714-506">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="19714-507">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="19714-507">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="19714-508">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19714-508">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="19714-509">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="19714-509">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="19714-510">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="19714-510">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="19714-511">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="19714-511">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="19714-512">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="19714-512">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-513">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="19714-513">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="19714-514">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="19714-514">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="19714-515">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="19714-515">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="19714-516">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="19714-516">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="19714-517">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="19714-517">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="19714-518">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="19714-518">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="19714-519">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="19714-519">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="19714-520">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="19714-520">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="19714-521">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="19714-521">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-522">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="19714-522">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-523">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19714-523">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19714-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-525">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="19714-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="19714-526">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="19714-526">State of the logical device.</span></span> <span data-ttu-id="19714-527">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="19714-527">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="19714-528">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="19714-529">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="19714-529">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19714-530">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="19714-530">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="19714-531">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="19714-531">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="19714-532">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="19714-532">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="19714-533">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="19714-533">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19714-534">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="19714-534">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-536">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-537">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="19714-537">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="19714-538">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="19714-538">The scoping system's creation class name.</span></span>

<span data-ttu-id="19714-539">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-539">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="19714-540">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="19714-540">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-541">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19714-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19714-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19714-543">Indica si la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema (**true**) o una dirección física (**false**).</span><span class="sxs-lookup"><span data-stu-id="19714-543">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="19714-544">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="19714-544">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="19714-545">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="19714-545">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19714-546">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19714-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19714-547">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19714-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19714-548">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="19714-548">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="19714-549">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="19714-549">The scoping system's name.</span></span>

<span data-ttu-id="19714-550">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="19714-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19714-551">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19714-551">Remarks</span></span>

<span data-ttu-id="19714-552">La clase de **\_ memoria CIM** se deriva [**de \_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="19714-552">The **CIM\_Memory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="19714-553">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="19714-553">WMI does not implement this class.</span></span> <span data-ttu-id="19714-554">Para las clases que se derivan de la **\_ memoria CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="19714-554">For classes that are derived from **CIM\_Memory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="19714-555">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="19714-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="19714-556">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="19714-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="19714-557">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19714-557">Requirements</span></span>



| <span data-ttu-id="19714-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="19714-558">Requirement</span></span> | <span data-ttu-id="19714-559">Value</span><span class="sxs-lookup"><span data-stu-id="19714-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19714-560">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19714-560">Minimum supported client</span></span><br/> | <span data-ttu-id="19714-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19714-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19714-562">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19714-562">Minimum supported server</span></span><br/> | <span data-ttu-id="19714-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19714-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19714-564">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19714-564">Namespace</span></span><br/>                | <span data-ttu-id="19714-565">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="19714-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19714-566">MOF</span><span class="sxs-lookup"><span data-stu-id="19714-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19714-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19714-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19714-568">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19714-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19714-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19714-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19714-570">Vea también</span><span class="sxs-lookup"><span data-stu-id="19714-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19714-571">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="19714-571">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

