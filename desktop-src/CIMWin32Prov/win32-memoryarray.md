---
description: La \_ clase WMI MemoryArray de Win32 representa las propiedades de la matriz de memoria del sistema del equipo y las direcciones asignadas.
ms.assetid: 56ff6960-cde3-4e34-b4df-d2993bafaa62
ms.tgt_platform: multiple
title: Win32_MemoryArray (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArray
- Win32_MemoryArray.Reset
- Win32_MemoryArray.SetPowerState
- Win32_MemoryArray.Access
- Win32_MemoryArray.AdditionalErrorData
- Win32_MemoryArray.Availability
- Win32_MemoryArray.BlockSize
- Win32_MemoryArray.Caption
- Win32_MemoryArray.ConfigManagerErrorCode
- Win32_MemoryArray.ConfigManagerUserConfig
- Win32_MemoryArray.CorrectableError
- Win32_MemoryArray.CreationClassName
- Win32_MemoryArray.Description
- Win32_MemoryArray.DeviceID
- Win32_MemoryArray.EndingAddress
- Win32_MemoryArray.ErrorAccess
- Win32_MemoryArray.ErrorAddress
- Win32_MemoryArray.ErrorCleared
- Win32_MemoryArray.ErrorData
- Win32_MemoryArray.ErrorDataOrder
- Win32_MemoryArray.ErrorDescription
- Win32_MemoryArray.ErrorGranularity
- Win32_MemoryArray.ErrorInfo
- Win32_MemoryArray.ErrorMethodology
- Win32_MemoryArray.ErrorResolution
- Win32_MemoryArray.ErrorTime
- Win32_MemoryArray.ErrorTransferSize
- Win32_MemoryArray.InstallDate
- Win32_MemoryArray.LastErrorCode
- Win32_MemoryArray.Name
- Win32_MemoryArray.NumberOfBlocks
- Win32_MemoryArray.OtherErrorDescription
- Win32_MemoryArray.PNPDeviceID
- Win32_MemoryArray.PowerManagementCapabilities
- Win32_MemoryArray.PowerManagementSupported
- Win32_MemoryArray.Purpose
- Win32_MemoryArray.StartingAddress
- Win32_MemoryArray.Status
- Win32_MemoryArray.StatusInfo
- Win32_MemoryArray.SystemCreationClassName
- Win32_MemoryArray.SystemLevelAddress
- Win32_MemoryArray.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c102d383502bec4808b26a87eb2f6d8445b6c2a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275080"
---
# <a name="win32_memoryarray-class"></a><span data-ttu-id="9fb26-103">\_Clase Win32 MemoryArray</span><span class="sxs-lookup"><span data-stu-id="9fb26-103">Win32\_MemoryArray class</span></span>

<span data-ttu-id="9fb26-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryArray de Win32** representa las propiedades de la matriz de memoria del sistema del equipo y las direcciones asignadas.</span><span class="sxs-lookup"><span data-stu-id="9fb26-104">The **Win32\_MemoryArray** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of the computer system memory array and mapped addresses.</span></span>

<span data-ttu-id="9fb26-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9fb26-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9fb26-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9fb26-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb26-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fb26-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryArray : Win32_SMBIOSMemory
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
  uint16   ErrorGranularity;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9fb26-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9fb26-108">Members</span></span>

<span data-ttu-id="9fb26-109">La **clase \_ MemoryArray de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9fb26-109">The **Win32\_MemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="9fb26-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9fb26-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9fb26-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fb26-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9fb26-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9fb26-112">Methods</span></span>

<span data-ttu-id="9fb26-113">La clase **Win32 \_ MemoryArray** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9fb26-113">The **Win32\_MemoryArray** class has these methods.</span></span>



| <span data-ttu-id="9fb26-114">Método</span><span class="sxs-lookup"><span data-stu-id="9fb26-114">Method</span></span>            | <span data-ttu-id="9fb26-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fb26-115">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb26-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="9fb26-116">**Reset**</span></span>         | <span data-ttu-id="9fb26-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9fb26-117">Not implemented.</span></span> <span data-ttu-id="9fb26-118">Para implementar este método, vea el método [**RESET**](reset-method-in-class-cim-controller.md) en [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="9fb26-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="9fb26-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9fb26-119">**SetPowerState**</span></span> | <span data-ttu-id="9fb26-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9fb26-120">Not implemented.</span></span> <span data-ttu-id="9fb26-121">Para implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="9fb26-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9fb26-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fb26-122">Properties</span></span>

<span data-ttu-id="9fb26-123">La **clase \_ MemoryArray de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9fb26-123">The **Win32\_MemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fb26-124">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="9fb26-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-127">Tipo de acceso a medios disponible.</span><span class="sxs-lookup"><span data-stu-id="9fb26-127">Type of media access available.</span></span>

<span data-ttu-id="9fb26-128">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9fb26-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="9fb26-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="9fb26-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-132">Editable</span><span class="sxs-lookup"><span data-stu-id="9fb26-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="9fb26-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="9fb26-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="9fb26-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="9fb26-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="9fb26-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-136">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="9fb26-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit información de error de memoria de bits \| "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="9fb26-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-139">Matriz de información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="9fb26-139">Array of additional error information.</span></span> <span data-ttu-id="9fb26-140">Un ejemplo es el síndrome de comprobación y corrección de errores (ECC) o el retorno de los bits de comprobación si se usa un valor de **ErrorMethodology** basado en la comprobación de redundancia cíclica (CRC).</span><span class="sxs-lookup"><span data-stu-id="9fb26-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based **ErrorMethodology** value is used.</span></span> <span data-ttu-id="9fb26-141">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, es posible determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="9fb26-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="9fb26-142">Este tipo de datos (síndrome ECC, bit de comprobación, datos de bit de paridad u otra información suministrada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="9fb26-143">Esta propiedad solo se usa cuando la propiedad **errorInfo** no es igual a 3.</span><span class="sxs-lookup"><span data-stu-id="9fb26-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="9fb26-144">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-145">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="9fb26-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-146">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-149">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-149">Availability and status of the device.</span></span>

<span data-ttu-id="9fb26-150">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9fb26-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9fb26-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9fb26-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-154">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="9fb26-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9fb26-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="9fb26-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9fb26-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="9fb26-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9fb26-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="9fb26-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9fb26-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="9fb26-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9fb26-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="9fb26-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9fb26-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="9fb26-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9fb26-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="9fb26-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9fb26-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="9fb26-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9fb26-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="9fb26-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9fb26-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="9fb26-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-165">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="9fb26-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9fb26-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="9fb26-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-167">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="9fb26-167">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9fb26-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="9fb26-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-169">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="9fb26-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9fb26-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="9fb26-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9fb26-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="9fb26-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-172">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="9fb26-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9fb26-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9fb26-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-174">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9fb26-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9fb26-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="9fb26-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-176">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9fb26-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="9fb26-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-178">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="9fb26-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9fb26-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="9fb26-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-180">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="9fb26-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="9fb26-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-182">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fb26-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-184">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-185">Tamaño en bytes de los bloques que forman esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9fb26-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="9fb26-186">Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.</span><span class="sxs-lookup"><span data-stu-id="9fb26-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="9fb26-187">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="9fb26-188">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fb26-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9fb26-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-192">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9fb26-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-193">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="9fb26-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="9fb26-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9fb26-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-196">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fb26-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-198">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9fb26-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-199">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9fb26-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="9fb26-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9fb26-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9fb26-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="9fb26-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-203">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9fb26-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9fb26-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9fb26-205">(1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-206">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9fb26-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9fb26-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9fb26-208">(2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9fb26-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9fb26-210">(3)</span><span class="sxs-lookup"><span data-stu-id="9fb26-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-211">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="9fb26-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9fb26-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9fb26-213">(4)</span><span class="sxs-lookup"><span data-stu-id="9fb26-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-214">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9fb26-214">Device is not working properly.</span></span> <span data-ttu-id="9fb26-215">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="9fb26-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9fb26-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9fb26-217">(5)</span><span class="sxs-lookup"><span data-stu-id="9fb26-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-218">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="9fb26-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9fb26-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9fb26-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="9fb26-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-221">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9fb26-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9fb26-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9fb26-223">(7)</span><span class="sxs-lookup"><span data-stu-id="9fb26-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9fb26-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9fb26-225">(8)</span><span class="sxs-lookup"><span data-stu-id="9fb26-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-226">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9fb26-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9fb26-228">(9)</span><span class="sxs-lookup"><span data-stu-id="9fb26-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-229">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9fb26-229">Device is not working properly.</span></span> <span data-ttu-id="9fb26-230">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9fb26-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9fb26-232">(10)</span><span class="sxs-lookup"><span data-stu-id="9fb26-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-233">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="9fb26-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9fb26-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9fb26-235">(11)</span><span class="sxs-lookup"><span data-stu-id="9fb26-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-236">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9fb26-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9fb26-238">(12)</span><span class="sxs-lookup"><span data-stu-id="9fb26-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-239">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="9fb26-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9fb26-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9fb26-241">(13)</span><span class="sxs-lookup"><span data-stu-id="9fb26-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-242">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9fb26-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9fb26-244">(14)</span><span class="sxs-lookup"><span data-stu-id="9fb26-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-245">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9fb26-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9fb26-247">(15)</span><span class="sxs-lookup"><span data-stu-id="9fb26-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-248">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="9fb26-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9fb26-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9fb26-250">(16)</span><span class="sxs-lookup"><span data-stu-id="9fb26-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-251">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9fb26-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9fb26-253">(17)</span><span class="sxs-lookup"><span data-stu-id="9fb26-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-254">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="9fb26-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9fb26-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9fb26-256">(18)</span><span class="sxs-lookup"><span data-stu-id="9fb26-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-257">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9fb26-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9fb26-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9fb26-259">(19)</span><span class="sxs-lookup"><span data-stu-id="9fb26-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9fb26-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9fb26-261">(20)</span><span class="sxs-lookup"><span data-stu-id="9fb26-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-262">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="9fb26-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9fb26-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9fb26-264">(21)</span><span class="sxs-lookup"><span data-stu-id="9fb26-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-265">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb26-265">System failure.</span></span> <span data-ttu-id="9fb26-266">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="9fb26-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9fb26-267">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9fb26-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9fb26-269">(22)</span><span class="sxs-lookup"><span data-stu-id="9fb26-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-270">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9fb26-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9fb26-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9fb26-272">(23)</span><span class="sxs-lookup"><span data-stu-id="9fb26-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-273">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb26-273">System failure.</span></span> <span data-ttu-id="9fb26-274">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="9fb26-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9fb26-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9fb26-276">(24)</span><span class="sxs-lookup"><span data-stu-id="9fb26-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-277">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="9fb26-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9fb26-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9fb26-279">(25)</span><span class="sxs-lookup"><span data-stu-id="9fb26-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-280">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9fb26-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9fb26-282">(26)</span><span class="sxs-lookup"><span data-stu-id="9fb26-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-283">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9fb26-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9fb26-285">(27)</span><span class="sxs-lookup"><span data-stu-id="9fb26-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-286">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="9fb26-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9fb26-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9fb26-288">(28)</span><span class="sxs-lookup"><span data-stu-id="9fb26-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-289">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="9fb26-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9fb26-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9fb26-291">(29)</span><span class="sxs-lookup"><span data-stu-id="9fb26-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-292">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9fb26-292">Device is disabled.</span></span> <span data-ttu-id="9fb26-293">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9fb26-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9fb26-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9fb26-295">(30)</span><span class="sxs-lookup"><span data-stu-id="9fb26-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-296">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="9fb26-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9fb26-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9fb26-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9fb26-298">31</span><span class="sxs-lookup"><span data-stu-id="9fb26-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-299">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9fb26-299">Device is not working properly.</span></span> <span data-ttu-id="9fb26-300">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9fb26-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9fb26-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-302">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9fb26-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-304">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9fb26-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-305">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9fb26-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9fb26-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="9fb26-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-308">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9fb26-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-310">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32: tipo de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-311">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="9fb26-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="9fb26-312">Esta propiedad no se utiliza si **errorInfo** se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="9fb26-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="9fb26-313">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9fb26-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-317">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9fb26-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-318">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="9fb26-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9fb26-319">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="9fb26-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="9fb26-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-321">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fb26-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-324">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="9fb26-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-325">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9fb26-325">Description of the object.</span></span>

<span data-ttu-id="9fb26-326">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-327">**ID**</span><span class="sxs-lookup"><span data-stu-id="9fb26-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-330">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="9fb26-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-331">Identificador único de la matriz de memoria.</span><span class="sxs-lookup"><span data-stu-id="9fb26-331">Unique identifier of the memory array.</span></span>

<span data-ttu-id="9fb26-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9fb26-333">Ejemplo: "matriz de memoria 1"</span><span class="sxs-lookup"><span data-stu-id="9fb26-333">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="9fb26-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-335">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fb26-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("se ha \| asignado el dispositivo de memoria de tipo SMBIOS 19 \| dirección final de direcciones \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-338">Dirección final a la que hace referencia una aplicación o un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="9fb26-339">Esta dirección de memoria está asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="9fb26-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="9fb26-340">Este valor procede de la estructura de la **dirección asignada** de la matriz de memoria en la información de la versión de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="9fb26-340">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="9fb26-341">En el caso de las versiones de SMBIOS 2,1 a 2,6, el valor procede del miembro de la **dirección final** .</span><span class="sxs-lookup"><span data-stu-id="9fb26-341">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Ending Address** member.</span></span> <span data-ttu-id="9fb26-342">En el caso de la versión 2.7 de SMBIOS, el valor procede del miembro de la **dirección de finalización extendida** .</span><span class="sxs-lookup"><span data-stu-id="9fb26-342">For SMBIOS version 2.7+ the value comes from the **Extended Ending Address** member.</span></span>

<span data-ttu-id="9fb26-343">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-343">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="9fb26-344">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fb26-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-345">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="9fb26-345">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-346">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-348">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32: error de la información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-348">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-349">Tipo de operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="9fb26-349">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="9fb26-350">Esta propiedad solo es válida cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="9fb26-350">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="9fb26-351">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-351">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9fb26-352">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-352">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-353">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-353">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="9fb26-354">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="9fb26-354">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="9fb26-355">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="9fb26-355">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="9fb26-356">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="9fb26-356">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-357">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="9fb26-357">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-358">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fb26-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-360">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32 bits información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-361">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="9fb26-361">Address of the last memory error.</span></span> <span data-ttu-id="9fb26-362">Esta propiedad solo se utiliza cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="9fb26-362">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="9fb26-363">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-363">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="9fb26-364">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fb26-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9fb26-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-366">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9fb26-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-368">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="9fb26-368">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="9fb26-369">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-370">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="9fb26-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-371">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="9fb26-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-373">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9fb26-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-374">Matriz de datos capturados del último acceso a memoria con un error.</span><span class="sxs-lookup"><span data-stu-id="9fb26-374">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="9fb26-375">Los datos ocupan los primeros *n* octetos de la matriz necesaria para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="9fb26-375">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="9fb26-376">Si **ErrorTransferSize** es 0 (cero), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9fb26-376">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="9fb26-377">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-377">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="9fb26-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-379">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-381">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="9fb26-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-382">Ordenación de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="9fb26-382">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="9fb26-383">Esta propiedad solo se utiliza cuando **ErrorTransferSize** es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="9fb26-383">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="9fb26-384">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-384">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-385">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9fb26-385">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="9fb26-386">**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-386">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="9fb26-387">**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-387">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-388">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9fb26-388">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-389">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-391">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="9fb26-391">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="9fb26-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-393">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="9fb26-393">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-394">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-396">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("granularidad de error de tipo de SMBIOS \| 18 \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-397">Nivel en el que se puede resolver el error.</span><span class="sxs-lookup"><span data-stu-id="9fb26-397">Level where the error can be resolved.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="9fb26-398">**1** (otro)</span><span class="sxs-lookup"><span data-stu-id="9fb26-398">**1** (Other)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="9fb26-399">**2** (desconocido)</span><span class="sxs-lookup"><span data-stu-id="9fb26-399">**2** (Unknown)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="9fb26-400">**3** (nivel de dispositivo)</span><span class="sxs-lookup"><span data-stu-id="9fb26-400">**3** (Device level)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="9fb26-401">**4** (nivel de partición de memoria)</span><span class="sxs-lookup"><span data-stu-id="9fb26-401">**4** (Memory partition level)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-402">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="9fb26-402">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-403">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-405">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| tipo 18 \| 32-bit memoria error tipo de error de memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-405">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-406">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="9fb26-406">Type of error that occurred most recently.</span></span> <span data-ttu-id="9fb26-407">Los valores 12-14, que indican si un error es corregible, no se usan con esta propiedad, pero esta información se encuentra en la propiedad **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="9fb26-407">The values 12-14, which indicate whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="9fb26-408">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-408">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9fb26-409">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-410">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9fb26-411">**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="9fb26-411">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="9fb26-412">**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="9fb26-412">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="9fb26-413">**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="9fb26-413">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="9fb26-414">**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="9fb26-414">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="9fb26-415">**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="9fb26-415">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="9fb26-416">**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="9fb26-416">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="9fb26-417">**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="9fb26-417">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="9fb26-418">**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="9fb26-418">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="9fb26-419">**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="9fb26-419">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="9fb26-420">Se **corrigió el error de un solo bit** (12)</span><span class="sxs-lookup"><span data-stu-id="9fb26-420">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="9fb26-421">**Error corregido** (13)</span><span class="sxs-lookup"><span data-stu-id="9fb26-421">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="9fb26-422">**Error no corregible** (14)</span><span class="sxs-lookup"><span data-stu-id="9fb26-422">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-423">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="9fb26-423">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-426">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) de error ("tipo de SMBIOS \| 16 corrección de errores de memoria de matriz de memoria \| física \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-427">Tipos de comprobación de errores utilizados por el hardware de memoria.</span><span class="sxs-lookup"><span data-stu-id="9fb26-427">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="9fb26-428">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="9fb26-429">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="9fb26-429">The values are:</span></span>

<dl> <dd><span data-ttu-id="9fb26-430">Distinta</span><span class="sxs-lookup"><span data-stu-id="9fb26-430">"Other"</span></span></dd> <dd><span data-ttu-id="9fb26-431">Unknown</span><span class="sxs-lookup"><span data-stu-id="9fb26-431">"Unknown"</span></span></dd> <dd><span data-ttu-id="9fb26-432">"None"</span><span class="sxs-lookup"><span data-stu-id="9fb26-432">"None"</span></span></dd> <dd><span data-ttu-id="9fb26-433">Parity</span><span class="sxs-lookup"><span data-stu-id="9fb26-433">"Parity"</span></span></dd> <dd><span data-ttu-id="9fb26-434">"ECC de un bit"</span><span class="sxs-lookup"><span data-stu-id="9fb26-434">"Single-bit ECC"</span></span></dd> <dd><span data-ttu-id="9fb26-435">"ECC de varios bits"</span><span class="sxs-lookup"><span data-stu-id="9fb26-435">"Multi-bit ECC"</span></span></dd> <dd><span data-ttu-id="9fb26-436">CRC</span><span class="sxs-lookup"><span data-stu-id="9fb26-436">"CRC"</span></span></dd> </dl>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9fb26-437">**Otro** ("otro")</span><span class="sxs-lookup"><span data-stu-id="9fb26-437">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-438">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9fb26-438">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9fb26-439">**Ninguno** ("ninguno")</span><span class="sxs-lookup"><span data-stu-id="9fb26-439">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="9fb26-440">**Paridad** ("paridad")</span><span class="sxs-lookup"><span data-stu-id="9fb26-440">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="9fb26-441">**ECC de un bit** ("ECC de un bit")</span><span class="sxs-lookup"><span data-stu-id="9fb26-441">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="9fb26-442">**ECC de varios bits** ("ECC de varios bits")</span><span class="sxs-lookup"><span data-stu-id="9fb26-442">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="9fb26-443">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="9fb26-443">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-444">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="9fb26-444">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-445">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fb26-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-447">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 18 \| 32-bit Memory error \| Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9fb26-447">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-448">Cantidad de datos realmente determinados para producir el error.</span><span class="sxs-lookup"><span data-stu-id="9fb26-448">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="9fb26-449">Esta propiedad no se utiliza cuando la propiedad **errorInfo** se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="9fb26-449">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="9fb26-450">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-450">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="9fb26-451">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fb26-451">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-452">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="9fb26-452">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-453">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9fb26-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-454">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-455">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="9fb26-455">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-456">Hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="9fb26-456">Time that the last memory error occurred.</span></span> <span data-ttu-id="9fb26-457">Esta propiedad solo es válida cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="9fb26-457">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="9fb26-458">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-458">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-459">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="9fb26-459">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-460">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fb26-460">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-461">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-462">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="9fb26-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-463">Tamaño de los datos (que contienen el último error) que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="9fb26-463">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="9fb26-464">Esta propiedad se establece en 0 (cero) si no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="9fb26-464">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="9fb26-465">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-465">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-466">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9fb26-466">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-467">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9fb26-467">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-469">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-470">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9fb26-470">Date and time the object was installed.</span></span> <span data-ttu-id="9fb26-471">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="9fb26-471">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9fb26-472">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-472">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-473">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9fb26-473">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-474">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fb26-474">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-476">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9fb26-476">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9fb26-477">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-478">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9fb26-478">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-479">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-481">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9fb26-481">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-482">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9fb26-482">Label by which the object is known.</span></span> <span data-ttu-id="9fb26-483">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="9fb26-483">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9fb26-484">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-484">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-485">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="9fb26-485">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-486">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fb26-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-488">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-489">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9fb26-489">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="9fb26-490">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9fb26-490">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="9fb26-491">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9fb26-491">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="9fb26-492">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-492">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="9fb26-493">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fb26-493">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-494">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9fb26-494">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-495">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-496">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-497">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-498">Más información cuando la propiedad **errorInfo** está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="9fb26-498">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="9fb26-499">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-499">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9fb26-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-501">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-502">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-503">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9fb26-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-504">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9fb26-504">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9fb26-505">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9fb26-506">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9fb26-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9fb26-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-508">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-510">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9fb26-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9fb26-511">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="9fb26-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9fb26-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9fb26-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9fb26-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9fb26-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9fb26-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-516">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9fb26-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9fb26-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9fb26-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-518">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="9fb26-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9fb26-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="9fb26-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-520">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="9fb26-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9fb26-521">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="9fb26-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9fb26-522">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9fb26-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9fb26-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="9fb26-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-524">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="9fb26-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9fb26-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="9fb26-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9fb26-526">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="9fb26-526">Timed Power-On Supported</span></span>

<span data-ttu-id="9fb26-527">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="9fb26-527">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-528">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9fb26-528">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-529">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9fb26-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-530">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-531">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="9fb26-531">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="9fb26-532">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="9fb26-532">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="9fb26-533">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-533">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-534">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="9fb26-534">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-536">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-537">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="9fb26-537">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="9fb26-538">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-538">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-539">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="9fb26-539">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-540">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fb26-540">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-541">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-542">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("el \| tipo de SMBIOS 19 \| memoria asignación de dispositivo \| dirección de inicio")</span><span class="sxs-lookup"><span data-stu-id="9fb26-542">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-543">Dirección inicial a la que hace referencia una aplicación o el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-543">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="9fb26-544">Esta dirección de memoria está asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="9fb26-544">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="9fb26-545">Este valor procede de la estructura de la **dirección asignada** de la matriz de memoria en la información de la versión de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="9fb26-545">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="9fb26-546">En el caso de las versiones de SMBIOS 2,1 a 2,6, el valor procede del miembro de la **dirección de inicio** .</span><span class="sxs-lookup"><span data-stu-id="9fb26-546">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Starting Address** member.</span></span> <span data-ttu-id="9fb26-547">En el caso de la versión 2.7 de SMBIOS, el valor procede del miembro de la **dirección de inicio extendido** .</span><span class="sxs-lookup"><span data-stu-id="9fb26-547">For SMBIOS version 2.7+ the value comes from the **Extended Starting Address** member.</span></span>

<span data-ttu-id="9fb26-548">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-548">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="9fb26-549">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fb26-549">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-550">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9fb26-550">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-551">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-552">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-553">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9fb26-553">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-554">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9fb26-554">Current status of the object.</span></span> <span data-ttu-id="9fb26-555">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="9fb26-555">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9fb26-556">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="9fb26-556">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9fb26-557">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="9fb26-557">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9fb26-558">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="9fb26-558">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9fb26-559">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="9fb26-559">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9fb26-560">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-560">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9fb26-561">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9fb26-561">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9fb26-562">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="9fb26-562">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9fb26-563">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="9fb26-563">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9fb26-564">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9fb26-564">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-565">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9fb26-565">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9fb26-566">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9fb26-566">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9fb26-567">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="9fb26-567">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9fb26-568">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="9fb26-568">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9fb26-569">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="9fb26-569">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9fb26-570">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="9fb26-570">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9fb26-571">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9fb26-571">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9fb26-572">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="9fb26-572">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9fb26-573">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="9fb26-573">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-574">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9fb26-574">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-575">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb26-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-576">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-577">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-577">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-578">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9fb26-578">State of the logical device.</span></span> <span data-ttu-id="9fb26-579">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="9fb26-579">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9fb26-580">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-580">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9fb26-581">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9fb26-581">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9fb26-582">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9fb26-582">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9fb26-583">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9fb26-583">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9fb26-584">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="9fb26-584">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9fb26-585">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="9fb26-585">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9fb26-586">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9fb26-586">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-587">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-588">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-589">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9fb26-589">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-590">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9fb26-590">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="9fb26-591">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-592">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="9fb26-592">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-593">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9fb26-593">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-594">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-594">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-595">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32 bits información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="9fb26-595">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-596">Si es **true**, la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb26-596">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="9fb26-597">Si es **false**, se trata de una dirección física.</span><span class="sxs-lookup"><span data-stu-id="9fb26-597">If **False**, it is a physical address.</span></span> <span data-ttu-id="9fb26-598">Esta propiedad solo se utiliza cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="9fb26-598">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="9fb26-599">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-599">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb26-600">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9fb26-600">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb26-601">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9fb26-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-602">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb26-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb26-603">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9fb26-603">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9fb26-604">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9fb26-604">Name of the scoping system.</span></span>

<span data-ttu-id="9fb26-605">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-605">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fb26-606">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fb26-606">Remarks</span></span>

<span data-ttu-id="9fb26-607">La **clase \_ MemoryArray de Win32** se deriva de [**\_ SMBIOSMemory de Win32**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9fb26-607">The **Win32\_MemoryArray** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb26-608">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb26-608">Requirements</span></span>



| <span data-ttu-id="9fb26-609">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb26-609">Requirement</span></span> | <span data-ttu-id="9fb26-610">Value</span><span class="sxs-lookup"><span data-stu-id="9fb26-610">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb26-611">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fb26-611">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb26-612">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fb26-612">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fb26-613">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fb26-613">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb26-614">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fb26-614">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fb26-615">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9fb26-615">Namespace</span></span><br/>                | <span data-ttu-id="9fb26-616">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9fb26-616">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9fb26-617">MOF</span><span class="sxs-lookup"><span data-stu-id="9fb26-617">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fb26-618"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fb26-618"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fb26-619">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fb26-619">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fb26-620"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fb26-620"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb26-621">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fb26-621">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb26-622">**Win32 \_ SMBIOSMemory**</span><span class="sxs-lookup"><span data-stu-id="9fb26-622">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="9fb26-623">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="9fb26-623">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

