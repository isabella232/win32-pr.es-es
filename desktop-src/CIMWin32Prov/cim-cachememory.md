---
description: La \_ clase CIM CacheMemory define las capacidades y la administración de la memoria caché.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: CIM_CacheMemory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907347"
---
# <a name="cim_cachememory-class"></a><span data-ttu-id="5895b-103">\_Clase CacheMemory de CIM</span><span class="sxs-lookup"><span data-stu-id="5895b-103">CIM\_CacheMemory class</span></span>

<span data-ttu-id="5895b-104">La clase **CIM \_ CacheMemory** define las capacidades y la administración de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5895b-104">The **CIM\_CacheMemory** class defines the capabilities and management of cache memory.</span></span>

<span data-ttu-id="5895b-105">La memoria caché es la RAM dedicada o asignada en la que un procesador busca los datos por primera vez.</span><span class="sxs-lookup"><span data-stu-id="5895b-105">Cache memory is the dedicated or allocated RAM where a processor first searches for data.</span></span> <span data-ttu-id="5895b-106">Los datos de la memoria caché se entregan rápidamente al procesador y normalmente se describen por su proximidad al procesador (por ejemplo, caché principal o secundaria).</span><span class="sxs-lookup"><span data-stu-id="5895b-106">Data in cache memory is quickly delivered to the processor and is usually described by its proximity to the processor (for example, primary or secondary cache).</span></span> <span data-ttu-id="5895b-107">Una unidad de disco que incluye la memoria RAM asignada para contener los datos de lectura o adyacentes más recientes del disco (para acelerar la recuperación) también se modela como memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5895b-107">A disk drive that includes RAM allocated for holding the disk's most recently read or adjacent data (to speed up retrieval) is also modeled as cache memory.</span></span>

> [!Note]  
> <span data-ttu-id="5895b-108">La memoria caché no es un búfer de nivel de aplicación o de sistema operativo; se trata de una RAM que se ha asignado para almacenar en caché los datos del procesador.</span><span class="sxs-lookup"><span data-stu-id="5895b-108">Cache memory is not an operating-system or application-level buffer; it is RAM that has been allocated for caching processor data.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="5895b-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5895b-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5895b-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5895b-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5895b-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5895b-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5895b-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5895b-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5895b-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5895b-113">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
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
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="5895b-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="5895b-114">Members</span></span>

<span data-ttu-id="5895b-115">La clase **CIM \_ CacheMemory** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5895b-115">The **CIM\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="5895b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5895b-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="5895b-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5895b-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5895b-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="5895b-118">Methods</span></span>

<span data-ttu-id="5895b-119">La clase **CIM \_ CacheMemory** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5895b-119">The **CIM\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="5895b-120">Método</span><span class="sxs-lookup"><span data-stu-id="5895b-120">Method</span></span>                                                                 | <span data-ttu-id="5895b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5895b-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5895b-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5895b-122">**Reset**</span></span>](reset-method-in-class-cim-cachememory.md)                 | <span data-ttu-id="5895b-123">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5895b-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="5895b-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="5895b-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="5895b-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5895b-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cachememory.md) | <span data-ttu-id="5895b-126">Define el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.</span><span class="sxs-lookup"><span data-stu-id="5895b-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="5895b-127">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="5895b-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5895b-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5895b-128">Properties</span></span>

