---
description: Uniscribe proporciona las API para admitir la tipografía y para admitir la visualización y edición de texto internacional, incluidas las complejas reglas de los scripts de Oriente Medio y asiático.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Usar Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678533"
---
# <a name="using-uniscribe"></a><span data-ttu-id="38210-103">Usar Uniscribe</span><span class="sxs-lookup"><span data-stu-id="38210-103">Using Uniscribe</span></span>

<span data-ttu-id="38210-104">Uniscribe proporciona las API para admitir la tipografía y para admitir la visualización y edición de texto internacional, incluidas las complejas reglas de los scripts de Oriente Medio y asiático.</span><span class="sxs-lookup"><span data-stu-id="38210-104">Uniscribe provides APIs to support typography and to support the display and editing of international text, including the complex rules of Middle Eastern and Asian scripts.</span></span> <span data-ttu-id="38210-105">Uniscribe proporciona rutinas de bajo nivel para controlar el texto con formato completo y un conjunto simple de API ScriptString para el texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="38210-105">Uniscribe provides low-level routines for handling fully formatted text, and a simple ScriptString API set for unformatted text.</span></span>

<span data-ttu-id="38210-106">Con Uniscribe, las aplicaciones solo tienen que administrar una memoria auxiliar de códigos de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="38210-106">Using Uniscribe, applications only have to manage a backing store of Unicode character codes.</span></span> <span data-ttu-id="38210-107">Las aplicaciones de diseño de texto no tienen que mantener ningún otro búfer ni tabla de asignación para realizar el seguimiento del orden de los caracteres.</span><span class="sxs-lookup"><span data-stu-id="38210-107">Text layout applications do not have to maintain any other buffer or mapping table to track character order.</span></span> <span data-ttu-id="38210-108">Cada aplicación solo tiene que almacenar y administrar el orden en el que el usuario escribe los caracteres, que es el mismo orden lógico definido por Unicode.</span><span class="sxs-lookup"><span data-stu-id="38210-108">Each application only has to store and manage the order in which the characters are entered by the user, which is the same logical order as defined by Unicode.</span></span> <span data-ttu-id="38210-109">La memoria auxiliar nunca cambia como resultado de las operaciones de diseño.</span><span class="sxs-lookup"><span data-stu-id="38210-109">The backing store never changes as a result of layout operations.</span></span> <span data-ttu-id="38210-110">Uniscribe mantiene un índice de los clústeres reordenados hasta los límites de caracteres originales pasados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38210-110">Uniscribe maintains an index from the reordered clusters to the original character boundaries passed by the application.</span></span>

<span data-ttu-id="38210-111">Los temas siguientes se tratan en esta sección.</span><span class="sxs-lookup"><span data-stu-id="38210-111">The following topics are covered in this section.</span></span>

<span data-ttu-id="38210-112">**Formas**</span><span class="sxs-lookup"><span data-stu-id="38210-112">**Shaping**</span></span>

-   [<span data-ttu-id="38210-113">Determinar si un script requiere la forma de glifos</span><span class="sxs-lookup"><span data-stu-id="38210-113">Determining If a Script Requires Glyph Shaping</span></span>](determining-if-a-script-requires-glyph-shaping.md)
-   [<span data-ttu-id="38210-114">Usar motores de modelado</span><span class="sxs-lookup"><span data-stu-id="38210-114">Using Shaping Engines</span></span>](using-shaping-engines.md)

<span data-ttu-id="38210-115">**Otro procesamiento**</span><span class="sxs-lookup"><span data-stu-id="38210-115">**Other Processing**</span></span>

-   [<span data-ttu-id="38210-116">Almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="38210-116">Caching</span></span>](caching.md)
-   [<span data-ttu-id="38210-117">Mostrar texto con Uniscribe</span><span class="sxs-lookup"><span data-stu-id="38210-117">Displaying Text with Uniscribe</span></span>](displaying-text-with-uniscribe.md)
-   [<span data-ttu-id="38210-118">Procesamiento de scripts complejos</span><span class="sxs-lookup"><span data-stu-id="38210-118">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
-   [<span data-ttu-id="38210-119">Usar la reserva de fuentes</span><span class="sxs-lookup"><span data-stu-id="38210-119">Using Font Fallback</span></span>](using-font-fallback.md)
-   [<span data-ttu-id="38210-120">Uso de las funciones ScriptString</span><span class="sxs-lookup"><span data-stu-id="38210-120">Using the ScriptString Functions</span></span>](using-the-scriptstring-functions.md)

<span data-ttu-id="38210-121">**Intercalación**</span><span class="sxs-lookup"><span data-stu-id="38210-121">**Caret**</span></span>

-   [<span data-ttu-id="38210-122">Mostrar el símbolo de intercalación en cadenas bidireccionales</span><span class="sxs-lookup"><span data-stu-id="38210-122">Displaying the Caret in Bidirectional Strings</span></span>](displaying-the-caret-in-bidirectional-strings.md)
-   [<span data-ttu-id="38210-123">Administrar la ubicación del símbolo de intercalación y la prueba de posicionamiento</span><span class="sxs-lookup"><span data-stu-id="38210-123">Managing Caret Placement and Hit Testing</span></span>](managing-caret-placement-and-hit-testing.md)
-   [<span data-ttu-id="38210-124">Trasladar el desplazamiento de la X hasta la posición del símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="38210-124">Translating Mouse Hit X Offset to Caret Position</span></span>](translating-mouse-hit-x-offset-to-caret-position.md)

<span data-ttu-id="38210-125">**Palabras y clústeres de caracteres**</span><span class="sxs-lookup"><span data-stu-id="38210-125">**Words and Character Clusters**</span></span>

-   [<span data-ttu-id="38210-126">Uso de clústeres de caracteres</span><span class="sxs-lookup"><span data-stu-id="38210-126">Using Character Clusters</span></span>](using-character-clusters.md)
-   [<span data-ttu-id="38210-127">Usar puntos de interrupción de palabras</span><span class="sxs-lookup"><span data-stu-id="38210-127">Using Word Break Points</span></span>](using-word-break-points.md)
-   [<span data-ttu-id="38210-128">Trabajar con relaciones entre posiciones del símbolo de intercalación, puntos de justificación y clústeres</span><span class="sxs-lookup"><span data-stu-id="38210-128">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



