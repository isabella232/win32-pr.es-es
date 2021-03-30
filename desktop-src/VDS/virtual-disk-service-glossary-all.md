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
# <a name="virtual-disk-service-glossary"></a>Glosario de servicio de disco virtual

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

En esta sección se proporciona un glosario de términos técnicos que se usan en la documentación del servicio de disco virtual (VDS).

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuración de automagic**
</dt> <dd>

Proveedor RAID de hardware que proporciona un conjunto de reglas para elegir la reasignación de bloques lógicos de LUN basada en atributos simples. Los proveedores de automagic también pueden modificar dinámicamente la asignación para el rendimiento o la administración de errores.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**Sugerencias de automagic**
</dt> <dd>

Información proporcionada a un proveedor de automagic para guiar la configuración de bloque lógico de LUN. Las sugerencias incluyen información sobre la tolerancia a errores deseada, la atomicidad física y el patrón de acceso de e/s previsto.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco básico**
</dt> <dd>

Un disco administrado por el proveedor de software más sencillo posible. El proveedor de discos básico solo admite los volúmenes que se asignan directamente a las estructuras de datos de configuración de la partición.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**enlace**
</dt> <dd>

Seleccionar para un conjunto de asignaciones a recursos físicos.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**verso**
</dt> <dd>

Proceso de conversión de un disco básico a un disco dinámico.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuraciones**
</dt> <dd>

Colección de los parámetros operativos que proporcionan la asignación de un volumen, o LUN, a los recursos físicos.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**módem**
</dt> <dd>

Programa de software que contiene la inteligencia en tiempo de ejecución de un proveedor de hardware.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**discos**
</dt> <dd>

Un disco físico o un LUN RAID de hardware. Los discos son destinos para la carga de e/s de almacenamiento en tiempo de ejecución. Plug and Play (PNP) no distingue entre JBOD y LUN.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disco duro**
</dt> <dd>

Un subconjunto de un paquete que se usa para exportar o importar volúmenes de un paquete.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**paquete de disco**
</dt> <dd>

Vea *Pack*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**dispositivo**
</dt> <dd>

Un eje de disco físico en un subsistema RAID de hardware. El subsistema enlaza las unidades a los LUN.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinámico**
</dt> <dd>

Un disco administrado por un proveedor RAID de software compatible con la reconfiguración de volumen flexible. Un disco dinámico utiliza una partición como contenedor de volúmenes; no hay ninguna asignación garantizada.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuración explícita**
</dt> <dd>

Una configuración con los parámetros, incluido el tipo de volumen y el diseño exacto, para una colección de volúmenes de destino.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**Portada**
</dt> <dd>

El acto de mover un disco duro y todos los volúmenes contenidos en ese platter de un paquete.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**expresa**
</dt> <dd>

Un intervalo contiguo de sectores lógicos que contribuyen a un solo volumen o disco. Una extensión también puede ser un rango de sectores sin asignar. Normalmente, un sistema de archivos muestra los detalles de la extensión a un usuario final.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabla de particiones GUID (GPT)**
</dt> <dd>

Estructuras utilizadas por el firmware EFI. GPT es uno de los dos formatos de datos de configuración de software de nivel más bajo usados por el firmware de plataforma para buscar un sistema operativo de arranque u otra imagen ejecutable.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**proveedor de hardware**
</dt> <dd>

Una colección de software que se ejecuta en el host, un adaptador de bus y, posiblemente, un subsistema de almacenamiento externo que funciona conjuntamente para exponer y administrar LUN de RAID. Los proveedores de hardware de la mayoría de los subsistemas de almacenamiento externo solo contienen software basado en el host y en el modo de usuario.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**enfermedad**
</dt> <dd>

El estado actual de la administración de errores de un volumen o LUN.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**reserva activa**
</dt> <dd>

Agregar temporalmente un Plex de volumen a un volumen.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**importar**
</dt> <dd>

El acto de mover un platter Disk y todos sus volúmenes a un paquete existente.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**solo un grupo de discos (JBOD)**
</dt> <dd>

Colección de ejes físicos sin el control coordinado proporcionado por un dispositivo RAID de hardware.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**número de bloque lógico (LBN)**
</dt> <dd>

La unidad más pequeña de datos de almacenamiento. LBN se usa con protocolos de comandos de e/s.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**asignación de bloques lógicos**
</dt> <dd>

La transformación de los bloques lógicos que se presentan a un proveedor a los expuestos por el proveedor.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**número de unidad lógica (LUN)**
</dt> <dd>

Una unidad de almacenamiento direccionable físicamente, expuesta por un subsistema RAID de hardware. Este término también puede hacer referencia al identificador SCSI de la unidad de almacenamiento.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Número de LUN**
</dt> <dd>

Número que un proveedor de hardware de VDS asigna a un LUN en una matriz. No es lo mismo que el "número de unidad lógica" en la dirección SCSI del disco.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**servicio de administración**
</dt> <dd>

