---
description: La \_ clase CIM NonVolatileStorage representa las capacidades y la administración de almacenamiento no volátil. La memoria no volátil incluye de forma nativa el almacenamiento en Flash y ROM.
ms.assetid: 39158b31-31f7-460c-aef1-1ca423badad6
ms.tgt_platform: multiple
title: CIM_NonVolatileStorage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage
- CIM_NonVolatileStorage.Access
- CIM_NonVolatileStorage.AdditionalErrorData
- CIM_NonVolatileStorage.Availability
- CIM_NonVolatileStorage.BlockSize
- CIM_NonVolatileStorage.Caption
- CIM_NonVolatileStorage.ConfigManagerErrorCode
- CIM_NonVolatileStorage.ConfigManagerUserConfig
- CIM_NonVolatileStorage.CorrectableError
- CIM_NonVolatileStorage.CreationClassName
- CIM_NonVolatileStorage.Description
- CIM_NonVolatileStorage.DeviceID
- CIM_NonVolatileStorage.EndingAddress
- CIM_NonVolatileStorage.ErrorAccess
- CIM_NonVolatileStorage.ErrorAddress
- CIM_NonVolatileStorage.ErrorCleared
- CIM_NonVolatileStorage.ErrorData
- CIM_NonVolatileStorage.ErrorDataOrder
- CIM_NonVolatileStorage.ErrorDescription
- CIM_NonVolatileStorage.ErrorInfo
- CIM_NonVolatileStorage.ErrorMethodology
- CIM_NonVolatileStorage.ErrorResolution
- CIM_NonVolatileStorage.ErrorTime
- CIM_NonVolatileStorage.ErrorTransferSize
- CIM_NonVolatileStorage.InstallDate
- CIM_NonVolatileStorage.IsWriteable
- CIM_NonVolatileStorage.LastErrorCode
- CIM_NonVolatileStorage.Name
- CIM_NonVolatileStorage.NumberOfBlocks
- CIM_NonVolatileStorage.OtherErrorDescription
- CIM_NonVolatileStorage.PNPDeviceID
- CIM_NonVolatileStorage.PowerManagementCapabilities
- CIM_NonVolatileStorage.PowerManagementSupported
- CIM_NonVolatileStorage.Purpose
- CIM_NonVolatileStorage.StartingAddress
- CIM_NonVolatileStorage.Status
- CIM_NonVolatileStorage.StatusInfo
- CIM_NonVolatileStorage.SystemCreationClassName
- CIM_NonVolatileStorage.SystemLevelAddress
- CIM_NonVolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fca29f0b279994dc0b844127fd1925850094da8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907044"
---
# <a name="cim_nonvolatilestorage-class"></a><span data-ttu-id="27b43-104">\_Clase NonVolatileStorage de CIM</span><span class="sxs-lookup"><span data-stu-id="27b43-104">CIM\_NonVolatileStorage class</span></span>

<span data-ttu-id="27b43-105">La clase **CIM \_ NonVolatileStorage** representa las capacidades y la administración de almacenamiento no volátil.</span><span class="sxs-lookup"><span data-stu-id="27b43-105">The **CIM\_NonVolatileStorage** class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="27b43-106">La memoria no volátil incluye de forma nativa el almacenamiento en Flash y ROM.</span><span class="sxs-lookup"><span data-stu-id="27b43-106">Nonvolatile memory natively includes flash and ROM storage.</span></span> <span data-ttu-id="27b43-107">Además, la memoria no volátil puede basarse en el almacenamiento volátil, si la memoria volátil está respaldada por una batería.</span><span class="sxs-lookup"><span data-stu-id="27b43-107">In addition, nonvolatile memory can be based on volatile storage, if the volatile memory is backed by a battery.</span></span> <span data-ttu-id="27b43-108">Por ejemplo, este escenario lo describiría una instancia de la relación [**\_ AssociatedBattery de CIM**](cim-associatedbattery.md) que hace referencia al almacenamiento no volátil como **dependiente** y la batería como **antecedente**, y una instancia de la [**relación \_ basada en CIM**](cim-basedon.md) que hace referencia al almacenamiento no volátil como el almacenamiento **dependiente** y el almacenamiento volátil como el **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="27b43-108">For example, this scenario would be described by an instance of the [**CIM\_AssociatedBattery**](cim-associatedbattery.md) relationship that references the nonvolatile storage as the **Dependent** and the battery as the **Antecedent**; and an instance of the [**CIM\_BasedOn**](cim-basedon.md) relationship that references the non-volatile storage as the **Dependent** and the volatile storage as the **Antecedent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27b43-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="27b43-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="27b43-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="27b43-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="27b43-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="27b43-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="27b43-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="27b43-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b43-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27b43-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{18074AFA-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_NonVolatileStorage : CIM_Memory
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
  boolean  IsWriteable;
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

