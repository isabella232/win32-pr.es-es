---
description: Para seleccionar una NIC de una tabla BLOB de NPP devuelta por Monitor de red, llame a la función GetNPPBlobTable. Esta función devuelve una tabla de BLOBs NPP, que la aplicación puede enumerar a continuación para seleccionar la NIC en la que está interesado.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Selección de una NIC de una tabla BLOB NPP devuelta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909802"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a><span data-ttu-id="62cc0-104">Selección de una NIC de una tabla BLOB NPP devuelta</span><span class="sxs-lookup"><span data-stu-id="62cc0-104">Selecting a NIC from a Returned NPP BLOB table</span></span>

<span data-ttu-id="62cc0-105">Para seleccionar una NIC de una tabla BLOB de NPP devuelta por Monitor de red, llame a la función [**GetNPPBlobTable**](getnppblobtable.md) .</span><span class="sxs-lookup"><span data-stu-id="62cc0-105">To select a NIC from an NPP BLOB table returned by Network Monitor, call the [**GetNPPBlobTable**](getnppblobtable.md) function.</span></span> <span data-ttu-id="62cc0-106">Esta función devuelve una tabla de BLOBs NPP, que la aplicación puede enumerar a continuación para seleccionar la NIC en la que está interesado.</span><span class="sxs-lookup"><span data-stu-id="62cc0-106">This function returns an NPP BLOB table, which can then be enumerated by your application to select the NIC you are interested in.</span></span>

<span data-ttu-id="62cc0-107">Cuando se llama a esta función, puede devolver una tabla BLOB de todas las NIC registradas en el equipo local o un conjunto más pequeño de NIC filtradas.</span><span class="sxs-lookup"><span data-stu-id="62cc0-107">When you call this function you can return either a BLOB table of all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="62cc0-108">Para filtrar las NIC que se devuelven, puede proporcionar un [*BLOB de filtro*](f.md) cuando se realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="62cc0-108">To filter the NICs that are returned, you can provide a [*filter BLOB*](f.md) when the call is made.</span></span>



| <span data-ttu-id="62cc0-109">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="62cc0-109">For information about</span></span>                                                       | <span data-ttu-id="62cc0-110">Vea</span><span class="sxs-lookup"><span data-stu-id="62cc0-110">See</span></span>                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62cc0-111">Cómo especificar un filtro que limite las NIC devueltas en una tabla de BLOBs NPP.</span><span class="sxs-lookup"><span data-stu-id="62cc0-111">How to specify a filter that limits the NICs returned in an NPP BLOB table.</span></span> | [<span data-ttu-id="62cc0-112">Especificación de un BLOB en filtro</span><span class="sxs-lookup"><span data-stu-id="62cc0-112">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="62cc0-113">Cómo seleccionar una NIC registrada en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="62cc0-113">How to select a NIC registered on a local computer.</span></span>                         | [<span data-ttu-id="62cc0-114">Selección de una NIC registrada</span><span class="sxs-lookup"><span data-stu-id="62cc0-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="62cc0-115">Cómo seleccionar una NIC de una tabla BLOB de NPP proporcionada</span><span class="sxs-lookup"><span data-stu-id="62cc0-115">How to select a NIC from a supplied NPP BLOB table</span></span>                          | [<span data-ttu-id="62cc0-116">Selección de una NIC de una tabla BLOB de NPP proporcionada</span><span class="sxs-lookup"><span data-stu-id="62cc0-116">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



