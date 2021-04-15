---
description: Objeto de paquete
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Objeto de paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b01978747df5ccc273a31ae2f516b35c01df96
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104561190"
---
# <a name="pack-object"></a>Objeto de paquete

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto Pack modela un grupo de discos, una colección de discos y volúmenes administrados por el proveedor de software básico o dinámico. Un proveedor puede contener varios objetos Pack.

Mediante la API, las aplicaciones pueden dirigir a VDS para agregar uno o más discos a un paquete, enlazar los discos a volúmenes y, opcionalmente, trasladar los discos como una unidad entre los hosts. No se puede importar un volumen existente en un paquete.

> [!Note]  
> La pertenencia a un paquete no implica la coherencia entre los discos con respecto al rendimiento, los medios, el protocolo de interconexión u otras características.

 

Los objetos de disco están sin asignar y administrados por VDS, o son miembros de exactamente un paquete. El proveedor de software básico puede tener cero o más paquetes, cada uno con un solo disco básico. El proveedor no impone ningún límite en el número de volúmenes de un disco básico. El proveedor dinámico puede tener cero o más paquetes con varios discos dinámicos en cada paquete. Este proveedor limita el número de volúmenes de un disco, en función del tamaño de un megabyte de la base de datos del administrador de discos lógicos (LDM). Dado que un volumen tiene al menos un Plex y una extensión de disco, el número máximo de volúmenes para un paquete es de aproximadamente 1000. El número máximo deja de funcionar a medida que el número de discos aumenta.

Además de los objetos de disco, un paquete puede contener uno o más objetos LUN implementados por uno o varios proveedores de hardware. En el kernel de Windows, un LUN es simplemente otro disco. (Los objetos de LUN no deben enmascararse en el equipo que ejecuta el programa de proveedor). Cuando el disco es un LUN, el objeto LUN expone las interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) y [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) . Un objeto Pack usa **IVdsDisk**, en lugar de **IVdsLun**, para enumerar los LUN de un paquete. Para obtener una descripción más detallada de un LUN, vea el [objeto LUN](lun-object.md).

En la ilustración siguiente se muestra un paquete con dos miembros: un disco y un LUN. Una aplicación puede agregar estos objetos a un paquete en línea y crear un volumen a partir de las extensiones de disco subyacente y de unidad representadas por ejes.

![Diagrama que muestra un ' Pack ' con un disco y un LUN agregado por una aplicación para crear un volumen representado por una ' unidad ' y ' eje '.](images/vdsdisksareluns.png)

Use el método [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para crear un nuevo objeto Pack. Los llamadores pueden obtener un puntero a un Pack específico seleccionando el objeto Pack deseado de la enumeración que devuelve el método [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) . Con un objeto de paquete, puede Agregar, quitar o reemplazar los miembros de un paquete. Cuando se agrega un objeto de disco a un paquete, VDS Inicializa un disco para desenlazar todos los volúmenes existentes. En cambio, un LUN conserva todos los detalles de enlace cuando se agrega a un paquete. Si quita el último disco de un paquete, VDS elimina el objeto Pack cuando el autor de la llamada libera la última referencia al objeto.

Las propiedades de objeto incluyen un identificador de objeto, un nombre, un estado de paquete y marcas. Hay disponible un paquete en línea para la configuración y el uso. un paquete sin conexión no está disponible. VDS es compatible con cualquier número de paquetes en línea y sin conexión.

**Windows Server 2003:** Solo admite un paquete en línea a la vez.

VDS fuerza el cuórum de los discos en línea dentro de un paquete. El cuórum determina si un paquete puede tener un estado en línea y evita que varios hosts concedan un estado en línea al mismo paquete. Si el número de discos en línea de un paquete cae por debajo del cuórum (n/2 + 1), VDS desconecta el paquete en línea.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) y [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Enumeraciones asociadas                           | [**VDS \_ \_Marca de paquete**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) y [**\_ \_ Estado del paquete de VDS**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Estructuras asociadas                             | [**VDS \_ PAQUETE \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) y [**\_ \_ notificación del paquete VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003:** esta interfaz no se admite hasta Windows Vista.

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

 

 