<span data-ttu-id="5895b-129">La clase **CIM \_ CacheMemory** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5895b-129">The **CIM\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5895b-130">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="5895b-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-133">Describe las propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="5895b-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="5895b-134">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-135">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5895b-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="5895b-136">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="5895b-137">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="5895b-138">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="5895b-139">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="5895b-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-141">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="5895b-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5895b-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,18 "," MIF. \|Matriz de memoria física DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5895b-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5895b-144">Matriz de octetos que contienen información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="5895b-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="5895b-145">Un ejemplo es el síndrome de comprobación y corrección de errores (ECC) o el retorno de los bits de comprobación si se usa una metodología de error basada en CRC.</span><span class="sxs-lookup"><span data-stu-id="5895b-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="5895b-146">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, se puede determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="5895b-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="5895b-147">Este tipo de datos (síndrome ECC, datos de bit de comprobación o de bits de paridad u otra información proporcionada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="5895b-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="5895b-148">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="5895b-149">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-150">**asociatividad**</span><span class="sxs-lookup"><span data-stu-id="5895b-150">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-153">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-154">Enumeración que define la asociatividad de la caché del sistema.</span><span class="sxs-lookup"><span data-stu-id="5895b-154">Enumeration that defines the system cache associativity.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-155">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-156">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-156">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="5895b-157">**Asignación directa** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-157">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5895b-158">**asociativo de conjuntos bidireccionales** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-158">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5895b-159">**asociativo de conjunto de 4 vías** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-159">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="5895b-160">**Totalmente asociativo** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-160">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5895b-161">**asociativa de conjunto de 8 vías** (7)</span><span class="sxs-lookup"><span data-stu-id="5895b-161">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5895b-162">**asociativa de conjunto de 16 vías** (8)</span><span class="sxs-lookup"><span data-stu-id="5895b-162">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-163">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="5895b-163">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-164">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-166">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5895b-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-167">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5895b-167">Availability and status of the device.</span></span>

<span data-ttu-id="5895b-168">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-168">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5895b-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5895b-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5895b-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5895b-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5895b-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="5895b-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5895b-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="5895b-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5895b-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="5895b-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5895b-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5895b-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5895b-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5895b-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5895b-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="5895b-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5895b-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="5895b-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-182">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="5895b-182">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5895b-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="5895b-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-184">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="5895b-184">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5895b-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5895b-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-186">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="5895b-186">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5895b-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="5895b-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5895b-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="5895b-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-189">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5895b-189">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5895b-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5895b-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-191">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="5895b-191">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5895b-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="5895b-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-193">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="5895b-193">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5895b-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5895b-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-195">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="5895b-195">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5895b-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5895b-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-197">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="5895b-197">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-198">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="5895b-198">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-199">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5895b-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-201">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5895b-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-202">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5895b-202">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="5895b-203">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5895b-203">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="5895b-204">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="5895b-204">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="5895b-205">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5895b-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5895b-206">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-207">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="5895b-207">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-210">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-211">Especifica el almacenamiento en caché de instrucciones, el almacenamiento en caché de datos o ambos.</span><span class="sxs-lookup"><span data-stu-id="5895b-211">Specifies instruction caching, data caching, or both.</span></span> <span data-ttu-id="5895b-212">También se pueden definir "otros" y "desconocidos".</span><span class="sxs-lookup"><span data-stu-id="5895b-212">"Other" and "Unknown" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-213">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-213">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-214">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-214">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="5895b-215">**Instrucción** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-215">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="5895b-216">**Datos** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-216">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="5895b-217">**Unificado** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-217">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5895b-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-221">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5895b-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-222">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5895b-222">A short textual description of the object.</span></span>

