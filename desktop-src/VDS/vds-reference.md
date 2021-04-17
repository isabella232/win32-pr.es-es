---
description: En esta sección se describe la interfaz de programación de aplicaciones para el servicio de disco virtual (VDS).
ms.assetid: d00fc772-331f-4d71-a418-e34acdfb6652
title: Referencia de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369111add0b3f4b7e2742c764a6cbf8b1d8bfdd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677974"
---
# <a name="vds-reference"></a><span data-ttu-id="6d034-103">Referencia de VDS</span><span class="sxs-lookup"><span data-stu-id="6d034-103">VDS Reference</span></span>

<span data-ttu-id="6d034-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d034-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="6d034-105">En esta sección se describe la interfaz de programación de aplicaciones para el servicio de disco virtual (VDS).</span><span class="sxs-lookup"><span data-stu-id="6d034-105">This section describes the application programming interface to the Virtual Disk Service (VDS).</span></span>

<span data-ttu-id="6d034-106">Los desarrolladores de aplicaciones usan las interfaces, estructuras, enumeraciones y constantes simbólicas en esta API para consultar y configurar el almacenamiento, desde discos hasta matrices de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6d034-106">Application developers use the interfaces, structures, enumerations, and symbolic constants in this API to query and configure storage—from disks to storage arrays.</span></span> <span data-ttu-id="6d034-107">Para obtener una visión detallada de la relación entre los tipos de VDS, consulte el [modelo de objetos de VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="6d034-107">For a detailed look at the relationship among VDS types, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="6d034-108">Los fabricantes de almacenamiento implementan muchas de las interfaces definidas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="6d034-108">Storage manufacturers implement many of the interfaces defined in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6d034-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6d034-109">In this Section</span></span>

<dl> <dt>

[<span data-ttu-id="6d034-110">Constantes de VDS</span><span class="sxs-lookup"><span data-stu-id="6d034-110">VDS Constants</span></span>](vds-constants.md)
</dt> <dd>

<span data-ttu-id="6d034-111">Enumera las constantes simbólicas en la API de VDS.</span><span class="sxs-lookup"><span data-stu-id="6d034-111">Lists the symbolic constants in the VDS API.</span></span>

</dd> <dt>

[<span data-ttu-id="6d034-112">Tipos de datos de VDS</span><span class="sxs-lookup"><span data-stu-id="6d034-112">VDS Data Types</span></span>](vds-data-types.md)
</dt> <dd>

<span data-ttu-id="6d034-113">Enumera los tipos de datos usados con VDS.</span><span class="sxs-lookup"><span data-stu-id="6d034-113">Lists the data types used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="6d034-114">Enumeraciones de VDS</span><span class="sxs-lookup"><span data-stu-id="6d034-114">VDS Enumerations</span></span>](vds-enumerations.md)
</dt> <dd>

<span data-ttu-id="6d034-115">Describe las enumeraciones utilizadas con VDS.</span><span class="sxs-lookup"><span data-stu-id="6d034-115">Describes the enumerations used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="6d034-116">Interfaces VDS</span><span class="sxs-lookup"><span data-stu-id="6d034-116">VDS Interfaces</span></span>](vds-interfaces.md)
</dt> <dd>

<span data-ttu-id="6d034-117">Describe las interfaces de VDS y los métodos que exponen.</span><span class="sxs-lookup"><span data-stu-id="6d034-117">Describes VDS interfaces and the methods they expose.</span></span>

</dd> <dt>

[<span data-ttu-id="6d034-118">Estructuras VDS</span><span class="sxs-lookup"><span data-stu-id="6d034-118">VDS Structures</span></span>](vds-structures.md)
</dt> <dd>

<span data-ttu-id="6d034-119">Describe las estructuras que se pasan como parámetros a los métodos de VDS.</span><span class="sxs-lookup"><span data-stu-id="6d034-119">Describes the structures passed as parameters to VDS methods.</span></span>

</dd> <dt>

[<span data-ttu-id="6d034-120">Códigos de retorno comunes de servicio de disco virtual</span><span class="sxs-lookup"><span data-stu-id="6d034-120">Virtual Disk Service Common Return Codes</span></span>](virtual-disk-service-common-return-codes.md)
</dt> <dd>

<span data-ttu-id="6d034-121">Describe los códigos de error más comunes que son específicos de VDS.</span><span class="sxs-lookup"><span data-stu-id="6d034-121">Describes the most common error codes that are specific to VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="6d034-122">Glosario de servicio de disco virtual</span><span class="sxs-lookup"><span data-stu-id="6d034-122">Virtual Disk Service Glossary</span></span>](virtual-disk-service-glossary-all.md)
</dt> <dd>

<span data-ttu-id="6d034-123">Glosario de términos técnicos usados en la documentación de VDS.</span><span class="sxs-lookup"><span data-stu-id="6d034-123">Glossary of technical terms used in VDS documentation.</span></span>

</dd> </dl>

 

 
