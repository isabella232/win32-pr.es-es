---
description: Representa un dispositivo que puede usar medios para almacenar y recuperar datos.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: CIM_MediaAccessDevice (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689620"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a><span data-ttu-id="660f6-103">CIM_MediaAccessDevice (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="660f6-103">CIM_MediaAccessDevice class (Hyper-V management)</span></span>

<span data-ttu-id="660f6-104">Representa un dispositivo que puede usar medios para almacenar y recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="660f6-104">Represents a device that can use media to store and retrieve data.</span></span>

## <a name="syntax"></a><span data-ttu-id="660f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="660f6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a><span data-ttu-id="660f6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="660f6-106">Members</span></span>

<span data-ttu-id="660f6-107">La clase **CIM \_ MediaAccessDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="660f6-107">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="660f6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="660f6-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="660f6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="660f6-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="660f6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="660f6-110">Methods</span></span>

<span data-ttu-id="660f6-111">La clase **CIM \_ MediaAccessDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="660f6-111">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="660f6-112">Método</span><span class="sxs-lookup"><span data-stu-id="660f6-112">Method</span></span>                                               | <span data-ttu-id="660f6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="660f6-113">Description</span></span>                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="660f6-114">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="660f6-114">**LockMedia**</span></span>](cim-mediaaccessdevice-lockmedia.md) | <span data-ttu-id="660f6-115">Bloquea y desbloquea los medios extraíbles en un dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="660f6-115">Locks and unlocks removable media in a media access device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="660f6-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="660f6-116">Properties</span></span>

<span data-ttu-id="660f6-117">La clase **CIM \_ MediaAccessDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="660f6-117">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="660f6-118">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="660f6-118">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-119">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="660f6-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="660f6-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-121">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "," MIF. \|Disco de host DMTF \| 001,2 "," MIF. \|Disco de host DMTF \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="660f6-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7", "MIF.DMTF\|Host Disk\|001.2", "MIF.DMTF\|Host Disk\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-122">Una matriz que contiene las funciones del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="660f6-122">An array that contains the capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="660f6-123">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="660f6-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="660f6-124">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="660f6-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="660f6-125">**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="660f6-125">**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="660f6-126">**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="660f6-126">**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="660f6-127">**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="660f6-127">**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="660f6-128">**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="660f6-128">**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="660f6-129">**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="660f6-129">**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="660f6-130">**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="660f6-130">**Supports Removeable Media** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="660f6-131">**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="660f6-131">**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="660f6-132">**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="660f6-132">**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="660f6-133">**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="660f6-133">**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="660f6-134">**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="660f6-134">**Supports Dual Sided Media** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="660f6-135">**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="660f6-135">**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="660f6-136">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="660f6-136">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-137">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="660f6-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="660f6-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-139">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="660f6-139">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-140">Matriz de descripciones de características para los elementos de la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="660f6-140">An array of feature descriptions for the items in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-141">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="660f6-141">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="660f6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-144">Nombre del algoritmo o herramienta que usa el dispositivo para admitir la compresión.</span><span class="sxs-lookup"><span data-stu-id="660f6-144">The name of the algorithm or tool used by the device to support compression.</span></span>

<span data-ttu-id="660f6-145">Si no se especifica un tipo de compresión, se puede usar uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="660f6-145">If a compression type is not specified, one of the following values can be used:</span></span>

-   <span data-ttu-id="660f6-146">La compatibilidad con la compresión "desconocida" es desconocida o no se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="660f6-146">"Unknown"   compression support is unknown or not specified.</span></span>
-   <span data-ttu-id="660f6-147">Se admite la compresión "comprimida", pero el tipo es desconocido o no se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="660f6-147">"Compressed"   compression is supported but the type is unknown or unspecified.</span></span>
-   <span data-ttu-id="660f6-148">"No comprimido" el dispositivo no admite capacidades de compresión.</span><span class="sxs-lookup"><span data-stu-id="660f6-148">"Not Compressed"   the device does not support compression capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-149">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="660f6-149">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-150">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-152">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="660f6-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-153">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-153">The default block size, in bytes, for the device.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="660f6-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="660f6-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-157">El tipo de detección y corrección de errores admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-157">The type of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-158">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="660f6-158">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-159">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="660f6-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-161">Fecha y hora en que se limpió por última vez el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-161">The date and time when the device was last cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-162">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="660f6-162">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-163">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-165">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos"), **punitivo** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="660f6-165">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-166">El tiempo que tarda, en milisegundos, para que el dispositivo pueda leer o escribir un medio después de que el dispositivo empiece a cargarse.</span><span class="sxs-lookup"><span data-stu-id="660f6-166">The time it takes, in milliseconds, for the device to be able to read or write a media after the device starts loading.</span></span> <span data-ttu-id="660f6-167">Por ejemplo, en el caso de las unidades de disco, es el intervalo entre un disco que no gira hasta el disco que informa de que está listo para las operaciones de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="660f6-167">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write operations.</span></span> <span data-ttu-id="660f6-168">En el caso de las unidades de cinta, esto se inicia cuando se inserta el medio y finaliza cuando la unidad informa de que está listo para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="660f6-168">For tape drives, this starts when media is inserted and ends when the drive reports that it is ready for an application.</span></span> <span data-ttu-id="660f6-169">Normalmente, se encuentra en el área de inicio de cinta (BOT) de la cinta.</span><span class="sxs-lookup"><span data-stu-id="660f6-169">This is usually at the tape's beginning-of-tape (BOT) area.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-170">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="660f6-170">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-171">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-173">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos"), **punitivo** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="660f6-173">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-174">El tiempo máximo de acceso del medio, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="660f6-174">The maximum access time of the media, in milliseconds.</span></span> <span data-ttu-id="660f6-175">En el caso de una unidad de disco, representa la búsqueda completa y el retraso de rotación completo.</span><span class="sxs-lookup"><span data-stu-id="660f6-175">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="660f6-176">En el caso de las unidades de cinta, representa una búsqueda desde el principio de la cinta hasta el punto más alejado físicamente.</span><span class="sxs-lookup"><span data-stu-id="660f6-176">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-177">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="660f6-177">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-178">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-180">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="660f6-180">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-181">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-181">The maximum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-182">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="660f6-182">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-183">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-185">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial \| de DMTF 001,2 "," MIF. \|Disco host DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="660f6-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2", "MIF.DMTF\|Host Disk\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-186">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-186">The maximum size, in kilobytes, of media supported by this device.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-187">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="660f6-187">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-188">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-190">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")</span><span class="sxs-lookup"><span data-stu-id="660f6-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-191">El número máximo de unidades que se pueden usar antes de que se limpie el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-191">The maximum number of units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="660f6-192">**UnitsDescription** define el tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="660f6-192">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-193">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="660f6-193">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-194">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="660f6-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-196">**true** si el medio está bloqueado en el dispositivo y no se puede expulsar; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="660f6-196">**true** if the media is locked in the device and can not be ejected; otherwise, **false**.</span></span> <span data-ttu-id="660f6-197">En el caso de los dispositivos no extraíbles, este valor debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="660f6-197">For non-removable devices, this value should be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-198">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="660f6-198">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-199">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-201">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="660f6-201">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-202">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-202">The minimum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-203">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="660f6-203">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-204">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-206">Calificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="660f6-206">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="660f6-207">El número de veces que se ha montado el medio para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-207">The number of times that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="660f6-208">Si el dispositivo no admite medios extraíbles, esta propiedad debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="660f6-208">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-209">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="660f6-209">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-210">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="660f6-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-212">**true** si el dispositivo necesita limpieza; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="660f6-212">**true** if the device needs cleaning; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="660f6-213">La propiedad **Capabilities** indica si es posible la limpieza manual o automática.</span><span class="sxs-lookup"><span data-stu-id="660f6-213">The **Capabilities** property indicates whether manual or automatic cleaning is possible.</span></span>

 

</dd> <dt>

<span data-ttu-id="660f6-214">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="660f6-214">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-215">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="660f6-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-217">Si el dispositivo admite varios medios individuales, esta propiedad define el número máximo que se puede admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="660f6-217">If the device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-218">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="660f6-218">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-219">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="660f6-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-221">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Discos DMTF \| 003,22 ")</span><span class="sxs-lookup"><span data-stu-id="660f6-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Disks\|003.22")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-222">La seguridad operativa del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-222">The operational security for the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="660f6-223">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="660f6-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="660f6-224">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="660f6-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="660f6-225">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="660f6-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

