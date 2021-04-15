---
description: Representa las capacidades y la administración de los dispositivos lógicos relacionados con la memoria.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: CIM_Memory (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546030"
---
# <a name="cim_memory-class-hyper-v-management"></a><span data-ttu-id="3e724-103">CIM_Memory (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="3e724-103">CIM_Memory class (Hyper-V management)</span></span>

<span data-ttu-id="3e724-104">Representa las capacidades y la administración de los dispositivos lógicos relacionados con la memoria.</span><span class="sxs-lookup"><span data-stu-id="3e724-104">Represents the capabilities and management of memory-related logical devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e724-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e724-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="3e724-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e724-106">Members</span></span>

<span data-ttu-id="3e724-107">La clase de **\_ memoria CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e724-107">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="3e724-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e724-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e724-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e724-109">Properties</span></span>

<span data-ttu-id="3e724-110">La clase de **\_ memoria CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3e724-110">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e724-111">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="3e724-111">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-112">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="3e724-112">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3e724-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-114">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 005,18 "," MIF. \|Matriz de memoria física DMTF \| 001,13 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-114">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.18", "MIF.DMTF\|Physical Memory Array\|001.13")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-115">Matriz de octetos que contiene información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="3e724-115">An array of octets that contains additional error information.</span></span> <span data-ttu-id="3e724-116">Un ejemplo es el síndrome ECC o el retorno de los bits de comprobación si se usa una metodología de error basada en CRC.</span><span class="sxs-lookup"><span data-stu-id="3e724-116">An example is ECC syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="3e724-117">En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, es posible determinar el bit exacto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="3e724-117">In the latter case, if a single bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span>

<span data-ttu-id="3e724-118">Si la propiedad **errorInfo** contiene "3" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-118">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-119">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="3e724-119">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3e724-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-122">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-123">**true** si el error más reciente es corregible; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3e724-123">**true** if the most recent error is correctable; otherwise, **false**.</span></span> <span data-ttu-id="3e724-124">Si la propiedad **errorInfo** contiene "3" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-124">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="3e724-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e724-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-128">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,4 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,5 "), **punitivo** (" byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-129">Dirección final a la que hace referencia una aplicación o un sistema operativo, y asignada por un controlador de memoria para el objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="3e724-129">The ending address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="3e724-130">La dirección final se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="3e724-130">The ending address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-131">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="3e724-131">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e724-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-134">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-134">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-135">La operación de acceso a memoria que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="3e724-135">The memory access operation that caused the last error.</span></span> <span data-ttu-id="3e724-136">Si la propiedad **errorInfo** contiene "3" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-136">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3e724-137">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3e724-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e724-138">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="3e724-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="3e724-139">**Lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="3e724-139">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="3e724-140">**Escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="3e724-140">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="3e724-141">**Escritura parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="3e724-141">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e724-142">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="3e724-142">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e724-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-145">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 005,19 "," MIF. \|Matriz de memoria física DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-145">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.19", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-146">Dirección del último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="3e724-146">The address of the last memory error.</span></span> <span data-ttu-id="3e724-147">La propiedad **errorInfo** describe el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="3e724-147">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="3e724-148">Si la propiedad **errorInfo** contiene "3" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-148">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-149">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="3e724-149">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-150">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="3e724-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3e724-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-152">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. datoserror"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,12 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-152">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.12")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-153">Una matriz que contiene los datos capturados durante el último acceso de memoria erróneo.</span><span class="sxs-lookup"><span data-stu-id="3e724-153">An array that contains data captured during the last erroneous memory access.</span></span> <span data-ttu-id="3e724-154">Los datos ocupan los primeros n octetos de la matriz necesaria para contener el número de bits especificado por la propiedad **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="3e724-154">The data occupies the first n octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span>