Programa de software que se ejecuta según sea necesario para realizar la configuración, la supervisión o el control de errores del volumen.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**asociaciones**
</dt> <dd>

Un volumen que se expone al sistema operativo y tiene un nombre de volumen asociado (una letra de unidad). Un volumen es accesible desde un sistema de archivos.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**enmascaramiento**
</dt> <dd>

Un disco no reconocido por el sistema operativo. Un disco se puede enmascarar mediante el subsistema RAID de hardware, el conmutador, la reserva SCSI por otro host del equipo o el software de la pila de discos.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**creación de particiones de registro de arranque maestro (MBR)**
</dt> <dd>

MBR es uno de los dos formatos de datos de configuración de software de nivel más bajo y lo utiliza el firmware de BIOS para buscar una imagen de sistema operativo de arranque.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**miembro**
</dt> <dd>

Colección de extensiones de disco concatenadas contenidas en uno o más discos. Un disco puede contribuir a un solo miembro de un volumen.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**creación**
</dt> <dd>

Asignación de volumen o disco que mantiene dos o más copias de datos idénticas. El tipo de asignación también se denomina RAID nivel 1.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**embalaje**
</dt> <dd>

Una colección de volúmenes lógicos y discos subyacentes. Un paquete es la unidad de cierre transitiva de un volumen. Los paquetes de discos dinámicos y los grupos de discos son términos para el mismo elemento.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**franja de paridad**
</dt> <dd>

Asignación de volumen o disco que mantiene la información de comprobación de la paridad, así como los datos. Cada proveedor proporciona la asignación y el esquema de protección exactos. Incluye RAID 3, 4, 5 y 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuración dirigida parcialmente**
</dt> <dd>

Un volumen o una configuración de disco que no es totalmente explícita. Se especifican el tipo de enlace y una colección de recursos de destino; el diseño real no es. La configuración dirigida parcialmente es la configuración de volumen más común.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**divide**
</dt> <dd>

Intervalo contiguo de sectores lógicos descrito por una sola entrada en la estructura MBR o GPT. En los discos básicos, las particiones se corresponden directamente con volúmenes simples. Las estructuras de partición se comparten entre el firmware de la plataforma BIOS o EFI, y un sistema operativo u otra imagen de arranque.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**camino**
</dt> <dd>

La ruta de acceso de un equipo a un disco o LUN de hardware externo.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**complejos**
</dt> <dd>

Un miembro de un volumen reflejado o LUN.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**casilla**
</dt> <dd>

Extremo de una ruta de acceso en un disco.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**matriz redundante de discos independientes (RAID)**
</dt> <dd>

Colección de técnicas para administrar varios discos.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**servicio de tiempo de ejecución**
</dt> <dd>

Programa de software que se ejecuta en una solicitud de e/s.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco simple**
</dt> <dd>

Un eje que no está conectado a una controladora RAID de hardware. Consulte también un grupo de discos (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**proveedor de software**
</dt> <dd>

Software basado en host que expone volúmenes lógicos y funciona en discos. Un proveedor de software incluye servicios en tiempo de ejecución en modo kernel, datos de configuración y servicios de administración en modo usuario.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**extienda**
</dt> <dd>

Asignación lineal de volumen o disco de varias extensiones de disco o unidad discontinuas. Las extensiones pueden estar en uno o varios ejes o LUN.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**giro**
</dt> <dd>

Unidad física de almacenamiento en disco.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**apilamiento**
</dt> <dd>

Acto de construir un volumen o LUN mediante la realización de más de una operación de asignación de bloques lógicos. Un ejemplo es un volumen seccionado reflejado. La apilación más común se produce cuando se usa RAID de software a través de LUN construidos por RAID de hardware.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**
</dt> <dd>

Asignación de volumen o disco que intercalan extensiones contiguas en varios volúmenes, discos o unidades. Esta asignación también se denomina RAID 0.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**estatus**
</dt> <dd>

La disponibilidad actual de un volumen, un disco o una unidad.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsistema**
</dt> <dd>

La creación de instancias del software de proveedor de hardware. Un subsistema contiene al menos un controlador y una unidad. Si el subsistema es externo al equipo, una o más rutas de acceso de red conectan el subsistema al equipo.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**Estado de transición**
</dt> <dd>

Estado de la asignación lógica a física que está en curso.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco no inicializado**
</dt> <dd>

Un disco que no es miembro de un paquete.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco sin máscara**
</dt> <dd>

Disco que es visible para el sistema operativo. El contenido de un disco sin máscara es visible para los administradores de volúmenes de software, los sistemas de archivos, etc.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**cantidad**
</dt> <dd>

Una serie de extensiones de disco enlazadas a un intervalo virtual prácticamente contiguo de bloques lógicos. Se puede acceder a un volumen a través de una letra de unidad, una carpeta montada o una ruta de acceso de GUID de volumen.

</dd> </dl>

 

 
