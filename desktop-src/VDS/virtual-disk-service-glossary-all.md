---
description: En esta sección se proporciona un glosario de términos técnicos usados en la documentación de Virtual Disk Service (VDS).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glosario de Virtual Disk Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7e73e9de8f6c30b69f2e39e78fae36e5c3ea547cccfed2f25f9a15327e3f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602998"
---
# <a name="virtual-disk-service-glossary"></a>Glosario de Virtual Disk Service

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

En esta sección se proporciona un glosario de términos técnicos usados en la documentación de Virtual Disk Service (VDS).

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuración de automagic**
</dt> <dd>

Proveedor RAID de hardware que proporciona un conjunto de reglas para elegir el remapping de bloques lógicos de LUN en función de atributos simples. Los proveedores de Automagic también pueden modificar dinámicamente la asignación para la administración de errores o rendimiento.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**sugerencias de automagic**
</dt> <dd>

Información proporcionada a un proveedor de automagic para guiar la configuración de bloques lógicos de LUN. Las sugerencias incluyen información sobre la tolerancia a errores deseada, la atomicidad física y el patrón de acceso de E/S previsto.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco básico**
</dt> <dd>

Un disco administrado por el proveedor de software más sencillo posible. El proveedor de discos básico solo admite volúmenes que se asignan directamente a estructuras de datos de configuración de particiones.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**Vinculante**
</dt> <dd>

Seleccionar para un conjunto de asignaciones a recursos físicos.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**Convertir**
</dt> <dd>

Proceso de conversión de un disco básico en un disco dinámico.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**Configuración**
</dt> <dd>

Colección de los parámetros operativos que suministran la asignación de un volumen, o LUN, a recursos físicos.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**Controlador**
</dt> <dd>

Un programa de software que contiene la inteligencia en tiempo de ejecución de un proveedor de hardware.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**Disco**
</dt> <dd>

UN DISCO físico o UN LUN RAID de hardware. Los discos son destinos para la carga de E/S de almacenamiento en tiempo de ejecución; Plug and Play (PNP) no distingue entre JBOD y LUN.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**bandeja de disco**
</dt> <dd>

Subconjunto de un paquete que se usa para exportar o importar volúmenes desde un paquete.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**paquete de disco**
</dt> <dd>

Consulte *pack*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**Conducir**
</dt> <dd>

Eje de disco físico dentro de un subsistema RAID de hardware. El subsistema enlaza las unidades a LUN.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinámico**
</dt> <dd>

Un disco administrado por un proveedor RAID de software compatible con la reconfiguración flexible del volumen. Un disco dinámico usa una partición como contenedor para los volúmenes; no hay ninguna asignación garantizada.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuración explícita**
</dt> <dd>

Una configuración con los parámetros, incluido el tipo de volumen y el diseño exacto, para una colección de volúmenes de destino.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**exportar**
</dt> <dd>

El acto de mover una bandeja de disco y todos los volúmenes contenidos en esa bandeja fuera de un paquete.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**Grado**
</dt> <dd>

Una gama contigua de sectores lógicos que contribuyen a un único volumen o disco. Una extensión también puede ser un intervalo de sectores sin asignar. Normalmente, un sistema de archivos muestra los detalles de la extensión a un usuario final.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabla de particiones GUID (GPT)**
</dt> <dd>

Estructuras usadas por el firmware EFI. GPT es uno de los dos formatos de datos de configuración de software de nivel más bajo que usa el firmware de la plataforma para localizar un sistema operativo de arranque u otra imagen ejecutable.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**proveedor de hardware**
</dt> <dd>

Una colección de software que se ejecuta en el host, un adaptador de bus y, posiblemente, un subsistema de almacenamiento externo que funciona conjuntamente para la superficie y administración de LUN RAID. Los proveedores de hardware para la mayoría de los subsistemas de almacenamiento externos solo contienen software basado en host en modo de usuario.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**Salud**
</dt> <dd>

El estado actual de administración de errores de un volumen o un LUN.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**
</dt> <dd>

Agregar temporalmente un plex de volumen a un volumen.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**Importación**
</dt> <dd>

El acto de mover una bandeja de disco y todos sus volúmenes a un paquete existente.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**solo un grupo de discos (JBOD)**
</dt> <dd>

Colección de ejes físicos sin el control coordinado proporcionado por un dispositivo RAID de hardware.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**número de bloque lógico (LBN)**
</dt> <dd>

Unidad direccionable más pequeña de datos de almacenamiento. LBN se usa con protocolos de comandos de E/S.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**asignación de bloques lógicos**
</dt> <dd>

Transformación de los bloques lógicos presentados a un proveedor a los expuestos por el proveedor.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**número de unidad lógica (LUN)**
</dt> <dd>

Unidad de almacenamiento direccionable físicamente tal como se muestra en un subsistema RAID de hardware. Este término también puede hacer referencia al identificador SCSI de la unidad de almacenamiento.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Número lun**
</dt> <dd>