<span data-ttu-id="3e724-155">Si la propiedad **ErrorTransferSize** contiene "0" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-155">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-156">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="3e724-156">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e724-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-159">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")</span><span class="sxs-lookup"><span data-stu-id="3e724-159">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorDataOrder")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-160">Orden de los datos almacenados en la propiedad **datoserror** .</span><span class="sxs-lookup"><span data-stu-id="3e724-160">The ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="3e724-161">Se puede especificar "byte menos significativo primero" (valor = 1) o "byte más significativo primero" (2).</span><span class="sxs-lookup"><span data-stu-id="3e724-161">"Least Significant Byte First" (value=1) or "Most Significant Byte First" (2) can be specified.</span></span> <span data-ttu-id="3e724-162">Si la propiedad **ErrorTransferSize** contiene "0" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-162">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e724-163">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3e724-163">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="3e724-164">**Primero el byte menos significativo** (1)</span><span class="sxs-lookup"><span data-stu-id="3e724-164">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="3e724-165">**Byte más significativo primero** (2)</span><span class="sxs-lookup"><span data-stu-id="3e724-165">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e724-166">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3e724-166">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e724-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-169">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. errorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 005,12 "," MIF. \|Matriz de memoria física DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ memoria de CIM**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="3e724-169">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-170">Tipo del último error que se va a producir.</span><span class="sxs-lookup"><span data-stu-id="3e724-170">The type of the last error to occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3e724-171">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3e724-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e724-172">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="3e724-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3e724-173">**Aceptar** (3)</span><span class="sxs-lookup"><span data-stu-id="3e724-173">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="3e724-174">**Lectura incorrecta** (4)</span><span class="sxs-lookup"><span data-stu-id="3e724-174">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="3e724-175">**Error de paridad** (5)</span><span class="sxs-lookup"><span data-stu-id="3e724-175">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="3e724-176">**Error de un bit** (6)</span><span class="sxs-lookup"><span data-stu-id="3e724-176">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="3e724-177">**Error de doble bit** (7)</span><span class="sxs-lookup"><span data-stu-id="3e724-177">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="3e724-178">**Error de varios bits** (8)</span><span class="sxs-lookup"><span data-stu-id="3e724-178">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="3e724-179">**Error de recorte** (9)</span><span class="sxs-lookup"><span data-stu-id="3e724-179">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="3e724-180">**Error de suma de comprobación** (10)</span><span class="sxs-lookup"><span data-stu-id="3e724-180">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="3e724-181">**Error de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="3e724-181">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="3e724-182">**Undefined** (12)</span><span class="sxs-lookup"><span data-stu-id="3e724-182">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="3e724-183">**Sin definir** (13)</span><span class="sxs-lookup"><span data-stu-id="3e724-183">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="3e724-184">**Undefined** (14)</span><span class="sxs-lookup"><span data-stu-id="3e724-184">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e724-185">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="3e724-185">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e724-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-188">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-188">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-189">Indica si el objeto de memoria utiliza algoritmos de paridad, algoritmos de CRC, ECC u otros mecanismos.</span><span class="sxs-lookup"><span data-stu-id="3e724-189">Indicates whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used by the memory object.</span></span> <span data-ttu-id="3e724-190">También se pueden proporcionar detalles sobre el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="3e724-190">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-191">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="3e724-191">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-192">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e724-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-194">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 005,21 "," MIF. \|Matriz de memoria física DMTF \| 001,15 "), **punitivo** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="3e724-194">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.21", "MIF.DMTF\|Physical Memory Array\|001.15"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-195">El intervalo, en bytes, en el que se puede resolver el último error.</span><span class="sxs-lookup"><span data-stu-id="3e724-195">The range, in bytes, in which the last error can be resolved.</span></span> <span data-ttu-id="3e724-196">Por ejemplo, si las direcciones de error se resuelven en el bit 11, como en el caso de una página típica; después, los errores pueden resolverse en los límites de 4K y esta propiedad se establece en "4000".</span><span class="sxs-lookup"><span data-stu-id="3e724-196">For example, if error addresses are resolved to bit 11, such as on a typical page basis; then the errors can be resolved to 4K boundaries, and this property is set to "4000".</span></span> <span data-ttu-id="3e724-197">Si la propiedad **errorInfo** contiene "3" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-197">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-198">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="3e724-198">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-199">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e724-199">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-201">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTime")</span><span class="sxs-lookup"><span data-stu-id="3e724-201">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTime")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-202">La hora en que se produjo el último error de memoria.</span><span class="sxs-lookup"><span data-stu-id="3e724-202">The time when the last memory error occurred.</span></span> <span data-ttu-id="3e724-203">Si la propiedad **errorInfo** contiene "3" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-203">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-204">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="3e724-204">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-205">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e724-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-207">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memoria física DMTF \| 001,11 "), **punitivo** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="3e724-207">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.11"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-208">Tamaño de la transferencia de datos, en bits, que causó el último error.</span><span class="sxs-lookup"><span data-stu-id="3e724-208">The size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="3e724-209">"0" indica que no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="3e724-209">"0" indicates no error.</span></span> <span data-ttu-id="3e724-210">Si la propiedad **errorInfo** contiene "3" (OK), no se utiliza esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e724-210">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-211">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3e724-211">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e724-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-214">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ memoria de CIM**.**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="3e724-214">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-215">Una descripción del tipo de error, cuando la propiedad **ErrorType** está establecida en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="3e724-215">A description of the error type, when the **ErrorType** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="3e724-216">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="3e724-216">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-217">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e724-217">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-219">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. La \| matriz de memoria DMTF asigna direcciones \| 001,3 "," MIF. \|Direcciones asignadas del dispositivo \| de memoria DMTF 001,4 "), **punitivo** (" byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="3e724-219">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-220">Dirección inicial a la que hace referencia una aplicación o un sistema operativo, y asignada por un controlador de memoria para el objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="3e724-220">The starting address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="3e724-221">La dirección de inicio se especifica en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="3e724-221">The starting address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-222">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="3e724-222">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-223">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3e724-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e724-225">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")</span><span class="sxs-lookup"><span data-stu-id="3e724-225">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.SystemLevelAddress")</span></span>
</dt> </dl>

<span data-ttu-id="3e724-226">**true** si la información de dirección de la propiedad **ErrorAddress** es una dirección de nivel de sistema, **false** si se trata de una dirección física.</span><span class="sxs-lookup"><span data-stu-id="3e724-226">**true** if the address information in the **ErrorAddress** property is a system-level address, **false** if it is a physical address.</span></span>

</dd> <dt>

<span data-ttu-id="3e724-227">**Volatil**</span><span class="sxs-lookup"><span data-stu-id="3e724-227">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e724-228">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3e724-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e724-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e724-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e724-230">**true** si la memoria es volátil; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3e724-230">**true** if the memory is volatile; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e724-231">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e724-231">Requirements</span></span>



| <span data-ttu-id="3e724-232">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e724-232">Requirement</span></span> | <span data-ttu-id="3e724-233">Value</span><span class="sxs-lookup"><span data-stu-id="3e724-233">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e724-234">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e724-234">Minimum supported client</span></span><br/> | <span data-ttu-id="3e724-235">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3e724-235">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3e724-236">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e724-236">Minimum supported server</span></span><br/> | <span data-ttu-id="3e724-237">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e724-237">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3e724-238">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e724-238">Namespace</span></span><br/>                | <span data-ttu-id="3e724-239">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3e724-239">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3e724-240">MOF</span><span class="sxs-lookup"><span data-stu-id="3e724-240">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e724-241"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e724-241"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e724-242">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e724-242">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e724-243"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e724-243"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e724-244">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e724-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e724-245">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3e724-245">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

