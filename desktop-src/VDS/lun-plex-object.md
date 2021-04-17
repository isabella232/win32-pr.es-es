---
description: Objeto de Plex LUN
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Objeto de Plex LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697748"
---
# <a name="lun-plex-object"></a>Objeto de Plex LUN

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto complejo LUN modela un complejo LUN que está incluido en un LUN. Solo un LUN reflejado puede tener varios Plex; todos los demás tipos de LUN tienen un complejo. Cada Plex contiene una copia de los datos en el LUN. Se pueden agregar complejos nuevos a un LUN y, con la excepción del Plex original, se pueden quitar los Plex existentes. VDS admite cuatro tipos de Plex LUN: simples, distribuidos, seccionados y seccionados con paridad. Para obtener una descripción de cada uno de estos tipos de LUN, consulte el [objeto LUN](lun-object.md).

Use el método [**IVdsLun:: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) para agregar un complejo a un LUN y el método [**IVdsLun:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) para eliminar el Plex. Puede consultar los Plex de LUN invocando el método [**IVdsLun:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) . Puede obtener un puntero a un complejo LUN específico seleccionando el objeto complejo deseado de la enumeración que devuelve el método **QueryPlexes** . Con un objeto complejo, puede consultar las extensiones de unidad y las sugerencias de automagic y aplicar nuevas sugerencias.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto de complejo LUN incluyen el tipo complejo, el tamaño, el estado, el estado, el estado de la transición y las marcas; una lista de desenmascaramiento y un tamaño de franja; y un valor de prioridad de recompilación.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Enumeraciones asociadas                           | [**VDS \_ \_ \_ Marca de Plex de LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**\_ \_ \_ Estado de Plex LUN de VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)y [**\_ \_ \_ tipo complejo de LUN de VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Estructuras asociadas                             | [**VDS \_ \_ \_ prop de Plex LUN**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> </dl>

 

 
