---
description: Disk (objeto)
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Disk (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d629f642d83c9e2c6954a4f09fe09091a2bbce9
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554060"
---
# <a name="disk-object"></a>Disk (objeto)

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de disco modela un disco físico basado en host. El proveedor de software que se ejecuta en el host local puede tener acceso a un LUN como disco cuando el objeto LUN se desenmascara en el host local. Para obtener más información sobre el enmascaramiento de LUN, vea el [objeto LUN](lun-object.md).

Cada objeto de disco contribuye exactamente a un objeto de paquete. sin embargo, un disco puede contribuir con extensiones a cualquier número de volúmenes de un paquete. Puede designar un disco como reserva activa.

## <a name="partition-to-volume-mapping"></a>Asignación de partición a volumen

El sistema operativo incluye compatibilidad con discos básicos y dinámicos. VDS proporciona un proveedor básico y un proveedor dinámico para administrar estos tipos de disco. Los discos básicos nunca son tolerantes a errores. Los discos dinámicos pueden ser tolerantes a errores si el sistema operativo permite dicho enlace de volumen. Los discos básicos y dinámicos pueden contener particiones estructuradas según uno de los siguientes estilos de partición: registro de arranque maestro (MBR) o tabla de particiones GUID (GPT). La creación de particiones MBR tiene hasta cuatro particiones primarias, o tres particiones primarias más una partición extendida con unidades lógicas infinitas. La creación de particiones GPT proporciona hasta 128 particiones principales.

La descripción siguiente es general por naturaleza. Muestra la relación típica entre las particiones y los volúmenes, a las que hay varias excepciones. Para obtener una descripción detallada de la asignación de particiones a volúmenes, consulte la interfaz [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) . La asignación de partición a volumen varía en función del tipo de disco, básico o dinámico.

-   Discos básicos

    Una partición de un disco básico se asigna directamente a un volumen, en la mayoría de los casos, y puede tener el estilo de partición MBR o GPT. En la ilustración siguiente se muestra la asignación de las dos versiones de las particiones MBR. En el primer caso, las particiones (P1 a P4) se asignan directamente a los volúmenes (V1 a v4). Una partición extendida (ext) reemplaza a P4 en el segundo estilo MBR. El número de unidades lógicas dentro de la partición extendida que se asignan a los volúmenes es ilimitado.

    ![Muestra dos opciones de asignación para las particiones de R B.](images/vdsbasicmapping.png)

    Las particiones GPT (P1 a P128) en la siguiente ilustración se asignan directamente a los volúmenes (V1 a v128), si todas las particiones disponibles están en uso. Un disco GPT no hace uso de una partición extendida como una manera de mejorar la facilidad de uso.

    ![Muestra una partición GPT.](images/vdsbasicmappinggpt.png)

-   Discos dinámicos

    Un tipo de partición especial en un disco dinámico se asigna a un gran número de volúmenes. Para obtener un límite Estimado impuesto por el proveedor dinámico, vea el [objeto Pack](pack-object.md). Como se muestra en la siguiente ilustración, puede haber cualquier número de extensiones en P1 que se asignen a los volúmenes.

    ![Muestra un tipo de partición especial en un disco dinámico.](images/vdsdynamicmapping.png)

Independientemente del tipo de disco, un disco puede contener una o varias extensiones de disco. Una extensión de disco es un intervalo contiguo de bloques lógicos expuestos por el disco. Por ejemplo, una extensión de disco puede representar un volumen completo, una parte de un volumen distribuido, un miembro de un volumen seccionado o un complejo de un volumen reflejado.

### <a name="working-with-disks"></a>Trabajar con discos

Use el método [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para agregar un disco a un paquete existente. Los llamadores pueden obtener un puntero a un disco específico seleccionando el objeto de disco deseado de la enumeración que devuelve el método [**IVdsPack:: QueryDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) . Del mismo modo, puede invocar el método [**IVdsDisk:: GetPack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) para determinar qué paquete contiene un disco determinado.

Puede trasladar un disco de un paquete a otro llamando al método [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) . (VDS no admite la migración de un disco básico entre paquetes controlados por el proveedor básico). También puede mover un paquete a otro host moviendo físicamente todos los discos del paquete al nuevo host. El paquete se mueve con los discos y aparece como un paquete externo en el nuevo host. Para obtener instrucciones, consulte [agregar discos externos a un paquete](adding-foreign-disks-to-a-pack.md).

Además de un identificador de objeto, un nombre, una dirección, un tipo de dispositivo y un tipo de medio, las propiedades de objeto de disco incluyen el estado del disco, el estado y las marcas. tamaño en bytes, bytes por sector, sectores por pista y pistas por cilindro; y el tipo de bus y partición.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf), [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)y [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex). **Windows Server 2008:** No se admite la interfaz [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) .<br/> **Windows Vista:** La interfaz [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) no se admite hasta Windows Vista con Service Pack 1 (SP1); Use [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) en su lugar. No se admite la interfaz [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) .<br/> **Windows Server 2003:** No se admiten las interfaces [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)y [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) .<br/> |
| Interfaces que puede exponer este objeto     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). (Consulte el [objeto LUN](lun-object.md) para obtener más interfaces que se exponen si el disco es un LUN).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Enumeraciones asociadas                           | [**VDS \_ \_Marca de disco**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag), [**\_ \_ Estado de disco de VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_status), [**\_ \_ marca de partición de VDS**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag), [**\_ \_ estilo de partición de VDS**](/windows/win32/api/vds/ne-vds-__vds_partition_style)y [**\_ \_ \_ tipo de extensión de disco de VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Estructuras asociadas                             | [**VDS \_ \_Prop**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop). de disco, [**notificación de \_ disco \_ de VDS**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**disco de \_ entrada \_ de VDS**](/windows/desktop/api/Vds/ns-vds-vds_input_disk), [**prop de \_ partición \_ de VDS**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop), [**información de partición de VDS \_ \_ \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt), [**información de partición de VDS \_ \_ \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)y [**extensión de \_ disco \_ de VDS**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto de paquete](pack-object.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> <dt>

[Adición de discos externos a un paquete](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

