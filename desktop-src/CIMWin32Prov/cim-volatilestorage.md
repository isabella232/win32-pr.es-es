---
description: La \_ clase CIM VolatileStorage representa las capacidades y la administración del almacenamiento volátil.
ms.assetid: c2f7e11e-d7e4-4709-be55-1c94a0b14010
ms.tgt_platform: multiple
title: CIM_VolatileStorage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage
- CIM_VolatileStorage.Access
- CIM_VolatileStorage.AdditionalErrorData
- CIM_VolatileStorage.Availability
- CIM_VolatileStorage.BlockSize
- CIM_VolatileStorage.Cacheable
- CIM_VolatileStorage.CacheType
- CIM_VolatileStorage.Caption
- CIM_VolatileStorage.ConfigManagerErrorCode
- CIM_VolatileStorage.ConfigManagerUserConfig
- CIM_VolatileStorage.CorrectableError
- CIM_VolatileStorage.CreationClassName
- CIM_VolatileStorage.Description
- CIM_VolatileStorage.DeviceID
- CIM_VolatileStorage.EndingAddress
- CIM_VolatileStorage.ErrorAccess
- CIM_VolatileStorage.ErrorAddress
- CIM_VolatileStorage.ErrorCleared
- CIM_VolatileStorage.ErrorData
- CIM_VolatileStorage.ErrorDataOrder
- CIM_VolatileStorage.ErrorDescription
- CIM_VolatileStorage.ErrorInfo
- CIM_VolatileStorage.ErrorMethodology
- CIM_VolatileStorage.ErrorResolution
- CIM_VolatileStorage.ErrorTime
- CIM_VolatileStorage.ErrorTransferSize
- CIM_VolatileStorage.InstallDate
- CIM_VolatileStorage.LastErrorCode
- CIM_VolatileStorage.Name
- CIM_VolatileStorage.NumberOfBlocks
- CIM_VolatileStorage.OtherErrorDescription
- CIM_VolatileStorage.PNPDeviceID
- CIM_VolatileStorage.PowerManagementCapabilities
- CIM_VolatileStorage.PowerManagementSupported
- CIM_VolatileStorage.Purpose
- CIM_VolatileStorage.StartingAddress
- CIM_VolatileStorage.Status
- CIM_VolatileStorage.StatusInfo
- CIM_VolatileStorage.SystemCreationClassName
- CIM_VolatileStorage.SystemLevelAddress
- CIM_VolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99add7401d92d82385a4182e466de8b28ad4fc09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907034"
---
# <a name="cim_volatilestorage-class"></a><span data-ttu-id="37069-103">\_Clase VolatileStorage de CIM</span><span class="sxs-lookup"><span data-stu-id="37069-103">CIM\_VolatileStorage class</span></span>

<span data-ttu-id="37069-104">La clase **CIM \_ VolatileStorage** representa las capacidades y la administración del almacenamiento volátil.</span><span class="sxs-lookup"><span data-stu-id="37069-104">The **CIM\_VolatileStorage** class represents the capabilities and management of volatile storage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37069-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="37069-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="37069-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="37069-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="37069-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="37069-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="37069-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="37069-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="37069-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37069-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36851DFE-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_VolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  boolean  Cacheable;
  uint16   CacheType;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="37069-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="37069-110">Members</span></span>

<span data-ttu-id="37069-111">La clase **CIM \_ VolatileStorage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="37069-111">The **CIM\_VolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="37069-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="37069-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="37069-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37069-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="37069-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="37069-114">Methods</span></span>

<span data-ttu-id="37069-115">La clase **CIM \_ VolatileStorage** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="37069-115">The **CIM\_VolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="37069-116">Método</span><span class="sxs-lookup"><span data-stu-id="37069-116">Method</span></span>                                                                     | <span data-ttu-id="37069-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="37069-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37069-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="37069-118">**Reset**</span></span>](reset-method-in-class-cim-volatilestorage.md)                 | <span data-ttu-id="37069-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37069-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="37069-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="37069-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="37069-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="37069-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volatilestorage.md) | <span data-ttu-id="37069-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="37069-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="37069-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="37069-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="37069-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37069-124">Properties</span></span>