## <a name="members"></a><span data-ttu-id="27b43-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="27b43-114">Members</span></span>

<span data-ttu-id="27b43-115">La clase **CIM \_ NonVolatileStorage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="27b43-115">The **CIM\_NonVolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="27b43-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="27b43-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="27b43-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27b43-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="27b43-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="27b43-118">Methods</span></span>

<span data-ttu-id="27b43-119">La clase **CIM \_ NonVolatileStorage** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="27b43-119">The **CIM\_NonVolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="27b43-120">Método</span><span class="sxs-lookup"><span data-stu-id="27b43-120">Method</span></span>                                                                        | <span data-ttu-id="27b43-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="27b43-121">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27b43-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="27b43-122">**Reset**</span></span>](reset-method-in-class-cim-nonvolatilestorage.md)                 | <span data-ttu-id="27b43-123">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="27b43-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="27b43-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="27b43-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="27b43-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="27b43-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-nonvolatilestorage.md) | <span data-ttu-id="27b43-126">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="27b43-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="27b43-127">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="27b43-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="27b43-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27b43-128">Properties</span></span>

<span data-ttu-id="27b43-129">La clase **CIM \_ NonVolatileStorage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="27b43-129">The **CIM\_NonVolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27b43-130">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="27b43-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27b43-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-133">Propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="27b43-133">Read/write properties of the media.</span></span>

<span data-ttu-id="27b43-134">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-135">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="27b43-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="27b43-136">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="27b43-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="27b43-137">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="27b43-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="27b43-138">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="27b43-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="27b43-139">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="27b43-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="27b43-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-141">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="27b43-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="27b43-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,18 "," MIF. \|Matriz de memoria física DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="27b43-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="27b43-144">Matriz de octetos que contienen información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="27b43-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="27b43-145">Un ejemplo es el síndrome de comprobación y corrección de errores (ECC) o el retorno de los bits de comprobación si se usa una metodología de error basada en CRC.</span><span class="sxs-lookup"><span data-stu-id="27b43-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="27b43-146">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, se puede determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="27b43-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="27b43-147">Este tipo de datos (síndrome ECC, datos de bit de comprobación o de bits de paridad u otra información proporcionada por el proveedor) se incluye en este campo.</span><span class="sxs-lookup"><span data-stu-id="27b43-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="27b43-148">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="27b43-149">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-150">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="27b43-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27b43-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-153">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="27b43-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-154">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-154">Availability and status of the device.</span></span>

<span data-ttu-id="27b43-155">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-155">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27b43-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="27b43-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="27b43-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="27b43-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="27b43-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="27b43-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="27b43-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="27b43-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="27b43-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="27b43-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="27b43-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="27b43-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="27b43-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="27b43-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="27b43-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="27b43-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="27b43-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="27b43-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="27b43-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="27b43-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="27b43-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="27b43-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="27b43-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="27b43-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="27b43-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-169">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="27b43-169">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="27b43-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="27b43-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-171">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="27b43-171">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="27b43-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="27b43-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-173">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="27b43-173">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="27b43-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="27b43-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="27b43-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="27b43-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-176">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="27b43-176">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="27b43-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="27b43-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-178">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="27b43-178">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="27b43-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="27b43-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-180">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="27b43-180">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="27b43-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="27b43-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-182">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="27b43-182">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="27b43-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="27b43-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-184">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="27b43-184">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-185">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="27b43-185">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-186">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27b43-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-188">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="27b43-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-189">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="27b43-189">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="27b43-190">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="27b43-190">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="27b43-191">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="27b43-191">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter 1 (one).</span></span>

