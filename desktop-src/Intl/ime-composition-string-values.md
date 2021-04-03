---
description: Estos valores se usan con la composición de ImmGetCompositionString y el IME de WM \_ \_ .
ms.assetid: 14087598-8041-4e02-a168-f5538a437be0
title: Valores de cadena de composición de IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5b3935329e56f015cdb08a764e1660142a067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908125"
---
# <a name="ime-composition-string-values"></a><span data-ttu-id="bf5ea-103">Valores de cadena de composición de IME</span><span class="sxs-lookup"><span data-stu-id="bf5ea-103">IME Composition String Values</span></span>

<span data-ttu-id="bf5ea-104">Estos valores se usan con la [**\_ \_ composición**](wm-ime-composition.md)de [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) y el IME de WM.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-104">These values are used with [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) and [**WM\_IME\_COMPOSITION**](wm-ime-composition.md).</span></span>



| <span data-ttu-id="bf5ea-105">Value</span><span class="sxs-lookup"><span data-stu-id="bf5ea-105">Value</span></span>                 | <span data-ttu-id="bf5ea-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf5ea-106">Description</span></span>                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5ea-107">GC \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="bf5ea-107">GCS\_COMPATTR</span></span>         | <span data-ttu-id="bf5ea-108">Recupere o actualice el atributo de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-108">Retrieve or update the attribute of the composition string.</span></span>                                |
| <span data-ttu-id="bf5ea-109">GC \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="bf5ea-109">GCS\_COMPCLAUSE</span></span>       | <span data-ttu-id="bf5ea-110">Recuperar o actualizar la información de la cláusula de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-110">Retrieve or update clause information of the composition string.</span></span>                           |
| <span data-ttu-id="bf5ea-111">GC \_ COMPREADATTR</span><span class="sxs-lookup"><span data-stu-id="bf5ea-111">GCS\_COMPREADATTR</span></span>     | <span data-ttu-id="bf5ea-112">Recuperar o actualizar los atributos de la cadena de lectura de la composición actual.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-112">Retrieve or update the attributes of the reading string of the current composition.</span></span>        |
| <span data-ttu-id="bf5ea-113">GC \_ COMPREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="bf5ea-113">GCS\_COMPREADCLAUSE</span></span>   | <span data-ttu-id="bf5ea-114">Recuperar o actualizar la información de la cláusula de lectura de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-114">Retrieve or update the clause information of the reading string of the composition string.</span></span> |
| <span data-ttu-id="bf5ea-115">GC \_ COMPREADSTR</span><span class="sxs-lookup"><span data-stu-id="bf5ea-115">GCS\_COMPREADSTR</span></span>      | <span data-ttu-id="bf5ea-116">Recupera o actualiza la cadena de lectura de la composición actual.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-116">Retrieve or update the reading string of the current composition.</span></span>                          |
| <span data-ttu-id="bf5ea-117">GC \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="bf5ea-117">GCS\_COMPSTR</span></span>          | <span data-ttu-id="bf5ea-118">Recuperar o actualizar la cadena de composición actual.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-118">Retrieve or update the current composition string.</span></span>                                         |
| <span data-ttu-id="bf5ea-119">GC \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="bf5ea-119">GCS\_CURSORPOS</span></span>        | <span data-ttu-id="bf5ea-120">Recupera o actualiza la posición del cursor en la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-120">Retrieve or update the cursor position in composition string.</span></span>                              |
| <span data-ttu-id="bf5ea-121">GC \_ DELTASTART</span><span class="sxs-lookup"><span data-stu-id="bf5ea-121">GCS\_DELTASTART</span></span>       | <span data-ttu-id="bf5ea-122">Recupera o actualiza la posición inicial de los cambios en la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-122">Retrieve or update the starting position of any changes in composition string.</span></span>             |
| <span data-ttu-id="bf5ea-123">GC \_ RESULTCLAUSE</span><span class="sxs-lookup"><span data-stu-id="bf5ea-123">GCS\_RESULTCLAUSE</span></span>     | <span data-ttu-id="bf5ea-124">Recuperar o actualizar la información de la cláusula de la cadena de resultado.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-124">Retrieve or update clause information of the result string.</span></span>                                |
| <span data-ttu-id="bf5ea-125">GC \_ RESULTREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="bf5ea-125">GCS\_RESULTREADCLAUSE</span></span> | <span data-ttu-id="bf5ea-126">Recuperar o actualizar la información de las cláusulas de la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-126">Retrieve or update clause information of the reading string.</span></span>                               |
| <span data-ttu-id="bf5ea-127">GC \_ RESULTREADSTR</span><span class="sxs-lookup"><span data-stu-id="bf5ea-127">GCS\_RESULTREADSTR</span></span>    | <span data-ttu-id="bf5ea-128">Recuperar o actualizar la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-128">Retrieve or update the reading string.</span></span>                                                     |
| <span data-ttu-id="bf5ea-129">RESULTSTR de GC \_</span><span class="sxs-lookup"><span data-stu-id="bf5ea-129">GCS\_RESULTSTR</span></span>        | <span data-ttu-id="bf5ea-130">Recupere o actualice la cadena del resultado de la composición.</span><span class="sxs-lookup"><span data-stu-id="bf5ea-130">Retrieve or update the string of the composition result.</span></span>                                   |



 

 

 