<span data-ttu-id="5895b-223">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5895b-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-225">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5895b-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-227">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5895b-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-228">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="5895b-228">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5895b-229">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5895b-230">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5895b-230">**This device is working properly.**</span></span> <span data-ttu-id="5895b-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="5895b-231">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5895b-232">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5895b-232">**This device is not configured correctly.**</span></span> <span data-ttu-id="5895b-233">(1)</span><span class="sxs-lookup"><span data-stu-id="5895b-233">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5895b-234">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-234">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5895b-235">(2)</span><span class="sxs-lookup"><span data-stu-id="5895b-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5895b-236">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5895b-236">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5895b-237">(3)</span><span class="sxs-lookup"><span data-stu-id="5895b-237">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5895b-238">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="5895b-238">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5895b-239">(4)</span><span class="sxs-lookup"><span data-stu-id="5895b-239">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5895b-240">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="5895b-240">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5895b-241">(5)</span><span class="sxs-lookup"><span data-stu-id="5895b-241">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5895b-242">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5895b-242">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5895b-243"> (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-243">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5895b-244">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5895b-244">**Cannot filter.**</span></span> <span data-ttu-id="5895b-245">(7)</span><span class="sxs-lookup"><span data-stu-id="5895b-245">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5895b-246">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-246">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5895b-247">(8)</span><span class="sxs-lookup"><span data-stu-id="5895b-247">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5895b-248">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="5895b-248">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5895b-249">(9)</span><span class="sxs-lookup"><span data-stu-id="5895b-249">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5895b-250">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="5895b-250">**This device cannot start.**</span></span> <span data-ttu-id="5895b-251">(10)</span><span class="sxs-lookup"><span data-stu-id="5895b-251">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5895b-252">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-252">**This device failed.**</span></span> <span data-ttu-id="5895b-253">(11)</span><span class="sxs-lookup"><span data-stu-id="5895b-253">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5895b-254">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="5895b-254">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5895b-255">(12)</span><span class="sxs-lookup"><span data-stu-id="5895b-255">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5895b-256">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-256">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5895b-257">(13)</span><span class="sxs-lookup"><span data-stu-id="5895b-257">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5895b-258">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-258">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5895b-259">(14)</span><span class="sxs-lookup"><span data-stu-id="5895b-259">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5895b-260">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="5895b-260">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5895b-261">(15)</span><span class="sxs-lookup"><span data-stu-id="5895b-261">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5895b-262">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-262">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5895b-263">(16)</span><span class="sxs-lookup"><span data-stu-id="5895b-263">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5895b-264">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="5895b-264">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5895b-265">(17)</span><span class="sxs-lookup"><span data-stu-id="5895b-265">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5895b-266">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-266">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5895b-267">(18)</span><span class="sxs-lookup"><span data-stu-id="5895b-267">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5895b-268">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="5895b-268">**Failure using the VxD loader.**</span></span> <span data-ttu-id="5895b-269">(19)</span><span class="sxs-lookup"><span data-stu-id="5895b-269">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5895b-270">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="5895b-270">**Your registry might be corrupted.**</span></span> <span data-ttu-id="5895b-271">(20)</span><span class="sxs-lookup"><span data-stu-id="5895b-271">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5895b-272">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-272">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5895b-273">(21)</span><span class="sxs-lookup"><span data-stu-id="5895b-273">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5895b-274">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5895b-274">**This device is disabled.**</span></span> <span data-ttu-id="5895b-275">(22)</span><span class="sxs-lookup"><span data-stu-id="5895b-275">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5895b-276">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="5895b-276">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5895b-277">(23)</span><span class="sxs-lookup"><span data-stu-id="5895b-277">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5895b-278">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="5895b-278">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5895b-279">(24)</span><span class="sxs-lookup"><span data-stu-id="5895b-279">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5895b-280">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-280">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5895b-281">(25)</span><span class="sxs-lookup"><span data-stu-id="5895b-281">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5895b-282">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-282">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5895b-283">(26)</span><span class="sxs-lookup"><span data-stu-id="5895b-283">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5895b-284">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="5895b-284">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5895b-285">(27)</span><span class="sxs-lookup"><span data-stu-id="5895b-285">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5895b-286">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="5895b-286">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5895b-287">(28)</span><span class="sxs-lookup"><span data-stu-id="5895b-287">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5895b-288">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="5895b-288">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5895b-289">(29)</span><span class="sxs-lookup"><span data-stu-id="5895b-289">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5895b-290">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5895b-290">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5895b-291">(30)</span><span class="sxs-lookup"><span data-stu-id="5895b-291">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5895b-292">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5895b-292">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5895b-293">31</span><span class="sxs-lookup"><span data-stu-id="5895b-293">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5895b-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-295">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5895b-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-297">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5895b-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-298">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5895b-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5895b-299">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-300">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="5895b-300">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-301">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5895b-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-303">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-304">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="5895b-304">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="5895b-305">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-305">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="5895b-306">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-306">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5895b-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-310">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5895b-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5895b-311">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5895b-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5895b-312">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5895b-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5895b-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-314">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5895b-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-317">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5895b-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-318">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5895b-318">A textual description of the object.</span></span>

