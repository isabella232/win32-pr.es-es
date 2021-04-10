---
description: La \_ clase WMI abstracta de Win32 SMBIOSMemory representa las propiedades de la memoria del sistema del equipo, tal como se muestra a través de la interfaz del BIOS de administración del sistema (SMBIOS).
ms.assetid: 2f609fc6-f0f5-45a5-9f9a-3873da034d49
ms.tgt_platform: multiple
title: Win32_SMBIOSMemory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SMBIOSMemory
- Win32_SMBIOSMemory.Reset
- Win32_SMBIOSMemory.SetPowerState
- Win32_SMBIOSMemory.Access
- Win32_SMBIOSMemory.AdditionalErrorData
- Win32_SMBIOSMemory.Availability
- Win32_SMBIOSMemory.BlockSize
- Win32_SMBIOSMemory.Caption
- Win32_SMBIOSMemory.ConfigManagerErrorCode
- Win32_SMBIOSMemory.ConfigManagerUserConfig
- Win32_SMBIOSMemory.CorrectableError
- Win32_SMBIOSMemory.CreationClassName
- Win32_SMBIOSMemory.Description
- Win32_SMBIOSMemory.DeviceID
- Win32_SMBIOSMemory.EndingAddress
- Win32_SMBIOSMemory.ErrorAccess
- Win32_SMBIOSMemory.ErrorAddress
- Win32_SMBIOSMemory.ErrorCleared
- Win32_SMBIOSMemory.ErrorData
- Win32_SMBIOSMemory.ErrorDataOrder
- Win32_SMBIOSMemory.ErrorDescription
- Win32_SMBIOSMemory.ErrorInfo
- Win32_SMBIOSMemory.ErrorMethodology
- Win32_SMBIOSMemory.ErrorResolution
- Win32_SMBIOSMemory.ErrorTime
- Win32_SMBIOSMemory.ErrorTransferSize
- Win32_SMBIOSMemory.InstallDate
- Win32_SMBIOSMemory.LastErrorCode
- Win32_SMBIOSMemory.Name
- Win32_SMBIOSMemory.NumberOfBlocks
- Win32_SMBIOSMemory.OtherErrorDescription
- Win32_SMBIOSMemory.PNPDeviceID
- Win32_SMBIOSMemory.PowerManagementCapabilities
- Win32_SMBIOSMemory.PowerManagementSupported
- Win32_SMBIOSMemory.Purpose
- Win32_SMBIOSMemory.StartingAddress
- Win32_SMBIOSMemory.Status
- Win32_SMBIOSMemory.StatusInfo
- Win32_SMBIOSMemory.SystemCreationClassName
- Win32_SMBIOSMemory.SystemLevelAddress
- Win32_SMBIOSMemory.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4dc7a42732dfb00d965f79045254878f690309fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153414"
---
# <a name="win32_smbiosmemory-class"></a><span data-ttu-id="18263-103">\_Clase Win32 SMBIOSMemory</span><span class="sxs-lookup"><span data-stu-id="18263-103">Win32\_SMBIOSMemory class</span></span>

<span data-ttu-id="18263-104">La [clase WMI](../wmisdk/retrieving-a-class.md) abstracta de **Win32 \_ SMBIOSMemory** representa las propiedades de la memoria del sistema del equipo, tal como se muestra a través de la interfaz del BIOS de administración del sistema (SMBIOS).</span><span class="sxs-lookup"><span data-stu-id="18263-104">The **Win32\_SMBIOSMemory** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a computer system memory as seen through the system management BIOS (SMBIOS) interface.</span></span> <span data-ttu-id="18263-105">La interfaz SMBIOS no distingue entre memorias no volátiles, volátiles y Flash.</span><span class="sxs-lookup"><span data-stu-id="18263-105">The SMBIOS interface does not distinguish between nonvolatile, volatile, and flash memories.</span></span> <span data-ttu-id="18263-106">La clase de [**\_ memoria CIM**](cim-memory.md) es la clase primaria de todos los tipos de memoria.</span><span class="sxs-lookup"><span data-stu-id="18263-106">The [**CIM\_Memory**](cim-memory.md) class is the parent class of all types of memory.</span></span>

