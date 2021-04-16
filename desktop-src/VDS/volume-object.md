---
description: Objeto de volumen
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: Objeto de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e47092a237e7b0e9441b08c410d95d0836dbdb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678550"
---
# <a name="volume-object"></a>Objeto de volumen

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de volumen modela una unidad de almacenamiento lógico que se crea mediante un proveedor de software y se presenta en el sistema de archivos como un disco. Cada volumen consta de al menos un Plex de volumen, que a su vez se compone de extensiones de uno o más discos.

## <a name="volume-types"></a>Tipos de volúmenes

VDS admite cinco tipos de volúmenes: simples, distribuidos, seccionados, reflejados y seccionados con paridad. Los volúmenes simples, distribuidos y seccionados no son tolerantes a errores. los volúmenes reflejados y de paridad son tolerantes a errores. En el resto de esta sección se describe cada uno de los tipos de volúmenes de VDS.

-   Un volumen simple es una parte de un disco físico que funciona como si fuera una unidad físicamente separada. Un volumen simple puede abarcar una sola región de un disco o varias regiones del mismo disco vinculadas entre sí.
-   Un volumen distribuido combina áreas de espacio sin asignar de varios discos en un volumen lógico, lo que le permite usar de forma más eficaz todo el espacio y todas las letras de unidad en un sistema de varios discos.
-   Un volumen seccionado se crea combinando áreas de espacio disponible en dos o más discos en un volumen lógico. Los volúmenes seccionados usan RAID-0, que secciona los datos en varios discos. Los volúmenes seccionados no se pueden extender ni reflejar, y no ofrecen tolerancia a errores. Si se produce un error en uno de los discos que contienen un volumen seccionado, se produce un error en todo el volumen. Al crear volúmenes seccionados, es mejor usar discos que tengan el mismo tamaño, modelo y fabricante.
-   Un volumen reflejado es un volumen tolerante a errores que proporciona redundancia de datos mediante el uso de dos copias, o complejos, del volumen para duplicar los datos almacenados en el volumen. Todos los datos que se escriben en el volumen reflejado se escriben en ambos Plex, que se encuentran en discos físicos independientes. Si se produce un error en uno de los discos físicos, los datos del disco con errores dejarán de estar disponibles, pero el sistema continuará funcionando con el disco no afectado.
-   Un volumen seccionado con paridad es un volumen tolerante a errores con datos y paridad seccionados intermitentemente en tres o más discos físicos. Si se produce un error en una parte de un disco físico, puede volver a crear los datos que se encontraban en la parte con errores a partir de los datos y la paridad restantes. Este tipo de volumen (también denominado volumen RAID-5) es una buena solución para la redundancia de datos en un entorno de equipo en el que la mayor parte de la actividad consiste en leer datos.

### <a name="volume-creation"></a>Creación de volúmenes

Los proveedores de software básico y dinámico admiten la creación de volúmenes dirigidos parcialmente; un autor de llamada especifica solo los atributos que son de especial interés y permite al proveedor elegir el resto. VDS monta automáticamente un volumen recién creado, excepto en las plataformas Windows Server 2003, Enterprise Edition y Windows Server 2003, Datacenter Edition.

### <a name="working-with-volumes"></a>Trabajar con volúmenes

Cree siempre un volumen en el mismo paquete que los discos que contribuyen a él. Use el método [**IVdsPack:: CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) para crear un nuevo objeto de volumen. Puede determinar los volúmenes contenidos dentro de un paquete específico invocando el método [**QueryVolumes**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) , también expuesto por [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack). Un llamador puede obtener un puntero a un volumen específico seleccionando el objeto de volumen deseado de la enumeración devuelta por **QueryVolumes**. Con un objeto de volumen, puede establecer el estado; consulta de complejos; extender y reducir el volumen; Agregar, romper y quitar complejos; y elimine el volumen.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades de objeto de volumen incluyen el tipo de volumen, el tamaño, el estado, el estado, el estado de la transición, las marcas y un tipo de sistema de archivos recomendado.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsVolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume), [**IVdsVolumeMF**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf), [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* , [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* y [**IVdsVolumeShrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* . |
| Enumeraciones asociadas                           | [**VDS \_ \_Marca de volumen**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag), [**\_ \_ Estado del volumen de VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status), [**\_ \_ tipo de volumen de VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)y [**\_ \_ \_ tipo de extensión de disco de VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).            |
| Estructuras asociadas                             | [**VDS \_ \_Expulsión de volumen**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) y [**\_ \_ notificación de volumen de VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification).                                                                                                        |



 

**\* Windows Server 2003:** estas interfaces no se admiten hasta Windows Vista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de software](software-provider-objects.md)
</dt> </dl>

 

 