<span data-ttu-id="5895b-319">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-320">**ID**</span><span class="sxs-lookup"><span data-stu-id="5895b-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-323">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5895b-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5895b-324">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5895b-324">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5895b-325">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-326">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="5895b-326">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-327">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5895b-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-329">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,4 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="5895b-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-330">Dirección final a la que hace referencia una aplicación o un sistema operativo y asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="5895b-330">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="5895b-331">La dirección final se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="5895b-331">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="5895b-332">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5895b-332">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5895b-333">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-333">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-334">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="5895b-334">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-335">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,15 "," MIF. \|Matriz de memoria física DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-338">Operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="5895b-338">Memory access operation that caused the last error.</span></span> <span data-ttu-id="5895b-339">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="5895b-339">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="5895b-340">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-340">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="5895b-341">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-342">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-343">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="5895b-344">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-344">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="5895b-345">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-345">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="5895b-346">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-346">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-347">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="5895b-347">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-348">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5895b-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-350">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,19 "," MIF. \|Dispositivo de memoria DMTF \| 002,20 "," MIF. \|Matriz de memoria física DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-350">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-351">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="5895b-351">Address of the last memory error.</span></span> <span data-ttu-id="5895b-352">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="5895b-352">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="5895b-353">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-353">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="5895b-354">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5895b-354">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5895b-355">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-355">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5895b-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-357">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5895b-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-359">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="5895b-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5895b-360">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-361">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="5895b-361">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-362">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="5895b-362">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5895b-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-364">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,17 "," MIF. \|Matriz de memoria física DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5895b-364">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5895b-365">Datos capturados durante el último acceso erróneo a la memoria.</span><span class="sxs-lookup"><span data-stu-id="5895b-365">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="5895b-366">Los datos ocupan los primeros *n* octetos de la matriz que son necesarios para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="5895b-366">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="5895b-367">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-367">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="5895b-368">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-368">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-369">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="5895b-369">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-370">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-372">Orden de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="5895b-372">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="5895b-373">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-373">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="5895b-374">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-374">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5895b-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-376">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="5895b-376">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="5895b-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-378">Byte menos significativo primero.</span><span class="sxs-lookup"><span data-stu-id="5895b-378">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="5895b-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-380">Byte más significativo en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="5895b-380">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5895b-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-384">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="5895b-384">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5895b-385">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5895b-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-387">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-389">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ memoria de CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="5895b-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-390">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="5895b-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="5895b-391">Los valores 12 a 14 no están definidos en el esquema CIM porque DMI mezcla la semántica del tipo de error y si es corregible.</span><span class="sxs-lookup"><span data-stu-id="5895b-391">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="5895b-392">El hecho de que se corrija un error se indica en la propiedad **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="5895b-392">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<span data-ttu-id="5895b-393">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-395">Otros.</span><span class="sxs-lookup"><span data-stu-id="5895b-395">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-397">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="5895b-397">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5895b-398"><span id="OK"></span><span id="ok"></span>**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-399">Aceptar.</span><span class="sxs-lookup"><span data-stu-id="5895b-399">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="5895b-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-401">Lectura incorrecta.</span><span class="sxs-lookup"><span data-stu-id="5895b-401">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="5895b-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-403">Error de paridad.</span><span class="sxs-lookup"><span data-stu-id="5895b-403">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="5895b-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-405">Error de un bit.</span><span class="sxs-lookup"><span data-stu-id="5895b-405">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="5895b-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="5895b-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-407">Error de doble bit.</span><span class="sxs-lookup"><span data-stu-id="5895b-407">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="5895b-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="5895b-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-409">Error de bits múltiple.</span><span class="sxs-lookup"><span data-stu-id="5895b-409">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="5895b-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="5895b-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-411">Error de recorte.</span><span class="sxs-lookup"><span data-stu-id="5895b-411">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="5895b-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="5895b-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-413">Error de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="5895b-413">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="5895b-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="5895b-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-415">Error de CRC.</span><span class="sxs-lookup"><span data-stu-id="5895b-415">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5895b-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span><span class="sxs-lookup"><span data-stu-id="5895b-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-417">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="5895b-417">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5895b-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (13)</span><span class="sxs-lookup"><span data-stu-id="5895b-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-419">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="5895b-419">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5895b-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span><span class="sxs-lookup"><span data-stu-id="5895b-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-421">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="5895b-421">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-422">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="5895b-422">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-423">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-425">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-426">Indica si se utilizan algoritmos de paridad o CRC, ECC u otros mecanismos.</span><span class="sxs-lookup"><span data-stu-id="5895b-426">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="5895b-427">También se pueden proporcionar detalles sobre el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="5895b-427">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="5895b-428">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-428">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-429">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="5895b-429">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-430">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5895b-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-432">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,21 "," MIF. \|Matriz de memoria física DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5895b-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-433">Especifica el intervalo, en bytes, en el que se puede resolver el último error.</span><span class="sxs-lookup"><span data-stu-id="5895b-433">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="5895b-434">Por ejemplo, si las direcciones de error se resuelven en el bit 11 (es decir, en una página típica), los errores pueden resolverse en límites de 4 KB y esta propiedad se establece en 4000.</span><span class="sxs-lookup"><span data-stu-id="5895b-434">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="5895b-435">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-435">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="5895b-436">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5895b-436">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5895b-437">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-437">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-438">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="5895b-438">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-439">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5895b-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-441">Fecha y hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="5895b-441">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="5895b-442">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="5895b-442">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="5895b-443">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-443">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="5895b-444">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-444">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-445">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="5895b-445">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-446">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5895b-446">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-448">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,16 "," MIF. \|Matriz de memoria física DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="5895b-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-449">Tamaño de la transferencia de datos, en bits, que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="5895b-449">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="5895b-450">Un valor de 0 indica que no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="5895b-450">A value of 0 indicates no error.</span></span> <span data-ttu-id="5895b-451">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="5895b-451">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

