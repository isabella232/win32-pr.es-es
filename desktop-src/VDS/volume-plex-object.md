---
description: Objeto Plex de volumen
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Objeto Plex de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140cbf50e1939be7f62499aa90a299e07c157cd22b1a2e039e5e7bb2053b497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603037"
---
# <a name="volume-plex-object"></a>Objeto Plex de volumen

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto plex de volumen modela un plex de volumen contenido por un volumen. Solo un volumen reflejado puede tener varios plexos; todos los demás tipos de volúmenes tienen un plex. Cada plex contiene una copia de los datos del volumen. VDS admite cuatro tipos de plex de volumen: simple, abarcado, seccionado y seccionado con paridad. Para obtener una descripción de cada uno de estos tipos de volumen, vea [el objeto Volume](volume-object.md).

Hay dos maneras de crear un volumen con varios plexos. Puede usar el método [**IVdsPack::CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) para crear el volumen reflejado directamente o usar el método [**IVdsVolume::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) para agregar un volumen a otro volumen. Los volúmenes (y los discos subyacentes) deben estar en el mismo paquete. En la ilustración siguiente se muestra un ejemplo de cómo agregar un volumen (B) como un plex a otro volumen (A) y el volumen multiplexado resultante (A). Los datos del volumen A permanecen intactos, mientras que los datos del volumen B se convierten en una copia reflejada de los datos del volumen A.

![Diagrama que muestra dos plexos únicos, uno con el volumen simple A y otro con el volumen simple B, igual a varios plexos con el volumen reflejado A.](images/vdsplex.png)

Puede consultar los plexos de volumen invocando el [**método IVdsVolume::QueryPlexes.**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) Puede obtener un puntero a un plex de volumen específico seleccionando el objeto plex deseado de la enumeración devuelta por **QueryPlexes**. A excepción del último plex, los plexos existentes se pueden dividir o quitar. Use [**IVdsVolume::BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) para dividir un plex de un volumen y convertir el objeto plex roto en un objeto de volumen. Use [**IVdsVolume::RemovePlex para**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) eliminar el plex por completo. Puede intentar reparar un plex tolerante a errores llamando al método [**IVdsVolumePlex::Repair,**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) que mueve los miembros defectuosos a discos buenos.

Además de un identificador de objeto y un tipo plex, las propiedades del objeto plex del volumen incluyen el estado, el estado y el estado de transición del plex. Este objeto no tiene marcas.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Enumeraciones asociadas                           | [**VDS \_ VOLUME \_ PLEX \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**VDS \_ VOLUME \_ PLEX TYPE \_ y**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type) [**VDS DISK EXTENT \_ \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Estructuras asociadas                             | [**VDS \_ VOLUME \_ PLEX \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop).                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto Volume](volume-object.md)
</dt> </dl>

 

 
