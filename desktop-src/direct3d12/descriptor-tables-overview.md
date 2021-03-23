---
title: Información general sobre tablas de descriptores
description: 'Cada tabla de descriptores almacena descriptores de uno o más tipos: SRVs, UAVe, CBVs y Samplers. Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105185"
---
# <a name="descriptor-tables-overview"></a><span data-ttu-id="40407-104">Información general sobre tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="40407-104">Descriptor Tables Overview</span></span>

<span data-ttu-id="40407-105">Cada tabla de descriptores almacena descriptores de uno o más tipos: SRVs, UAVe, CBVs y Samplers.</span><span class="sxs-lookup"><span data-stu-id="40407-105">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="40407-106">Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="40407-106">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span>

-   [<span data-ttu-id="40407-107">Referencia a tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="40407-107">Referencing descriptor tables</span></span>](#referencing-descriptor-tables)
-   [<span data-ttu-id="40407-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40407-108">Related topics</span></span>](#related-topics)

## <a name="referencing-descriptor-tables"></a><span data-ttu-id="40407-109">Referencia a tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="40407-109">Referencing descriptor tables</span></span>

<span data-ttu-id="40407-110">La canalización de gráficos, a través de la firma raíz, obtiene acceso a los recursos haciendo referencia a las tablas de descriptores por índice.</span><span class="sxs-lookup"><span data-stu-id="40407-110">The graphics pipeline, through the root signature, gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="40407-111">Una tabla de descriptores es en realidad solo un subintervalo de un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="40407-111">A descriptor table is actually just a sub-range of a descriptor heap.</span></span> <span data-ttu-id="40407-112">Los montones descriptores representan la asignación de memoria subyacente para una colección de descriptores.</span><span class="sxs-lookup"><span data-stu-id="40407-112">Descriptor heaps represent the underlying memory allocation for a collection of descriptors.</span></span> <span data-ttu-id="40407-113">Dado que la asignación de memoria es una propiedad de la creación de un montón de descriptores, se garantiza que la definición de una tabla de descriptores fuera de uno es tan barata como identificar una región del montón en el hardware.</span><span class="sxs-lookup"><span data-stu-id="40407-113">Since memory allocation is a property of a creating a descriptor heap, defining a descriptor table out of one is guaranteed to be as cheap as identifying a region in the heap to the hardware.</span></span> <span data-ttu-id="40407-114">No es necesario crear ni destruir tablas de descriptores en el nivel de API: simplemente se identifican como un desplazamiento y el tamaño de un montón cuando se hace referencia a ellos.</span><span class="sxs-lookup"><span data-stu-id="40407-114">Descriptor tables don’t need to be created or destroyed at the API level– they are merely identified to drivers as an offset and size out of a heap whenever referenced.</span></span>

<span data-ttu-id="40407-115">En realidad, una aplicación puede definir tablas de descriptores muy grandes cuando sus sombreadores quieren tener la libertad de seleccionar entre un amplio conjunto de descriptores disponibles (a menudo, hacer referencia a texturas) sobre la marcha (quizás controlado por datos materiales).</span><span class="sxs-lookup"><span data-stu-id="40407-115">It is certainly possible for an app to define very large descriptor tables when its shaders want the freedom to select from a vast set of available descriptors (often referencing textures) on the fly (perhaps driven by material data).</span></span>

<span data-ttu-id="40407-116">La firma raíz hace referencia a la entrada de la tabla de descriptores con una referencia al montón, la ubicación inicial de la tabla (un desplazamiento desde el inicio del montón) y la longitud (en entradas) de la tabla.</span><span class="sxs-lookup"><span data-stu-id="40407-116">The Root Signature references the descriptor table entry with a reference to the heap, the start location of the table (an offset from the start of the heap), and the length (in entries) of the table.</span></span> <span data-ttu-id="40407-117">En la imagen siguiente se muestran estos conceptos: los punteros de tabla del descriptor de la firma raíz y los descriptores dentro del montón del descriptor que hace referencia a los datos de búfer o textura completos en un montón de carga.</span><span class="sxs-lookup"><span data-stu-id="40407-117">The image below shows these concepts: the descriptor table pointers from the Root Signature and the descriptors within the descriptor heap referencing the full texture or buffer data in an upload heap.</span></span>

![tablas de descriptores](images/descriptor-table.png)

## <a name="related-topics"></a><span data-ttu-id="40407-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40407-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40407-120">Tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="40407-120">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