<span data-ttu-id="5895b-452">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-452">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-453">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="5895b-453">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-454">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5895b-454">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-456">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="5895b-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-457">Cantidad máxima de tiempo, en segundos, que las líneas o los cubos sucios pueden permanecer en la memoria caché antes de que se vacíen.</span><span class="sxs-lookup"><span data-stu-id="5895b-457">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="5895b-458">Un valor de 0 indica que un volcado de memoria caché no está controlado por un temporizador de vaciado.</span><span class="sxs-lookup"><span data-stu-id="5895b-458">A value of 0 indicates that a cache flush is not controlled by a flushing timer.</span></span>

</dd> <dt>

<span data-ttu-id="5895b-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5895b-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-460">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5895b-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-461">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-462">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5895b-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-463">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5895b-463">Indicates when the object was installed.</span></span> <span data-ttu-id="5895b-464">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="5895b-464">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5895b-465">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-466">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5895b-466">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-467">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5895b-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-469">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5895b-469">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5895b-470">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-471">**Level**</span><span class="sxs-lookup"><span data-stu-id="5895b-471">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-472">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-473">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-474">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-475">Especifica si se trata de la caché primaria, secundaria o terciaria.</span><span class="sxs-lookup"><span data-stu-id="5895b-475">Specifies whether this is the primary, secondary or tertiary cache.</span></span> <span data-ttu-id="5895b-476">También se pueden definir "otro", "desconocido" y "no aplicable".</span><span class="sxs-lookup"><span data-stu-id="5895b-476">"Other", "Unknown", and "Not Applicable" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-478">Otros.</span><span class="sxs-lookup"><span data-stu-id="5895b-478">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-480">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="5895b-480">Unknown.</span></span>

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="5895b-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-482">Principal.</span><span class="sxs-lookup"><span data-stu-id="5895b-482">Primary.</span></span>

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="5895b-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secundario** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-484">Secundaria.</span><span class="sxs-lookup"><span data-stu-id="5895b-484">Secondary.</span></span>

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="5895b-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terciario** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-486">Terciaria.</span><span class="sxs-lookup"><span data-stu-id="5895b-486">Tertiary.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5895b-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-488">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="5895b-488">Not applicable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-489">**Líneas de cuadrícula**</span><span class="sxs-lookup"><span data-stu-id="5895b-489">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-490">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5895b-490">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-491">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-492">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5895b-492">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-493">Tamaño, en bytes, de una sola línea o depósito de caché.</span><span class="sxs-lookup"><span data-stu-id="5895b-493">Size, in bytes, of a single cache bucket or line.</span></span>

