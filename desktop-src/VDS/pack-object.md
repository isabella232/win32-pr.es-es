---
description: Pack (objeto)
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Pack (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8c565c45b802258b9d8b9955a2d28adc13c73c989805ce6b2663bc3006d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058033"
---
# <a name="pack-object"></a>Pack (objeto)

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual [de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto pack modela un grupo de discos, una colección de discos y volúmenes administrados por el proveedor de software básico o dinámico. Un proveedor puede contener varios objetos pack.

Con la API, las aplicaciones pueden dirigir VDS para agregar uno o varios discos a un paquete, enlazar los discos a volúmenes y, opcionalmente, mover los discos como una unidad entre hosts. No se puede importar un volumen existente en un paquete.

> [!Note]  
> La pertenencia a un paquete no implica la coherencia entre los discos con respecto al rendimiento, los medios, el protocolo de interconexión u otras características.

 

Los objetos de disco no están asignados y se administran mediante VDS, o son miembros de exactamente un paquete. El proveedor de software básico puede tener cero o más paquetes, cada uno con un único disco básico. El proveedor no impone ningún límite al número de volúmenes en un disco básico. El proveedor dinámico puede tener cero o más paquetes con varios discos dinámicos en cada paquete. Este proveedor limita el número de volúmenes de un disco, en función del tamaño de un megabyte de la base de datos del administrador de discos lógicos (LDM). Dado que un volumen tiene al menos un plex y una extensión de disco, el número máximo de volúmenes para un paquete es aproximadamente 1000. El número máximo va a la baja a medida que el número de discos sube.

Además de los objetos de disco, un paquete puede contener uno o varios objetos LUN implementados por uno o varios proveedores de hardware. Para el Windows kernel, un LUN es simplemente otro disco. (Los objetos LUN se deben desenmascarar en el equipo que ejecuta el programa de proveedor). Cuando el disco es un LUN, el objeto LUN expone las interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk.**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) Un objeto pack **usa IVdsDisk,** en lugar de **IVdsLun,** para enumerar los LUN de un paquete. Para obtener una descripción más detallada de un LUN, vea el objeto [LUN](lun-object.md).

En la ilustración siguiente se muestra un paquete con dos miembros: un disco y un LUN. Una aplicación puede agregar estos objetos a un paquete en línea y crear un volumen a partir del disco subyacente y las extensiones de unidad representadas por ejes.

![Diagrama que muestra un "Pack" con un disco y un LUN agregados por una aplicación para crear un volumen representado por "Unidad" y "Eje".](images/vdsdisksareluns.png)

Use el [**método IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para crear un nuevo objeto pack. Los llamadores pueden obtener un puntero a un paquete específico seleccionando el objeto pack deseado de la enumeración devuelta por el método [**IVdsSwProvider:: QueryPacks.**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) Con un objeto pack, puede agregar, quitar o reemplazar los miembros de un paquete. Cuando se agrega un objeto de disco a un paquete, VDS inicializa un disco para desenlatar todos los volúmenes existentes. En cambio, un LUN conserva todos los detalles de enlace cuando se agrega a un paquete. Si quita el último disco de un paquete, VDS elimina el objeto pack cuando el autor de la llamada libera la última referencia al objeto.

Las propiedades del objeto incluyen un identificador de objeto, un nombre, el estado del paquete y las marcas. Un paquete en línea está disponible para su configuración y uso, y un paquete sin conexión no está disponible. VDS admite cualquier número de paquetes en línea y sin conexión.

**Windows Server 2003:** Solo admite un paquete en línea a la vez.

VDS aplica un cuórum de discos en línea dentro de un paquete. El cuórum determina si un paquete puede tener un estado en línea e impide que varios hosts concedan un estado en línea al mismo paquete. Si el número de discos en línea de un paquete está por debajo del cuórum (n/2 + 1), VDS desconecta el paquete en línea.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) e [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Enumeraciones asociadas                           | [**VDS \_ PACK \_ FLAG y**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) [**VDS PACK \_ \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Estructuras asociadas                             | [**VDS \_ PACK \_ PROP y**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) [**VDS PACK \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003: esta** interfaz no se admite hasta Windows Vista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