<span data-ttu-id="18263-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="18263-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="18263-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="18263-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18263-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18263-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FECB095B-F0FA-11d2-8617-0000F8102E5F}"), AMENDMENT]
class Win32_SMBIOSMemory : CIM_StorageExtent
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16e  StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="18263-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="18263-110">Members</span></span>

<span data-ttu-id="18263-111">La **clase \_ SMBIOSMemory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="18263-111">The **Win32\_SMBIOSMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="18263-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="18263-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="18263-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18263-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18263-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="18263-114">Methods</span></span>

<span data-ttu-id="18263-115">La clase **Win32 \_ SMBIOSMemory** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="18263-115">The **Win32\_SMBIOSMemory** class has these methods.</span></span>



| <span data-ttu-id="18263-116">Método</span><span class="sxs-lookup"><span data-stu-id="18263-116">Method</span></span>            | <span data-ttu-id="18263-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="18263-117">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18263-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="18263-118">**Reset**</span></span>         | <span data-ttu-id="18263-119">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="18263-119">Not implemented.</span></span> <span data-ttu-id="18263-120">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/>                 |
| <span data-ttu-id="18263-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="18263-121">**SetPowerState**</span></span> | <span data-ttu-id="18263-122">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="18263-122">Not implemented.</span></span> <span data-ttu-id="18263-123">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="18263-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18263-124">Properties</span></span>

<span data-ttu-id="18263-125">La **clase \_ SMBIOSMemory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="18263-125">The **Win32\_SMBIOSMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18263-126">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="18263-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18263-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18263-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18263-129">Tipo de acceso.</span><span class="sxs-lookup"><span data-stu-id="18263-129">Type of access.</span></span>

