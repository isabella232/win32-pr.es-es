---
description: ICE78 comprueba que la tabla AdvtUISequence no existe o está vacía. Esto es necesario porque no se permite ninguna interfaz de usuario durante la publicidad.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154813"
---
# <a name="ice78"></a><span data-ttu-id="5c482-104">ICE78</span><span class="sxs-lookup"><span data-stu-id="5c482-104">ICE78</span></span>

<span data-ttu-id="5c482-105">ICE78 comprueba que la [tabla AdvtUISequence](advtuisequence-table.md) no existe o está vacía.</span><span class="sxs-lookup"><span data-stu-id="5c482-105">ICE78 verifies that the [AdvtUISequence table](advtuisequence-table.md) either does not exist or is empty.</span></span> <span data-ttu-id="5c482-106">Esto es necesario porque no se permite ninguna interfaz de usuario durante la publicidad.</span><span class="sxs-lookup"><span data-stu-id="5c482-106">This is required because no user interface is allowed during advertising.</span></span>

## <a name="result"></a><span data-ttu-id="5c482-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="5c482-107">Result</span></span>

<span data-ttu-id="5c482-108">ICE78 publica un error si la tabla AdvtUISequence existe y no está vacía.</span><span class="sxs-lookup"><span data-stu-id="5c482-108">ICE78 posts an error if the AdvtUISequence table exists and is not empty.</span></span>

## <a name="example"></a><span data-ttu-id="5c482-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c482-109">Example</span></span>

<span data-ttu-id="5c482-110">ICE78 notifica el siguiente error para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5c482-110">ICE78 reports the following error for the example:</span></span>

<span data-ttu-id="5c482-111">Se encontró la acción ' Action1 ' en la tabla AdvtUISequence.</span><span class="sxs-lookup"><span data-stu-id="5c482-111">Action 'Action1' found in AdvtUISequence table.</span></span> <span data-ttu-id="5c482-112">No se permite ninguna interfaz de usuario durante la publicidad.</span><span class="sxs-lookup"><span data-stu-id="5c482-112">No UI is allowed during advertising.</span></span> <span data-ttu-id="5c482-113">Por lo tanto, la tabla AdvtUISequence debe estar vacía o no presente.</span><span class="sxs-lookup"><span data-stu-id="5c482-113">Therefore AdvtUISequence table must be empty or not present.</span></span>

<span data-ttu-id="5c482-114">[Tabla AdvtUISequence](advtuisequence-table.md)(parcial)</span><span class="sxs-lookup"><span data-stu-id="5c482-114">[AdvtUISequence table](advtuisequence-table.md)(partial)</span></span>



| <span data-ttu-id="5c482-115">Acción</span><span class="sxs-lookup"><span data-stu-id="5c482-115">Action</span></span>  | <span data-ttu-id="5c482-116">Condición</span><span class="sxs-lookup"><span data-stu-id="5c482-116">Condition</span></span> | <span data-ttu-id="5c482-117">Secuencia</span><span class="sxs-lookup"><span data-stu-id="5c482-117">Sequence</span></span> |
|---------|-----------|----------|
| <span data-ttu-id="5c482-118">Action1</span><span class="sxs-lookup"><span data-stu-id="5c482-118">Action1</span></span> | <span data-ttu-id="5c482-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="5c482-119">TRUE</span></span>      | <span data-ttu-id="5c482-120">1</span><span class="sxs-lookup"><span data-stu-id="5c482-120">1</span></span>        |



 

<span data-ttu-id="5c482-121">Para corregir el error, quite "Action1" de la tabla o quite la tabla.</span><span class="sxs-lookup"><span data-stu-id="5c482-121">To fix the error, either remove "Action1" from the table, or remove the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c482-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c482-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c482-123">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="5c482-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