<span data-ttu-id="37069-125">La clase **CIM \_ VolatileStorage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="37069-125">The **CIM\_VolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37069-126">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="37069-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37069-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-129">Propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="37069-129">Read/write properties of the media.</span></span>

<span data-ttu-id="37069-130">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37069-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-131">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="37069-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="37069-132">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="37069-133">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="37069-134">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="37069-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="37069-135">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="37069-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="37069-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-137">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="37069-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="37069-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,18 "," MIF. \|Matriz de memoria física DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="37069-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="37069-140">Información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="37069-140">Additional error information.</span></span> <span data-ttu-id="37069-141">Un ejemplo es el síndrome de comprobación y corrección de errores (ECC) o el retorno de los bits de comprobación si se usa una metodología de error basada en CRC.</span><span class="sxs-lookup"><span data-stu-id="37069-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="37069-142">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, se puede determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="37069-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="37069-143">Este tipo de datos (síndrome ECC, datos de bit de comprobación o de bits de paridad u otra información proporcionada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="37069-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="37069-144">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="37069-145">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-145">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-146">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="37069-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37069-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-149">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="37069-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="37069-150">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-150">Availability and status of the device.</span></span>

<span data-ttu-id="37069-151">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37069-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="37069-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="37069-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="37069-155">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="37069-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="37069-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="37069-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="37069-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="37069-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37069-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="37069-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="37069-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="37069-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="37069-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="37069-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="37069-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="37069-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37069-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="37069-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="37069-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="37069-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="37069-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="37069-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="37069-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="37069-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="37069-166">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="37069-166">The device is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="37069-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="37069-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="37069-168">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="37069-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="37069-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="37069-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="37069-170">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="37069-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="37069-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="37069-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="37069-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="37069-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="37069-173">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="37069-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="37069-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="37069-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="37069-175">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="37069-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="37069-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="37069-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="37069-177">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="37069-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="37069-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="37069-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="37069-179">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="37069-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="37069-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="37069-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="37069-181">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="37069-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="37069-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-183">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37069-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37069-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-185">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="37069-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="37069-186">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="37069-186">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="37069-187">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="37069-187">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="37069-188">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="37069-188">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="37069-189">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37069-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="37069-190">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37069-190">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37069-191">**Almacenable en caché**</span><span class="sxs-lookup"><span data-stu-id="37069-191">**Cacheable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-192">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37069-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37069-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-194">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información de memoria de recursos del sistema DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="37069-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="37069-195">Si **es true**, esta memoria puede almacenarse en caché.</span><span class="sxs-lookup"><span data-stu-id="37069-195">If **TRUE**, this memory can be cached.</span></span>

</dd> <dt>

<span data-ttu-id="37069-196">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="37069-196">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-197">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37069-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-199">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información de memoria de recursos del sistema DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="37069-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="37069-200">Tipo de caché que es compatible con la memoria.</span><span class="sxs-lookup"><span data-stu-id="37069-200">Cache type that is compatible with the memory.</span></span> <span data-ttu-id="37069-201">Si la propiedad **almacenable en caché** está establecida en **false**, esta propiedad no tiene significado y debe establecerse en 4 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="37069-201">If the **Cacheable** property is set to **FALSE**, then this property does not have meaning and should be set to 4 ("Not Applicable").</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37069-202">**Otro** (0)</span><span class="sxs-lookup"><span data-stu-id="37069-202">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-203">**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-203">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Back"></span><span id="write-back"></span><span id="WRITE-BACK"></span>

<span data-ttu-id="37069-204">**Reescritura** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-204">**Write-Back** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Through"></span><span id="write-through"></span><span id="WRITE-THROUGH"></span>

<span data-ttu-id="37069-205">**Escritura a través** (3)</span><span class="sxs-lookup"><span data-stu-id="37069-205">**Write-Through** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37069-206">**No aplicable** (4)</span><span class="sxs-lookup"><span data-stu-id="37069-206">**Not Applicable** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="37069-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-210">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="37069-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="37069-211">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="37069-211">Short textual description of the object.</span></span>

