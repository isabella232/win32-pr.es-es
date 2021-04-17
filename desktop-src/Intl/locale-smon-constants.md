---
description: Constantes de SMON de configuración regional \_ \*
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Constantes de LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666809"
---
# <a name="locale_smon-constants"></a><span data-ttu-id="3e3a9-103">Constantes de SMON de configuración regional \_ \*</span><span class="sxs-lookup"><span data-stu-id="3e3a9-103">LOCALE\_SMON\* Constants</span></span>

<span data-ttu-id="3e3a9-104">En este tema se definen las \_ constantes de SMON de configuración regional \* utilizadas por NLS en que representan valores monetarios.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-104">This topic defines the LOCALE\_SMON\* constants used by NLS in representing monetary values.</span></span>



| <span data-ttu-id="3e3a9-105">Value</span><span class="sxs-lookup"><span data-stu-id="3e3a9-105">Value</span></span>                   | <span data-ttu-id="3e3a9-106">Significado</span><span class="sxs-lookup"><span data-stu-id="3e3a9-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3a9-107">configuración regional \_ SMONDECIMALSEP</span><span class="sxs-lookup"><span data-stu-id="3e3a9-107">LOCALE\_SMONDECIMALSEP</span></span>  | <span data-ttu-id="3e3a9-108">Caracteres usados como separador decimal monetario.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-108">Character(s) used as the monetary decimal separator.</span></span> <span data-ttu-id="3e3a9-109">El número máximo de caracteres permitido para esta cadena es cuatro, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="3e3a9-110">Por ejemplo, si se muestra un importe monetario como "$3,40", del mismo modo que se muestra "tres dólares y 40 céntimos" en el Estados Unidos, el separador decimal monetario es ".".</span><span class="sxs-lookup"><span data-stu-id="3e3a9-110">For example, if a monetary amount is displayed as "$3.40", just as "three dollars and forty cents" is displayed in the United States, then the monetary decimal separator is ".".</span></span>                                                                                                                                             |
| <span data-ttu-id="3e3a9-111">configuración regional \_ SMONGROUPING</span><span class="sxs-lookup"><span data-stu-id="3e3a9-111">LOCALE\_SMONGROUPING</span></span>    | <span data-ttu-id="3e3a9-112">Tamaños de cada grupo de dígitos monetarios a la izquierda del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-112">Sizes for each group of monetary digits to the left of the decimal.</span></span> <span data-ttu-id="3e3a9-113">El número máximo de caracteres permitido para esta cadena es diez, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-113">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="3e3a9-114">Se necesita un tamaño explícito para cada grupo y los tamaños se separan mediante signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-114">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="3e3a9-115">Si el último valor es 0, el valor anterior se repite.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-115">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="3e3a9-116">Por ejemplo, para agrupar miles, especifique 3; 0.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-116">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="3e3a9-117">Los idiomas indios agrupan los primeros mil y luego agrupan por cientos.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-117">Indic languages group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="3e3a9-118">Por ejemplo, 12, 34, 56789 se representa mediante 3; 2; 0.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-118">For example 12,34,56,789 is represented by 3;2;0.</span></span> |
| <span data-ttu-id="3e3a9-119">configuración regional \_ SMONTHOUSANDSEP</span><span class="sxs-lookup"><span data-stu-id="3e3a9-119">LOCALE\_SMONTHOUSANDSEP</span></span> | <span data-ttu-id="3e3a9-120">Caracteres usados como separador monetario entre grupos de dígitos a la izquierda del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-120">Character(s) used as the monetary separator between groups of digits to the left of the decimal.</span></span> <span data-ttu-id="3e3a9-121">El número máximo de caracteres permitido para esta cadena es cuatro, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-121">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="3e3a9-122">Normalmente, los grupos representan miles.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-122">Typically, the groups represent thousands.</span></span> <span data-ttu-id="3e3a9-123">Sin embargo, en función del valor especificado para SMONGROUPING de configuración regional \_ , pueden representar otra cosa.</span><span class="sxs-lookup"><span data-stu-id="3e3a9-123">However, depending on the value specified for LOCALE\_SMONGROUPING, they can represent something else.</span></span>                                                                                                                                 |



 

 

 



