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
# <a name="lun-plex-object"></a><span data-ttu-id="c6a67-103">Objeto de Plex LUN</span><span class="sxs-lookup"><span data-stu-id="c6a67-103">LUN Plex Object</span></span>

<span data-ttu-id="c6a67-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c6a67-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="c6a67-105">Un objeto complejo LUN modela un complejo LUN que está incluido en un LUN.</span><span class="sxs-lookup"><span data-stu-id="c6a67-105">A LUN plex object models a LUN plex that is contained by a LUN.</span></span> <span data-ttu-id="c6a67-106">Solo un LUN reflejado puede tener varios Plex; todos los demás tipos de LUN tienen un complejo.</span><span class="sxs-lookup"><span data-stu-id="c6a67-106">Only a mirrored LUN can have multiple plexes; all other LUN types have one plex.</span></span> <span data-ttu-id="c6a67-107">Cada Plex contiene una copia de los datos en el LUN.</span><span class="sxs-lookup"><span data-stu-id="c6a67-107">Each plex contains a copy of the data on the LUN.</span></span> <span data-ttu-id="c6a67-108">Se pueden agregar complejos nuevos a un LUN y, con la excepción del Plex original, se pueden quitar los Plex existentes.</span><span class="sxs-lookup"><span data-stu-id="c6a67-108">New plexes can be added to a LUN, and, with the exception of the original plex, existing plexes can be removed.</span></span> <span data-ttu-id="c6a67-109">VDS admite cuatro tipos de Plex LUN: simples, distribuidos, seccionados y seccionados con paridad.</span><span class="sxs-lookup"><span data-stu-id="c6a67-109">VDS supports four LUN plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="c6a67-110">Para obtener una descripción de cada uno de estos tipos de LUN, consulte el [objeto LUN](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="c6a67-110">For a description of each of these LUN types, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="c6a67-111">Use el método [**IVdsLun:: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) para agregar un complejo a un LUN y el método [**IVdsLun:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) para eliminar el Plex.</span><span class="sxs-lookup"><span data-stu-id="c6a67-111">Use the [**IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) method to add a plex to a LUN and the [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) method to delete the plex.</span></span> <span data-ttu-id="c6a67-112">Puede consultar los Plex de LUN invocando el método [**IVdsLun:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) .</span><span class="sxs-lookup"><span data-stu-id="c6a67-112">You can query for LUN plexes by invoking the [**IVdsLun::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) method.</span></span> <span data-ttu-id="c6a67-113">Puede obtener un puntero a un complejo LUN específico seleccionando el objeto complejo deseado de la enumeración que devuelve el método **QueryPlexes** .</span><span class="sxs-lookup"><span data-stu-id="c6a67-113">You can get a pointer to a specific LUN plex by selecting the desired plex object from the enumeration that is returned by the **QueryPlexes** method.</span></span> <span data-ttu-id="c6a67-114">Con un objeto complejo, puede consultar las extensiones de unidad y las sugerencias de automagic y aplicar nuevas sugerencias.</span><span class="sxs-lookup"><span data-stu-id="c6a67-114">With a plex object, you can query for the drive extents and automagic hints, and apply new hints.</span></span>

<span data-ttu-id="c6a67-115">Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto de complejo LUN incluyen el tipo complejo, el tamaño, el estado, el estado, el estado de la transición y las marcas; una lista de desenmascaramiento y un tamaño de franja; y un valor de prioridad de recompilación.</span><span class="sxs-lookup"><span data-stu-id="c6a67-115">In addition to an object identifier, a name, and a serial number, LUN plex object properties include the plex type, size, status, health, transition state, and flags; an unmasking list and stripe size; and a rebuild priority setting.</span></span>

<span data-ttu-id="c6a67-116">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c6a67-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="c6a67-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6a67-117">Type</span></span>                                              | <span data-ttu-id="c6a67-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="c6a67-118">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a67-119">Interfaces que siempre expone este objeto</span><span class="sxs-lookup"><span data-stu-id="c6a67-119">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="c6a67-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span><span class="sxs-lookup"><span data-stu-id="c6a67-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span></span>                                                                                                                              |
| <span data-ttu-id="c6a67-121">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="c6a67-121">Associated enumerations</span></span>                           | <span data-ttu-id="c6a67-122">[**VDS \_ \_ \_ Marca de Plex de LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**\_ \_ \_ Estado de Plex LUN de VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)y [**\_ \_ \_ tipo complejo de LUN de VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span><span class="sxs-lookup"><span data-stu-id="c6a67-122">[**VDS\_LUN\_PLEX\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS\_LUN\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status), and [**VDS\_LUN\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span></span> |
| <span data-ttu-id="c6a67-123">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="c6a67-123">Associated structures</span></span>                             | <span data-ttu-id="c6a67-124">[**VDS \_ \_ \_ prop de Plex LUN**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span><span class="sxs-lookup"><span data-stu-id="c6a67-124">[**VDS\_LUN\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span></span>                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c6a67-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6a67-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a67-126">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="c6a67-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="c6a67-127">Objeto LUN</span><span class="sxs-lookup"><span data-stu-id="c6a67-127">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

 