</dd> <dt>

<span data-ttu-id="5895b-494">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5895b-494">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-495">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-496">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-497">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5895b-497">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-498">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5895b-498">Label by which the object is known.</span></span> <span data-ttu-id="5895b-499">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5895b-499">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5895b-500">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-500">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-501">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="5895b-501">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-502">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5895b-502">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-503">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-504">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="5895b-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-505">Número de bloques consecutivos, cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5895b-505">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="5895b-506">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5895b-506">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="5895b-507">Si el valor de **blocksize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5895b-507">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="5895b-508">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5895b-508">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5895b-509">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-509">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-510">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5895b-510">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-511">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-512">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-513">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="5895b-513">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-514">Cadena de forma libre que proporciona información si la propiedad de **ErrorType** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="5895b-514">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="5895b-515">Si no se establece en 1, esta cadena no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-515">If it is not set to 1, then this string has no meaning.</span></span>

<span data-ttu-id="5895b-516">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-516">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-517">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5895b-517">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-518">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-520">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5895b-520">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-521">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5895b-521">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5895b-522">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5895b-522">Example: "\*PNP030b"</span></span>

<span data-ttu-id="5895b-523">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-524">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5895b-524">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-525">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-525">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5895b-526">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-527">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5895b-527">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="5895b-528">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5895b-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-530">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="5895b-530">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5895b-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-532">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5895b-532">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5895b-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-534">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="5895b-534">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5895b-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-536">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5895b-536">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5895b-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-538">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="5895b-538">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5895b-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-540">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="5895b-540">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="5895b-541">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="5895b-541">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="5895b-542">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5895b-542">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5895b-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-544">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="5895b-544">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5895b-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="5895b-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-546">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="5895b-546">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-547">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5895b-547">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-548">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5895b-548">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-549">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-550">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5895b-550">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5895b-551">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5895b-551">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5895b-552">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="5895b-552">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5895b-553">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5895b-553">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5895b-554">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-554">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-555">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="5895b-555">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-556">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-557">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-557">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-558">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="5895b-558">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="5895b-559">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-559">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-560">**Los**</span><span class="sxs-lookup"><span data-stu-id="5895b-560">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-561">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-562">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-563">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-563">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-564">Directiva empleada por la memoria caché para controlar las solicitudes de lectura.</span><span class="sxs-lookup"><span data-stu-id="5895b-564">Policy employed by the cache for handling read requests.</span></span> <span data-ttu-id="5895b-565">Si la Directiva de lectura se determina individualmente, es decir, para cada solicitud, se debe especificar el valor 6 ("determinación por e/s").</span><span class="sxs-lookup"><span data-stu-id="5895b-565">If the read policy is determined individually, that is, for each request, then the value 6 ("Determination per I/O") should be specified.</span></span> <span data-ttu-id="5895b-566">"Otros" y "desconocidos" también son valores válidos.</span><span class="sxs-lookup"><span data-stu-id="5895b-566">"Other" and "Unknown" are also valid values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-568">Otros.</span><span class="sxs-lookup"><span data-stu-id="5895b-568">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-570">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="5895b-570">Unknown.</span></span>

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="5895b-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-572">Lectura.</span><span class="sxs-lookup"><span data-stu-id="5895b-572">Read.</span></span>

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="5895b-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Lectura previa** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-574">Lectura previa.</span><span class="sxs-lookup"><span data-stu-id="5895b-574">Read-ahead.</span></span>

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="5895b-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Lectura y lectura previa** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read and Read-Ahead** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-576">Lectura y lectura previa.</span><span class="sxs-lookup"><span data-stu-id="5895b-576">Read and read-ahead.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="5895b-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinación por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-578">Determinación por e/s.</span><span class="sxs-lookup"><span data-stu-id="5895b-578">Determination per I/O.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-579">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="5895b-579">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-580">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-580">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-581">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-582">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-583">Enumeración de enteros que describe el algoritmo que determina qué líneas de caché o depósitos se deben volver a utilizar.</span><span class="sxs-lookup"><span data-stu-id="5895b-583">Integer enumeration describing the algorithm that determines which cache lines or buckets should be re-used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-585">Otros.</span><span class="sxs-lookup"><span data-stu-id="5895b-585">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-587">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="5895b-587">Unknown.</span></span>

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="5895b-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Usados menos recientemente (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-589">Usado menos recientemente (LRU).</span><span class="sxs-lookup"><span data-stu-id="5895b-589">Least recently used (LRU).</span></span>

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="5895b-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**Primero en salir (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-591">Primero en salir, primero en salir (FIFO).</span><span class="sxs-lookup"><span data-stu-id="5895b-591">First-in, first-out (FIFO).</span></span>

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="5895b-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Último en salir (LIFO)** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-593">Último en salir, primero en salir (LIFO).</span><span class="sxs-lookup"><span data-stu-id="5895b-593">Last-in, first-out (LIFO).</span></span>

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="5895b-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Uso menos frecuente (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-595">Usados con menos frecuencia (LFU).</span><span class="sxs-lookup"><span data-stu-id="5895b-595">Least frequently used (LFU.)</span></span>

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="5895b-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Usados con mayor frecuencia (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="5895b-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-597">Usados con mayor frecuencia (MFU).</span><span class="sxs-lookup"><span data-stu-id="5895b-597">Most frequently used (MFU).</span></span>

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="5895b-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Varios algoritmos dependientes de datos** (8)</span><span class="sxs-lookup"><span data-stu-id="5895b-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-599">Varios algoritmos dependientes de datos.</span><span class="sxs-lookup"><span data-stu-id="5895b-599">Data-dependent multiple algorithms.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-600">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="5895b-600">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-601">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5895b-601">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-602">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-603">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,3 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="5895b-603">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-604">Dirección inicial, a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria, para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="5895b-604">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="5895b-605">La dirección de inicio se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="5895b-605">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="5895b-606">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5895b-606">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5895b-607">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-607">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-608">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5895b-608">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-609">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-609">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-610">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-610">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-611">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5895b-611">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-612">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5895b-612">String that indicates the current status of the object.</span></span> <span data-ttu-id="5895b-613">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="5895b-613">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5895b-614">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="5895b-614">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5895b-615">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="5895b-615">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5895b-616">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="5895b-616">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5895b-617">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="5895b-617">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5895b-618">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="5895b-618">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5895b-619">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-619">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5895b-620">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5895b-620">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5895b-621">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5895b-621">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5895b-622">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5895b-622">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5895b-623">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5895b-623">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-624">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5895b-624">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5895b-625">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5895b-625">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5895b-626">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5895b-626">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5895b-627">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5895b-627">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5895b-628">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5895b-628">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5895b-629">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5895b-629">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5895b-630">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5895b-630">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5895b-631">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5895b-631">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5895b-632">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5895b-632">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-633">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5895b-633">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-634">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-634">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-635">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-636">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-637">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5895b-637">State of the logical device.</span></span> <span data-ttu-id="5895b-638">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="5895b-638">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="5895b-639">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-640">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-640">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-641">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-641">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5895b-642">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-642">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5895b-643">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-643">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5895b-644">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-644">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5895b-645">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5895b-645">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-646">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-647">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-648">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5895b-648">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5895b-649">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5895b-649">The scoping system's creation class name.</span></span>

