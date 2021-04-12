---
title: DirectComposition
description: En este tema se explica el propósito de Microsoft DirectComposition, se identifican los requisitos de tiempo de ejecución y se describe el fondo de programación que necesita para usar Microsoft DirectComposition de forma eficaz.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API de DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356898"
---
# <a name="directcomposition"></a><span data-ttu-id="64b09-106">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="64b09-106">DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="64b09-107">En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="64b09-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="64b09-108">Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="64b09-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

## <a name="purpose"></a><span data-ttu-id="64b09-109">Propósito</span><span class="sxs-lookup"><span data-stu-id="64b09-109">Purpose</span></span>

<span data-ttu-id="64b09-110">Microsoft DirectComposition es un componente de Windows que permite la composición de mapas de bits de alto rendimiento con transformaciones, efectos y animaciones.</span><span class="sxs-lookup"><span data-stu-id="64b09-110">Microsoft DirectComposition is a Windows component that enables high-performance bitmap composition with transforms, effects, and animations.</span></span> <span data-ttu-id="64b09-111">Los desarrolladores de aplicaciones pueden usar la API DirectComposition para crear interfaces de usuario visualmente atractivas y que ofrezcan transiciones animadas fluidas y enriquecidas, de un objeto visual a otro.</span><span class="sxs-lookup"><span data-stu-id="64b09-111">Application developers can use the DirectComposition API to create visually engaging user interfaces that feature rich and fluid animated transitions from one visual to another.</span></span>

<span data-ttu-id="64b09-112">DirectComposition permite transiciones enriquecidas y fluidas al conseguir una velocidad de fotogramas alta, usar hardware de gráficos y trabajar independientemente del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="64b09-112">DirectComposition enables rich and fluid transitions by achieving a high framerate, using graphics hardware, and operating independently of the UI thread.</span></span> <span data-ttu-id="64b09-113">DirectComposition puede aceptar el contenido del mapa de bits dibujado por diferentes bibliotecas de representación, incluidos los mapas de bits de Microsoft DirectX, y los mapas de bits representados en una ventana (mapas de bits HWND).</span><span class="sxs-lookup"><span data-stu-id="64b09-113">DirectComposition can accept bitmap content drawn by different rendering libraries, including Microsoft DirectX bitmaps, and bitmaps rendered to a window (HWND bitmaps).</span></span> <span data-ttu-id="64b09-114">Además, DirectComposition admite una variedad de transformaciones, como transformaciones afines de 2D y transformaciones de perspectiva 3D, así como efectos básicos como el recorte y la opacidad.</span><span class="sxs-lookup"><span data-stu-id="64b09-114">Also, DirectComposition supports a variety of transformations, such as 2D affine transforms and 3D perspective transforms, as well as basic effects such as clipping and opacity.</span></span>

<span data-ttu-id="64b09-115">DirectComposition está diseñado para simplificar el proceso de composición de [*objetos visuales*](directcomposition-glossary.md) y la creación de transiciones animadas.</span><span class="sxs-lookup"><span data-stu-id="64b09-115">DirectComposition is designed to simplify the process of composing [*visuals*](directcomposition-glossary.md) and creating animated transitions.</span></span> <span data-ttu-id="64b09-116">Si su aplicación ya contiene código de representación o ya usa la API de DirectX recomendada, solo tiene que realizar una cantidad mínima de trabajo para usar DirectComposition de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="64b09-116">If your application already contains rendering code or already uses the recommended DirectX API, you only need to do a minimal amount of work to use DirectComposition effectively.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="64b09-117">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="64b09-117">Developer audience</span></span>

<span data-ttu-id="64b09-118">La API de DirectComposition está destinada a desarrolladores de gráficos experimentados y altamente compatibles que saben C/C++, tienen una comprensión sólida del modelo de objetos componentes (COM) y están familiarizados con los conceptos de programación de Windows.</span><span class="sxs-lookup"><span data-stu-id="64b09-118">The DirectComposition API is intended for experienced and highly-capable graphics developers who know C/C++, have a solid understanding of the Component Object Model (COM), and are familiar with Windows programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="64b09-119">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="64b09-119">Run-time requirements</span></span>

<span data-ttu-id="64b09-120">DirectComposition se presentó en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="64b09-120">DirectComposition was introduced in Windows 8.</span></span> <span data-ttu-id="64b09-121">Se incluye en plataformas de 32 bits, 64 bits y ARM.</span><span class="sxs-lookup"><span data-stu-id="64b09-121">It is included in 32-bit, 64-bit, and ARM platforms.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64b09-122">En esta sección</span><span class="sxs-lookup"><span data-stu-id="64b09-122">In this section</span></span>



| <span data-ttu-id="64b09-123">Tema</span><span class="sxs-lookup"><span data-stu-id="64b09-123">Topic</span></span>                                                                       | <span data-ttu-id="64b09-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="64b09-124">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64b09-125">¿Por qué usar DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="64b09-125">Why use DirectComposition?</span></span>](why-use-directcomposition-.md)<br/>     | <span data-ttu-id="64b09-126">En este tema se describen las capacidades y ventajas de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="64b09-126">This topic describes the capabilities and benefits of DirectComposition.</span></span> <br/>                                                                           |
| [<span data-ttu-id="64b09-127">Cómo usar DirectComposition</span><span class="sxs-lookup"><span data-stu-id="64b09-127">How to Use DirectComposition</span></span>](how-to-use-directcomposition.md)<br/> | <span data-ttu-id="64b09-128">En esta sección se describen los procedimientos recomendados para usar la API de DirectComposition y se muestra cómo usar la API para realizar varias tareas comunes.</span><span class="sxs-lookup"><span data-stu-id="64b09-128">This section describes best practices for using the DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span> <br/> |
| [<span data-ttu-id="64b09-129">Conceptos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="64b09-129">DirectComposition concepts</span></span>](directcomposition-concepts.md)<br/>     | <span data-ttu-id="64b09-130">En esta sección se proporciona información general conceptual de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="64b09-130">This section provides a conceptual overview of DirectComposition.</span></span><br/>                                                                                   |
| [<span data-ttu-id="64b09-131">Referencia de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="64b09-131">DirectComposition reference</span></span>](reference.md)<br/>                     | <span data-ttu-id="64b09-132">En esta sección se proporciona información de referencia detallada para los elementos que componen la API de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="64b09-132">This section provides detailed reference information for the elements that make up the DirectComposition API.</span></span><br/>                                       |
| [<span data-ttu-id="64b09-133">Ejemplos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="64b09-133">DirectComposition samples</span></span>](directcomposition-code-samples.md)<br/>  | <span data-ttu-id="64b09-134">Las aplicaciones de ejemplo siguientes muestran cómo usar la API de DirectComposition y demostrar sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="64b09-134">The following sample applications show how to use the DirectComposition API and demonstrate its capabilities.</span></span> <br/>                                      |
| [<span data-ttu-id="64b09-135">Glosario DirectComposition</span><span class="sxs-lookup"><span data-stu-id="64b09-135">DirectComposition glossary</span></span>](directcomposition-glossary.md)<br/>     | <span data-ttu-id="64b09-136">En este tema se definen los términos de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="64b09-136">This topic defines DirectComposition terms.</span></span> <br/>                                                                                                        |



 

 

 





