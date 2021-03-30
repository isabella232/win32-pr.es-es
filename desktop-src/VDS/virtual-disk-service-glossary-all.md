---
description: En esta sección se proporciona un glosario de términos técnicos que se usan en la documentación del servicio de disco virtual (VDS).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glosario de servicio de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002059"
---
# <a name="virtual-disk-service-glossary"></a><span data-ttu-id="12efb-103">Glosario de servicio de disco virtual</span><span class="sxs-lookup"><span data-stu-id="12efb-103">Virtual Disk Service Glossary</span></span>

<span data-ttu-id="12efb-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="12efb-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="12efb-105">En esta sección se proporciona un glosario de términos técnicos que se usan en la documentación del servicio de disco virtual (VDS).</span><span class="sxs-lookup"><span data-stu-id="12efb-105">This section provides a glossary of technical terms used in the Virtual Disk Service (VDS) documentation.</span></span>

<dl> <dt>

<span data-ttu-id="12efb-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuración de automagic**</span><span class="sxs-lookup"><span data-stu-id="12efb-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic configuration**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-107">Proveedor RAID de hardware que proporciona un conjunto de reglas para elegir la reasignación de bloques lógicos de LUN basada en atributos simples.</span><span class="sxs-lookup"><span data-stu-id="12efb-107">Hardware RAID provider that supplies a set of rules for choosing LUN logical block remapping based on simple attributes.</span></span> <span data-ttu-id="12efb-108">Los proveedores de automagic también pueden modificar dinámicamente la asignación para el rendimiento o la administración de errores.</span><span class="sxs-lookup"><span data-stu-id="12efb-108">Automagic providers can also dynamically alter the mapping for performance or fault management.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**Sugerencias de automagic**</span><span class="sxs-lookup"><span data-stu-id="12efb-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic hints**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-110">Información proporcionada a un proveedor de automagic para guiar la configuración de bloque lógico de LUN.</span><span class="sxs-lookup"><span data-stu-id="12efb-110">Information supplied to an automagic provider to guide the LUN logical block configuration.</span></span> <span data-ttu-id="12efb-111">Las sugerencias incluyen información sobre la tolerancia a errores deseada, la atomicidad física y el patrón de acceso de e/s previsto.</span><span class="sxs-lookup"><span data-stu-id="12efb-111">Hints include information as to the desired fault tolerance, physical atomicity, and intended I/O access pattern.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco básico**</span><span class="sxs-lookup"><span data-stu-id="12efb-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**basic disk**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-113">Un disco administrado por el proveedor de software más sencillo posible.</span><span class="sxs-lookup"><span data-stu-id="12efb-113">A disk managed by the simplest possible software provider.</span></span> <span data-ttu-id="12efb-114">El proveedor de discos básico solo admite los volúmenes que se asignan directamente a las estructuras de datos de configuración de la partición.</span><span class="sxs-lookup"><span data-stu-id="12efb-114">The basic disk provider supports only volumes that directly map to partition configuration data structures.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**enlace**</span><span class="sxs-lookup"><span data-stu-id="12efb-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-116">Seleccionar para un conjunto de asignaciones a recursos físicos.</span><span class="sxs-lookup"><span data-stu-id="12efb-116">Selecting for a set of mappings to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**verso**</span><span class="sxs-lookup"><span data-stu-id="12efb-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convert**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-118">Proceso de conversión de un disco básico a un disco dinámico.</span><span class="sxs-lookup"><span data-stu-id="12efb-118">The process of converting a basic disk to a dynamic disk.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuraciones**</span><span class="sxs-lookup"><span data-stu-id="12efb-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuration**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-120">Colección de los parámetros operativos que proporcionan la asignación de un volumen, o LUN, a los recursos físicos.</span><span class="sxs-lookup"><span data-stu-id="12efb-120">A collection of the operating parameters that supply the mapping from a volume, or LUN, to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**módem**</span><span class="sxs-lookup"><span data-stu-id="12efb-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-122">Programa de software que contiene la inteligencia en tiempo de ejecución de un proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-122">A software program that contains the runtime intelligence for a hardware provider.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**discos**</span><span class="sxs-lookup"><span data-stu-id="12efb-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disk**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-124">Un disco físico o un LUN RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-124">A physical disk or hardware RAID LUN.</span></span> <span data-ttu-id="12efb-125">Los discos son destinos para la carga de e/s de almacenamiento en tiempo de ejecución. Plug and Play (PNP) no distingue entre JBOD y LUN.</span><span class="sxs-lookup"><span data-stu-id="12efb-125">Disks are targets for runtime storage I/O load; Plug and Play (PNP) does not distinguish between JBOD and LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disco duro**</span><span class="sxs-lookup"><span data-stu-id="12efb-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disk platter**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-127">Un subconjunto de un paquete que se usa para exportar o importar volúmenes de un paquete.</span><span class="sxs-lookup"><span data-stu-id="12efb-127">A subset of a pack used for exporting or importing volumes from a pack.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**paquete de disco**</span><span class="sxs-lookup"><span data-stu-id="12efb-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-129">Vea *Pack*.</span><span class="sxs-lookup"><span data-stu-id="12efb-129">See *pack*.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**dispositivo**</span><span class="sxs-lookup"><span data-stu-id="12efb-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**drive**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-131">Un eje de disco físico en un subsistema RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-131">A physical disk spindle within a hardware RAID subsystem.</span></span> <span data-ttu-id="12efb-132">El subsistema enlaza las unidades a los LUN.</span><span class="sxs-lookup"><span data-stu-id="12efb-132">Drives are bound into LUNs by the subsystem.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinámico**</span><span class="sxs-lookup"><span data-stu-id="12efb-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamic disk**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-134">Un disco administrado por un proveedor RAID de software compatible con la reconfiguración de volumen flexible.</span><span class="sxs-lookup"><span data-stu-id="12efb-134">A disk managed by a software RAID provider with support for flexible volume reconfiguration.</span></span> <span data-ttu-id="12efb-135">Un disco dinámico utiliza una partición como contenedor de volúmenes; no hay ninguna asignación garantizada.</span><span class="sxs-lookup"><span data-stu-id="12efb-135">A dynamic disk uses a partition as a container for volumes; there is no guaranteed mapping.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuración explícita**</span><span class="sxs-lookup"><span data-stu-id="12efb-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explicit configuration**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-137">Una configuración con los parámetros, incluido el tipo de volumen y el diseño exacto, para una colección de volúmenes de destino.</span><span class="sxs-lookup"><span data-stu-id="12efb-137">A configuration with the parameters, including the volume type and the exact layout, for a collection of target volumes.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**Portada**</span><span class="sxs-lookup"><span data-stu-id="12efb-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**export**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-139">El acto de mover un disco duro y todos los volúmenes contenidos en ese platter de un paquete.</span><span class="sxs-lookup"><span data-stu-id="12efb-139">The act of moving a disk platter and all volumes contained on that platter out of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**expresa**</span><span class="sxs-lookup"><span data-stu-id="12efb-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-141">Un intervalo contiguo de sectores lógicos que contribuyen a un solo volumen o disco.</span><span class="sxs-lookup"><span data-stu-id="12efb-141">A contiguous range of logical sectors contributing to a single volume or disk.</span></span> <span data-ttu-id="12efb-142">Una extensión también puede ser un rango de sectores sin asignar.</span><span class="sxs-lookup"><span data-stu-id="12efb-142">An extent can also be range of unallocated sectors.</span></span> <span data-ttu-id="12efb-143">Normalmente, un sistema de archivos muestra los detalles de la extensión a un usuario final.</span><span class="sxs-lookup"><span data-stu-id="12efb-143">Commonly, a file system displays the extent details to an end-user.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabla de particiones GUID (GPT)**</span><span class="sxs-lookup"><span data-stu-id="12efb-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID Partition Table (GPT)**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-145">Estructuras utilizadas por el firmware EFI.</span><span class="sxs-lookup"><span data-stu-id="12efb-145">Structures used by EFI firmware.</span></span> <span data-ttu-id="12efb-146">GPT es uno de los dos formatos de datos de configuración de software de nivel más bajo usados por el firmware de plataforma para buscar un sistema operativo de arranque u otra imagen ejecutable.</span><span class="sxs-lookup"><span data-stu-id="12efb-146">GPT is one of two lowest level software configuration data formats used by platform firmware to locate a bootable operating system or other executable image.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**proveedor de hardware**</span><span class="sxs-lookup"><span data-stu-id="12efb-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**hardware provider**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-148">Una colección de software que se ejecuta en el host, un adaptador de bus y, posiblemente, un subsistema de almacenamiento externo que funciona conjuntamente para exponer y administrar LUN de RAID.</span><span class="sxs-lookup"><span data-stu-id="12efb-148">A collection of software that executes on the host, a bus adapter, and possibly an external storage subsystem that works together to surface and manage RAID LUNs.</span></span> <span data-ttu-id="12efb-149">Los proveedores de hardware de la mayoría de los subsistemas de almacenamiento externo solo contienen software basado en el host y en el modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="12efb-149">Hardware providers for most external storage subsystems contain only user-mode, host-based software.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**enfermedad**</span><span class="sxs-lookup"><span data-stu-id="12efb-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**health**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-151">El estado actual de la administración de errores de un volumen o LUN.</span><span class="sxs-lookup"><span data-stu-id="12efb-151">The current fault-management status of a volume or a LUN.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**reserva activa**</span><span class="sxs-lookup"><span data-stu-id="12efb-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-153">Agregar temporalmente un Plex de volumen a un volumen.</span><span class="sxs-lookup"><span data-stu-id="12efb-153">Temporarily adding a volume plex to a volume.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**importar**</span><span class="sxs-lookup"><span data-stu-id="12efb-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**import**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-155">El acto de mover un platter Disk y todos sus volúmenes a un paquete existente.</span><span class="sxs-lookup"><span data-stu-id="12efb-155">The act of moving a disk platter and all its volumes into an existing pack.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**solo un grupo de discos (JBOD)**</span><span class="sxs-lookup"><span data-stu-id="12efb-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**just a bunch of disks (JBOD)**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-157">Colección de ejes físicos sin el control coordinado proporcionado por un dispositivo RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-157">A collection of physical spindles without the coordinated control provided by a hardware RAID device.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**número de bloque lógico (LBN)**</span><span class="sxs-lookup"><span data-stu-id="12efb-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logical block number (LBN)**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-159">La unidad más pequeña de datos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="12efb-159">The smallest addressable unit of storage data.</span></span> <span data-ttu-id="12efb-160">LBN se usa con protocolos de comandos de e/s.</span><span class="sxs-lookup"><span data-stu-id="12efb-160">LBN is used with I/O command protocols.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**asignación de bloques lógicos**</span><span class="sxs-lookup"><span data-stu-id="12efb-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logical block mapping**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-162">La transformación de los bloques lógicos que se presentan a un proveedor a los expuestos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="12efb-162">The transformation of the logical blocks presented to a provider to those exposed by the provider.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**número de unidad lógica (LUN)**</span><span class="sxs-lookup"><span data-stu-id="12efb-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logical unit number (LUN)**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-164">Una unidad de almacenamiento direccionable físicamente, expuesta por un subsistema RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-164">A physically addressable storage unit as surfaced by a hardware RAID subsystem.</span></span> <span data-ttu-id="12efb-165">Este término también puede hacer referencia al identificador SCSI de la unidad de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="12efb-165">This term can also refer to the SCSI identifier for the storage unit.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Número de LUN**</span><span class="sxs-lookup"><span data-stu-id="12efb-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN number**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-167">Número que un proveedor de hardware de VDS asigna a un LUN en una matriz.</span><span class="sxs-lookup"><span data-stu-id="12efb-167">A number that a VDS hardware provider assigns to a LUN in an array.</span></span> <span data-ttu-id="12efb-168">No es lo mismo que el "número de unidad lógica" en la dirección SCSI del disco.</span><span class="sxs-lookup"><span data-stu-id="12efb-168">This is not the same as the "logical unit number" in the disk's SCSI address.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**servicio de administración**</span><span class="sxs-lookup"><span data-stu-id="12efb-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**management service**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-170">Programa de software que se ejecuta según sea necesario para realizar la configuración, la supervisión o el control de errores del volumen.</span><span class="sxs-lookup"><span data-stu-id="12efb-170">A software program that executes as needed to perform volume configuration, monitoring, or fault handling.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**asociaciones**</span><span class="sxs-lookup"><span data-stu-id="12efb-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-172">Un volumen que se expone al sistema operativo y tiene un nombre de volumen asociado (una letra de unidad).</span><span class="sxs-lookup"><span data-stu-id="12efb-172">A volume that is exposed to the operating system and has an associated volume name (a drive letter).</span></span> <span data-ttu-id="12efb-173">Un volumen es accesible desde un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="12efb-173">A volume is accessible by a file system.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**enmascaramiento**</span><span class="sxs-lookup"><span data-stu-id="12efb-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masking**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-175">Un disco no reconocido por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="12efb-175">A disk not recognized by the operating system.</span></span> <span data-ttu-id="12efb-176">Un disco se puede enmascarar mediante el subsistema RAID de hardware, el conmutador, la reserva SCSI por otro host del equipo o el software de la pila de discos.</span><span class="sxs-lookup"><span data-stu-id="12efb-176">A disk can be masked by the hardware RAID subsystem, switch, SCSI RESERVE by another computer host, or software in the disk stack.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**creación de particiones de registro de arranque maestro (MBR)**</span><span class="sxs-lookup"><span data-stu-id="12efb-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**master boot record partitioning (MBR)**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-178">MBR es uno de los dos formatos de datos de configuración de software de nivel más bajo y lo utiliza el firmware de BIOS para buscar una imagen de sistema operativo de arranque.</span><span class="sxs-lookup"><span data-stu-id="12efb-178">MBR is one of two lowest level software configuration data formats, and is used by BIOS firmware to locate a bootable operating system image.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**miembro**</span><span class="sxs-lookup"><span data-stu-id="12efb-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**member**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-180">Colección de extensiones de disco concatenadas contenidas en uno o más discos.</span><span class="sxs-lookup"><span data-stu-id="12efb-180">A collection of concatenated disk extents contained on one more disks.</span></span> <span data-ttu-id="12efb-181">Un disco puede contribuir a un solo miembro de un volumen.</span><span class="sxs-lookup"><span data-stu-id="12efb-181">A disk can contribute to only one member of a volume.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**creación**</span><span class="sxs-lookup"><span data-stu-id="12efb-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mirror**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-183">Asignación de volumen o disco que mantiene dos o más copias de datos idénticas.</span><span class="sxs-lookup"><span data-stu-id="12efb-183">A volume or disk mapping that maintains two or more identical data copies.</span></span> <span data-ttu-id="12efb-184">El tipo de asignación también se denomina RAID nivel 1.</span><span class="sxs-lookup"><span data-stu-id="12efb-184">The type of mapping is also called RAID Level 1.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**embalaje**</span><span class="sxs-lookup"><span data-stu-id="12efb-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pack**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-186">Una colección de volúmenes lógicos y discos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="12efb-186">A collection of logical volumes and underlying disks.</span></span> <span data-ttu-id="12efb-187">Un paquete es la unidad de cierre transitiva de un volumen.</span><span class="sxs-lookup"><span data-stu-id="12efb-187">A pack is the unit of transitive closure for a volume.</span></span> <span data-ttu-id="12efb-188">Los paquetes de discos dinámicos y los grupos de discos son términos para el mismo elemento.</span><span class="sxs-lookup"><span data-stu-id="12efb-188">Dynamic disk packs and disk groups are terms for the same item.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**franja de paridad**</span><span class="sxs-lookup"><span data-stu-id="12efb-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**parity stripe**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-190">Asignación de volumen o disco que mantiene la información de comprobación de la paridad, así como los datos.</span><span class="sxs-lookup"><span data-stu-id="12efb-190">A volume or disk mapping that maintains parity check information as well as data.</span></span> <span data-ttu-id="12efb-191">Cada proveedor proporciona la asignación y el esquema de protección exactos.</span><span class="sxs-lookup"><span data-stu-id="12efb-191">Each vendor supplies the exact mapping and protection scheme.</span></span> <span data-ttu-id="12efb-192">Incluye RAID 3, 4, 5 y 6.</span><span class="sxs-lookup"><span data-stu-id="12efb-192">Includes RAID 3, 4, 5, and 6.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuración dirigida parcialmente**</span><span class="sxs-lookup"><span data-stu-id="12efb-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**partially directed configuration**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-194">Un volumen o una configuración de disco que no es totalmente explícita.</span><span class="sxs-lookup"><span data-stu-id="12efb-194">A volume or disk configuration that is not fully explicit.</span></span> <span data-ttu-id="12efb-195">Se especifican el tipo de enlace y una colección de recursos de destino; el diseño real no es.</span><span class="sxs-lookup"><span data-stu-id="12efb-195">The binding type and a collection of target resources are specified; the actual layout is not.</span></span> <span data-ttu-id="12efb-196">La configuración dirigida parcialmente es la configuración de volumen más común.</span><span class="sxs-lookup"><span data-stu-id="12efb-196">Partially directed configuration is the most common volume configuration.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**divide**</span><span class="sxs-lookup"><span data-stu-id="12efb-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partition**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-198">Intervalo contiguo de sectores lógicos descrito por una sola entrada en la estructura MBR o GPT.</span><span class="sxs-lookup"><span data-stu-id="12efb-198">A contiguous range of logical sectors described by a single entry in the MBR or GPT structure.</span></span> <span data-ttu-id="12efb-199">En los discos básicos, las particiones se corresponden directamente con volúmenes simples.</span><span class="sxs-lookup"><span data-stu-id="12efb-199">On basic disks, partitions directly correspond to simple volumes.</span></span> <span data-ttu-id="12efb-200">Las estructuras de partición se comparten entre el firmware de la plataforma BIOS o EFI, y un sistema operativo u otra imagen de arranque.</span><span class="sxs-lookup"><span data-stu-id="12efb-200">Partition structures are shared between the BIOS or EFI platform firmware and an operating system or other bootable image.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-201"><span id="base.path"></span><span id="BASE.PATH"></span>**camino**</span><span class="sxs-lookup"><span data-stu-id="12efb-201"><span id="base.path"></span><span id="BASE.PATH"></span>**path**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-202">La ruta de acceso de un equipo a un disco o LUN de hardware externo.</span><span class="sxs-lookup"><span data-stu-id="12efb-202">The access path from a computer to a disk or external hardware LUN.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**complejos**</span><span class="sxs-lookup"><span data-stu-id="12efb-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plex**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-204">Un miembro de un volumen reflejado o LUN.</span><span class="sxs-lookup"><span data-stu-id="12efb-204">One member of a mirrored volume or LUN.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-205"><span id="base.port"></span><span id="BASE.PORT"></span>**casilla**</span><span class="sxs-lookup"><span data-stu-id="12efb-205"><span id="base.port"></span><span id="BASE.PORT"></span>**port**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-206">Extremo de una ruta de acceso en un disco.</span><span class="sxs-lookup"><span data-stu-id="12efb-206">The endpoint of a path at a disk.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**matriz redundante de discos independientes (RAID)**</span><span class="sxs-lookup"><span data-stu-id="12efb-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundant array of independent disks (RAID)**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-208">Colección de técnicas para administrar varios discos.</span><span class="sxs-lookup"><span data-stu-id="12efb-208">A collection of techniques for managing multiple disks.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**servicio de tiempo de ejecución**</span><span class="sxs-lookup"><span data-stu-id="12efb-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**runtime service**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-210">Programa de software que se ejecuta en una solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="12efb-210">A software program that executes on an I/O-request basis.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco simple**</span><span class="sxs-lookup"><span data-stu-id="12efb-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**simple disk**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-212">Un eje que no está conectado a una controladora RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-212">A spindle that is not connected to a hardware RAID controller.</span></span> <span data-ttu-id="12efb-213">Consulte también un grupo de discos (JBOD).</span><span class="sxs-lookup"><span data-stu-id="12efb-213">See also Just a Bunch Of Disks (JBOD).</span></span>