<span data-ttu-id="27b43-192">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-192">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="27b43-193">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="27b43-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-194">**Caption**</span><span class="sxs-lookup"><span data-stu-id="27b43-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-197">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="27b43-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-198">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="27b43-198">Short textual description of the object.</span></span>

<span data-ttu-id="27b43-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-200">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="27b43-200">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27b43-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-203">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27b43-203">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-204">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="27b43-204">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="27b43-205">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-205">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="27b43-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="27b43-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="27b43-207"> (0)</span><span class="sxs-lookup"><span data-stu-id="27b43-207">(0)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-208">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="27b43-208">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="27b43-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="27b43-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="27b43-210">(1)</span><span class="sxs-lookup"><span data-stu-id="27b43-210">(1)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-211">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="27b43-211">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27b43-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="27b43-213">(2)</span><span class="sxs-lookup"><span data-stu-id="27b43-213">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="27b43-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="27b43-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="27b43-215">(3)</span><span class="sxs-lookup"><span data-stu-id="27b43-215">(3)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-216">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="27b43-216">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="27b43-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="27b43-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="27b43-218">(4)</span><span class="sxs-lookup"><span data-stu-id="27b43-218">(4)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-219">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="27b43-219">Device is not working properly.</span></span> <span data-ttu-id="27b43-220">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="27b43-220">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="27b43-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="27b43-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="27b43-222">(5)</span><span class="sxs-lookup"><span data-stu-id="27b43-222">(5)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-223">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="27b43-223">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="27b43-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="27b43-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="27b43-225"> (6)</span><span class="sxs-lookup"><span data-stu-id="27b43-225">(6)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-226">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="27b43-226">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="27b43-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="27b43-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="27b43-228">(7)</span><span class="sxs-lookup"><span data-stu-id="27b43-228">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="27b43-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="27b43-230">(8)</span><span class="sxs-lookup"><span data-stu-id="27b43-230">(8)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-231">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-231">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="27b43-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="27b43-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="27b43-233">(9)</span><span class="sxs-lookup"><span data-stu-id="27b43-233">(9)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-234">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-234">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="27b43-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="27b43-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="27b43-236">(10)</span><span class="sxs-lookup"><span data-stu-id="27b43-236">(10)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-237">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="27b43-237">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="27b43-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="27b43-239">(11)</span><span class="sxs-lookup"><span data-stu-id="27b43-239">(11)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-240">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-240">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="27b43-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="27b43-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="27b43-242">(12)</span><span class="sxs-lookup"><span data-stu-id="27b43-242">(12)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-243">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="27b43-243">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="27b43-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="27b43-245">(13)</span><span class="sxs-lookup"><span data-stu-id="27b43-245">(13)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-246">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-246">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="27b43-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="27b43-248">(14)</span><span class="sxs-lookup"><span data-stu-id="27b43-248">(14)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-249">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="27b43-249">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="27b43-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="27b43-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="27b43-251">(15)</span><span class="sxs-lookup"><span data-stu-id="27b43-251">(15)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-252">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="27b43-252">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="27b43-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="27b43-254">(16)</span><span class="sxs-lookup"><span data-stu-id="27b43-254">(16)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-255">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-255">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="27b43-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="27b43-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="27b43-257">(17)</span><span class="sxs-lookup"><span data-stu-id="27b43-257">(17)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-258">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="27b43-258">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27b43-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="27b43-260">(18)</span><span class="sxs-lookup"><span data-stu-id="27b43-260">(18)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-261">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="27b43-261">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="27b43-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="27b43-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="27b43-263">(19)</span><span class="sxs-lookup"><span data-stu-id="27b43-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="27b43-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="27b43-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="27b43-265">(20)</span><span class="sxs-lookup"><span data-stu-id="27b43-265">(20)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-266">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="27b43-266">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="27b43-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="27b43-268">(21)</span><span class="sxs-lookup"><span data-stu-id="27b43-268">(21)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-269">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="27b43-269">System failure.</span></span> <span data-ttu-id="27b43-270">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="27b43-270">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="27b43-271">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-271">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="27b43-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="27b43-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="27b43-273">(22)</span><span class="sxs-lookup"><span data-stu-id="27b43-273">(22)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-274">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="27b43-274">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="27b43-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="27b43-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="27b43-276">(23)</span><span class="sxs-lookup"><span data-stu-id="27b43-276">(23)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-277">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="27b43-277">System failure.</span></span> <span data-ttu-id="27b43-278">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="27b43-278">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="27b43-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="27b43-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="27b43-280">(24)</span><span class="sxs-lookup"><span data-stu-id="27b43-280">(24)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-281">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="27b43-281">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="27b43-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="27b43-283">(25)</span><span class="sxs-lookup"><span data-stu-id="27b43-283">(25)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-284">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="27b43-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="27b43-286">(26)</span><span class="sxs-lookup"><span data-stu-id="27b43-286">(26)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-287">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27b43-287">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="27b43-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="27b43-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="27b43-289">(27)</span><span class="sxs-lookup"><span data-stu-id="27b43-289">(27)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-290">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="27b43-290">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="27b43-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="27b43-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="27b43-292">(28)</span><span class="sxs-lookup"><span data-stu-id="27b43-292">(28)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-293">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="27b43-293">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="27b43-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="27b43-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="27b43-295">(29)</span><span class="sxs-lookup"><span data-stu-id="27b43-295">(29)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-296">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="27b43-296">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="27b43-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="27b43-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="27b43-298">(30)</span><span class="sxs-lookup"><span data-stu-id="27b43-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-299">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="27b43-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27b43-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="27b43-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="27b43-301">31</span><span class="sxs-lookup"><span data-stu-id="27b43-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-302">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="27b43-302">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-303">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="27b43-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-304">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="27b43-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-306">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27b43-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-307">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="27b43-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="27b43-308">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-309">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="27b43-309">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-310">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="27b43-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-312">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="27b43-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-313">Si **es true**, el error más reciente se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="27b43-313">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="27b43-314">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-314">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="27b43-315">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-315">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="27b43-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-319">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27b43-319">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27b43-320">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="27b43-320">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="27b43-321">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="27b43-321">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="27b43-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-323">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27b43-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-326">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="27b43-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-327">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="27b43-327">Textual description of the object.</span></span>

