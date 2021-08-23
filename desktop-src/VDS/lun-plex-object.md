---
description: Lun Plex (objeto)
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Lun Plex (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df52b60bcbd23269d766435749b40b8c636361390359182a38a695ab6252a27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999454"
---
# <a name="lun-plex-object"></a>Lun Plex (objeto)

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual [de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto lun plex modela un plex LUN contenido en un LUN. Solo un LUN reflejado puede tener varios plexos; todos los demás tipos lun tienen un plex. Cada plex contiene una copia de los datos en el LUN. Se pueden agregar nuevos plexos a un LUN y, a excepción del plex original, se pueden quitar los plex existentes. VDS admite cuatro tipos de plex LUN: simple, abarcado, seccionado y seccionado con paridad. Para obtener una descripción de cada uno de estos tipos de LUN, vea el objeto [LUN](lun-object.md).

Use el [**método IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) para agregar un plex a un LUN y el método [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) para eliminar el plex. Puede consultar los plexos LUN invocando el [**método IVdsLun::QueryPlexes.**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) Puede obtener un puntero a un plex LUN específico seleccionando el objeto plex deseado de la enumeración que devuelve el **método QueryPlexes.** Con un objeto plex, puede consultar las extensiones de unidad y las sugerencias de automagic, y aplicar nuevas sugerencias.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto lun plex incluyen el tipo de plex, el tamaño, el estado, el estado, el estado de transición y las marcas. una lista de desenmascaramiento y un tamaño de franja; y una configuración de prioridad de recompilación.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Enumeraciones asociadas                           | [**VDS \_ LUN \_ PLEX \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS \_ LUN \_ PLEX \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)y [**VDS LUN \_ \_ PLEX \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Estructuras asociadas                             | [**VDS \_ LUN \_ PLEX \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> </dl>

 

 