<span data-ttu-id="37069-212">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37069-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="37069-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-214">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37069-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37069-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-216">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="37069-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="37069-217">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="37069-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="37069-218">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="37069-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="37069-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="37069-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="37069-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="37069-221">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="37069-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="37069-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="37069-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="37069-223">(1)</span><span class="sxs-lookup"><span data-stu-id="37069-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="37069-224">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="37069-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="37069-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="37069-226">(2)</span><span class="sxs-lookup"><span data-stu-id="37069-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="37069-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="37069-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="37069-228">(3)</span><span class="sxs-lookup"><span data-stu-id="37069-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="37069-229">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="37069-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="37069-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="37069-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="37069-231">(4)</span><span class="sxs-lookup"><span data-stu-id="37069-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="37069-232">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="37069-232">Device is not working properly.</span></span> <span data-ttu-id="37069-233">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="37069-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="37069-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="37069-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="37069-235">(5)</span><span class="sxs-lookup"><span data-stu-id="37069-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="37069-236">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="37069-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="37069-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="37069-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="37069-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="37069-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="37069-239">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="37069-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="37069-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="37069-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="37069-241">(7)</span><span class="sxs-lookup"><span data-stu-id="37069-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="37069-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="37069-243">(8)</span><span class="sxs-lookup"><span data-stu-id="37069-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="37069-244">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="37069-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="37069-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="37069-246">(9)</span><span class="sxs-lookup"><span data-stu-id="37069-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="37069-247">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="37069-247">Device is not working properly.</span></span> <span data-ttu-id="37069-248">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="37069-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="37069-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="37069-250">(10)</span><span class="sxs-lookup"><span data-stu-id="37069-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="37069-251">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="37069-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="37069-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="37069-253">(11)</span><span class="sxs-lookup"><span data-stu-id="37069-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="37069-254">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="37069-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="37069-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="37069-256">(12)</span><span class="sxs-lookup"><span data-stu-id="37069-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="37069-257">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="37069-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="37069-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="37069-259">(13)</span><span class="sxs-lookup"><span data-stu-id="37069-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="37069-260">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="37069-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="37069-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="37069-262">(14)</span><span class="sxs-lookup"><span data-stu-id="37069-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="37069-263">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="37069-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="37069-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="37069-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="37069-265">(15)</span><span class="sxs-lookup"><span data-stu-id="37069-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="37069-266">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="37069-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="37069-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="37069-268">(16)</span><span class="sxs-lookup"><span data-stu-id="37069-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="37069-269">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="37069-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="37069-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="37069-271">(17)</span><span class="sxs-lookup"><span data-stu-id="37069-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="37069-272">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="37069-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="37069-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="37069-274">(18)</span><span class="sxs-lookup"><span data-stu-id="37069-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="37069-275">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="37069-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="37069-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="37069-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="37069-277">(19)</span><span class="sxs-lookup"><span data-stu-id="37069-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="37069-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="37069-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="37069-279">(20)</span><span class="sxs-lookup"><span data-stu-id="37069-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="37069-280">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="37069-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="37069-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="37069-282">(21)</span><span class="sxs-lookup"><span data-stu-id="37069-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="37069-283">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="37069-283">System failure.</span></span> <span data-ttu-id="37069-284">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="37069-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="37069-285">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="37069-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="37069-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="37069-287">(22)</span><span class="sxs-lookup"><span data-stu-id="37069-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="37069-288">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="37069-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="37069-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="37069-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="37069-290">(23)</span><span class="sxs-lookup"><span data-stu-id="37069-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="37069-291">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="37069-291">System failure.</span></span> <span data-ttu-id="37069-292">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="37069-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="37069-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="37069-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="37069-294">(24)</span><span class="sxs-lookup"><span data-stu-id="37069-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="37069-295">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="37069-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="37069-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="37069-297">(25)</span><span class="sxs-lookup"><span data-stu-id="37069-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="37069-298">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="37069-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="37069-300">(26)</span><span class="sxs-lookup"><span data-stu-id="37069-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="37069-301">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37069-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="37069-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="37069-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="37069-303">(27)</span><span class="sxs-lookup"><span data-stu-id="37069-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="37069-304">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="37069-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="37069-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="37069-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="37069-306">(28)</span><span class="sxs-lookup"><span data-stu-id="37069-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="37069-307">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="37069-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="37069-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="37069-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="37069-309">(29)</span><span class="sxs-lookup"><span data-stu-id="37069-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="37069-310">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="37069-310">Device is disabled.</span></span> <span data-ttu-id="37069-311">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="37069-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="37069-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="37069-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="37069-313">(30)</span><span class="sxs-lookup"><span data-stu-id="37069-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="37069-314">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="37069-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="37069-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37069-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="37069-316">31</span><span class="sxs-lookup"><span data-stu-id="37069-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="37069-317">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="37069-317">Device is not working properly.</span></span> <span data-ttu-id="37069-318">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="37069-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="37069-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-320">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37069-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37069-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-322">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="37069-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="37069-323">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="37069-323">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="37069-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-325">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="37069-325">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-326">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37069-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37069-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-328">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="37069-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="37069-329">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="37069-329">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="37069-330">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-330">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="37069-331">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-331">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37069-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-335">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37069-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37069-336">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="37069-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="37069-337">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="37069-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="37069-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-339">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37069-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-342">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="37069-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="37069-343">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="37069-343">Textual description of the object.</span></span>