<span data-ttu-id="27b43-328">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-329">**ID**</span><span class="sxs-lookup"><span data-stu-id="27b43-329">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-332">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27b43-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27b43-333">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="27b43-333">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="27b43-334">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-335">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="27b43-335">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-336">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27b43-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-338">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,4 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="27b43-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-339">Dirección final, a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria para el objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="27b43-339">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="27b43-340">La dirección final se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="27b43-340">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="27b43-341">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="27b43-342">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="27b43-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-343">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="27b43-343">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27b43-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-346">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,15 "," MIF. \|Matriz de memoria física DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="27b43-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-347">Enumeración que indica la operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="27b43-347">Enumeration that indicates the memory access operation that caused the last error.</span></span> <span data-ttu-id="27b43-348">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="27b43-348">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="27b43-349">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-349">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="27b43-350">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-350">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27b43-351">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="27b43-351">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-352">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="27b43-352">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="27b43-353">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="27b43-353">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="27b43-354">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="27b43-354">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="27b43-355">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="27b43-355">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-356">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="27b43-356">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-357">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27b43-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-359">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,19 "," MIF. \|Dispositivo de memoria DMTF \| 002,20 "," MIF. \|Matriz de memoria física DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="27b43-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-360">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="27b43-360">Address of the last memory error.</span></span> <span data-ttu-id="27b43-361">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="27b43-361">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="27b43-362">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-362">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="27b43-363">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-363">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="27b43-364">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="27b43-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="27b43-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-366">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="27b43-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-368">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="27b43-368">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="27b43-369">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-370">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="27b43-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-371">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="27b43-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="27b43-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-373">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,17 "," MIF. \|Matriz de memoria física DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="27b43-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="27b43-374">Datos capturados durante el último acceso erróneo a la memoria.</span><span class="sxs-lookup"><span data-stu-id="27b43-374">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="27b43-375">Los datos ocupan los primeros *n* octetos de la matriz que son necesarios para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="27b43-375">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="27b43-376">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-376">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="27b43-377">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-377">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="27b43-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-379">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27b43-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-381">Ordenación de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="27b43-381">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="27b43-382">Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-382">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="27b43-383">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-383">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-384">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="27b43-384">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="27b43-385">**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="27b43-385">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="27b43-386">**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="27b43-386">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-387">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="27b43-387">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-390">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="27b43-390">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="27b43-391">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-392">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="27b43-392">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-393">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27b43-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-395">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ memoria de CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="27b43-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-396">Tipo de error que se produjo más recientemente.</span><span class="sxs-lookup"><span data-stu-id="27b43-396">Type of error that occurred most recently.</span></span> <span data-ttu-id="27b43-397">Los valores 12 a 14 no están definidos en el esquema CIM porque DMI mezcla la semántica del tipo de error y si es corregible.</span><span class="sxs-lookup"><span data-stu-id="27b43-397">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="27b43-398">El hecho de que se corrija un error se indica en la propiedad **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="27b43-398">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span> <span data-ttu-id="27b43-399">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27b43-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="27b43-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-401">Otros.</span><span class="sxs-lookup"><span data-stu-id="27b43-401">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="27b43-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-403">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="27b43-403">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="27b43-404"><span id="OK"></span><span id="ok"></span>**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="27b43-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-405">Aceptar.</span><span class="sxs-lookup"><span data-stu-id="27b43-405">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="27b43-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="27b43-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-407">Lectura incorrecta.</span><span class="sxs-lookup"><span data-stu-id="27b43-407">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="27b43-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="27b43-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-409">Error de paridad.</span><span class="sxs-lookup"><span data-stu-id="27b43-409">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="27b43-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="27b43-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-411">Error de un bit.</span><span class="sxs-lookup"><span data-stu-id="27b43-411">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="27b43-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="27b43-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-413">Error de doble bit.</span><span class="sxs-lookup"><span data-stu-id="27b43-413">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="27b43-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="27b43-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-415">Error de bits múltiple.</span><span class="sxs-lookup"><span data-stu-id="27b43-415">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="27b43-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="27b43-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-417">Error de recorte.</span><span class="sxs-lookup"><span data-stu-id="27b43-417">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="27b43-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="27b43-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-419">Error de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="27b43-419">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="27b43-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="27b43-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-421">Error de CRC.</span><span class="sxs-lookup"><span data-stu-id="27b43-421">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="27b43-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span><span class="sxs-lookup"><span data-stu-id="27b43-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-423">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="27b43-423">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="27b43-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (13)</span><span class="sxs-lookup"><span data-stu-id="27b43-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-425">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="27b43-425">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="27b43-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span><span class="sxs-lookup"><span data-stu-id="27b43-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-427">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="27b43-427">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-428">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="27b43-428">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-429">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-431">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="27b43-431">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-432">Especifica si se utilizan algoritmos de paridad, algoritmos de CRC, ECC u otros mecanismos.</span><span class="sxs-lookup"><span data-stu-id="27b43-432">Specifies whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used.</span></span> <span data-ttu-id="27b43-433">También se pueden proporcionar detalles sobre el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="27b43-433">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="27b43-434">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-434">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-435">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="27b43-435">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-436">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27b43-436">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-438">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,21 "," MIF. \|Matriz de memoria física DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="27b43-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-439">Intervalo, en bytes, en el que se puede resolver el último error.</span><span class="sxs-lookup"><span data-stu-id="27b43-439">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="27b43-440">Por ejemplo, si las direcciones de error se resuelven en el bit 11 (es decir, en una página típica), los errores pueden resolverse en límites de 4 KB y esta propiedad se establece en 4000.</span><span class="sxs-lookup"><span data-stu-id="27b43-440">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="27b43-441">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-441">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="27b43-442">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="27b43-443">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="27b43-443">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-444">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="27b43-444">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-445">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="27b43-445">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-447">Hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="27b43-447">Time that the last memory error occurred.</span></span> <span data-ttu-id="27b43-448">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="27b43-448">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="27b43-449">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-449">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="27b43-450">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-450">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-451">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="27b43-451">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-452">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27b43-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-454">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,16 "," MIF. \|Matriz de memoria física DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="27b43-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-455">Tamaño de la transferencia de datos, en bits, que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="27b43-455">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="27b43-456">Un valor de 0 (cero) indica que no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="27b43-456">A value of 0 (zero) indicates no error.</span></span> <span data-ttu-id="27b43-457">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad se debe establecer en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="27b43-457">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="27b43-458">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="27b43-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-460">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="27b43-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-461">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-462">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="27b43-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-463">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="27b43-463">Date and time the object was installed.</span></span> <span data-ttu-id="27b43-464">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="27b43-464">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="27b43-465">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-466">**IsWriteable**</span><span class="sxs-lookup"><span data-stu-id="27b43-466">**IsWriteable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-467">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="27b43-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-469">Si es **true**, el almacenamiento no volátil es grabable.</span><span class="sxs-lookup"><span data-stu-id="27b43-469">If **TRUE**, non-volatile storage is writeable.</span></span>

