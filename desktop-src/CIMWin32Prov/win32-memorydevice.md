---
description: La \_ clase WMI MemoryDevice de Win32 representa las propiedades de un dispositivo de memoria del sistema del equipo y sus direcciones asignadas asociadas.
ms.assetid: d609dca5-2f5f-4f23-8fcc-bcc197d6c24b
ms.tgt_platform: multiple
title: Win32_MemoryDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDevice
- Win32_MemoryDevice.Reset
- Win32_MemoryDevice.SetPowerState
- Win32_MemoryDevice.Access
- Win32_MemoryDevice.AdditionalErrorData
- Win32_MemoryDevice.Availability
- Win32_MemoryDevice.BlockSize
- Win32_MemoryDevice.Caption
- Win32_MemoryDevice.ConfigManagerErrorCode
- Win32_MemoryDevice.ConfigManagerUserConfig
- Win32_MemoryDevice.CorrectableError
- Win32_MemoryDevice.CreationClassName
- Win32_MemoryDevice.Description
- Win32_MemoryDevice.DeviceID
- Win32_MemoryDevice.EndingAddress
- Win32_MemoryDevice.ErrorAccess
- Win32_MemoryDevice.ErrorAddress
- Win32_MemoryDevice.ErrorCleared
- Win32_MemoryDevice.ErrorData
- Win32_MemoryDevice.ErrorDataOrder
- Win32_MemoryDevice.ErrorDescription
- Win32_MemoryDevice.ErrorGranularity
- Win32_MemoryDevice.ErrorInfo
- Win32_MemoryDevice.ErrorMethodology
- Win32_MemoryDevice.ErrorResolution
- Win32_MemoryDevice.ErrorTime
- Win32_MemoryDevice.ErrorTransferSize
- Win32_MemoryDevice.InstallDate
- Win32_MemoryDevice.LastErrorCode
- Win32_MemoryDevice.Name
- Win32_MemoryDevice.NumberOfBlocks
- Win32_MemoryDevice.OtherErrorDescription
- Win32_MemoryDevice.PNPDeviceID
- Win32_MemoryDevice.PowerManagementCapabilities
- Win32_MemoryDevice.PowerManagementSupported
- Win32_MemoryDevice.Purpose
- Win32_MemoryDevice.StartingAddress
- Win32_MemoryDevice.Status
- Win32_MemoryDevice.StatusInfo
- Win32_MemoryDevice.SystemCreationClassName
- Win32_MemoryDevice.SystemLevelAddress
- Win32_MemoryDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 277b868f1b92b9f7c6a0c520c77ab76fac6b544d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998156"
---
# <a name="win32_memorydevice-class"></a><span data-ttu-id="b4dcf-103">\_Clase Win32 MemoryDevice</span><span class="sxs-lookup"><span data-stu-id="b4dcf-103">Win32\_MemoryDevice class</span></span>

<span data-ttu-id="b4dcf-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDevice de Win32** representa las propiedades de un dispositivo de memoria del sistema del equipo y sus direcciones asignadas asociadas.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-104">The **Win32\_MemoryDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a computer system memory device and its associated mapped addresses.</span></span>

<span data-ttu-id="b4dcf-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b4dcf-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4dcf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4dcf-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDevice : Win32_SMBIOSMemory
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

## <a name="members"></a><span data-ttu-id="b4dcf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4dcf-108">Members</span></span>

<span data-ttu-id="b4dcf-109">La **clase \_ MemoryDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b4dcf-109">The **Win32\_MemoryDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="b4dcf-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4dcf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b4dcf-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4dcf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b4dcf-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4dcf-112">Methods</span></span>

<span data-ttu-id="b4dcf-113">La clase **Win32 \_ MemoryDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-113">The **Win32\_MemoryDevice** class has these methods.</span></span>



