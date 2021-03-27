---
title: RWBuffer
description: Un búfer de lectura/escritura.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- HLSL de RWBuffer
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358113"
---
# <a name="rwbuffer"></a><span data-ttu-id="b1a91-104">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="b1a91-104">RWBuffer</span></span>

<span data-ttu-id="b1a91-105">Un búfer de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="b1a91-105">A read/write buffer.</span></span>



| <span data-ttu-id="b1a91-106">Método</span><span class="sxs-lookup"><span data-stu-id="b1a91-106">Method</span></span>                                                     | <span data-ttu-id="b1a91-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1a91-107">Description</span></span>                            |
|------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="b1a91-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="b1a91-108">**GetDimensions**</span></span>](sm5-object-rwbuffer-getdimensions.md) | <span data-ttu-id="b1a91-109">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1a91-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="b1a91-110">**Carga**</span><span class="sxs-lookup"><span data-stu-id="b1a91-110">**Load**</span></span>](rwbuffer-load.md)                              | <span data-ttu-id="b1a91-111">Obtiene un valor en un búfer de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b1a91-111">Gets one value in a read-write buffer.</span></span> |
| <span data-ttu-id="b1a91-112">[**Operador\[\]**](sm5-object-rwbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b1a91-112">[**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="b1a91-113">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="b1a91-113">Returns a resource variable.</span></span>           |



 

<span data-ttu-id="b1a91-114">También se puede pasar una variable de recurso a cualquier operación sin ordenar o interbloqueada.</span><span class="sxs-lookup"><span data-stu-id="b1a91-114">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="b1a91-115">Los objetos **RWBuffer** pueden ir precedidos de la clase de almacenamiento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-115">**RWBuffer** objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="b1a91-116">Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras.</span><span class="sxs-lookup"><span data-stu-id="b1a91-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="b1a91-117">Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.</span><span class="sxs-lookup"><span data-stu-id="b1a91-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="b1a91-118">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b1a91-118">Minimum Shader Model</span></span>

<span data-ttu-id="b1a91-119">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b1a91-119">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="b1a91-120">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b1a91-120">Shader Model</span></span>                                                                | <span data-ttu-id="b1a91-121">Compatible</span><span class="sxs-lookup"><span data-stu-id="b1a91-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b1a91-122">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b1a91-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b1a91-123">sí</span><span class="sxs-lookup"><span data-stu-id="b1a91-123">yes</span></span>       |



 

<span data-ttu-id="b1a91-124">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b1a91-124">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b1a91-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="b1a91-125">Vertex</span></span> | <span data-ttu-id="b1a91-126">Casco</span><span class="sxs-lookup"><span data-stu-id="b1a91-126">Hull</span></span> | <span data-ttu-id="b1a91-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="b1a91-127">Domain</span></span> | <span data-ttu-id="b1a91-128">Geometría</span><span class="sxs-lookup"><span data-stu-id="b1a91-128">Geometry</span></span> | <span data-ttu-id="b1a91-129">Píxel</span><span class="sxs-lookup"><span data-stu-id="b1a91-129">Pixel</span></span> | <span data-ttu-id="b1a91-130">Compute</span><span class="sxs-lookup"><span data-stu-id="b1a91-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b1a91-131">x</span><span class="sxs-lookup"><span data-stu-id="b1a91-131">x</span></span>     | <span data-ttu-id="b1a91-132">x</span><span class="sxs-lookup"><span data-stu-id="b1a91-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b1a91-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1a91-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a91-134">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b1a91-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




