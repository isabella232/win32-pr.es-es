---
description: Win32 \_ CacheMemory&\# 32; La clase WMI representa la memoria caché interna y externa de un equipo.
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Clase Win32_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83a8fefbe1104f24f208d232b8f6bc134efefd83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907426"
---
# <a name="win32_cachememory-class"></a><span data-ttu-id="2c3c6-103">\_Clase Win32 CacheMemory</span><span class="sxs-lookup"><span data-stu-id="2c3c6-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="2c3c6-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CacheMemory de Win32** representa la memoria caché interna y externa en un equipo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="2c3c6-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2c3c6-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c3c6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c3c6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="2c3c6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c3c6-108">Members</span></span>

<span data-ttu-id="2c3c6-109">La **clase \_ CacheMemory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2c3c6-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="2c3c6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c3c6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2c3c6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c3c6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2c3c6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c3c6-112">Methods</span></span>

<span data-ttu-id="2c3c6-113">La clase **Win32 \_ CacheMemory** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="2c3c6-114">Método</span><span class="sxs-lookup"><span data-stu-id="2c3c6-114">Method</span></span>            | <span data-ttu-id="2c3c6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c3c6-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3c6-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-116">**Reset**</span></span>         | <span data-ttu-id="2c3c6-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-117">Not implemented.</span></span> <span data-ttu-id="2c3c6-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ CacheMemory**](cim-cachememory.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="2c3c6-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-119">**SetPowerState**</span></span> | <span data-ttu-id="2c3c6-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-120">Not implemented.</span></span> <span data-ttu-id="2c3c6-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ CacheMemory**](cim-cachememory.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2c3c6-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c3c6-122">Properties</span></span>

<span data-ttu-id="2c3c6-123">La **clase \_ CacheMemory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c3c6-124">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-127">Tipo de acceso.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-127">Type of access.</span></span>

<span data-ttu-id="2c3c6-128">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="2c3c6-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="2c3c6-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-132">Editable</span><span class="sxs-lookup"><span data-stu-id="2c3c6-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="2c3c6-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="2c3c6-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-136">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="2c3c6-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,18 "," MIF. \|Matriz de memoria física DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-139">Matriz de octetos que contienen información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="2c3c6-140">Un ejemplo es el síndrome ECC o el retorno de los bits de comprobación si se usa una metodología de error basada en CRC.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="2c3c6-141">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, es posible determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="2c3c6-142">Este tipo de datos (síndrome ECC, bit de comprobación, datos de bit de paridad u otra información suministrada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="2c3c6-143">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-144">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-145">**asociatividad**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-146">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-149">Una enumeración de enteros que define la asociatividad de la caché del sistema.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="2c3c6-150">Este valor procede del miembro **asociativity** de la estructura de **información de caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2c3c6-151">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-152">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-153">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="2c3c6-154">**Asignación directa** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="2c3c6-155">**asociativo de conjuntos bidireccionales** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="2c3c6-156">**asociativo de conjunto de 4 vías** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="2c3c6-157">**Totalmente asociativo** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="2c3c6-158">**asociativa de conjunto de 8 vías** (7)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="2c3c6-159">**asociativa de conjunto de 16 vías** (8)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-160">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-163">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-164">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-164">Availability and status of the device.</span></span>

<span data-ttu-id="2c3c6-165">Este valor procede del miembro de **configuración de caché** de la estructura de información de **caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2c3c6-166">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2c3c6-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-170">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="2c3c6-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2c3c6-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2c3c6-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2c3c6-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2c3c6-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="2c3c6-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2c3c6-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="2c3c6-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2c3c6-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2c3c6-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2c3c6-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2c3c6-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2c3c6-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-181">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2c3c6-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-183">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2c3c6-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-185">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2c3c6-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2c3c6-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-188">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2c3c6-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-190">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2c3c6-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-192">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2c3c6-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-194">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2c3c6-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-196">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-198">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-200">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-201">Tamaño en bytes de los bloques que forman esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="2c3c6-202">Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="2c3c6-203">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2c3c6-204">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-205">**CacheSpeed**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-206">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-208">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| velocidad de caché de tipo de SMBIOS 7"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-209">Velocidad de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-209">Speed of the cache.</span></span>

<span data-ttu-id="2c3c6-210">Este valor procede del miembro **velocidad de caché** de la estructura de **información de caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-214">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-215">Tipo de caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-215">Type of cache.</span></span>

<span data-ttu-id="2c3c6-216">Este valor procede del miembro de **tipo de caché del sistema** de la estructura de **información de caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2c3c6-217">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-218">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-219">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="2c3c6-220">**Instrucción** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="2c3c6-221">**Datos** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="2c3c6-222">**Unificado** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-223">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-226">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-227">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="2c3c6-228">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-229">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-230">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-232">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-233">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2c3c6-234">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2c3c6-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2c3c6-236"> (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-237">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2c3c6-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2c3c6-239">(1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-240">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2c3c6-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2c3c6-242">(2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2c3c6-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2c3c6-244">(3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-245">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2c3c6-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2c3c6-247">(4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-248">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-248">Device is not working properly.</span></span> <span data-ttu-id="2c3c6-249">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2c3c6-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2c3c6-251">(5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-252">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2c3c6-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2c3c6-254"> (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-255">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2c3c6-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2c3c6-257">(7)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2c3c6-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2c3c6-259">(8)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-260">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2c3c6-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2c3c6-262">(9)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-263">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-263">Device is not working properly.</span></span> <span data-ttu-id="2c3c6-264">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2c3c6-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2c3c6-266">(10)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-267">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2c3c6-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2c3c6-269">(11)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-270">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2c3c6-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2c3c6-272">(12)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-273">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2c3c6-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2c3c6-275">(13)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-276">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2c3c6-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2c3c6-278">(14)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-279">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2c3c6-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2c3c6-281">(15)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-282">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2c3c6-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2c3c6-284">(16)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-285">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2c3c6-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2c3c6-287">(17)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-288">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2c3c6-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2c3c6-290">(18)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-291">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2c3c6-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2c3c6-293">(19)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2c3c6-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2c3c6-295">(20)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-296">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2c3c6-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2c3c6-298">(21)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-299">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-299">System failure.</span></span> <span data-ttu-id="2c3c6-300">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2c3c6-301">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2c3c6-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2c3c6-303">(22)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-304">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2c3c6-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2c3c6-306">(23)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-307">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-307">System failure.</span></span> <span data-ttu-id="2c3c6-308">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2c3c6-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2c3c6-310">(24)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-311">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2c3c6-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2c3c6-313">(25)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-314">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2c3c6-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2c3c6-316">(26)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-317">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2c3c6-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2c3c6-319">(27)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-320">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2c3c6-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2c3c6-322">(28)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-323">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2c3c6-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2c3c6-325">(29)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-326">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-326">Device is disabled.</span></span> <span data-ttu-id="2c3c6-327">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2c3c6-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2c3c6-329">(30)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-330">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2c3c6-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2c3c6-332">31</span><span class="sxs-lookup"><span data-stu-id="2c3c6-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-333">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-333">Device is not working properly.</span></span> <span data-ttu-id="2c3c6-334">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-335">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-336">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-338">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-339">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2c3c6-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-341">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-342">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-344">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-345">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="2c3c6-346">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-347">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-348">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-351">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-352">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="2c3c6-353">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2c3c6-354">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-355">**CurrentSRAM**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-356">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-358">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| Current SRAM Type")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-359">Matriz de tipos de memoria de acceso aleatorio (SRAM) estática que se utiliza para la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="2c3c6-360">Este valor procede del miembro de **tipo SRAM actual** de la estructura de **información de caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-361">**Otro** (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-362">**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="2c3c6-363">**Sin ráfagas** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="2c3c6-364">**Ráfaga** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="2c3c6-365">**Ráfaga de canalización** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="2c3c6-366">**Sincrónico** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="2c3c6-367">**Asincrónico** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-368">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-369">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-371">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-372">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-372">Description of the object.</span></span>

<span data-ttu-id="2c3c6-373">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-374">**ID**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-375">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-377">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-378">Identificador único de la memoria caché representada por una instancia de **Win32 \_ CacheMemory**.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="2c3c6-379">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2c3c6-380">Ejemplo: "memoria caché 1"</span><span class="sxs-lookup"><span data-stu-id="2c3c6-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-381">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-382">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-384">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,4 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-385">Dirección final, a la que hace referencia una aplicación o un sistema operativo y que se asigna mediante un controlador de memoria, para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="2c3c6-386">La dirección final se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="2c3c6-387">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2c3c6-388">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-389">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-390">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-392">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,15 "," MIF. \|Matriz de memoria física DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-393">Operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="2c3c6-394">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="2c3c6-395">Si **errorInfo** es igual a 3 (OK), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-396">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-397">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-398">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="2c3c6-399">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="2c3c6-400">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="2c3c6-401">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-402">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-403">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-405">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,19 "," MIF. \|Dispositivo de memoria DMTF \| 002,20 "," MIF. \|Matriz de memoria física DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-406">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-406">Address of the last memory error.</span></span> <span data-ttu-id="2c3c6-407">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="2c3c6-408">Si **errorInfo** es igual a 3 (OK), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-409">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2c3c6-410">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-411">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-412">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-414">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="2c3c6-415">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-416">**ErrorCorrectType**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-417">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-419">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de corrección de errores de tipo de SMBIOS \| 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-420">Método de corrección de errores usado por la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="2c3c6-421">Este valor procede del miembro de **tipo de corrección de errores** de la estructura de información de **caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2c3c6-422">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-423">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-424">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="2c3c6-425">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="2c3c6-426">**Paridad** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="2c3c6-427">**ECC de un bit** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="2c3c6-428">**ECC de varios bits** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-429">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-430">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="2c3c6-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-432">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,17 "," MIF. \|Matriz de memoria física DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-433">Matriz de los datos capturados durante el último acceso erróneo a la memoria.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="2c3c6-434">Los datos ocupan los primeros *n* octetos de la matriz necesaria para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="2c3c6-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="2c3c6-435">Si **ErrorTransferSize** es 0 (cero), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-436">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-437">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-438">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-440">Ordenación de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="2c3c6-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="2c3c6-441">Si **ErrorTransferSize** es 0 (cero), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-442">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-443">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="2c3c6-444">**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="2c3c6-445">**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-447">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-449">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="2c3c6-450">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-452">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-454">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ memoria de CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-455">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="2c3c6-456">Los valores 12-14 no están definidos en el esquema CIM porque, en DMI, mezclan la semántica del tipo de error y si se han corregido o no.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="2c3c6-457">El último se indica en la propiedad **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="2c3c6-458">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-459">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-460">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2c3c6-461">**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="2c3c6-462">**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="2c3c6-463">**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="2c3c6-464">**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="2c3c6-465">**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="2c3c6-466">**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="2c3c6-467">**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="2c3c6-468">**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="2c3c6-469">**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2c3c6-470">**Undefined** (12)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2c3c6-471">**Sin definir** (13)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2c3c6-472">**Undefined** (14)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-473">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-476">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-477">Detalles sobre los algoritmos de paridad o CRC, ECC u otros mecanismos utilizados.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="2c3c6-478">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-479">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-480">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-482">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,21 "," MIF. \|Matriz de memoria física DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-483">Intervalo, en bytes, en el que se puede resolver el último error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="2c3c6-484">Por ejemplo, si las direcciones de error se resuelven en el bit 11 (es decir, en una página típica), los errores pueden resolverse en límites de 4 KB y esta propiedad se establece en 4000.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="2c3c6-485">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-486">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2c3c6-487">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-489">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-490">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-491">Hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="2c3c6-492">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="2c3c6-493">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-494">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-495">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-496">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-497">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-498">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,16 "," MIF. \|Matriz de memoria física DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-499">Tamaño de la transferencia de datos en bits que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="2c3c6-500">0 (cero) indica que no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="2c3c6-501">Si el valor de la propiedad **errorInfo** es 3 (correcto), esta propiedad se debe establecer en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="2c3c6-502">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-503">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-504">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-505">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-506">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-507">Cantidad máxima de tiempo, en segundos, que las líneas o los cubos sucios pueden permanecer en la memoria caché antes de que se vacíen.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="2c3c6-508">Un valor de 0 (cero) indica que un vaciado de la memoria caché no está controlado por un temporizador de vaciado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="2c3c6-509">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-511">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-512">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-513">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-514">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-514">Date and time the object was installed.</span></span> <span data-ttu-id="2c3c6-515">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2c3c6-516">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-517">**InstalledSize**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-518">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-520">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamaño de SMBIOS \| 7 \| instalado"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-521">Tamaño actual de la memoria caché instalada.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="2c3c6-522">Este valor procede del miembro de **Tamaño instalado** de la estructura de **información de caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-523">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-524">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-525">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-526">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2c3c6-527">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-528">**Level**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-529">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-530">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-531">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-532">Nivel de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-532">Level of the cache.</span></span>

<span data-ttu-id="2c3c6-533">Este valor procede del miembro de **configuración de caché** de la estructura de información de **caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2c3c6-534">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="2c3c6-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="2c3c6-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secundario** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="2c3c6-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terciario** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2c3c6-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-541">**Líneas de cuadrícula**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-542">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-543">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-544">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-545">Tamaño, en bytes, de una sola línea o depósito de caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="2c3c6-546">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-547">**Ubicación**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-548">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-549">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-550">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 7 \| Location")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-551">Ubicación física de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="2c3c6-552">Este valor procede del miembro de **configuración de caché** de la estructura de información de **caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="2c3c6-553">**Interno** (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="2c3c6-554">**Externo** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2c3c6-555">**Reservado** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-556">**Desconocido** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-557">**MaxCacheSize**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-558">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-559">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-560">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tamaño de \| caché máximo 7 de tipo de SMBIOS"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-561">Tamaño máximo de caché instalable en esta memoria caché determinada.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="2c3c6-562">Este valor proviene del miembro **tamaño máximo de la memoria caché** de la estructura de información de **caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-563">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-564">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-565">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-566">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-567">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-567">Label by which the object is known.</span></span> <span data-ttu-id="2c3c6-568">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="2c3c6-569">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-571">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-572">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-573">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-574">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="2c3c6-575">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="2c3c6-576">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="2c3c6-577">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2c3c6-578">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-579">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-580">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-581">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-582">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-583">Cadena de forma libre que proporciona más información si la propiedad **ErrorType** está establecida en 1, otra.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="2c3c6-584">De lo contrario, esta cadena no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="2c3c6-585">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-587">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-588">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-589">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-590">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2c3c6-591">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2c3c6-592">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2c3c6-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-593">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-594">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-595">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-596">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2c3c6-597">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2c3c6-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2c3c6-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2c3c6-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-602">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2c3c6-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-604">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2c3c6-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-606">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="2c3c6-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2c3c6-607">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2c3c6-608">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2c3c6-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-610">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2c3c6-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2c3c6-612">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="2c3c6-612">Timed Power-On Supported</span></span>

<span data-ttu-id="2c3c6-613">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-614">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-615">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-616">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-617">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="2c3c6-618">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="2c3c6-619">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-620">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-621">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-622">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-623">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="2c3c6-624">Este valor procede del miembro **designación de socket** de la estructura de **información de caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2c3c6-625">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-626">**Los**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-627">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-628">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-629">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-630">Directiva que la memoria caché debe emplear para controlar las solicitudes de lectura.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="2c3c6-631">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-632">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-633">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="2c3c6-634">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="2c3c6-635">**Lectura previa** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="2c3c6-636">**Lectura y lectura previa** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="2c3c6-637">**Determinación por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-638">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-639">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-640">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-641">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-642">Para determinar qué líneas de caché o depósitos se deben volver a utilizar.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="2c3c6-643">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-644">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-645">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="2c3c6-646">**Usados menos recientemente (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="2c3c6-647">**Primero en salir (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="2c3c6-648">**Último en salir (LIFO)** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="2c3c6-649">**Uso menos frecuente (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="2c3c6-650">**Usados con mayor frecuencia (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="2c3c6-651">**Varios algoritmos dependientes de datos** (8)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-652">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-653">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-654">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-655">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,3 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-656">Dirección inicial, a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria, para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="2c3c6-657">La dirección de inicio se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="2c3c6-658">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2c3c6-659">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-660">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-661">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-662">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-663">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-664">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-664">Current status of the object.</span></span> <span data-ttu-id="2c3c6-665">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2c3c6-666">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2c3c6-667">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="2c3c6-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2c3c6-668">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2c3c6-669">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2c3c6-670">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2c3c6-671">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c3c6-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2c3c6-672">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2c3c6-673">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2c3c6-674">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-675">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2c3c6-676">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c3c6-677">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2c3c6-678">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2c3c6-679">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2c3c6-680">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2c3c6-681">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2c3c6-682">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2c3c6-683">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-685">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-686">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-687">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-688">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-688">State of the logical device.</span></span> <span data-ttu-id="2c3c6-689">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2c3c6-690">Este valor procede del miembro de **configuración de caché** de la estructura de información de **caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2c3c6-691">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-692">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-693">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2c3c6-694">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2c3c6-695">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2c3c6-696">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-697">**SupportedSRAM**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-698">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-699">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-700">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo \| SRAM compatible con el tipo de SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-701">Matriz de tipos admitidos de memoria de acceso aleatorio estática (SRAM) que se puede usar para la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="2c3c6-702">Este valor procede del miembro de **tipo SRAM compatible** de la estructura de **información de caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-703">**Otro** (0)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-704">**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="2c3c6-705">**Sin ráfagas** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="2c3c6-706">**Ráfaga** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="2c3c6-707">**Ráfaga de canalización** (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="2c3c6-708">**Sincrónico** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="2c3c6-709">**Asincrónico** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c3c6-710">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-711">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-712">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-713">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-714">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="2c3c6-715">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-716">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-717">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-718">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-719">Si es **true**, la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="2c3c6-720">Si es **false**, se trata de una dirección física.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="2c3c6-721">Si la propiedad **errorInfo** es igual a 3, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="2c3c6-722">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-723">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-724">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-725">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-726">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-727">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-727">Name of the scoping system.</span></span>

<span data-ttu-id="2c3c6-728">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c3c6-729">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3c6-730">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-731">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c3c6-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c3c6-732">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="2c3c6-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="2c3c6-733">Escribir la definición de directiva.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-733">Write policy definition.</span></span>

<span data-ttu-id="2c3c6-734">Este valor procede del miembro de **configuración de caché** de la estructura de información de **caché** de la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2c3c6-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2c3c6-735">Esta propiedad se hereda de [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c3c6-736">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c3c6-737">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="2c3c6-738">**Escritura inversa** (3)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="2c3c6-739">**Escritura a través** de (4)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="2c3c6-740">**Varía con la dirección** (5)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="2c3c6-741">**Determinación por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="2c3c6-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="2c3c6-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c3c6-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2c3c6-743">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c3c6-743">Remarks</span></span>

<span data-ttu-id="2c3c6-744">La **clase \_ CacheMemory de Win32** se deriva de [**\_ CacheMemory de CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="2c3c6-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c3c6-745">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c3c6-745">Requirements</span></span>



| <span data-ttu-id="2c3c6-746">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c3c6-746">Requirement</span></span> | <span data-ttu-id="2c3c6-747">Value</span><span class="sxs-lookup"><span data-stu-id="2c3c6-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3c6-748">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c3c6-748">Minimum supported client</span></span><br/> | <span data-ttu-id="2c3c6-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c3c6-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c3c6-750">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c3c6-750">Minimum supported server</span></span><br/> | <span data-ttu-id="2c3c6-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c3c6-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c3c6-752">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c3c6-752">Namespace</span></span><br/>                | <span data-ttu-id="2c3c6-753">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2c3c6-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c3c6-754">MOF</span><span class="sxs-lookup"><span data-stu-id="2c3c6-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c3c6-755"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c3c6-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c3c6-756">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c3c6-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c3c6-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c3c6-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c3c6-758">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c3c6-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c3c6-759">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="2c3c6-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="2c3c6-760">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="2c3c6-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