<span data-ttu-id="18263-130">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="18263-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="18263-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="18263-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="18263-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="18263-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18263-134">Editable</span><span class="sxs-lookup"><span data-stu-id="18263-134">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="18263-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="18263-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="18263-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="18263-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-137">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="18263-137">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-138">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="18263-138">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="18263-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-140">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32-bit información de error de memoria de bits \| "), [**máx**](../wmisdk/standard-qualifiers.md) . (64)</span><span class="sxs-lookup"><span data-stu-id="18263-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="18263-141">Matriz de octetos que contienen información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="18263-141">Array of octets that hold additional error information.</span></span> <span data-ttu-id="18263-142">Un ejemplo es el síndrome de comprobación y corrección de errores (ECC) o el retorno de los bits de comprobación si se usa una metodología de error basada en CRC.</span><span class="sxs-lookup"><span data-stu-id="18263-142">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="18263-143">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo de comprobación de redundancia cíclica (CRC), es posible determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="18263-143">In the latter case, if a single bit error is recognized and the cyclical redundancy check (CRC) algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="18263-144">Este tipo de datos (síndrome ECC, bits de comprobación o datos de bits de paridad u otra información proporcionada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="18263-144">This type of data (ECC Syndrome, Check Bit or Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="18263-145">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-145">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="18263-146">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="18263-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18263-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18263-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-149">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="18263-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="18263-150">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-150">Availability and status of the device.</span></span>

<span data-ttu-id="18263-151">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18263-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="18263-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="18263-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="18263-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="18263-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18263-155">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="18263-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="18263-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="18263-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="18263-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="18263-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18263-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="18263-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="18263-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="18263-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="18263-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="18263-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="18263-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="18263-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18263-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="18263-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="18263-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="18263-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="18263-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="18263-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="18263-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="18263-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="18263-166">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="18263-166">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="18263-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="18263-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="18263-168">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="18263-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="18263-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="18263-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="18263-170">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="18263-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="18263-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="18263-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="18263-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="18263-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="18263-173">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="18263-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="18263-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="18263-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="18263-175">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="18263-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="18263-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="18263-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="18263-177">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="18263-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="18263-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="18263-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="18263-179">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="18263-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="18263-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="18263-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="18263-181">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="18263-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="18263-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-183">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18263-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18263-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-185">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="18263-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="18263-186">Tamaño en bytes de los bloques que forman esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="18263-186">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="18263-187">Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.</span><span class="sxs-lookup"><span data-stu-id="18263-187">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="18263-188">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18263-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="18263-189">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18263-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-193">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="18263-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18263-194">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="18263-194">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="18263-195">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18263-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-196">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18263-196">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-197">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18263-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18263-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-199">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18263-199">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18263-200">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="18263-200">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="18263-201">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-201">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="18263-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="18263-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="18263-203"> (0)</span><span class="sxs-lookup"><span data-stu-id="18263-203">(0)</span></span>


</dt> <dd>

<span data-ttu-id="18263-204">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="18263-204">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="18263-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="18263-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="18263-206">(1)</span><span class="sxs-lookup"><span data-stu-id="18263-206">(1)</span></span>


</dt> <dd>

<span data-ttu-id="18263-207">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="18263-207">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18263-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="18263-209">(2)</span><span class="sxs-lookup"><span data-stu-id="18263-209">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="18263-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="18263-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="18263-211">(3)</span><span class="sxs-lookup"><span data-stu-id="18263-211">(3)</span></span>


</dt> <dd>

<span data-ttu-id="18263-212">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="18263-212">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18263-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="18263-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="18263-214">(4)</span><span class="sxs-lookup"><span data-stu-id="18263-214">(4)</span></span>


</dt> <dd>

<span data-ttu-id="18263-215">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="18263-215">Device is not working properly.</span></span> <span data-ttu-id="18263-216">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="18263-216">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="18263-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="18263-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="18263-218">(5)</span><span class="sxs-lookup"><span data-stu-id="18263-218">(5)</span></span>


</dt> <dd>

<span data-ttu-id="18263-219">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="18263-219">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="18263-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="18263-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="18263-221"> (6)</span><span class="sxs-lookup"><span data-stu-id="18263-221">(6)</span></span>


</dt> <dd>

<span data-ttu-id="18263-222">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="18263-222">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="18263-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="18263-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="18263-224">(7)</span><span class="sxs-lookup"><span data-stu-id="18263-224">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="18263-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="18263-226">(8)</span><span class="sxs-lookup"><span data-stu-id="18263-226">(8)</span></span>


</dt> <dd>

<span data-ttu-id="18263-227">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-227">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="18263-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="18263-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="18263-229">(9)</span><span class="sxs-lookup"><span data-stu-id="18263-229">(9)</span></span>


</dt> <dd>

<span data-ttu-id="18263-230">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="18263-230">Device is not working properly.</span></span> <span data-ttu-id="18263-231">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-231">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="18263-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="18263-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="18263-233">(10)</span><span class="sxs-lookup"><span data-stu-id="18263-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="18263-234">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="18263-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="18263-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="18263-236">(11)</span><span class="sxs-lookup"><span data-stu-id="18263-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="18263-237">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="18263-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="18263-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="18263-239">(12)</span><span class="sxs-lookup"><span data-stu-id="18263-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="18263-240">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="18263-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="18263-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="18263-242">(13)</span><span class="sxs-lookup"><span data-stu-id="18263-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="18263-243">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="18263-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="18263-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="18263-245">(14)</span><span class="sxs-lookup"><span data-stu-id="18263-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="18263-246">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="18263-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="18263-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="18263-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="18263-248">(15)</span><span class="sxs-lookup"><span data-stu-id="18263-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="18263-249">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="18263-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="18263-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="18263-251">(16)</span><span class="sxs-lookup"><span data-stu-id="18263-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="18263-252">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="18263-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="18263-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="18263-254">(17)</span><span class="sxs-lookup"><span data-stu-id="18263-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="18263-255">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="18263-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18263-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="18263-257">(18)</span><span class="sxs-lookup"><span data-stu-id="18263-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="18263-258">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="18263-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="18263-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="18263-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="18263-260">(19)</span><span class="sxs-lookup"><span data-stu-id="18263-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18263-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="18263-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="18263-262">(20)</span><span class="sxs-lookup"><span data-stu-id="18263-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="18263-263">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="18263-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="18263-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="18263-265">(21)</span><span class="sxs-lookup"><span data-stu-id="18263-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="18263-266">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="18263-266">System failure.</span></span> <span data-ttu-id="18263-267">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="18263-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="18263-268">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="18263-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="18263-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="18263-270">(22)</span><span class="sxs-lookup"><span data-stu-id="18263-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="18263-271">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="18263-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="18263-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="18263-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="18263-273">(23)</span><span class="sxs-lookup"><span data-stu-id="18263-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="18263-274">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="18263-274">System failure.</span></span> <span data-ttu-id="18263-275">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="18263-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="18263-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="18263-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="18263-277">(24)</span><span class="sxs-lookup"><span data-stu-id="18263-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="18263-278">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="18263-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18263-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18263-280">(25)</span><span class="sxs-lookup"><span data-stu-id="18263-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="18263-281">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18263-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18263-283">(26)</span><span class="sxs-lookup"><span data-stu-id="18263-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="18263-284">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18263-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="18263-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="18263-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="18263-286">(27)</span><span class="sxs-lookup"><span data-stu-id="18263-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="18263-287">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="18263-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="18263-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="18263-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="18263-289">(28)</span><span class="sxs-lookup"><span data-stu-id="18263-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="18263-290">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="18263-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="18263-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="18263-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="18263-292">(29)</span><span class="sxs-lookup"><span data-stu-id="18263-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="18263-293">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="18263-293">Device is disabled.</span></span> <span data-ttu-id="18263-294">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="18263-294">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="18263-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="18263-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="18263-296">(30)</span><span class="sxs-lookup"><span data-stu-id="18263-296">(30)</span></span>


</dt> <dd>

<span data-ttu-id="18263-297">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="18263-297">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18263-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18263-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="18263-299">31</span><span class="sxs-lookup"><span data-stu-id="18263-299">(31)</span></span>


</dt> <dd>

<span data-ttu-id="18263-300">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="18263-300">Device is not working properly.</span></span> <span data-ttu-id="18263-301">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="18263-301">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-302">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="18263-302">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-303">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="18263-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18263-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-305">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18263-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18263-306">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="18263-306">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="18263-307">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-308">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="18263-308">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-309">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="18263-309">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18263-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-311">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32: tipo de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="18263-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="18263-312">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="18263-312">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="18263-313">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-313">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="18263-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18263-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-317">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18263-317">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18263-318">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="18263-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="18263-319">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="18263-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="18263-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-321">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18263-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-324">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="18263-324">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18263-325">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="18263-325">Description of the object.</span></span>

<span data-ttu-id="18263-326">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18263-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-327">**ID**</span><span class="sxs-lookup"><span data-stu-id="18263-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-330">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18263-330">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18263-331">Identificador único del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="18263-331">Unique identifier of the logical device.</span></span>

<span data-ttu-id="18263-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-333">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="18263-333">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-334">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18263-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18263-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-336">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("se ha \| asignado el dispositivo de memoria de tipo SMBIOS 19 \| dirección final de direcciones \| ")</span><span class="sxs-lookup"><span data-stu-id="18263-336">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="18263-337">Dirección final, a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="18263-337">Ending address, referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="18263-338">La dirección final se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="18263-338">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="18263-339">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18263-339">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-340">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="18263-340">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-341">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18263-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18263-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-343">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32: error de la información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="18263-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="18263-344">Operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="18263-344">Memory access operation that caused the last error.</span></span> <span data-ttu-id="18263-345">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="18263-345">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="18263-346">Si **errorInfo** es igual a 3 (OK), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-346">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18263-347">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="18263-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-348">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="18263-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="18263-349">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="18263-349">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="18263-350">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="18263-350">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="18263-351">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="18263-351">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-352">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="18263-352">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-353">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18263-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18263-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-355">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32 bits información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="18263-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="18263-356">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="18263-356">Address of the last memory error.</span></span> <span data-ttu-id="18263-357">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="18263-357">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="18263-358">Si **errorInfo** es igual a 3 (OK), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-358">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="18263-359">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18263-359">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-360">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="18263-360">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-361">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="18263-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18263-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18263-363">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="18263-363">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="18263-364">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-365">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="18263-365">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-366">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="18263-366">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="18263-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-368">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="18263-368">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="18263-369">Matriz de los datos capturados durante el último acceso erróneo a la memoria.</span><span class="sxs-lookup"><span data-stu-id="18263-369">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="18263-370">Los datos ocupan los primeros *n* octetos de la matriz necesaria para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="18263-370">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="18263-371">Si **ErrorTransferSize** es 0 (cero), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-371">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="18263-372">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="18263-372">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-373">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18263-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18263-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-375">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="18263-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="18263-376">Ordenación de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="18263-376">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="18263-377">Si **ErrorTransferSize** es 0 (cero), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-377">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-378">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="18263-378">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="18263-379">**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="18263-379">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="18263-380">**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="18263-380">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18263-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18263-384">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="18263-384">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="18263-385">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="18263-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-387">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18263-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18263-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-389">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ memoria de CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS \| tipo 18 \| 32-bit memoria error tipo de error de memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="18263-389">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="18263-390">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="18263-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="18263-391">Los valores 12 a 14 no se usan.</span><span class="sxs-lookup"><span data-stu-id="18263-391">The values 12 through 14 are unused.</span></span> <span data-ttu-id="18263-392">La capacidad de corregir se indica en la propiedad **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="18263-392">The ability to be corrected is indicated in the property **CorrectableError**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18263-393">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="18263-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-394">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="18263-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18263-395">**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="18263-395">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="18263-396">**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="18263-396">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="18263-397">**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="18263-397">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="18263-398">**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="18263-398">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="18263-399">**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="18263-399">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="18263-400">**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="18263-400">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="18263-401">**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="18263-401">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="18263-402">**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="18263-402">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="18263-403">**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="18263-403">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="18263-404">Se **corrigió el error de un solo bit** (12)</span><span class="sxs-lookup"><span data-stu-id="18263-404">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="18263-405">**Error corregido** (13)</span><span class="sxs-lookup"><span data-stu-id="18263-405">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="18263-406">**Error no corregible** (14)</span><span class="sxs-lookup"><span data-stu-id="18263-406">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-407">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="18263-407">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-408">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-410">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 16 corrección de errores de memoria de matriz de memoria \| física \| ")</span><span class="sxs-lookup"><span data-stu-id="18263-410">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="18263-411">Detalles sobre los algoritmos de paridad o CRC, ECC u otros mecanismos utilizados.</span><span class="sxs-lookup"><span data-stu-id="18263-411">Details on the parity or CRC algorithms, ECC or other mechanisms used.</span></span>

<span data-ttu-id="18263-412">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-412">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18263-413">**Otro** ("otro")</span><span class="sxs-lookup"><span data-stu-id="18263-413">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-414">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="18263-414">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="18263-415">**Ninguno** ("ninguno")</span><span class="sxs-lookup"><span data-stu-id="18263-415">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="18263-416">**Paridad** ("paridad")</span><span class="sxs-lookup"><span data-stu-id="18263-416">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="18263-417">**ECC de un bit** ("ECC de un bit")</span><span class="sxs-lookup"><span data-stu-id="18263-417">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="18263-418">**ECC de varios bits** ("ECC de varios bits")</span><span class="sxs-lookup"><span data-stu-id="18263-418">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="18263-419">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="18263-419">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-420">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="18263-420">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-421">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18263-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18263-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-423">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 18 \| 32-bit Memory error \| Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="18263-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="18263-424">Intervalo, en bytes, en el que se puede resolver el último error.</span><span class="sxs-lookup"><span data-stu-id="18263-424">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="18263-425">Por ejemplo, si las direcciones de error se resuelven en el bit 11 (es decir, en una página típica), los errores pueden resolverse en límites de 4 KB y esta propiedad se establece en 4000.</span><span class="sxs-lookup"><span data-stu-id="18263-425">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="18263-426">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-426">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="18263-427">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18263-427">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-428">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="18263-428">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-429">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18263-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18263-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-431">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="18263-431">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="18263-432">Hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="18263-432">Time that the last memory error occurred.</span></span> <span data-ttu-id="18263-433">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="18263-433">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="18263-434">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-434">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="18263-435">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="18263-435">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-436">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18263-436">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18263-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-438">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="18263-438">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="18263-439">Tamaño de la transferencia de datos en bits que causó el último error; 0 (cero) indica que no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="18263-439">Size of the data transfer in bits that caused the last error—0 (zero) indicates no error.</span></span> <span data-ttu-id="18263-440">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad se debe establecer en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="18263-440">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="18263-441">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18263-441">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-442">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18263-442">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18263-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-444">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="18263-444">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18263-445">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="18263-445">Date and time the object was installed.</span></span> <span data-ttu-id="18263-446">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="18263-446">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="18263-447">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18263-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-448">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18263-448">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-449">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18263-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18263-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18263-451">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="18263-451">Last error code reported by the logical device.</span></span>

<span data-ttu-id="18263-452">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-453">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="18263-453">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-454">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-456">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="18263-456">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="18263-457">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="18263-457">Label by which the object is known.</span></span> <span data-ttu-id="18263-458">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="18263-458">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="18263-459">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18263-459">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-460">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="18263-460">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-461">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18263-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18263-462">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-463">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="18263-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="18263-464">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="18263-464">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="18263-465">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="18263-465">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="18263-466">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="18263-466">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="18263-467">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18263-467">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="18263-468">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-468">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-469">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18263-469">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-470">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-470">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-471">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-472">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ memoria de CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="18263-472">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="18263-473">Cadena de forma libre que proporciona más información si la propiedad **ErrorType** está establecida en 1; de lo contrario, esta cadena no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-473">Free-form string that provides more information if the **ErrorType** property is set to 1; otherwise, this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="18263-474">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="18263-474">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-475">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-477">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18263-477">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18263-478">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="18263-478">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="18263-479">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="18263-479">Example: "\*PNP030b"</span></span>

<span data-ttu-id="18263-480">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-481">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18263-481">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-482">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18263-482">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18263-483">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18263-484">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="18263-484">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="18263-485">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="18263-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="18263-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="18263-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18263-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="18263-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18263-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="18263-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18263-490">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="18263-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="18263-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="18263-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18263-492">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="18263-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="18263-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="18263-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="18263-494">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="18263-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="18263-495">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="18263-495">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="18263-496">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="18263-496">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="18263-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="18263-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="18263-498">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="18263-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="18263-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="18263-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="18263-500">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="18263-500">Timed Power-On Supported</span></span>

<span data-ttu-id="18263-501">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="18263-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="18263-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-503">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="18263-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18263-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18263-505">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="18263-505">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="18263-506">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="18263-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="18263-507">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-508">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="18263-508">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-509">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-509">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-510">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18263-511">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="18263-511">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="18263-512">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-512">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-513">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="18263-513">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-514">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18263-514">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18263-515">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-516">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("el \| tipo de SMBIOS 19 \| memoria asignación de dispositivo \| dirección de inicio")</span><span class="sxs-lookup"><span data-stu-id="18263-516">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="18263-517">Dirección inicial a la que hace referencia una aplicación o un sistema operativo, y asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="18263-517">Beginning address that is referenced by an application or operating system, and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="18263-518">La dirección de inicio se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="18263-518">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="18263-519">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18263-519">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-520">**Estado**</span><span class="sxs-lookup"><span data-stu-id="18263-520">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-521">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-522">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-523">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="18263-523">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18263-524">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="18263-524">Current status of the object.</span></span> <span data-ttu-id="18263-525">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="18263-525">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="18263-526">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="18263-526">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="18263-527">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="18263-527">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18263-528">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="18263-528">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18263-529">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="18263-529">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18263-530">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18263-530">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18263-531">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="18263-531">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18263-532">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="18263-532">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18263-533">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="18263-533">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18263-534">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="18263-534">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-535">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="18263-535">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18263-536">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="18263-536">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18263-537">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="18263-537">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18263-538">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="18263-538">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18263-539">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="18263-539">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18263-540">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="18263-540">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18263-541">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="18263-541">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18263-542">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="18263-542">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18263-543">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="18263-543">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-544">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="18263-544">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-545">Tipo de datos: **uint16e**</span><span class="sxs-lookup"><span data-stu-id="18263-545">Data type: **uint16e**</span></span>
</dt> <dt>

<span data-ttu-id="18263-546">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-547">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="18263-547">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="18263-548">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="18263-548">State of the logical device.</span></span> <span data-ttu-id="18263-549">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="18263-549">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="18263-550">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18263-551">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="18263-551">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18263-552">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="18263-552">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18263-553">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="18263-553">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18263-554">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="18263-554">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18263-555">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="18263-555">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18263-556">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18263-556">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-557">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-558">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-559">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18263-559">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18263-560">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="18263-560">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="18263-561">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-561">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18263-562">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="18263-562">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-563">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="18263-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18263-564">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-565">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32 bits información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="18263-565">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="18263-566">Si es **true**, la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="18263-566">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="18263-567">Si es **false**, se trata de una dirección física.</span><span class="sxs-lookup"><span data-stu-id="18263-567">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="18263-568">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="18263-568">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="18263-569">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18263-569">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18263-570">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="18263-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18263-571">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="18263-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18263-572">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18263-572">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18263-573">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="18263-573">Name of the scoping system.</span></span>

<span data-ttu-id="18263-574">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18263-574">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18263-575">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18263-575">Remarks</span></span>

<span data-ttu-id="18263-576">La **clase \_ SMBIOSMemory de Win32** se deriva de [**\_ StorageExtent de CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18263-576">The **Win32\_SMBIOSMemory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18263-577">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18263-577">Requirements</span></span>



| <span data-ttu-id="18263-578">Requisito</span><span class="sxs-lookup"><span data-stu-id="18263-578">Requirement</span></span> | <span data-ttu-id="18263-579">Value</span><span class="sxs-lookup"><span data-stu-id="18263-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18263-580">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18263-580">Minimum supported client</span></span><br/> | <span data-ttu-id="18263-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18263-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18263-582">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18263-582">Minimum supported server</span></span><br/> | <span data-ttu-id="18263-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18263-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18263-584">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="18263-584">Namespace</span></span><br/>                | <span data-ttu-id="18263-585">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="18263-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18263-586">MOF</span><span class="sxs-lookup"><span data-stu-id="18263-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18263-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18263-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18263-588">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18263-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18263-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18263-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18263-590">Vea también</span><span class="sxs-lookup"><span data-stu-id="18263-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18263-591">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="18263-591">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="18263-592">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="18263-592">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