<span data-ttu-id="660f6-226">**Solo lectura** (4)</span><span class="sxs-lookup"><span data-stu-id="660f6-226">**Read Only** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

<span data-ttu-id="660f6-227">**Bloqueado** (5)</span><span class="sxs-lookup"><span data-stu-id="660f6-227">**Locked Out** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="660f6-228">**Omisión de arranque** (6)</span><span class="sxs-lookup"><span data-stu-id="660f6-228">**Boot Bypass** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

<span data-ttu-id="660f6-229">**Omisión de arranque y solo lectura** (7)</span><span class="sxs-lookup"><span data-stu-id="660f6-229">**Boot Bypass and Read Only** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="660f6-230">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="660f6-230">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-231">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="660f6-231">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-233">La fecha y hora más recientes en que se montó el medio en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-233">The most recent date and time when media was mounted on the device.</span></span> <span data-ttu-id="660f6-234">Esta propiedad solo la usan los dispositivos que admiten medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="660f6-234">This property is only used by devices that support removable media.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-235">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="660f6-235">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-236">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-236">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="660f6-238">El tiempo, en segundos, que los medios se han montado para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-238">The time, in seconds, that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="660f6-239">Si el dispositivo no admite medios extraíbles, esta propiedad debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="660f6-239">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-240">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="660f6-240">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-241">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="660f6-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-243">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes por segundo"), **punitivo** ("byte/segundo \* 10 ^ 3")</span><span class="sxs-lookup"><span data-stu-id="660f6-243">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes per Second"), **PUnit** ("byte / second \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-244">La velocidad de transferencia de datos sostenida en kilobytes en la que el dispositivo puede leer y escribir en un medio.</span><span class="sxs-lookup"><span data-stu-id="660f6-244">The sustained data transfer rate in kilobytes at which the device can read and write to a media.</span></span> <span data-ttu-id="660f6-245">Se trata de una velocidad de datos sin procesar y sostenida.</span><span class="sxs-lookup"><span data-stu-id="660f6-245">This is a sustained, raw data rate.</span></span> <span data-ttu-id="660f6-246">No se deben informar de las tarifas máximas con compresión en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="660f6-246">Maximum rates or rates with compression should not be reported in this property.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-247">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="660f6-247">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="660f6-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-250">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**","**\_ MediaAccessDevice CIM**.**UnitsUsed**")</span><span class="sxs-lookup"><span data-stu-id="660f6-250">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM\_MediaAccessDevice**.**UnitsUsed**")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-251">Describe el tipo de unidad de las propiedades **MaxUnitsBeforeCleaning** y **UnitsUsed** .</span><span class="sxs-lookup"><span data-stu-id="660f6-251">Describes the unit type of the **MaxUnitsBeforeCleaning** and **UnitsUsed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-252">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="660f6-252">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-253">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-253">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-255">Calificadores: [**medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**","**\_ MediaAccessDevice CIM**.**MaxUnitsBeforeCleaning**")</span><span class="sxs-lookup"><span data-stu-id="660f6-255">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**", "**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-256">El número de unidades utilizadas por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-256">The number of units used by the device.</span></span> <span data-ttu-id="660f6-257">Esta propiedad se usa para determinar cuándo se debe limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="660f6-257">This property is used to determine when the device should be cleaned.</span></span> <span data-ttu-id="660f6-258">**UnitsDescription** define el tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="660f6-258">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="660f6-259">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="660f6-259">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="660f6-260">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="660f6-260">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="660f6-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="660f6-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="660f6-262">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos"), **punitivo** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="660f6-262">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="660f6-263">El tiempo que tarda, en milisegundos, para que el dispositivo pase de la lectura o escritura de archivos multimedia a la descarga.</span><span class="sxs-lookup"><span data-stu-id="660f6-263">The time it takes, in milliseconds, for the device to transition from reading or writing media to unloading.</span></span> <span data-ttu-id="660f6-264">Por ejemplo, en el caso de las unidades de disco, es el intervalo entre un giro de disco a velocidades nominales y un disco que no gira.</span><span class="sxs-lookup"><span data-stu-id="660f6-264">For example, for disk drives, this is the interval between a disk spinning at nominal speeds and a disk not spinning.</span></span> <span data-ttu-id="660f6-265">En el caso de las unidades de cinta, es el momento en que un medio puede pasar de su BOT a ser completamente expulsado y accesible a un elemento selector o operador humano.</span><span class="sxs-lookup"><span data-stu-id="660f6-265">For tape drives, this is the time for a media to go from its BOT to being fully ejected and accessible to a picker element or human operator.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="660f6-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="660f6-266">Requirements</span></span>



| <span data-ttu-id="660f6-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="660f6-267">Requirement</span></span> | <span data-ttu-id="660f6-268">Value</span><span class="sxs-lookup"><span data-stu-id="660f6-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="660f6-269">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="660f6-269">Minimum supported client</span></span><br/> | <span data-ttu-id="660f6-270">Windows 8</span><span class="sxs-lookup"><span data-stu-id="660f6-270">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="660f6-271">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="660f6-271">Minimum supported server</span></span><br/> | <span data-ttu-id="660f6-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="660f6-272">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="660f6-273">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="660f6-273">Namespace</span></span><br/>                | <span data-ttu-id="660f6-274">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="660f6-274">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="660f6-275">MOF</span><span class="sxs-lookup"><span data-stu-id="660f6-275">MOF</span></span><br/>                      | <dl> <span data-ttu-id="660f6-276"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="660f6-276"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="660f6-277">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="660f6-277">DLL</span></span><br/>                      | <dl> <span data-ttu-id="660f6-278"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="660f6-278"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="660f6-279">Vea también</span><span class="sxs-lookup"><span data-stu-id="660f6-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="660f6-280">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="660f6-280">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