Número que un proveedor de hardware VDS asigna a un LUN en una matriz. Esto no es lo mismo que el "número de unidad lógica" en la dirección SCSI del disco.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**servicio de administración**
</dt> <dd>

Un programa de software que se ejecuta según sea necesario para realizar la configuración del volumen, la supervisión o el control de errores.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**Asignación**
</dt> <dd>

Volumen que se expone al sistema operativo y tiene un nombre de volumen asociado (una letra de unidad). Un sistema de archivos puede acceder a un volumen.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**Enmascarar**
</dt> <dd>

Un disco no reconocido por el sistema operativo. Otro host de equipo o software de la pila de disco puede enmascarar un disco mediante el subsistema RAID de hardware, el conmutador, la reserva SCSI.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**creación de particiones de registros de arranque maestro (MBR)**
</dt> <dd>

MBR es uno de los dos formatos de datos de configuración de software de nivel más bajo y lo usa el firmware del BIOS para buscar una imagen de sistema operativo de arranque.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**Miembro**
</dt> <dd>

Colección de extensiones de disco concatenadas contenidas en uno más discos. Un disco solo puede contribuir a un miembro de un volumen.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**Espejo**
</dt> <dd>

Asignación de volumen o disco que mantiene dos o más copias de datos idénticas. El tipo de asignación también se denomina RAID Nivel 1.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**Pack**
</dt> <dd>

Colección de volúmenes lógicos y discos subyacentes. Un paquete es la unidad de cierre transitivo de un volumen. Los paquetes de discos dinámicos y los grupos de discos son términos para el mismo elemento.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**franja de paridad**
</dt> <dd>

Asignación de volumen o disco que mantiene la información de comprobación de paridad, así como los datos. Cada proveedor proporciona el esquema exacto de asignación y protección. Incluye RAID 3, 4, 5 y 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuración dirigida parcialmente**
</dt> <dd>

Configuración de volumen o disco que no es totalmente explícita. Se especifican el tipo de enlace y una colección de recursos de destino; el diseño real no es . La configuración dirigida parcialmente es la configuración de volumen más común.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**Partición**
</dt> <dd>

Un intervalo contiguo de sectores lógicos descritos por una sola entrada en la estructura MBR o GPT. En los discos básicos, las particiones corresponden directamente a volúmenes simples. Las estructuras de partición se comparten entre el firmware de la plataforma BIOS o EFI y un sistema operativo u otra imagen de arranque.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**Camino**
</dt> <dd>

Ruta de acceso de un equipo a un LUN de disco o hardware externo.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**Plex**
</dt> <dd>

Un miembro de un volumen reflejado o LUN.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**Puerto**
</dt> <dd>

Punto de conexión de una ruta de acceso en un disco.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**Matriz redundante de discos independientes (RAID)**
</dt> <dd>

Colección de técnicas para administrar varios discos.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**servicio en tiempo de ejecución**
</dt> <dd>

Un programa de software que se ejecuta en una solicitud de E/S.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco simple**
</dt> <dd>

Eje que no está conectado a una controladora RAID de hardware. Consulte también Just a Bunch Of Disks (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**proveedor de software**
</dt> <dd>

Software basado en host que expone volúmenes lógicos y opera en discos. Un proveedor de software incluye servicios en tiempo de ejecución en modo kernel, datos de configuración y servicios de administración en modo de usuario.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**envergadura**
</dt> <dd>

Asignación lineal de volumen o disco de varias extensiones de disco o unidad discontinuas. Las extensiones pueden estar en uno o varios ejes o LUN.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Huso**
</dt> <dd>

Unidad física de almacenamiento en disco.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**Apilamiento**
</dt> <dd>

El acto de construir un volumen o LUN realizando más de una operación de asignación de bloques lógicos. Un ejemplo es un volumen seccionado reflejado. El apilamiento más común se produce cuando se usa RAID de software en lun creados por RAID de hardware.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Raya**
</dt> <dd>

Asignación de volúmenes o discos que intercala extensiones contiguas en varios volúmenes, discos o unidades. Esta asignación también se denomina RAID 0.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**Estado**
</dt> <dd>

Disponibilidad actual de un volumen, disco o unidad.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**Subsistema**
</dt> <dd>

Creación de instancias de software de proveedor de hardware. Un subsistema contiene al menos un controlador y una unidad. Si el subsistema es externo al equipo, una o varias rutas de acceso de red conectan el subsistema al equipo.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**estado de transición**
</dt> <dd>

Estado de la asignación lógica a física que está en proceso de cambio.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco sin inicializar**
</dt> <dd>

Disco que no es miembro de un paquete.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco sin máscara**
</dt> <dd>

Disco visible para el sistema operativo. El contenido de un disco sin máscara es visible para los administradores de volúmenes de software, los sistemas de archivos, entre otros.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**Volumen**
</dt> <dd>

Número de extensiones de disco enlazadas a un intervalo de bloques lógicos prácticamente contiguo. Se puede acceder a un volumen a través de una letra de unidad, una carpeta montada o una ruta de acceso GUID de volumen.

</dd> </dl>

 

 
