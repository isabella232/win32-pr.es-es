---
description: El Monitor de red objeto binario grande (BLOB) es una estructura de datos genérica que contiene información de configuración y ubicación de tarjetas de interfaz de red (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Blobs Monitor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689560"
---
# <a name="network-monitor-blobs"></a><span data-ttu-id="8a4a6-103">Blobs Monitor de red</span><span class="sxs-lookup"><span data-stu-id="8a4a6-103">Network Monitor BLOBs</span></span>

<span data-ttu-id="8a4a6-104">El Monitor de red objeto binario grande (BLOB) es una estructura de datos genérica que contiene información de configuración y ubicación de tarjetas de interfaz de red (NIC).</span><span class="sxs-lookup"><span data-stu-id="8a4a6-104">The Network Monitor binary large object (BLOB) is a generic data structure that contains configuration and location information of network interface cards (NICs).</span></span> <span data-ttu-id="8a4a6-105">Use blobs para representar NIC y filtrar entradas en una lista de NIC.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-105">Use BLOBs to represent NICs and to filter entries in a list of NICs.</span></span> <span data-ttu-id="8a4a6-106">Los blobs también pueden contener datos específicos de la aplicación sin que ello afecte a los demás datos que contienen.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-106">BLOBS can also contain application-specific data without affecting the other data that they hold.</span></span> <span data-ttu-id="8a4a6-107">La implementación de BLOB es opaca para todos los niveles que deben tener acceso a los blobs con las API de BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-107">BLOB implementation is opaque to all levels that must access BLOBs with BLOB APIs.</span></span>

## <a name="blob-structure"></a><span data-ttu-id="8a4a6-108">Estructura de BLOB</span><span class="sxs-lookup"><span data-stu-id="8a4a6-108">BLOB Structure</span></span>

<span data-ttu-id="8a4a6-109">Un BLOB se puede considerar como un árbol jerárquico que se usa para designar cadenas.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-109">A BLOB can be considered as a hierarchical tree used to designate strings.</span></span> <span data-ttu-id="8a4a6-110">Este árbol tiene tres niveles: propietario, categoría y etiqueta.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-110">This tree has three layers: Owner, Category, and Tag.</span></span> <span data-ttu-id="8a4a6-111">Owner es una cadena que indica, en general, quién lee una entrada.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-111">Owner is a string that indicates, in general, who reads an entry.</span></span> <span data-ttu-id="8a4a6-112">La categoría también es una cadena, que designa una agrupación funcional general de etiquetas bajo el propietario.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-112">The Category is also a string, which designates a general functional grouping of tags under the owner.</span></span> <span data-ttu-id="8a4a6-113">La etiqueta es el nombre real de la entrada.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-113">The Tag is the actual name of the entry.</span></span>

<span data-ttu-id="8a4a6-114">Las características estructurales de los blobs incluyen:</span><span class="sxs-lookup"><span data-stu-id="8a4a6-114">The structural characteristics of BLOBs include:</span></span>

-   <span data-ttu-id="8a4a6-115">Las aplicaciones auxiliares de BLOB dentro de un proceso están protegidas entre sí mediante una exclusión mutua integrada en cada BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-115">BLOB helpers within one process are protected from one another by a mutex built into each BLOB.</span></span>
-   <span data-ttu-id="8a4a6-116">Cada BLOB tiene un número de versión interno para que las aplicaciones auxiliares puedan administrar formularios de BLOB presentes y futuros.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-116">Each BLOB has an internal version number so that the helpers can handle both present and future BLOB forms.</span></span> <span data-ttu-id="8a4a6-117">Pueden producirse conflictos de versión si envía un BLOB a otro equipo a través de una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-117">Version conflicts may occur if you send a BLOB to another computer via a remote procedure call.</span></span>
-   <span data-ttu-id="8a4a6-118">El propio BLOB es un puntero a un void.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-118">The BLOB itself is a pointer to a void.</span></span> <span data-ttu-id="8a4a6-119">Tenga en cuenta que las aplicaciones deben asignar blobs con el modificador **const** para evitar modificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-119">Be aware that applications should allocate BLOBs with the **const** modifier to avoid altering the contents.</span></span>
-   <span data-ttu-id="8a4a6-120">Cada uno de los designadores, así como sus valores, son cadenas.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-120">Each of the designators, as well as their values, are strings.</span></span> <span data-ttu-id="8a4a6-121">Tenga en cuenta que las cadenas devueltas por las funciones **GetString** son realmente punteros en el BLOB y no se deben cambiar.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-121">Be aware that the strings returned by **GetString** functions are actually pointers into the BLOB and should not be changed.</span></span> <span data-ttu-id="8a4a6-122">Por este motivo, estas cadenas se deben especificar como **const char** _ \_ PX \* para evitar que las aplicaciones las cambien accidentalmente.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-122">For this reason, these strings must be specified as **const char** _\_pX\* to keep applications from accidentally changing them.</span></span>

<span data-ttu-id="8a4a6-123">En general, todos los parámetros con el designador **const** animan al autor de la llamada a abstenerse de cambiar los valores en lugar de impedir que las funciones auxiliares las cambien.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-123">In general, all parameters with the **const** designator encourage the caller to refrain from changing the values rather than prohibit the helper functions from changing them.</span></span> <span data-ttu-id="8a4a6-124">De hecho, las funciones auxiliares normalmente cambiarán esos valores.</span><span class="sxs-lookup"><span data-stu-id="8a4a6-124">In fact, the helper functions will usually change those values.</span></span>

 

 