<span data-ttu-id="37069-344">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37069-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-345">**ID**</span><span class="sxs-lookup"><span data-stu-id="37069-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-348">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37069-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37069-349">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37069-349">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="37069-350">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-351">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="37069-351">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-352">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37069-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37069-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-354">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,4 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="37069-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37069-355">Dirección final, a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria para el objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="37069-355">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="37069-356">La dirección final se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="37069-356">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="37069-357">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-357">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="37069-358">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37069-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37069-359">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="37069-359">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-360">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37069-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-362">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,15 "," MIF. \|Matriz de memoria física DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="37069-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="37069-363">Operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="37069-363">Memory access operation that caused the last error.</span></span> <span data-ttu-id="37069-364">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="37069-364">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="37069-365">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-365">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="37069-366">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-366">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37069-367">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-367">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-368">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-368">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="37069-369">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="37069-369">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="37069-370">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="37069-370">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="37069-371">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="37069-371">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-372">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="37069-372">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-373">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37069-373">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37069-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-375">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,19 "," MIF. \|Dispositivo de memoria DMTF \| 002,20 "," MIF. \|Matriz de memoria física DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="37069-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="37069-376">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="37069-376">Address of the last memory error.</span></span> <span data-ttu-id="37069-377">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="37069-377">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="37069-378">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-378">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="37069-379">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-379">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="37069-380">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37069-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37069-381">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="37069-381">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-382">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37069-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37069-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-384">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="37069-384">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="37069-385">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-386">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="37069-386">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-387">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="37069-387">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="37069-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-389">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,17 "," MIF. \|Matriz de memoria física DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="37069-389">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="37069-390">Datos capturados durante el último acceso erróneo a la memoria.</span><span class="sxs-lookup"><span data-stu-id="37069-390">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="37069-391">Los datos ocupan los primeros *n* octetos de la matriz necesaria para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="37069-391">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="37069-392">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-392">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="37069-393">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-394">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="37069-394">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-395">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37069-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-397">Ordenación de los datos almacenados en la matriz **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="37069-397">Ordering for data stored in the **ErrorData** array.</span></span> <span data-ttu-id="37069-398">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-398">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="37069-399">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="37069-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="37069-401">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="37069-401">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="37069-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="37069-403">Byte menos significativo primero.</span><span class="sxs-lookup"><span data-stu-id="37069-403">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="37069-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="37069-405">Byte más significativo en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="37069-405">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-406">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="37069-406">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-407">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-409">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="37069-409">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="37069-410">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-411">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="37069-411">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-412">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37069-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-414">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ memoria de CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="37069-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="37069-415">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="37069-415">Type of error that occurred most recently.</span></span> <span data-ttu-id="37069-416">Los valores 12-14 no están definidos en el esquema CIM, ya que la semántica del tipo de error y si se ha corregido o no se ha mezclado en DMI.</span><span class="sxs-lookup"><span data-stu-id="37069-416">The values 12-14 are undefined in the CIM schema since the semantics of the type of error and whether or not it was correctable are mixed in DMI.</span></span> <span data-ttu-id="37069-417">La propiedad **CorrectableError** indica si se ha corregido.</span><span class="sxs-lookup"><span data-stu-id="37069-417">The **CorrectableError** property indicates whether it was correctable.</span></span>