<span data-ttu-id="5895b-650">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-650">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-651">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="5895b-651">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-652">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5895b-652">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-653">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-653">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5895b-654">Indica si la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema (**true**) o una dirección física (**false**).</span><span class="sxs-lookup"><span data-stu-id="5895b-654">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="5895b-655">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="5895b-655">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="5895b-656">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-656">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-657">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5895b-657">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-658">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5895b-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-659">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-659">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-660">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5895b-660">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5895b-661">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5895b-661">The scoping system's name.</span></span>

<span data-ttu-id="5895b-662">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-662">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5895b-663">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="5895b-663">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895b-664">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5895b-664">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5895b-665">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5895b-665">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895b-666">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caché del sistema DMTF \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="5895b-666">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="5895b-667">Define si la memoria caché es de reescritura o de escritura a través, o si la información "varía con dirección" o se define individualmente para cada entrada/salida.</span><span class="sxs-lookup"><span data-stu-id="5895b-667">Defines whether the cache is write-back or write-through, or whether the information "Varies with Address" or is defined individually for each input/output.</span></span> <span data-ttu-id="5895b-668">También se pueden especificar "otros" y "desconocidos".</span><span class="sxs-lookup"><span data-stu-id="5895b-668">"Other" and "Unknown" also can be specified.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5895b-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5895b-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-670">Otros.</span><span class="sxs-lookup"><span data-stu-id="5895b-670">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5895b-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5895b-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-672">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="5895b-672">Unknown.</span></span>

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="5895b-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Escritura inversa** (3)</span><span class="sxs-lookup"><span data-stu-id="5895b-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write Back** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-674">Escritura inversa.</span><span class="sxs-lookup"><span data-stu-id="5895b-674">Write back.</span></span>

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="5895b-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Escritura a través** de (4)</span><span class="sxs-lookup"><span data-stu-id="5895b-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Write Through** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-676">Escritura a través de.</span><span class="sxs-lookup"><span data-stu-id="5895b-676">Write through.</span></span>

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="5895b-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varía con la dirección** (5)</span><span class="sxs-lookup"><span data-stu-id="5895b-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varies with Address** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-678">Varía con la dirección.</span><span class="sxs-lookup"><span data-stu-id="5895b-678">Varies with address.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="5895b-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinación por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="5895b-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5895b-680">Determinación por e/s.</span><span class="sxs-lookup"><span data-stu-id="5895b-680">Determination per I/O.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5895b-681">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5895b-681">Remarks</span></span>

