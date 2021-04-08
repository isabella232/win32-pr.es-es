---
description: Describe dos tipos de almacenamiento en disco y describe los estilos de partición.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Discos básicos y dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3b52767983c7707f619b83c93e987b51879fdd
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "104003446"
---
# <a name="basic-and-dynamic-disks"></a>Discos básicos y dinámicos

Antes de crear particiones de una unidad u obtener información acerca del diseño de la partición de una unidad, primero debe comprender las características y limitaciones de los tipos de almacenamiento en disco básico y dinámico.

Para los fines de este tema, el término *volumen* se usa para hacer referencia al concepto de una partición de disco formateada con un sistema de archivos válido (normalmente NTFS) que usa el sistema operativo Windows para almacenar archivos. Un volumen tiene un nombre de ruta de acceso de Win32, se puede enumerar mediante las funciones [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) y [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) y, normalmente, tiene una letra de unidad asignada, como C:. Para obtener más información acerca de los volúmenes y los sistemas de archivos, consulte [sistemas de archivos](file-systems.md).

En este tema:

-   [Discos básicos](#basic-disks)
-   [Discos dinámicos](#dynamic-disks)
-   [Estilos de partición](#partition-styles)
    -   [registro de arranque maestro](#master-boot-record)
    -   [tabla de particiones GUID](#guid-partition-table)
-   [Detección del tipo de disco](#detecting-the-type-of-disk)
-   [Temas relacionados](#related-topics)

Hay dos tipos de discos al hacer referencia a los tipos de almacenamiento en este contexto: *discos básicos* y *discos dinámicos*. Tenga en cuenta que los tipos de almacenamiento que se describen aquí no son los mismos que los discos físicos o los estilos de partición, que están relacionados, pero son conceptos independientes. Por ejemplo, si se hace referencia a un disco básico no implica un estilo de partición determinado, también debe especificarse el estilo de partición utilizado para el disco en debate. Para obtener una descripción simplificada de cómo se relaciona un tipo de almacenamiento en disco básico con un disco duro físico, consulte [discos y particiones de disco](disk-devices-and-partitions.md).

## <a name="basic-disks"></a>Discos básicos

Los *discos básicos* son los tipos de almacenamiento que se usan con más frecuencia con Windows. El término *disco básico* hace referencia a un disco que contiene particiones, como particiones primarias y unidades lógicas, y que a su vez están formateadas con un sistema de archivos para convertirse en un volumen para el almacenamiento de archivos. Los discos básicos proporcionan una solución de almacenamiento simple que puede dar cabida a una matriz útil de escenarios de requisitos de almacenamiento variables. Los discos básicos también admiten discos en clúster, discos de Instituto de ingenieros de electricidad y electrónica (IEEE) 1394 y unidades extraíbles de bus serie universal (USB). Por compatibilidad con versiones anteriores, los discos básicos suelen usar el mismo estilo de partición de registro de arranque maestro (MBR) que los discos utilizados por el sistema operativo Microsoft MS-DOS y todas las versiones de Windows, pero también pueden admitir particiones de tabla de particiones **GUID** (GPT) en sistemas que lo admitan. Para obtener más información acerca de los estilos de partición MBR y GPT, consulte la sección [estilos de partición](#partition-styles) .

Puedes agregar más espacio a las particiones existentes principales y unidades lógicas ampliándolas con espacio sin asignar, contiguo y adyacente en el mismo disco. Para extender un volumen básico, debe estar formateado con el sistema de archivos NTFS. Puedes ampliar una unidad lógica en el espacio disponible contiguo en la partición extendida que lo contiene. Si se extiende a una unidad lógica más allá del espacio disponible en la partición extendida, la partición extendida crece para incluir la unidad lógica siempre que la partición extendida vaya seguida de un espacio contiguo y sin asignar. Para obtener más información, vea [Cómo funcionan los discos y volúmenes básicos](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)).

Las siguientes operaciones solo se pueden realizar en discos básicos:

-   Crear y eliminar particiones principales y extendidas.
-   Crear y eliminar unidades lógicas dentro de una partición extendida.
-   Dar formato a una partición y marcarla como activa.

## <a name="dynamic-disks"></a>Discos dinámicos

> [!NOTE]
> En el caso de todos los usos excepto los volúmenes de arranque reflejado (mediante un volumen reflejado para hospedar el sistema operativo), los discos dinámicos están desusados. En el caso de los datos que requieren resistencia frente a errores de unidad, use espacios de almacenamiento, una solución de virtualización de almacenamiento resistente. Para obtener más información, consulte [Introducción a los espacios de almacenamiento](/windows-server/storage/storage-spaces/overview).

Los *discos dinámicos* proporcionan características que no son de los discos básicos, como la capacidad de crear volúmenes que abarquen varios discos (volúmenes distribuidos y seccionados) y la capacidad de crear volúmenes tolerantes a errores (volúmenes reflejados y RAID-5). Al igual que los discos básicos, los discos dinámicos pueden usar los estilos de partición MBR o GPT en los sistemas que admiten ambos. Todos los volúmenes de los discos dinámicos se conocen como volúmenes dinámicos. Los discos dinámicos ofrecen una mayor flexibilidad para la administración de volúmenes porque usan una base de datos para realizar un seguimiento de la información acerca de los volúmenes dinámicos del disco y de otros discos dinámicos del equipo. Dado que cada disco dinámico de un equipo almacena una réplica de la base de datos de disco dinámico, por ejemplo, una base de datos de disco dinámico dañada puede reparar un disco dinámico mediante la base de datos de otro disco dinámico. La ubicación de la base de datos viene determinada por el estilo de partición del disco. En las particiones MBR, la base de datos se encuentra en el último megabyte (MB) del disco. En las particiones GPT, la base de datos se encuentra en una partición reservada de 1 MB (oculta).

Los discos dinámicos son una forma independiente de administración de volúmenes que permite a los volúmenes tener extensiones no contiguas en uno o más discos físicos. Los discos dinámicos y los volúmenes se basan en el administrador de discos lógicos (LDM) y el servicio de disco virtual (VDS) y sus características asociadas. Estas características permiten realizar tareas como la conversión de discos básicos en discos dinámicos y la creación de volúmenes tolerantes a errores. Para fomentar el uso de discos dinámicos, se ha quitado la compatibilidad con volúmenes de varias particiones de los discos básicos y ahora se admite exclusivamente en discos dinámicos.

Las siguientes operaciones solo se pueden realizar en discos dinámicos:

-   Crear y eliminar volúmenes simples, distribuidos, seccionados, reflejados y RAID-5.
-   Extender un volumen simple o distribuido.
-   Quitar un reflejo de un volumen reflejado o dividir el volumen reflejado en dos volúmenes.
-   Reparar volúmenes reflejados o RAID-5.
-   Reactivar un disco que falta o que está sin conexión.

Otra diferencia entre los discos básicos y los dinámicos es que los volúmenes de discos dinámicos pueden estar compuestos por un conjunto de extensiones no contiguas en uno o varios discos físicos. Por el contrario, un volumen en un disco básico se compone de un conjunto de extensiones contiguas en un único disco. Debido a la ubicación y el tamaño del espacio en disco que necesita la base de datos LDM, Windows no puede convertir un disco básico a un disco dinámico a menos que haya al menos 1 MB de espacio sin usar en el disco.

Independientemente de si los discos dinámicos de un sistema usan el estilo de partición MBR o GPT, puede crear hasta 2.000 volúmenes dinámicos en un sistema, aunque el número recomendado de volúmenes dinámicos es 32 o menos. Para obtener información detallada y otras consideraciones sobre el uso de volúmenes y discos dinámicos, consulte [volúmenes y discos dinámicos](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10)).

Para obtener más características de y escenarios de uso de discos dinámicos, consulte [¿Qué son los discos y volúmenes dinámicos?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

Las operaciones comunes a los discos básicos y dinámicos son las siguientes:

-   Admite los estilos de partición MBR y GPT.
-   Compruebe las propiedades del disco, como la capacidad, el espacio libre disponible y el estado actual.
-   Ver las propiedades de la partición, como desplazamiento, longitud, tipo y, si la partición se puede usar como el volumen del sistema en el arranque.
-   Ver las propiedades del volumen, como el tamaño, la asignación de la letra de la unidad, la etiqueta, el tipo, el nombre de la ruta de acceso de Win32, el tipo de partición y el sistema de archivos.
-   Establezca asignaciones de letra de unidad para volúmenes de disco o particiones, y para dispositivos de CD-ROM.
-   Convertir un disco básico en un disco dinámico o en un disco dinámico en un disco básico.

A menos que se especifique lo contrario, Windows particiona inicialmente una unidad como un disco básico de forma predeterminada. Debe convertir explícitamente un disco básico a un disco dinámico. Sin embargo, hay consideraciones de espacio en disco que se deben tener en cuenta antes de intentar hacerlo. Para obtener más información, consulte [How to Convert to Basic and Dynamic Disks in Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Estilos de partición

Los *estilos de partición*, que a veces se denominan *esquemas de partición*, son un término que hace referencia a la estructura subyacente concreta del diseño del disco y cómo se organizan realmente las particiones, cuáles son las capacidades y también cuáles son las limitaciones. Para arrancar Windows, las implementaciones de BIOS en equipos basados en x86 y x64 requieren un disco básico que debe contener al menos una partición de registro de arranque maestro (MBR) marcada como activa, donde la información sobre el sistema operativo Windows (pero no necesariamente toda la instalación del sistema operativo) y dónde se almacena la información acerca de las particiones en el disco. Esta información se coloca en lugares independientes, y estos dos lugares pueden encontrarse en particiones independientes o en una sola partición. El resto del almacenamiento en disco físico se puede configurar como varias combinaciones de los dos estilos de partición disponibles, que se describen en las secciones siguientes. Para obtener más información sobre otros tipos de sistema, vea el tema de TechNet sobre los [estilos de partición](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10)).

Los discos dinámicos siguen escenarios de uso ligeramente diferentes, como se ha descrito anteriormente, y la forma en que usan los dos estilos de partición se ve afectada por ese uso. Dado que los discos dinámicos no se suelen usar para contener volúmenes de arranque del sistema, este debate se simplifica para excluir escenarios de casos especiales. Para obtener información más detallada sobre los diseños de bloques de datos de particiones y los escenarios de uso de disco básico o dinámico relacionados con los estilos de partición, vea cómo funcionan los [discos y volúmenes básicos](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) y [Cómo funcionan los discos dinámicos y los volúmenes](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10)).

### <a name="master-boot-record"></a>registro de arranque maestro

Todos los equipos basados en x86 y x64 que ejecutan Windows pueden usar el estilo de partición conocido como *registro de arranque maestro* (MBR). El estilo de partición MBR contiene una tabla de particiones que describe dónde se encuentran las particiones en el disco. Dado que MBR es el único estilo de partición disponible en equipos basados en x86 anteriores a Windows Server 2003 con Service Pack 1 (SP1), no es necesario elegir este estilo. Se usa automáticamente.

Puede crear hasta cuatro particiones en un disco básico mediante el esquema de partición MBR: cuatro particiones primarias o tres principales y una extendida. La partición extendida puede contener una o más unidades lógicas. En la ilustración siguiente se muestra un diseño de ejemplo de tres particiones primarias y una partición extendida en un disco básico mediante MBR. La partición extendida contiene cuatro unidades lógicas extendidas. La partición extendida puede o no estar ubicada al final del disco, pero siempre es un único espacio contiguo para las unidades lógicas 1-n.

![tres particiones primarias y una partición extendida en un disco básico mediante MBR](images/basic-mbr.png)

Se puede dar formato a cada partición, ya sea principal o extendida, para que sea un volumen de Windows, con una correlación uno a uno de volumen a partición. En otras palabras, una sola partición no puede contener más de un único volumen. En este ejemplo, hay un total de siete volúmenes disponibles para el almacenamiento de archivos en Windows. Una partición sin formato no está disponible para el almacenamiento de archivos en Windows.

El diseño MBR del disco dinámico es muy similar al diseño MBR del disco básico, excepto en que solo se permite una partición principal (denominada partición LDM), no se permite la creación de particiones extendida y hay una partición oculta al final del disco para la base de datos LDM. Para obtener más información sobre el LDM, consulte la sección [discos dinámicos](#basic-and-dynamic-disks) .

### <a name="guid-partition-table"></a>tabla de particiones GUID

Los sistemas que ejecutan Windows Server 2003 con SP1 y versiones posteriores pueden utilizar un estilo de partición conocido como tabla de particiones de identificador único global (**GUID**), además del estilo de partición MBR. Un disco básico que usa el estilo de partición GPT puede tener hasta 128 particiones principales, mientras que los discos dinámicos tendrán una sola partición LDM como con la creación de particiones MBR. Dado que los discos básicos que usan la creación de particiones GPT no limitan a cuatro particiones, no es necesario crear particiones extendidas ni unidades lógicas.

El estilo de partición GPT también tiene las siguientes propiedades:

-   Permite particiones de más de 2 terabytes.
-   Confiabilidad agregada de la protección de replicación y de comprobación de redundancia cíclica (CRC) de la tabla de particiones.
-   Compatibilidad con **GUID** de tipo de partición adicionales definidos por fabricantes de equipos originales (OEM), fabricantes de software independientes (ISV) y otros sistemas operativos.

En la ilustración siguiente se muestra el diseño de particiones GPT para un disco básico.

![diseño de GPT](images/basic-gpt.png)

El área MBR de protección existe en un diseño de partición GPT para la compatibilidad con versiones anteriores de las utilidades de administración de discos que operan en MBR. El encabezado GPT define el intervalo de direcciones de bloques lógicos que pueden usar las entradas de partición. El encabezado GPT también define su ubicación en el disco, su **GUID** y una suma de comprobación de la redundancia cíclica de 32 bits (CRC32) que se usa para comprobar la integridad del encabezado GPT. Cada entrada de partición **GUID** comienza con un GUID de tipo de partición. El **GUID** de tipo de partición de 16 bytes, que es similar a un identificador del sistema en la tabla de particiones de un disco MBR, identifica el tipo de datos que contiene la partición e identifica cómo se usa la partición, por ejemplo, si se trata de un disco básico o dinámico. Tenga en cuenta que cada entrada de partición **GUID** tiene una copia de seguridad.

El diseño de particiones **GPT** de disco dinámico es similar a este ejemplo de disco básico, pero como se indicó anteriormente solo tiene una entrada de partición LDM en lugar de 1-n particiones principales, como se permite en los discos básicos. También hay una partición de base de datos LDM oculta con una entrada de partición **GUID** correspondiente. Para obtener más información sobre el LDM, consulte la sección [discos dinámicos](#basic-and-dynamic-disks) .

## <a name="detecting-the-type-of-disk"></a>Detección del tipo de disco

No hay ninguna función específica para detectar mediante programación el tipo de disco en el que se encuentra un archivo o un directorio determinado. Hay un método indirecto.

* Pase el archivo o la ruta de acceso del directorio a [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) para obtener el punto de montaje.
* Pase el punto de montaje a [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) para obtener el nombre del volumen.
* Quite la barra diagonal inversa final del nombre del volumen.
* Pase el nombre del volumen sin la barra diagonal inversa hacia [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir el volumen.
* Use [**ioctl \_ volumen \_ obtener \_ \_ \_ extensiones de disco de volumen**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) con el identificador de volumen para obtener los números de disco.
* Use los números de disco para construir las rutas de acceso del disco, como " \\ \\ ? \\ PhysicalDrive *X*".
* Pase cada ruta de acceso del disco a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir el disco.
* Use [**ioctl \_ disco \_ Get \_ Drive \_ layout \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) para obtener la lista de particiones.
* Compruebe el valor de **origen partitiontype** para cada entrada de la lista de particiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de volúmenes](about-volume-management.md)
</dt> <dt>

[Referencia técnica de discos y volúmenes básicos](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Referencia técnica de volúmenes y discos dinámicos](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Almacenamiento básico frente a almacenamiento dinámico en Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
