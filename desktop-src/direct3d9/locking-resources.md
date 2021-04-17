---
description: El bloqueo de un recurso implica conceder acceso de CPU a su almacenamiento.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Bloquear recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705231"
---
# <a name="locking-resources-direct3d-9"></a><span data-ttu-id="88a21-103">Bloquear recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="88a21-103">Locking Resources (Direct3D 9)</span></span>

<span data-ttu-id="88a21-104">El bloqueo de un recurso implica conceder acceso de CPU a su almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="88a21-104">Locking a resource means granting CPU access to its storage.</span></span> <span data-ttu-id="88a21-105">Las siguientes opciones de bloqueo se definen para los recursos:</span><span class="sxs-lookup"><span data-stu-id="88a21-105">The following locking options are defined for resources:</span></span>

-   <span data-ttu-id="88a21-106">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="88a21-106">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="88a21-107">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="88a21-107">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="88a21-108">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="88a21-108">D3DLOCK\_NOOVERWRITE</span></span>
-   <span data-ttu-id="88a21-109">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="88a21-109">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="88a21-110">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="88a21-110">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>

<span data-ttu-id="88a21-111">Para obtener más información sobre las marcas de bloqueo y cómo se relacionan con recursos específicos, vea las páginas de referencia en los métodos de bloqueo de recursos individuales.</span><span class="sxs-lookup"><span data-stu-id="88a21-111">For details on locking flags and how they relate to specific resources, see the reference pages on the individual resource locking methods.</span></span> <span data-ttu-id="88a21-112">Los desarrolladores de aplicaciones deben tener en cuenta que las \_ marcas D3DLOCK discard, D3DLOCK \_ ReadOnly y D3DLOCK \_ NOOVERWRITE solo son sugerencias.</span><span class="sxs-lookup"><span data-stu-id="88a21-112">Application developers should note that the D3DLOCK\_DISCARD, D3DLOCK\_READONLY, and D3DLOCK\_NOOVERWRITE flags are only hints.</span></span> <span data-ttu-id="88a21-113">El tiempo de ejecución no comprueba que las aplicaciones estén siguiendo la funcionalidad especificada por estas marcas.</span><span class="sxs-lookup"><span data-stu-id="88a21-113">The run time does not check that applications are following the functionality specified by these flags.</span></span> <span data-ttu-id="88a21-114">Una aplicación que especifica D3DLOCK \_ ReadOnly pero después escribe en el recurso debe esperar resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="88a21-114">An application that specifies D3DLOCK\_READONLY but then writes to the resource should expect undefined results.</span></span> <span data-ttu-id="88a21-115">En general, no se garantiza que el trabajo con marcas de bloqueo, incluidas las marcas de uso de bloqueo, funcione en versiones posteriores y puede suponer una penalización significativa en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="88a21-115">In general, working against locking flags, including the locking usage flags, is not guaranteed to work in later releases and may incur a significant performance penalty.</span></span>

<span data-ttu-id="88a21-116">Una operación de bloqueo va seguida de una operación de desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="88a21-116">A lock operation is followed by an unlock operation.</span></span> <span data-ttu-id="88a21-117">Por ejemplo, después de bloquear una textura, la aplicación abandona posteriormente el acceso directo a las texturas bloqueadas mediante su desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="88a21-117">For example, after locking a texture, the application subsequently relinquishes direct access to locked textures by unlocking them.</span></span> <span data-ttu-id="88a21-118">Además de conceder acceso al procesador, cualquier otra operación que implique ese recurso se serializa mientras dure un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="88a21-118">In addition to granting processor access, any other operations involving that resource are serialized for the duration of a lock.</span></span> <span data-ttu-id="88a21-119">Solo se permite un bloqueo único para un recurso, incluso para las regiones que no se superponen, y no se pueden realizar operaciones de acelerador en una superficie mientras una operación de bloqueo esté pendiente en esa superficie.</span><span class="sxs-lookup"><span data-stu-id="88a21-119">Only a single lock for a resource is allowed, even for non-overlapping regions, and no accelerator operations on a surface can be ongoing while a lock operation is outstanding on that surface.</span></span>

<span data-ttu-id="88a21-120">Cada interfaz de recursos tiene métodos para bloquear los búferes contenidos.</span><span class="sxs-lookup"><span data-stu-id="88a21-120">Each resource interface has methods for locking the contained buffers.</span></span> <span data-ttu-id="88a21-121">Cada recurso de textura también puede bloquear una subparte de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="88a21-121">Each texture resource can also lock a sub-portion of that resource.</span></span> <span data-ttu-id="88a21-122">los recursos 2D (superficies) permiten el bloqueo de los subrectángulos y los recursos de volumen permiten el bloqueo de los subvolumens o cuadros.</span><span class="sxs-lookup"><span data-stu-id="88a21-122">2D resources (surfaces) allow the locking of sub-rectangles, and volume resources allow the locking of sub-volumes or boxes.</span></span> <span data-ttu-id="88a21-123">Cada método de bloqueo devuelve una estructura que contiene un puntero al almacenamiento que respalda el recurso y los valores que representan las distancias entre las filas o los planos de datos, dependiendo del tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="88a21-123">Each lock method returns a structure that contains a pointer to the storage backing the resource and values representing the distances between rows or planes of data, depending on the resource type.</span></span> <span data-ttu-id="88a21-124">Para obtener más información, consulte las listas de métodos de las interfaces de recursos.</span><span class="sxs-lookup"><span data-stu-id="88a21-124">For details, see the method lists for the resource interfaces.</span></span> <span data-ttu-id="88a21-125">El puntero devuelto siempre apunta al byte superior izquierdo de las subregiones bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="88a21-125">The returned pointer always points to the top-left byte in the locked sub-regions.</span></span>

<span data-ttu-id="88a21-126">Al trabajar con búferes de índice y vértices, puede realizar varias llamadas de bloqueo; sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="88a21-126">When working with index and vertex buffers, you can make multiple lock calls; however, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="88a21-127">DXTn almacena píxeles en bloques 4x4 codificados y solo se puede bloquear en límites 4x4.</span><span class="sxs-lookup"><span data-stu-id="88a21-127">The DXTn store pixels in encoded 4x4 blocks, and can only be locked on 4x4 boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88a21-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88a21-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88a21-129">Recursos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="88a21-129">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