<span data-ttu-id="37069-418">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-418">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37069-419">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-419">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-420">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-420">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="37069-421">**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="37069-421">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="37069-422">**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="37069-422">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="37069-423">**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="37069-423">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="37069-424">**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="37069-424">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="37069-425">**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="37069-425">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="37069-426">**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="37069-426">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="37069-427">**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="37069-427">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="37069-428">**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="37069-428">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="37069-429">**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="37069-429">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="37069-430">**Undefined** (12)</span><span class="sxs-lookup"><span data-stu-id="37069-430">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="37069-431">**Sin definir** (13)</span><span class="sxs-lookup"><span data-stu-id="37069-431">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="37069-432">**Undefined** (14)</span><span class="sxs-lookup"><span data-stu-id="37069-432">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-433">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="37069-433">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-436">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="37069-436">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="37069-437">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="37069-437">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="37069-438">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-438">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-439">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="37069-439">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-440">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37069-440">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37069-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-442">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,21 "," MIF. \|Matriz de memoria física DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="37069-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="37069-443">Intervalo, en bytes, en el que se puede resolver el último error.</span><span class="sxs-lookup"><span data-stu-id="37069-443">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="37069-444">Por ejemplo, si las direcciones de error se resuelven en el bit 11 (es decir, en una página típica), los errores pueden resolverse en límites de 4 KB y esta propiedad se establece en 4000.</span><span class="sxs-lookup"><span data-stu-id="37069-444">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="37069-445">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-445">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="37069-446">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-446">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="37069-447">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37069-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37069-448">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="37069-448">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-449">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="37069-449">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37069-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-451">Hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="37069-451">Time that the last memory error occurred.</span></span> <span data-ttu-id="37069-452">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="37069-452">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="37069-453">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-453">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="37069-454">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-454">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-455">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="37069-455">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-456">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37069-456">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37069-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-458">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,16 "," MIF. \|Matriz de memoria física DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="37069-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="37069-459">Tamaño de la transferencia de datos en bits que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="37069-459">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="37069-460">0 indica que no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="37069-460">0 indicates no error.</span></span> <span data-ttu-id="37069-461">Si la propiedad **errorInfo** es igual a 3, "OK", esta propiedad debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="37069-461">If the **ErrorInfo** property is equal to 3, "OK", then this property should be set to 0.</span></span>

<span data-ttu-id="37069-462">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-462">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-463">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="37069-463">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-464">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="37069-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37069-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-466">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="37069-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="37069-467">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="37069-467">Date and time the object was installed.</span></span> <span data-ttu-id="37069-468">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="37069-468">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="37069-469">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37069-469">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="37069-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-471">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37069-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37069-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-473">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37069-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="37069-474">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-475">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="37069-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-476">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-478">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="37069-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="37069-479">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="37069-479">Label by which the object is known.</span></span> <span data-ttu-id="37069-480">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="37069-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="37069-481">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37069-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="37069-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-483">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37069-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37069-484">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-485">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="37069-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="37069-486">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="37069-486">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="37069-487">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="37069-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="37069-488">Si el valor de **blocksize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="37069-488">If the value of **BlockSize** is 1 (one), then this property is the total size of the storage extent.</span></span>

<span data-ttu-id="37069-489">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37069-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="37069-490">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37069-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37069-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="37069-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-492">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-493">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-494">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="37069-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="37069-495">Cadena de forma libre que proporciona información adicional si la propiedad de **ErrorType** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="37069-495">Free-form string that provides additional information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="37069-496">Si un valor distinto de 1 (uno), esta cadena no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-496">If a value other than 1 (one), this string has no meaning.</span></span>

