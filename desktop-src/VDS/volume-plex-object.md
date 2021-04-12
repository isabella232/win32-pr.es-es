---
description: Volume Plex (objeto)
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Volume Plex (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a858bc6ce98761bb687e8dca473b1b68879da8
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104361777"
---
# <a name="volume-plex-object"></a>Volume Plex (objeto)

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de complejo de volumen modela un complejo de volumen que está contenido en un volumen. Solo un volumen reflejado puede tener varios Plex; todos los demás tipos de volúmenes tienen un complejo. Cada Plex contiene una copia de los datos del volumen. VDS admite cuatro tipos de Plex de volumen: simples, distribuidos, seccionados y seccionados con paridad. Para obtener una descripción de cada uno de estos tipos de volúmenes, consulte el [objeto de volumen](volume-object.md).

Hay dos maneras de crear un volumen con varios complejos. Puede usar el método [**IVdsPack:: CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) para crear el volumen reflejado directamente o usar el método [**IVdsVolume:: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) para agregar un volumen a otro volumen. Los volúmenes (y los discos subyacentes) deben estar en el mismo paquete. En la ilustración siguiente se muestra un ejemplo de cómo agregar un volumen (B) como complejo a otro volumen (A) y el volumen multiplexado resultante (A). Los datos del volumen A permanecen intactos, mientras que los datos del volumen B se convierten en una copia reflejada de los datos en el volumen A.

![Diagrama que muestra dos complejos individuales, uno con el volumen simple A y otro con el volumen simple B, igual a varios complejos con el volumen reflejado A.](images/vdsplex.png)

Puede consultar los Plex de volumen mediante la invocación del método [**IVdsVolume:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) . Puede obtener un puntero a un Plex de volumen específico seleccionando el objeto de Plex deseado de la enumeración devuelta por **QueryPlexes**. Con la excepción del último Plex, los Plex existentes se pueden romper o quitar. Use [**IVdsVolume:: BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) para dividir un Plex de un volumen y convertir el objeto de complejo roto en un objeto de volumen. Use [**IVdsVolume:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) para eliminar el Plex por completo. Puede intentar reparar un Plex tolerante a errores llamando al método [**IVdsVolumePlex:: repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) , que mueve los miembros incorrectos a los discos correctos.

Además de un identificador de objeto y un tipo de Plex, las propiedades del objeto de Plex de volumen incluyen el estado, el estado y el estado de transición del complejo. Este objeto no tiene marcas.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Enumeraciones asociadas                           | [**VDS \_ \_ \_ Estado del Plex del volumen**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**\_ \_ \_ tipo de Plex del volumen de VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)y [**\_ \_ \_ tipo de extensión de disco de VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Estructuras asociadas                             | [**VDS \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop). del Plex del volumen.                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto de volumen](volume-object.md)
</dt> </dl>

 

 