| <span data-ttu-id="b4dcf-114">Método</span><span class="sxs-lookup"><span data-stu-id="b4dcf-114">Method</span></span>            | <span data-ttu-id="b4dcf-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4dcf-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4dcf-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-116">**Reset**</span></span>         | <span data-ttu-id="b4dcf-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-117">Not implemented.</span></span> <span data-ttu-id="b4dcf-118">Para implementar este método, vea el método [**RESET**](reset-method-in-class-cim-controller.md) en [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/>                 |
| <span data-ttu-id="b4dcf-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-119">**SetPowerState**</span></span> | <span data-ttu-id="b4dcf-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-120">Not implemented.</span></span> <span data-ttu-id="b4dcf-121">Para implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b4dcf-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4dcf-122">Properties</span></span>

<span data-ttu-id="b4dcf-123">La **clase \_ MemoryDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-123">The **Win32\_MemoryDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4dcf-124">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-127">Acceso a medios disponible.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-127">Media access available.</span></span>

<span data-ttu-id="b4dcf-128">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="b4dcf-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="b4dcf-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-132">Editable</span><span class="sxs-lookup"><span data-stu-id="b4dcf-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="b4dcf-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="b4dcf-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-136">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="b4dcf-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit información de error de memoria de bits \| "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-139">Matriz de información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-139">Array of additional error information.</span></span> <span data-ttu-id="b4dcf-140">Un ejemplo es el síndrome de comprobación y corrección de errores (ECC) o el retorno de los bits de comprobación si se usa una metodología de error basada en una comprobación de redundancia cíclica (CRC).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based error methodology is used.</span></span> <span data-ttu-id="b4dcf-141">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, es posible determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="b4dcf-142">Este tipo de datos (síndrome ECC, bit de comprobación, datos de bit de paridad u otra información suministrada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="b4dcf-143">Esta propiedad solo se usa cuando la propiedad **errorInfo** no es igual a 3.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="b4dcf-144">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-145">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-146">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-149">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-149">Availability and status of the device.</span></span>

<span data-ttu-id="b4dcf-150">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4dcf-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b4dcf-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-154">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="b4dcf-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b4dcf-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b4dcf-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b4dcf-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b4dcf-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="b4dcf-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b4dcf-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="b4dcf-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b4dcf-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b4dcf-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b4dcf-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b4dcf-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b4dcf-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-165">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b4dcf-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-167">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-167">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b4dcf-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-169">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b4dcf-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b4dcf-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-172">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b4dcf-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-174">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b4dcf-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-176">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b4dcf-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-178">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b4dcf-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-180">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-182">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-184">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-185">Tamaño en bytes de los bloques que forman esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="b4dcf-186">Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="b4dcf-187">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b4dcf-188">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-192">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-193">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b4dcf-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-196">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-198">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-199">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b4dcf-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b4dcf-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b4dcf-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-203">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b4dcf-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b4dcf-205">(1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-206">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b4dcf-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b4dcf-208">(2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b4dcf-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b4dcf-210">(3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-211">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b4dcf-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b4dcf-213">(4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-214">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-214">Device is not working properly.</span></span> <span data-ttu-id="b4dcf-215">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b4dcf-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b4dcf-217">(5)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-218">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b4dcf-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b4dcf-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-221">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b4dcf-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b4dcf-223">(7)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b4dcf-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b4dcf-225">(8)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-226">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b4dcf-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b4dcf-228">(9)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-229">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-229">Device is not working properly.</span></span> <span data-ttu-id="b4dcf-230">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b4dcf-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b4dcf-232">(10)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-233">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b4dcf-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b4dcf-235">(11)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-236">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b4dcf-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b4dcf-238">(12)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-239">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b4dcf-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b4dcf-241">(13)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-242">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b4dcf-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b4dcf-244">(14)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-245">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b4dcf-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b4dcf-247">(15)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-248">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b4dcf-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b4dcf-250">(16)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-251">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b4dcf-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b4dcf-253">(17)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-254">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b4dcf-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b4dcf-256">(18)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-257">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b4dcf-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b4dcf-259">(19)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b4dcf-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b4dcf-261">(20)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-262">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b4dcf-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b4dcf-264">(21)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-265">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-265">System failure.</span></span> <span data-ttu-id="b4dcf-266">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b4dcf-267">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b4dcf-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b4dcf-269">(22)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-270">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b4dcf-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b4dcf-272">(23)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-273">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-273">System failure.</span></span> <span data-ttu-id="b4dcf-274">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b4dcf-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b4dcf-276">(24)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-277">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b4dcf-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b4dcf-279">(25)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-280">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b4dcf-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b4dcf-282">(26)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-283">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b4dcf-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b4dcf-285">(27)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-286">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b4dcf-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b4dcf-288">(28)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-289">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b4dcf-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b4dcf-291">(29)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-292">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-292">Device is disabled.</span></span> <span data-ttu-id="b4dcf-293">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b4dcf-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b4dcf-295">(30)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-296">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b4dcf-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b4dcf-298">31</span><span class="sxs-lookup"><span data-stu-id="b4dcf-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-299">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-299">Device is not working properly.</span></span> <span data-ttu-id="b4dcf-300">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-302">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-304">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-305">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b4dcf-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-308">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-310">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32: tipo de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-311">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="b4dcf-312">Esta propiedad no se utiliza si **errorInfo** se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="b4dcf-313">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-317">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-318">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-318">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b4dcf-319">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b4dcf-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-321">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-324">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-325">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-325">Description of the object.</span></span>

<span data-ttu-id="b4dcf-326">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-327">**ID**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-330">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-331">Identificador único del dispositivo de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-331">Unique identifier of the memory device.</span></span>

<span data-ttu-id="b4dcf-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b4dcf-333">Ejemplo: "dispositivo de memoria 1"</span><span class="sxs-lookup"><span data-stu-id="b4dcf-333">Example: "Memory Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-335">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("se ha \| asignado el dispositivo de memoria de tipo SMBIOS 19 \| dirección final de direcciones \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-338">Dirección final a la que hace referencia una aplicación o un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="b4dcf-339">Esta dirección de memoria está asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="b4dcf-340">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-340">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b4dcf-341">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-341">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-342">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-342">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-343">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-345">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32: error de la información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-346">Tipo de operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-346">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="b4dcf-347">Esta propiedad solo es válida cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-347">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b4dcf-348">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-348">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4dcf-349">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-350">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="b4dcf-351">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-351">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="b4dcf-352">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-352">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="b4dcf-353">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-353">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-354">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-354">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-355">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-357">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32 bits información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-357">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-358">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-358">Address of the last memory error.</span></span> <span data-ttu-id="b4dcf-359">Esta propiedad solo se utiliza cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-359">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b4dcf-360">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-360">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b4dcf-361">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-362">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-362">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-363">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-365">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-365">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b4dcf-366">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-367">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-367">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-368">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="b4dcf-368">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-370">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-370">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-371">Matriz de datos capturados del último acceso a memoria con un error.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-371">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="b4dcf-372">Los datos ocupan los primeros *n* octetos de la matriz necesaria para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="b4dcf-372">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="b4dcf-373">Si **ErrorTransferSize** es 0 (cero), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-373">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="b4dcf-374">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-374">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-375">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-375">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-376">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-378">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-379">Ordenación de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="b4dcf-379">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="b4dcf-380">Esta propiedad solo se utiliza cuando **ErrorTransferSize** es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-380">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="b4dcf-381">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-381">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-382">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-382">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="b4dcf-383">**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-383">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="b4dcf-384">**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-384">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-385">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-385">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-386">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-388">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-388">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="b4dcf-389">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-390">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-390">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-391">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-393">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("granularidad de error de tipo de SMBIOS \| 18 \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-394">Nivel en el que se puede resolver el error.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-394">Level where the error can be resolved.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4dcf-395">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-396">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_level"></span><span id="device_level"></span><span id="DEVICE_LEVEL"></span>

<span data-ttu-id="b4dcf-397">**Nivel de dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-397">**Device level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_partition_level"></span><span id="memory_partition_level"></span><span id="MEMORY_PARTITION_LEVEL"></span>

<span data-ttu-id="b4dcf-398">**Nivel de partición de memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-398">**Memory partition level** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-399">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-399">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-400">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-400">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-401">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-402">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| tipo 18 \| 32-bit memoria error tipo de error de memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-402">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-403">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-403">Type of error that occurred most recently.</span></span> <span data-ttu-id="b4dcf-404">Los valores 12-14, que indican si un error es corregible, no se utilizan con esta propiedad, pero esta información se encuentra en la propiedad **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="b4dcf-404">The values 12-14, indicating whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="b4dcf-405">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-405">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4dcf-406">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-406">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-407">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-407">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b4dcf-408">**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-408">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="b4dcf-409">**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-409">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="b4dcf-410">**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-410">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="b4dcf-411">**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-411">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="b4dcf-412">**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-412">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="b4dcf-413">**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-413">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="b4dcf-414">**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-414">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="b4dcf-415">**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-415">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="b4dcf-416">**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-416">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="b4dcf-417">Se **corrigió el error de un solo bit** (12)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-417">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="b4dcf-418">**Error corregido** (13)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-418">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="b4dcf-419">**Error no corregible** (14)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-419">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-420">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-420">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-423">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) de error ("tipo de SMBIOS \| 16 corrección de errores de memoria de matriz de memoria \| física \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-424">Tipos de comprobación de errores utilizados por el hardware de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-424">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="b4dcf-425">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-425">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b4dcf-426">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="b4dcf-426">The values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4dcf-427">**Otro** ("otro")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-427">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-428">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-428">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="b4dcf-429">**Paridad** ("paridad")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-429">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="b4dcf-430">**ECC de un bit** ("ECC de un bit")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-430">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="b4dcf-431">**ECC de varios bits** ("ECC de varios bits")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-431">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b4dcf-432">**Ninguno** ("ninguno")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-432">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="b4dcf-433">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-433">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-434">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-434">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-435">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-435">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-437">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 18 \| 32-bit Memory error \| Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-438">Cantidad de datos realmente determinados para producir el error.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-438">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="b4dcf-439">Esta propiedad no se utiliza cuando la propiedad **errorInfo** se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-439">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="b4dcf-440">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-440">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b4dcf-441">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-441">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-442">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-442">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-443">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-445">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-445">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-446">Hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-446">Time that the last memory error occurred.</span></span> <span data-ttu-id="b4dcf-447">Esta propiedad solo es válida cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-447">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b4dcf-448">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-448">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-449">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-449">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-450">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-452">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-453">Tamaño de los datos (que contienen el último error) que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-453">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="b4dcf-454">Esta propiedad se establece en 0 (cero) si no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-454">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="b4dcf-455">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-455">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-456">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-456">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-457">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-459">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-460">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-460">Date and time the object was installed.</span></span> <span data-ttu-id="b4dcf-461">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-461">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b4dcf-462">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-462">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-463">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-463">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-464">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-464">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-466">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-466">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b4dcf-467">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-468">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-468">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-471">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-471">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-472">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-472">Label by which the object is known.</span></span> <span data-ttu-id="b4dcf-473">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-473">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b4dcf-474">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-474">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-475">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-475">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-476">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-476">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-478">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-479">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-479">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="b4dcf-480">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-480">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="b4dcf-481">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-481">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="b4dcf-482">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-482">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b4dcf-483">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-483">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-484">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-484">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-485">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-487">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-487">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-488">Más información cuando la propiedad **errorInfo** está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-488">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="b4dcf-489">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-489">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-490">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-490">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-491">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-492">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-493">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-493">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-494">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-494">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b4dcf-495">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b4dcf-496">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b4dcf-496">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-497">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-497">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-498">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-498">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-500">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-500">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b4dcf-501">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-501">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b4dcf-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b4dcf-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b4dcf-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-506">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-506">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b4dcf-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-508">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-508">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b4dcf-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-510">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b4dcf-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b4dcf-511">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-511">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b4dcf-512">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-512">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b4dcf-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-514">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-514">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b4dcf-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b4dcf-516">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="b4dcf-516">Timed Power-On Supported</span></span>

<span data-ttu-id="b4dcf-517">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-517">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-518">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-518">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-519">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-519">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-520">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-520">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-521">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-521">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b4dcf-522">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-522">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b4dcf-523">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-524">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-524">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-525">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-526">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-527">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-527">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="b4dcf-528">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-528">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-529">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-529">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-530">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-531">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-532">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("el \| tipo de SMBIOS 19 \| memoria asignación de dispositivo \| dirección de inicio")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-532">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-533">Dirección inicial a la que hace referencia una aplicación o el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-533">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="b4dcf-534">Esta dirección de memoria está asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-534">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="b4dcf-535">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-535">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b4dcf-536">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-536">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-537">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-537">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-538">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-539">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-540">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-540">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-541">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-541">Current status of the object.</span></span> <span data-ttu-id="b4dcf-542">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-542">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b4dcf-543">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-543">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b4dcf-544">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b4dcf-544">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b4dcf-545">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-545">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b4dcf-546">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-546">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b4dcf-547">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-547">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b4dcf-548">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b4dcf-548">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b4dcf-549">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-549">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b4dcf-550">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-550">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b4dcf-551">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-551">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-552">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-552">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b4dcf-553">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-553">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b4dcf-554">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-554">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b4dcf-555">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-555">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b4dcf-556">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-556">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b4dcf-557">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-557">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b4dcf-558">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-558">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b4dcf-559">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-559">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b4dcf-560">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-560">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-561">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-561">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-562">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-562">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-563">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-563">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-564">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-564">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-565">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-565">State of the logical device.</span></span> <span data-ttu-id="b4dcf-566">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-566">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b4dcf-567">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-567">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4dcf-568">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4dcf-569">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-569">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b4dcf-570">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-570">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b4dcf-571">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-571">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b4dcf-572">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-572">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4dcf-573">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-573">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-574">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-575">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-575">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-576">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-576">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-577">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-577">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b4dcf-578">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-578">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-579">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-579">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-580">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-580">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-581">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-582">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32 bits información de error de memoria de bits \| ")</span><span class="sxs-lookup"><span data-stu-id="b4dcf-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-583">Si es **true**, la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-583">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="b4dcf-584">Si es **false**, se trata de una dirección física.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-584">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="b4dcf-585">Esta propiedad solo se utiliza cuando **errorInfo** no se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-585">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b4dcf-586">Esta propiedad se hereda de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-586">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4dcf-587">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-587">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dcf-588">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-589">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4dcf-589">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4dcf-590">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b4dcf-590">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b4dcf-591">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-591">Name of the scoping system.</span></span>

<span data-ttu-id="b4dcf-592">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-592">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4dcf-593">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4dcf-593">Remarks</span></span>

<span data-ttu-id="b4dcf-594">La **clase \_ MemoryDevice de Win32** se deriva de [**\_ SMBIOSMemory de Win32**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4dcf-594">The **Win32\_MemoryDevice** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b4dcf-595">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b4dcf-595">Examples</span></span>

<span data-ttu-id="b4dcf-596">El ejemplo [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl devuelve las direcciones de inicio y finalización de todos los dispositivos de memoria instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-596">The [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl sample returns starting and ending addresses for all memory devices installed on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4dcf-597">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4dcf-597">Requirements</span></span>



| <span data-ttu-id="b4dcf-598">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4dcf-598">Requirement</span></span> | <span data-ttu-id="b4dcf-599">Value</span><span class="sxs-lookup"><span data-stu-id="b4dcf-599">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4dcf-600">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4dcf-600">Minimum supported client</span></span><br/> | <span data-ttu-id="b4dcf-601">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4dcf-601">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4dcf-602">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4dcf-602">Minimum supported server</span></span><br/> | <span data-ttu-id="b4dcf-603">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4dcf-603">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4dcf-604">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4dcf-604">Namespace</span></span><br/>                | <span data-ttu-id="b4dcf-605">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b4dcf-605">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4dcf-606">MOF</span><span class="sxs-lookup"><span data-stu-id="b4dcf-606">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4dcf-607"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-607"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4dcf-608">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4dcf-608">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4dcf-609"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-609"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4dcf-610">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4dcf-610">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4dcf-611">**Win32 \_ SMBIOSMemory**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-611">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="b4dcf-612">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="b4dcf-612">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

