---
title: Cadenas de formato de procedimiento
description: La siguiente es una descripción completa de la cadena de formato. Ensambla todas las capas relacionadas con diferentes fases de la evolución del intérprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995490"
---
# <a name="procedure-format-strings"></a><span data-ttu-id="444ea-104">Cadenas de formato de procedimiento</span><span class="sxs-lookup"><span data-stu-id="444ea-104">Procedure Format Strings</span></span>

<span data-ttu-id="444ea-105">La siguiente es una descripción completa de la cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="444ea-105">The following is a complete format string description.</span></span> <span data-ttu-id="444ea-106">Ensambla todas las capas relacionadas con diferentes fases de la evolución del intérprete.</span><span class="sxs-lookup"><span data-stu-id="444ea-106">It assembles all layers related to different stages of the interpreter evolution.</span></span>

## <a name="procedure-descriptor-overview"></a><span data-ttu-id="444ea-107">Introducción a los descriptores de procedimientos</span><span class="sxs-lookup"><span data-stu-id="444ea-107">Procedure Descriptor Overview</span></span>

<span data-ttu-id="444ea-108">Un descriptor de procedimiento consta de los descriptores de encabezado y los descriptores de parámetros.</span><span class="sxs-lookup"><span data-stu-id="444ea-108">A procedure descriptor consists of the header descriptors and the parameter descriptors.</span></span> <span data-ttu-id="444ea-109">La descripción del estilo [**– OI**](/windows/desktop/Midl/-oi) se considera obsoleta, en términos de uso común en la programación RPC actual.</span><span class="sxs-lookup"><span data-stu-id="444ea-109">The [**–Oi**](/windows/desktop/Midl/-oi) style description is considered outdated, in terms of common usage in current RPC programming.</span></span> <span data-ttu-id="444ea-110">**: Los salientes** se consideran más actuales.</span><span class="sxs-lookup"><span data-stu-id="444ea-110">The **–Oif** is considered more current.</span></span>

## <a name="the-oi-style-description"></a><span data-ttu-id="444ea-111">La descripción del estilo – OI</span><span class="sxs-lookup"><span data-stu-id="444ea-111">The –Oi Style Description</span></span>

<span data-ttu-id="444ea-112">Esta descripción consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="444ea-112">This description consists of the following:</span></span>

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

<span data-ttu-id="444ea-113">El encabezado tendría de 6 a 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="444ea-113">The header would have from 6 to 16 bytes.</span></span>

<span data-ttu-id="444ea-114">La descripción completa se genera al compilar en el modo [**OI**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="444ea-114">The complete description is generated when compiling in [**–Oi**](/windows/desktop/Midl/-oi) mode.</span></span> <span data-ttu-id="444ea-115">En el modo [**– os**](/windows/desktop/Midl/-os) , solo se generan los descriptores de parámetro, que se usan para la conversión.</span><span class="sxs-lookup"><span data-stu-id="444ea-115">In [**–Os**](/windows/desktop/Midl/-os) mode, only the parameter descriptors are generated, which are used for conversion.</span></span> <span data-ttu-id="444ea-116">El intérprete de selección usa descriptores de parámetros de estilo antiguos.</span><span class="sxs-lookup"><span data-stu-id="444ea-116">The pickling interpreter uses old style parameter descriptors.</span></span>

## <a name="the-oif-style-description"></a><span data-ttu-id="444ea-117">La descripción del estilo – salientes</span><span class="sxs-lookup"><span data-stu-id="444ea-117">The –Oif Style Description</span></span>

<span data-ttu-id="444ea-118">La descripción consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="444ea-118">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

<span data-ttu-id="444ea-119">El descriptor de encabezado de estilo [**–FUL**](/windows/desktop/Midl/-oi) está compuesto por</span><span class="sxs-lookup"><span data-stu-id="444ea-119">The [**–Oif**](/windows/desktop/Midl/-oi) style header descriptor consists of</span></span>

<span data-ttu-id="444ea-120">La descripción del estilo – interfaces se genera al compilar en el modo [**-**](/windows/desktop/Midl/-oi) transformated o **– Oicf** del compilador.</span><span class="sxs-lookup"><span data-stu-id="444ea-120">The –Oif style description is generated when compiling in [**–Oif**](/windows/desktop/Midl/-oi) or **–Oicf** mode of the compiler.</span></span>

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

<span data-ttu-id="444ea-121">Algunas características más recientes como canalización, Async y [**/Robust**](/windows/desktop/Midl/-robust) fuerzan el modo [**– Oicf**](/windows/desktop/Midl/-oi) del compilador cuando se usan.</span><span class="sxs-lookup"><span data-stu-id="444ea-121">Some more recent features like pipe, async, and [**/robust**](/windows/desktop/Midl/-robust) force the [**–Oicf**](/windows/desktop/Midl/-oi) mode of the compiler, when used.</span></span>

## <a name="the-extended-oif-description"></a><span data-ttu-id="444ea-122">Descripción extendida – interfaces</span><span class="sxs-lookup"><span data-stu-id="444ea-122">The Extended –Oif Description</span></span>

<span data-ttu-id="444ea-123">La descripción consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="444ea-123">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 