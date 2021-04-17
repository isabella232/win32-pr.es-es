---
description: ICE08 valida que la tabla de componentes no contiene GUID duplicados. Cada componente debe tener un GUID único. No se realiza ninguna validación si la tabla de componentes no existe.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667774"
---
# <a name="ice08"></a><span data-ttu-id="a1f56-105">ICE08</span><span class="sxs-lookup"><span data-stu-id="a1f56-105">ICE08</span></span>

<span data-ttu-id="a1f56-106">ICE08 valida que la [tabla de componentes](component-table.md) no contiene [GUID](guid.md)duplicados.</span><span class="sxs-lookup"><span data-stu-id="a1f56-106">ICE08 validates that the [Component table](component-table.md) contains no duplicate [GUIDs](guid.md).</span></span> <span data-ttu-id="a1f56-107">Cada componente debe tener un GUID único.</span><span class="sxs-lookup"><span data-stu-id="a1f56-107">Every component must have a unique GUID.</span></span> <span data-ttu-id="a1f56-108">No se realiza ninguna validación si la tabla de componentes no existe.</span><span class="sxs-lookup"><span data-stu-id="a1f56-108">No validation is done if the Component table does not exist.</span></span>

## <a name="result"></a><span data-ttu-id="a1f56-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="a1f56-109">Result</span></span>

<span data-ttu-id="a1f56-110">ICE08 envía un mensaje de error si dos o más entradas de la columna ComponentId de la tabla de componentes contienen el mismo GUID.</span><span class="sxs-lookup"><span data-stu-id="a1f56-110">ICE08 posts an error message if two or more entries in the ComponentId column of the Component table contain the same GUID.</span></span>

## <a name="example"></a><span data-ttu-id="a1f56-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1f56-111">Example</span></span>

<span data-ttu-id="a1f56-112">En el ejemplo siguiente, ICE08 publicaría un mensaje que indica que los componentes rojo y verde tienen GUID duplicados.</span><span class="sxs-lookup"><span data-stu-id="a1f56-112">For the following example, ICE08 would post a message stating that components Red and Green have duplicate GUIDs.</span></span>

<span data-ttu-id="a1f56-113">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a1f56-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a1f56-114">Componente</span><span class="sxs-lookup"><span data-stu-id="a1f56-114">Component</span></span> | <span data-ttu-id="a1f56-115">ComponentId</span><span class="sxs-lookup"><span data-stu-id="a1f56-115">ComponentId</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="a1f56-116">Rojo</span><span class="sxs-lookup"><span data-stu-id="a1f56-116">Red</span></span>       | <span data-ttu-id="a1f56-117">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="a1f56-117">{0000000A-0003-0000-0000-624474736554}</span></span> |
| <span data-ttu-id="a1f56-118">Azul</span><span class="sxs-lookup"><span data-stu-id="a1f56-118">Blue</span></span>      | <span data-ttu-id="a1f56-119">{0000000A-0003-0000-0000-624474736354}</span><span class="sxs-lookup"><span data-stu-id="a1f56-119">{0000000A-0003-0000-0000-624474736354}</span></span> |
| <span data-ttu-id="a1f56-120">Verde</span><span class="sxs-lookup"><span data-stu-id="a1f56-120">Green</span></span>     | <span data-ttu-id="a1f56-121">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="a1f56-121">{0000000A-0003-0000-0000-624474736554}</span></span> |



 

<span data-ttu-id="a1f56-122">Para corregir este error, cambie uno de los GUID duplicados.</span><span class="sxs-lookup"><span data-stu-id="a1f56-122">To fix this error, change either of the duplicate GUIDs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1f56-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1f56-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1f56-124">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="a1f56-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