<span data-ttu-id="37069-497">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="37069-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-499">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-501">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="37069-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="37069-502">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37069-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="37069-503">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="37069-504">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="37069-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="37069-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="37069-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-506">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37069-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-508">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37069-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="37069-509">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="37069-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="37069-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="37069-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37069-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37069-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="37069-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="37069-514">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="37069-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="37069-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="37069-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="37069-516">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="37069-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="37069-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="37069-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="37069-518">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="37069-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="37069-519">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="37069-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="37069-520">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="37069-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="37069-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="37069-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="37069-522">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="37069-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="37069-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="37069-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="37069-524">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="37069-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="37069-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-526">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37069-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37069-527">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-528">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="37069-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="37069-529">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="37069-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="37069-530">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="37069-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="37069-531">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="37069-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="37069-532">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-533">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="37069-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-534">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-535">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-536">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="37069-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="37069-537">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37069-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-538">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="37069-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-539">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37069-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37069-540">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-541">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,3 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="37069-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37069-542">Dirección inicial, a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria para el objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="37069-542">Beginning address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="37069-543">La dirección de inicio se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="37069-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="37069-544">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="37069-545">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37069-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37069-546">**Estado**</span><span class="sxs-lookup"><span data-stu-id="37069-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-547">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-549">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="37069-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="37069-550">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="37069-550">Current status of the object.</span></span> <span data-ttu-id="37069-551">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37069-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="37069-552">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="37069-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="37069-553">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="37069-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="37069-554">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="37069-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37069-555">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="37069-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-556">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="37069-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="37069-557">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="37069-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="37069-558">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="37069-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="37069-559">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="37069-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="37069-560">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="37069-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="37069-561">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="37069-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="37069-562">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="37069-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="37069-563">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="37069-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="37069-564">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="37069-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="37069-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-566">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37069-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37069-567">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-568">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="37069-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="37069-569">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37069-569">State of the logical device.</span></span> <span data-ttu-id="37069-570">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="37069-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="37069-571">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37069-572">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="37069-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37069-573">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="37069-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37069-574">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="37069-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37069-575">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="37069-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37069-576">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="37069-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37069-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37069-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-578">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-579">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-580">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37069-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37069-581">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="37069-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="37069-582">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="37069-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-584">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37069-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37069-585">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37069-586">Si es **true**, la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema; Si es **false**, se trata de una dirección física.</span><span class="sxs-lookup"><span data-stu-id="37069-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address; if **FALSE**, it is a physical address.</span></span> <span data-ttu-id="37069-587">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="37069-587">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="37069-588">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-588">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="37069-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="37069-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37069-590">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37069-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37069-591">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37069-591">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37069-592">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37069-592">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37069-593">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="37069-593">Scoping system's name.</span></span>

<span data-ttu-id="37069-594">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37069-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37069-595">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37069-595">Remarks</span></span>

<span data-ttu-id="37069-596">La clase **CIM \_ VolatileStorage** se deriva de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="37069-596">The **CIM\_VolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="37069-597">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="37069-597">WMI does not implement this class.</span></span>

<span data-ttu-id="37069-598">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="37069-598">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="37069-599">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="37069-599">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="37069-600">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37069-600">Requirements</span></span>



| <span data-ttu-id="37069-601">Requisito</span><span class="sxs-lookup"><span data-stu-id="37069-601">Requirement</span></span> | <span data-ttu-id="37069-602">Value</span><span class="sxs-lookup"><span data-stu-id="37069-602">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37069-603">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37069-603">Minimum supported client</span></span><br/> | <span data-ttu-id="37069-604">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37069-604">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37069-605">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37069-605">Minimum supported server</span></span><br/> | <span data-ttu-id="37069-606">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37069-606">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37069-607">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37069-607">Namespace</span></span><br/>                | <span data-ttu-id="37069-608">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="37069-608">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37069-609">MOF</span><span class="sxs-lookup"><span data-stu-id="37069-609">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37069-610"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37069-610"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37069-611">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37069-611">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37069-612"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37069-612"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37069-613">Vea también</span><span class="sxs-lookup"><span data-stu-id="37069-613">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37069-614">**Memoria de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="37069-614">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