</dd> <dt>

<span data-ttu-id="12efb-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**proveedor de software**</span><span class="sxs-lookup"><span data-stu-id="12efb-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-215">Software basado en host que expone volúmenes lógicos y funciona en discos.</span><span class="sxs-lookup"><span data-stu-id="12efb-215">Host-based software that exposes logical volumes and operates on disks.</span></span> <span data-ttu-id="12efb-216">Un proveedor de software incluye servicios en tiempo de ejecución en modo kernel, datos de configuración y servicios de administración en modo usuario.</span><span class="sxs-lookup"><span data-stu-id="12efb-216">A software provider includes kernel-mode runtime services, configuration data, and user-mode management services.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**extienda**</span><span class="sxs-lookup"><span data-stu-id="12efb-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**span**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-218">Asignación lineal de volumen o disco de varias extensiones de disco o unidad discontinuas.</span><span class="sxs-lookup"><span data-stu-id="12efb-218">A volume or disk linear mapping of multiple discontinuous disk or drive extents.</span></span> <span data-ttu-id="12efb-219">Las extensiones pueden estar en uno o varios ejes o LUN.</span><span class="sxs-lookup"><span data-stu-id="12efb-219">The extents can be on one or more spindles or LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**giro**</span><span class="sxs-lookup"><span data-stu-id="12efb-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-221">Unidad física de almacenamiento en disco.</span><span class="sxs-lookup"><span data-stu-id="12efb-221">A physical unit of disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**apilamiento**</span><span class="sxs-lookup"><span data-stu-id="12efb-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**stacking**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-223">Acto de construir un volumen o LUN mediante la realización de más de una operación de asignación de bloques lógicos.</span><span class="sxs-lookup"><span data-stu-id="12efb-223">The act of constructing a volume or LUN by performing more than one logical block mapping operation.</span></span> <span data-ttu-id="12efb-224">Un ejemplo es un volumen seccionado reflejado.</span><span class="sxs-lookup"><span data-stu-id="12efb-224">An example is a mirrored striped volume.</span></span> <span data-ttu-id="12efb-225">La apilación más común se produce cuando se usa RAID de software a través de LUN construidos por RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-225">The most common stacking occurs when software RAID is used across LUNs constructed by hardware RAID.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span><span class="sxs-lookup"><span data-stu-id="12efb-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-227">Asignación de volumen o disco que intercalan extensiones contiguas en varios volúmenes, discos o unidades.</span><span class="sxs-lookup"><span data-stu-id="12efb-227">A volume or disk mapping that interleaves contiguous extents across multiple volumes, disks, or drives.</span></span> <span data-ttu-id="12efb-228">Esta asignación también se denomina RAID 0.</span><span class="sxs-lookup"><span data-stu-id="12efb-228">This mapping is also called RAID 0.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**estatus**</span><span class="sxs-lookup"><span data-stu-id="12efb-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**status**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-230">La disponibilidad actual de un volumen, un disco o una unidad.</span><span class="sxs-lookup"><span data-stu-id="12efb-230">The current availability of a volume, disk, or drive.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsistema**</span><span class="sxs-lookup"><span data-stu-id="12efb-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsystem**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-232">La creación de instancias del software de proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="12efb-232">The instantiation of hardware-provider software.</span></span> <span data-ttu-id="12efb-233">Un subsistema contiene al menos un controlador y una unidad.</span><span class="sxs-lookup"><span data-stu-id="12efb-233">A subsystem contains at least one controller and one drive.</span></span> <span data-ttu-id="12efb-234">Si el subsistema es externo al equipo, una o más rutas de acceso de red conectan el subsistema al equipo.</span><span class="sxs-lookup"><span data-stu-id="12efb-234">If the subsystem is external to the computer, one or more network paths connect the subsystem to the computer.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**Estado de transición**</span><span class="sxs-lookup"><span data-stu-id="12efb-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**transition state**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-236">Estado de la asignación lógica a física que está en curso.</span><span class="sxs-lookup"><span data-stu-id="12efb-236">Status of the logical to physical mapping that is undergoing change.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco no inicializado**</span><span class="sxs-lookup"><span data-stu-id="12efb-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**uninitialized disk**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-238">Un disco que no es miembro de un paquete.</span><span class="sxs-lookup"><span data-stu-id="12efb-238">A disk that is not a member of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco sin máscara**</span><span class="sxs-lookup"><span data-stu-id="12efb-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmasked disk**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-240">Disco que es visible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="12efb-240">A disk that is visible to the operating system.</span></span> <span data-ttu-id="12efb-241">El contenido de un disco sin máscara es visible para los administradores de volúmenes de software, los sistemas de archivos, etc.</span><span class="sxs-lookup"><span data-stu-id="12efb-241">The contents of an unmasked disk are visible to software volume managers, file systems, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="12efb-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**cantidad**</span><span class="sxs-lookup"><span data-stu-id="12efb-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="12efb-243">Una serie de extensiones de disco enlazadas a un intervalo virtual prácticamente contiguo de bloques lógicos.</span><span class="sxs-lookup"><span data-stu-id="12efb-243">A number of disk extents bound into a virtually contiguous range of logical blocks.</span></span> <span data-ttu-id="12efb-244">Se puede acceder a un volumen a través de una letra de unidad, una carpeta montada o una ruta de acceso de GUID de volumen.</span><span class="sxs-lookup"><span data-stu-id="12efb-244">A volume can be accessed through a drive letter, a mounted folder, or a volume GUID path.</span></span>

</dd> </dl>

 

 
