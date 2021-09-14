---
description: Objeto de disco
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Objeto de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d629f642d83c9e2c6954a4f09fe09091a2bbce9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890396"
---
# <a name="disk-object"></a>Objeto de disco

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de disco modela un disco físico basado en host. El proveedor de software que se ejecuta en el host local puede acceder a un LUN como disco cuando el objeto LUN se desenmascara en el host local. Para obtener más información sobre el enmascaramiento de LUN, vea el [objeto LUN](lun-object.md).

Cada objeto de disco contribuye exactamente a un objeto pack; sin embargo, un disco puede contribuir con extensiones a cualquier número de volúmenes dentro de un paquete. Puede designar un disco para que sea una reserva en caliente.

## <a name="partition-to-volume-mapping"></a>Asignación de partición a volumen

El sistema operativo incluye compatibilidad con discos básicos y dinámicos. VDS proporciona un proveedor básico y un proveedor dinámico para administrar estos tipos de disco. Los discos básicos nunca son tolerantes a errores. Los discos dinámicos pueden ser tolerantes a errores si el sistema operativo permite dicho enlace de volumen. Los discos básicos y dinámicos pueden contener particiones estructuradas según uno de los siguientes estilos de partición: registro de arranque maestro (MBR) o tabla de particiones GUID (GPT). La creación de particiones de MBR tiene hasta cuatro particiones principales, o tres particiones principales más una partición extendida que tiene unidades lógicas infinitas. La creación de particiones GPT proporciona hasta 128 particiones principales.

La descripción siguiente es de naturaleza general. Muestra la relación típica entre particiones y volúmenes, en la que hay varias excepciones. Para obtener una descripción detallada de la asignación de partición a volumen, consulte la [**interfaz IVdsAdvancedDisk.**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) La asignación de partición a volumen varía en función del tipo de disco, básico o dinámico.

-   Discos básicos

    Una partición de un disco básico se asigna directamente a un volumen, en la mayoría de los casos, y se puede dar estilo como una partición MBR o GPT. En la ilustración siguiente se muestra la asignación para ambas versiones de particiones de MBR. En el primer caso, las particiones (de P1 a P4) se asignan directamente a volúmenes (de V1 a V4). Una partición extendida (Ext) reemplaza a P4 en el segundo estilo MBR. El número de unidades lógicas dentro de la partición extendida que se asignan a volúmenes es ilimitado.

    ![Muestra dos opciones de asignación para particiones de M B R.](images/vdsbasicmapping.png)

    Las particiones GPT (de P1 a P128) de la ilustración siguiente se asignan directamente a los volúmenes (de la V1 a la V128), si todas las particiones disponibles están en uso. Un disco GPT no usa una partición extendida como una manera de mejorar la facilidad de uso.

    ![Muestra una partición GPT.](images/vdsbasicmappinggpt.png)

-   Discos dinámicos

    Un tipo de partición especial en un disco dinámico se asigna a un gran número de volúmenes. Para obtener un límite estimado impuesto por el proveedor dinámico, vea el [objeto pack](pack-object.md). Como se muestra en la ilustración siguiente, puede haber cualquier número de extensiones dentro de P1 que se asignen a volúmenes.

    ![Muestra un tipo de partición especial en un disco dinámico.](images/vdsdynamicmapping.png)

Independientemente del tipo de disco, un disco puede contener una o varias extensiones de disco. Una extensión de disco es un intervalo contiguo de bloques lógicos expuestos por el disco. Por ejemplo, una extensión de disco puede representar un volumen completo, una parte de un volumen abarcado, un miembro de un volumen seccionado o un plex de un volumen reflejado.

### <a name="working-with-disks"></a>Trabajar con discos

Use el [**método IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para agregar un disco a un paquete existente. Los llamadores pueden obtener un puntero a un disco específico seleccionando el objeto de disco deseado de la enumeración que devuelve el [**método IVdsPack::QueryDisks.**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) Del mismo modo, puede invocar el método [**IVdsDisk::GetPack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) para determinar qué paquete contiene un disco determinado.

Puede mover un disco de un paquete a otro llamando al [**método IVdsPack::MigrateDisks.**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) (VDS no admite la migración de un disco básico entre paquetes controlados por el proveedor básico). También puede mover un paquete a otro host moviendo físicamente todos los discos del paquete al nuevo host. El paquete se mueve con los discos y aparece como un paquete externo en el nuevo host. Para obtener instrucciones, consulte [Incorporación de discos externos a un paquete.](adding-foreign-disks-to-a-pack.md)

Además de un identificador de objeto, un nombre, una dirección, un tipo de dispositivo y un tipo de medio, las propiedades del objeto de disco incluyen el estado del disco, el estado y las marcas. el tamaño en bytes, bytes por sector, sectores por pista y pistas por cilindro; y el tipo de bus y partición.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**IVdsDiskOnline,**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2,**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2) [**IVdsDiskPartitionMF,**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf) [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)e [**IVdsCreatePartitionEx.**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex) **Windows Server 2008:** No se admite la interfaz [**IVdsDiskPartitionMF2.**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)<br/> **Windows Vista:** La [**interfaz IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) no se admite hasta Windows Vista con Service Pack 1 (SP1); use [**IVdsDisk2 en**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) su lugar. No se admite la interfaz [**IVdsDiskPartitionMF2.**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)<br/> **Windows Server 2003:** No se admiten las [**interfaces IVdsAdvancedDisk2,**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2) [**IVdsDisk2,**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) [**IVdsDiskOnline,**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)e [**IVdsDiskPartitionMF2.**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)<br/> |
| Interfaces que puede exponer este objeto     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). (Vea [Objeto LUN para](lun-object.md) obtener interfaces adicionales que se exponen si el disco es un LUN).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Enumeraciones asociadas                           | [**VDS \_ MARCA \_ DE DISCO,**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) [**ESTADO DEL DISCO VDS, \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_status)MARCA DE [**PARTICIÓN VDS, \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag)ESTILO DE [**\_ PARTICIÓN \_ VDS**](/windows/win32/api/vds/ne-vds-__vds_partition_style)y [**TIPO DE EXTENSIÓN DE DISCO \_ \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Estructuras asociadas                             | [**VDS \_ DISK \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop), [**VDS DISK \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**VDS INPUT \_ \_ DISK**](/windows/desktop/api/Vds/ns-vds-vds_input_disk), [**VDS \_ PARTITION \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop), [**VDS PARTITION INFO \_ \_ \_ GPT,**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt) [**VDS PARTITION INFO \_ \_ \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)y [**VDS DISK \_ \_ EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de software](software-provider-objects.md)
</dt> <dt>

[Pack (objeto)](pack-object.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> <dt>

[Agregar discos externos a un paquete](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

