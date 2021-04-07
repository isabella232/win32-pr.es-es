---
description: configuración regional \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003221"
---
# <a name="locale_sgrouping"></a><span data-ttu-id="084f3-103">configuración regional \_ SGROUPING</span><span class="sxs-lookup"><span data-stu-id="084f3-103">LOCALE\_SGROUPING</span></span>

<span data-ttu-id="084f3-104">Tamaños de cada grupo de dígitos a la izquierda del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="084f3-104">Sizes for each group of digits to the left of the decimal.</span></span> <span data-ttu-id="084f3-105">El número máximo de caracteres permitido para esta cadena es diez, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="084f3-105">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="084f3-106">Se necesita un tamaño explícito para cada grupo y los tamaños se separan mediante signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="084f3-106">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="084f3-107">Si el último valor es 0, el valor anterior se repite.</span><span class="sxs-lookup"><span data-stu-id="084f3-107">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="084f3-108">Por ejemplo, para agrupar miles, especifique 3; 0.</span><span class="sxs-lookup"><span data-stu-id="084f3-108">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="084f3-109">Configuraciones regionales indias agrupe los primeros mil y, después, agrupe por cientos.</span><span class="sxs-lookup"><span data-stu-id="084f3-109">Indic locales group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="084f3-110">Por ejemplo, 12, 34, 56789 se representa mediante 3; 2; 0.</span><span class="sxs-lookup"><span data-stu-id="084f3-110">For example, 12,34,56,789 is represented by 3;2;0.</span></span>

<span data-ttu-id="084f3-111">Otros ejemplos:</span><span class="sxs-lookup"><span data-stu-id="084f3-111">Further examples:</span></span>



| <span data-ttu-id="084f3-112">Especificación</span><span class="sxs-lookup"><span data-stu-id="084f3-112">Specification</span></span> | <span data-ttu-id="084f3-113">Cadena resultante</span><span class="sxs-lookup"><span data-stu-id="084f3-113">Resulting string</span></span>   |
|---------------|--------------------|
| <span data-ttu-id="084f3-114">3; 0</span><span class="sxs-lookup"><span data-stu-id="084f3-114">3;0</span></span>           | <span data-ttu-id="084f3-115">3 billones</span><span class="sxs-lookup"><span data-stu-id="084f3-115">3,000,000,000,000</span></span>  |
| <span data-ttu-id="084f3-116">3; 2; 0</span><span class="sxs-lookup"><span data-stu-id="084f3-116">3;2;0</span></span>         | <span data-ttu-id="084f3-117">30, 00, 00, 00, 00000</span><span class="sxs-lookup"><span data-stu-id="084f3-117">30,00,00,00,00,000</span></span> |
| <span data-ttu-id="084f3-118">3</span><span class="sxs-lookup"><span data-stu-id="084f3-118">3</span></span>             | <span data-ttu-id="084f3-119">3 billones</span><span class="sxs-lookup"><span data-stu-id="084f3-119">3000000000,000</span></span>     |
| <span data-ttu-id="084f3-120">3; 2</span><span class="sxs-lookup"><span data-stu-id="084f3-120">3;2</span></span>           | <span data-ttu-id="084f3-121">30000000, 00000</span><span class="sxs-lookup"><span data-stu-id="084f3-121">30000000,00,000</span></span>    |



 

 

 