</dd> <dt>

<span data-ttu-id="27b43-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="27b43-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-471">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27b43-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-473">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="27b43-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="27b43-474">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-475">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="27b43-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-476">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-478">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="27b43-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-479">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="27b43-479">Label by which the object is known.</span></span> <span data-ttu-id="27b43-480">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="27b43-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="27b43-481">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="27b43-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-483">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27b43-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-484">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-485">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="27b43-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-486">Número total de bloques consecutivos; cada bloque es el tamaño del valor contenido en la propiedad **blocksize** , que constituye la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="27b43-486">Total number of consecutive blocks, each block is the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="27b43-487">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="27b43-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="27b43-488">Si el valor de **blocksize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="27b43-488">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="27b43-489">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="27b43-490">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="27b43-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="27b43-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-492">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-493">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-494">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memoria de CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="27b43-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-495">Cadena de forma libre que proporciona información si la propiedad de **ErrorType** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="27b43-495">Free-form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="27b43-496">Si no se establece en 1, esta cadena no tiene significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-496">If not set to 1, this string has no meaning.</span></span>

<span data-ttu-id="27b43-497">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="27b43-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-499">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-501">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27b43-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-502">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="27b43-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="27b43-503">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="27b43-504">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="27b43-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="27b43-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="27b43-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-506">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27b43-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27b43-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-508">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="27b43-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="27b43-509">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="27b43-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="27b43-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="27b43-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="27b43-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="27b43-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="27b43-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="27b43-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="27b43-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-514">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="27b43-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="27b43-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="27b43-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-516">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="27b43-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="27b43-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="27b43-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-518">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="27b43-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="27b43-519">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="27b43-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="27b43-520">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="27b43-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="27b43-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="27b43-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-522">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="27b43-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="27b43-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="27b43-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="27b43-524">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="27b43-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="27b43-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-526">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="27b43-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-527">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-528">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="27b43-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="27b43-529">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="27b43-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="27b43-530">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="27b43-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="27b43-531">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="27b43-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="27b43-532">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-533">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="27b43-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-534">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-535">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-536">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="27b43-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="27b43-537">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-538">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="27b43-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-539">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27b43-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-540">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-541">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,3 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="27b43-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-542">Dirección inicial a la que hace referencia una aplicación o un sistema operativo y que está asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="27b43-542">Beginning address that is referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="27b43-543">La dirección de inicio se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="27b43-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="27b43-544">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="27b43-545">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="27b43-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-546">**Estado**</span><span class="sxs-lookup"><span data-stu-id="27b43-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-547">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-549">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="27b43-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-550">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="27b43-550">Current status of the object.</span></span>

