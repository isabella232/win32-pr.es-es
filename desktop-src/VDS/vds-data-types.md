---
description: Los tipos de datos compatibles con VDS definen los valores devueltos de la función, los parámetros de función y los miembros de la estructura. Los tipos de datos definen el tamaño y el significado de estos elementos.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipos de datos de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697686"
---
# <a name="vds-data-types"></a><span data-ttu-id="970b0-104">Tipos de datos de VDS</span><span class="sxs-lookup"><span data-stu-id="970b0-104">VDS Data Types</span></span>

<span data-ttu-id="970b0-105">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="970b0-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="970b0-106">Los tipos de datos compatibles con VDS definen los valores devueltos de la función, los parámetros de función y los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="970b0-106">The data types supported by VDS define function return values, function parameters, and structure members.</span></span> <span data-ttu-id="970b0-107">Los tipos de datos definen el tamaño y el significado de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="970b0-107">Data types define the size and meaning of these elements.</span></span>



| <span data-ttu-id="970b0-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="970b0-108">Data type</span></span>                                                                                      | <span data-ttu-id="970b0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="970b0-109">Description</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="970b0-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_identificador de objeto VDS \_**</span><span class="sxs-lookup"><span data-stu-id="970b0-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS\_OBJECT\_ID**</span></span><br/> | <span data-ttu-id="970b0-111">IDENTIFICADOR de objeto VDS.</span><span class="sxs-lookup"><span data-stu-id="970b0-111">VDS object ID.</span></span> <span data-ttu-id="970b0-112">No se garantiza que estos valores sean únicos en los reinicios.</span><span class="sxs-lookup"><span data-stu-id="970b0-112">These values are not guaranteed to be unique across reboots.</span></span> <br/> <span data-ttu-id="970b0-113">Este tipo se declara en Vds. h (VdsHwPrv. h para proveedores de hardware) como un GUID.</span><span class="sxs-lookup"><span data-stu-id="970b0-113">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a GUID.</span></span> <br/> |
| <span data-ttu-id="970b0-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**identificador de la ruta de acceso de VDS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="970b0-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS\_PATH\_ID**</span></span><br/>       | <span data-ttu-id="970b0-115">IDENTIFICADOR de la ruta de acceso de VDS para e/s de múltiples rutas (MPIO).</span><span class="sxs-lookup"><span data-stu-id="970b0-115">VDS path ID for multipath I/O (MPIO).</span></span> <br/> <span data-ttu-id="970b0-116">Este tipo se declara en Vds. h (VdsHwPrv. h para proveedores de hardware) como UINT64.</span><span class="sxs-lookup"><span data-stu-id="970b0-116">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a UINT64.</span></span><br/>                                      |



 

 