<span data-ttu-id="5895b-682">La clase **CIM \_ CacheMemory** se deriva de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-682">The **CIM\_CacheMemory** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="5895b-683">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5895b-683">WMI does not implement this class.</span></span> <span data-ttu-id="5895b-684">Para obtener más información sobre las clases derivadas de **CIM \_ CacheMemory**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-684">For more information about classes derived from **CIM\_CacheMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5895b-685">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5895b-685">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5895b-686">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5895b-686">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5895b-687">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5895b-687">Requirements</span></span>



| <span data-ttu-id="5895b-688">Requisito</span><span class="sxs-lookup"><span data-stu-id="5895b-688">Requirement</span></span> | <span data-ttu-id="5895b-689">Value</span><span class="sxs-lookup"><span data-stu-id="5895b-689">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5895b-690">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5895b-690">Minimum supported client</span></span><br/> | <span data-ttu-id="5895b-691">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5895b-691">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5895b-692">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5895b-692">Minimum supported server</span></span><br/> | <span data-ttu-id="5895b-693">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5895b-693">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5895b-694">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5895b-694">Namespace</span></span><br/>                | <span data-ttu-id="5895b-695">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5895b-695">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5895b-696">MOF</span><span class="sxs-lookup"><span data-stu-id="5895b-696">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5895b-697"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5895b-697"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5895b-698">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5895b-698">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5895b-699"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5895b-699"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5895b-700">Vea también</span><span class="sxs-lookup"><span data-stu-id="5895b-700">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5895b-701">**Memoria de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5895b-701">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