<span data-ttu-id="27b43-551">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="27b43-552">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="27b43-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="27b43-553">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="27b43-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="27b43-554">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="27b43-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="27b43-555">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="27b43-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-556">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="27b43-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="27b43-557">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="27b43-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="27b43-558">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="27b43-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="27b43-559">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="27b43-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="27b43-560">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="27b43-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="27b43-561">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="27b43-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="27b43-562">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="27b43-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="27b43-563">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="27b43-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="27b43-564">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="27b43-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="27b43-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-566">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27b43-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-567">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-568">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="27b43-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="27b43-569">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="27b43-569">State of the logical device.</span></span> <span data-ttu-id="27b43-570">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="27b43-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="27b43-571">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27b43-572">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="27b43-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27b43-573">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="27b43-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="27b43-574">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="27b43-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="27b43-575">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="27b43-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="27b43-576">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="27b43-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27b43-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="27b43-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-578">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-579">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-580">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27b43-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27b43-581">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="27b43-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="27b43-582">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="27b43-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-584">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="27b43-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-585">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27b43-586">Si es **true**, la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="27b43-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="27b43-587">Si es **false**, se trata de una dirección física.</span><span class="sxs-lookup"><span data-stu-id="27b43-587">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="27b43-588">Si la propiedad **errorInfo** es igual a 3 ("OK"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="27b43-588">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="27b43-589">Esta propiedad se hereda de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-589">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="27b43-590">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="27b43-590">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27b43-591">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27b43-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27b43-592">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b43-592">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27b43-593">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27b43-593">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27b43-594">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="27b43-594">Scoping system's name.</span></span>

