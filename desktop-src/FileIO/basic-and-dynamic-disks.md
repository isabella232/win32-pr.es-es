---
description: Describe dos tipos de almacenamiento en disco y describe los estilos de partición.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Discos básicos y dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f134f0dd7c8d81522733d26a6c5efb433d0e425978e1cbffd7edf3b0937b949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582639"
---
# <a name="basic-and-dynamic-disks"></a>Discos básicos y dinámicos

Antes de crear particiones de una unidad u obtener información sobre el diseño de partición de una unidad, primero debe comprender las características y limitaciones de los tipos de almacenamiento en disco básico y dinámico.

Para los fines de este  tema, el término volumen se usa para hacer referencia al concepto de una partición de disco con formato de sistema de archivos válido, normalmente NTFS, que usa el sistema operativo Windows para almacenar archivos. Un volumen tiene un nombre de ruta de acceso win32, se puede enumerar mediante las funciones [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) y [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) y normalmente tiene asignada una letra de unidad, como C:. Para obtener más información sobre volúmenes y sistemas de archivos, vea [Sistemas de archivos](file-systems.md).

En este tema:

-   [Discos básicos](#basic-disks)
-   [Discos dinámicos](#dynamic-disks)
-   [Estilos de partición](#partition-styles)
    -   [registro de arranque maestro](#master-boot-record)
    -   [tabla de particiones GUID](#guid-partition-table)
-   [Detectar el tipo de disco](#detecting-the-type-of-disk)
-   [Temas relacionados](#related-topics)

Hay dos tipos de discos al hacer referencia a tipos de almacenamiento en este contexto: discos *básicos* y *discos dinámicos.* Tenga en cuenta que los tipos de almacenamiento aquí analizados no son los mismos que los discos físicos o los estilos de partición, que están relacionados pero son conceptos independientes. Por ejemplo, hacer referencia a un disco básico no implica un estilo de partición determinado; también es necesario especificar el estilo de partición usado para el disco en discusión. Para obtener una descripción simplificada de cómo un tipo de almacenamiento de disco básico se relaciona con un disco duro físico, vea Dispositivos de disco [y particiones.](disk-devices-and-partitions.md)

## <a name="basic-disks"></a>Discos básicos

*Los discos básicos* son los tipos de almacenamiento más usados con Windows. El término *disco* básico hace referencia a un disco que contiene particiones, como particiones principales y unidades lógicas, y a su vez se les da formato con un sistema de archivos para que se convierta en un volumen para el almacenamiento de archivos. Los discos básicos proporcionan una solución de almacenamiento simple que puede dar cabida a una matriz útil de escenarios de requisitos de almacenamiento cambiantes. Los discos básicos también admiten discos en clúster, discos 1394 del Instituto de Ingenieros eléctricos y electrónicos (IEEE) y unidades extraíbles de bus serie universal (USB). Por motivos de compatibilidad con versiones anteriores, los discos básicos suelen usar el mismo estilo de partición de registro de arranque maestro (MBR) que los discos usados por el sistema operativo Microsoft MS-DOS y todas las versiones de Windows, pero también pueden admitir particiones de tabla de particiones **GUID** (GPT) en sistemas que lo admitan. Para obtener más información sobre los estilos de partición MBR y GPT, vea la sección [Estilos de partición.](#partition-styles)

Puedes agregar más espacio a las particiones existentes principales y unidades lógicas ampliándolas con espacio sin asignar, contiguo y adyacente en el mismo disco. Para extender un volumen básico, debe estar formateado con el sistema de archivos NTFS. Puedes ampliar una unidad lógica en el espacio disponible contiguo en la partición extendida que lo contiene. Si se extiende a una unidad lógica más allá del espacio disponible en la partición extendida, la partición extendida crece para incluir la unidad lógica siempre que la partición extendida vaya seguida de un espacio contiguo y sin asignar. Para obtener más información, vea [Cómo funcionan los discos y volúmenes básicos.](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10))

Las siguientes operaciones solo se pueden realizar en discos básicos:

-   Crear y eliminar particiones principales y extendidas.
-   Crear y eliminar unidades lógicas dentro de una partición extendida.
-   Dar formato a una partición y marcarla como activa.

## <a name="dynamic-disks"></a>Discos dinámicos

> [!NOTE]
> Para todos los usos excepto los volúmenes de arranque reflejado (mediante un volumen reflejado para hospedar el sistema operativo), los discos dinámicos están en desuso. Para los datos que requieren resistencia frente a errores de unidad, use Espacios de almacenamiento, una solución de virtualización de almacenamiento resistente. Para obtener más información, [vea Espacios de almacenamiento información general.](/windows-server/storage/storage-spaces/overview)

Los *discos dinámicos* proporcionan características que los discos básicos no tienen, como la capacidad de crear volúmenes que abarquen varios discos (volúmenes abarcados y seccionados) y la capacidad de crear volúmenes tolerantes a errores (volúmenes reflejados y RAID-5). Al igual que los discos básicos, los discos dinámicos pueden usar los estilos de partición MBR o GPT en sistemas que admiten ambos. Todos los volúmenes de discos dinámicos se conocen como volúmenes dinámicos. Los discos dinámicos ofrecen mayor flexibilidad para la administración de volúmenes porque usan una base de datos para realizar un seguimiento de la información sobre los volúmenes dinámicos en el disco y sobre otros discos dinámicos del equipo. Dado que cada disco dinámico de un equipo almacena una réplica de la base de datos de disco dinámico, por ejemplo, una base de datos de disco dinámico dañada puede reparar un disco dinámico mediante el uso de la base de datos en otro disco dinámico. La ubicación de la base de datos viene determinada por el estilo de partición del disco. En las particiones MBR, la base de datos se encuentra en los últimos 1 megabytes (MB) del disco. En las particiones GPT, la base de datos se encuentra en una partición reservada (oculta) de 1 MB.

Los discos dinámicos son una forma independiente de administración de volúmenes que permite que los volúmenes tengan extensiones no continuas en uno o varios discos físicos. Los discos y volúmenes dinámicos se basan en el Administrador de discos lógicos (LDM) y el Servicio de disco virtual (VDS) y sus características asociadas. Estas características permiten realizar tareas como convertir discos básicos en discos dinámicos y crear volúmenes tolerantes a errores. Para fomentar el uso de discos dinámicos, se quitó la compatibilidad con volúmenes de varias particiones de los discos básicos y ahora se admite exclusivamente en discos dinámicos.

Las siguientes operaciones solo se pueden realizar en discos dinámicos:

-   Cree y elimine volúmenes simples, abarcados, seccionados, reflejados y RAID-5.
-   Extienda un volumen simple o abarcado.
-   Quite un reflejo de un volumen reflejado o rompa el volumen reflejado en dos volúmenes.
-   Reparar volúmenes reflejados o RAID-5.
-   Reactivar un disco que falta o está sin conexión.

Otra diferencia entre los discos básicos y dinámicos es que los volúmenes de disco dinámicos se pueden componer de un conjunto de extensiones no continuas en uno o varios discos físicos. Por el contrario, un volumen de un disco básico consta de un conjunto de extensiones contiguas en un solo disco. Debido a la ubicación y el tamaño del espacio en disco que necesita la base de datos LDM, Windows no puede convertir un disco básico en un disco dinámico a menos que haya al menos 1 MB de espacio sin usar en el disco.

Independientemente de si los discos dinámicos de un sistema usan el estilo de partición MBR o GPT, puede crear hasta 2000 volúmenes dinámicos en un sistema, aunque el número recomendado de volúmenes dinámicos es 32 o menos. Para más información y otras consideraciones sobre el uso de volúmenes y discos dinámicos, consulte [Discos dinámicos y volúmenes.](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10))

Para obtener más características de y escenarios de uso para discos dinámicos, consulte [¿Qué son los discos dinámicos y los volúmenes?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

Las operaciones comunes a los discos básicos y dinámicos son las siguientes:

-   Admite estilos de partición MBR y GPT.
-   Compruebe las propiedades del disco, como la capacidad, el espacio disponible y el estado actual.
-   Vea las propiedades de partición, como desplazamiento, longitud, tipo y si la partición se puede usar como volumen del sistema en el arranque.
-   Vea las propiedades del volumen, como tamaño, asignación de letra de unidad, etiqueta, tipo, nombre de ruta de acceso de Win32, tipo de partición y sistema de archivos.
-   Establezca asignaciones de letra de unidad para volúmenes o particiones de disco y para dispositivos CD-ROM.
-   Convertir un disco básico en un disco dinámico o un disco dinámico en un disco básico.

A menos que se especifique lo contrario, Windows particiona inicialmente una unidad como un disco básico de forma predeterminada. Debe convertir explícitamente un disco básico en un disco dinámico. Sin embargo, hay consideraciones sobre el espacio en disco que deben tenerse en cuenta antes de intentar hacerlo. Para obtener más información, [vea How to Convert to Basic and Dynamic Disks in Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Estilos de partición

*Los estilos de* partición, también *denominados* esquemas de partición, son un término que hace referencia a la estructura subyacente concreta del diseño del disco y a cómo se organiza realmente la creación de particiones, cuáles son las funcionalidades y también cuáles son las limitaciones. Para arrancar Windows, las implementaciones de BIOS en equipos basados en x86 y x64 requieren un disco básico que debe contener al menos una partición de registro de arranque maestro (MBR) marcada como activa donde se almacena información sobre el sistema operativo Windows (pero no necesariamente toda la instalación del sistema operativo) y dónde se almacena información sobre las particiones en el disco. Esta información se coloca en lugares independientes y estos dos lugares pueden encontrarse en particiones independientes o en una sola partición. El resto del almacenamiento en disco físico se puede configurar como varias combinaciones de los dos estilos de partición disponibles, que se describen en las secciones siguientes. Para obtener más información sobre otros tipos de sistema, vea el tema de TechNet sobre los estilos [de partición](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10)).

Los discos dinámicos siguen escenarios de uso ligeramente diferentes, como se ha descrito anteriormente, y la forma en que usan los dos estilos de partición se ve afectada por ese uso. Dado que los discos dinámicos no se usan normalmente para contener volúmenes de arranque del sistema, esta explicación se simplifica para excluir escenarios de casos especiales. Para obtener información más detallada sobre los diseños de bloques de datos [](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) de partición y los escenarios de uso de discos básicos o dinámicos relacionados con los estilos de partición, vea Cómo funcionan los discos y volúmenes básicos y cómo funcionan los discos dinámicos y [los volúmenes.](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10))

### <a name="master-boot-record"></a>registro de arranque maestro

Todos los equipos basados en x86 y x64 que ejecutan Windows pueden usar el estilo de partición conocido como registro de arranque *maestro* (MBR). El estilo de partición MBR contiene una tabla de particiones que describe dónde se encuentran las particiones en el disco. Dado que MBR es el único estilo de partición disponible en equipos basados en x86 antes de Windows Server 2003 con Service Pack 1 (SP1), no es necesario elegir este estilo. Se usa automáticamente.

Puede crear hasta cuatro particiones en un disco básico mediante el esquema de partición MBR: cuatro particiones principales o tres principales y una extendida. La partición extendida puede contener una o varias unidades lógicas. En la ilustración siguiente se muestra un diseño de ejemplo de tres particiones principales y una partición extendida en un disco básico mediante MBR. La partición extendida contiene cuatro unidades lógicas extendidas. La partición extendida puede o no estar ubicada al final del disco, pero siempre es un único espacio contiguo para las unidades lógicas de 1 a n.

![tres particiones principales y una partición extendida en un disco básico mediante mbr](images/basic-mbr.png)

Cada partición, ya sea principal o extendida, se puede formatear para que sea un volumen Windows, con una correlación uno a uno de volumen a partición. En otras palabras, una sola partición no puede contener más de un solo volumen. En este ejemplo, habría un total de siete volúmenes disponibles para Windows almacenamiento de archivos. Una partición sin formato no está disponible para el almacenamiento de archivos en Windows.

El diseño de MBR de disco dinámico es muy similar al diseño mbr de disco básico, salvo que solo se permite una partición principal (denominada partición LDM), no se permite ninguna partición extendida y hay una partición oculta al final del disco para la base de datos LDM. Para obtener más información sobre LDM, consulte la [sección Discos dinámicos.](#basic-and-dynamic-disks)

### <a name="guid-partition-table"></a>tabla de particiones GUID

Los sistemas que ejecutan Windows Server 2003 con SP1 y versiones posteriores pueden usar un estilo de partición conocido como tabla de particiones (GPT) de identificador único global **(GUID),** además del estilo de partición MBR. Un disco básico que use el estilo de partición GPT puede tener hasta 128 particiones principales, mientras que los discos dinámicos tendrán una sola partición LDM como con la creación de particiones mbr. Dado que los discos básicos que usan la creación de particiones GPT no le limitan a cuatro particiones, no es necesario crear particiones extendidas ni unidades lógicas.

El estilo de partición GPT también tiene las siguientes propiedades:

-   Permite particiones de más de 2 terabytes.
-   Se ha agregado confiabilidad de la replicación y la protección de comprobación de redundancia cíclica (CRC) de la tabla de particiones.
-   Compatibilidad con GUID de tipo **de partición** adicionales definidos por fabricantes de equipos originales (OEM), proveedores de software independientes (ISV) y otros sistemas operativos.

El diseño de creación de particiones GPT para un disco básico se muestra en la ilustración siguiente.

![Diseño de gpt](images/basic-gpt.png)

El área de PROTECCIÓN de MBR existe en un diseño de partición GPT para la compatibilidad con versiones anteriores con las utilidades de administración de discos que operan en MBR. El encabezado GPT define el intervalo de direcciones de bloque lógico que pueden ser utilizables por las entradas de partición. El encabezado GPT también define su ubicación en el disco, su **GUID** y una suma de comprobación de redundancia cíclica de 32 bits (CRC32) que se usa para comprobar la integridad del encabezado GPT. Cada **entrada de** partición GUID comienza con un GUID de tipo de partición. El GUID de tipo de partición de 16 **bytes**, que es similar a un identificador de sistema en la tabla de particiones de un disco MBR, identifica el tipo de datos que contiene la partición e identifica cómo se usa la partición, por ejemplo, si es un disco básico o un disco dinámico. Tenga en cuenta que cada **entrada de partición GUID** tiene una copia de seguridad.

Los diseños de **partición GPT** de disco dinámico son similares a este ejemplo de disco básico, pero, como se indicó anteriormente, solo tienen una entrada de partición LDM en lugar de 1-n particiones principales, como se permite en los discos básicos. También hay una partición de base de datos LDM oculta con una entrada de **partición GUID** correspondiente. Para obtener más información sobre LDM, consulte la [sección Discos dinámicos.](#basic-and-dynamic-disks)

## <a name="detecting-the-type-of-disk"></a>Detección del tipo de disco

No hay ninguna función específica para detectar mediante programación el tipo de disco en el que se encuentra un archivo o directorio determinado. Hay un método indirecto.

* Pase la ruta de acceso del archivo o directorio [**a GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) para obtener el punto de montaje.
* Pase el punto de montaje [**a GetVolumeNameForVolumeMountPoint para**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) obtener el nombre del volumen.
* Quite la barra diagonal inversa final del nombre del volumen.
* Pase el nombre del volumen sin la barra diagonal inversa final a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir el volumen.
* Use [**IOCTL \_ VOLUME GET VOLUME DISK \_ \_ \_ \_ EXTENTS**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) con el identificador de volumen para obtener los números de disco.
* Use los números de disco para construir las rutas de acceso del disco, como " \\ \\ ? \\ PhysicalDrive *X".*
* Pase cada ruta de acceso de disco [**a CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir el disco.
* Use [**IOCTL \_ DISK GET DRIVE LAYOUT EX \_ \_ \_ \_ para**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) obtener la lista de particiones.
* Compruebe **partitionType para** cada entrada de la lista de particiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de volúmenes](about-volume-management.md)
</dt> <dt>

[Referencia técnica de discos y volúmenes básicos](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Referencia técnica de discos y volúmenes dinámicos](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Basic Storage versus Dynamic Storage en Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