<span data-ttu-id="27b43-595">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-595">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27b43-596">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27b43-596">Remarks</span></span>

<span data-ttu-id="27b43-597">La clase **CIM \_ NonVolatileStorage** se deriva de [**la \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="27b43-597">The **CIM\_NonVolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="27b43-598">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="27b43-598">WMI does not implement this class.</span></span>

<span data-ttu-id="27b43-599">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="27b43-599">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="27b43-600">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="27b43-600">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b43-601">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27b43-601">Requirements</span></span>



| <span data-ttu-id="27b43-602">Requisito</span><span class="sxs-lookup"><span data-stu-id="27b43-602">Requirement</span></span> | <span data-ttu-id="27b43-603">Value</span><span class="sxs-lookup"><span data-stu-id="27b43-603">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27b43-604">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27b43-604">Minimum supported client</span></span><br/> | <span data-ttu-id="27b43-605">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27b43-605">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27b43-606">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27b43-606">Minimum supported server</span></span><br/> | <span data-ttu-id="27b43-607">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27b43-607">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27b43-608">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27b43-608">Namespace</span></span><br/>                | <span data-ttu-id="27b43-609">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="27b43-609">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27b43-610">MOF</span><span class="sxs-lookup"><span data-stu-id="27b43-610">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27b43-611"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27b43-611"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27b43-612">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27b43-612">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27b43-613"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27b43-613"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27b43-614">Vea también</span><span class="sxs-lookup"><span data-stu-id="27b43-614">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b43-615">**Memoria de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="27b43-615">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

