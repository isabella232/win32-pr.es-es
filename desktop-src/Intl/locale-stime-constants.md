---
description: Constantes de \_ STime de configuración regional \*
ms.assetid: d16e7e0c-93f1-4f08-a319-02b717b7d33b
title: Constantes de LOCALE_STIME *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603d1ae16f57c3944ce6803bea0cc6ad0354372b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811311"
---
# <a name="locale_stime-constants"></a><span data-ttu-id="a134b-103">Constantes de \_ STime de configuración regional \*</span><span class="sxs-lookup"><span data-stu-id="a134b-103">LOCALE\_STIME\* Constants</span></span>

<span data-ttu-id="a134b-104">En este tema se definen las \_ constantes STime de configuración regional \* utilizadas por NLS.</span><span class="sxs-lookup"><span data-stu-id="a134b-104">This topic defines the LOCALE\_STIME\* constants used by NLS.</span></span>



| <span data-ttu-id="a134b-105">Value</span><span class="sxs-lookup"><span data-stu-id="a134b-105">Value</span></span>               | <span data-ttu-id="a134b-106">Significado</span><span class="sxs-lookup"><span data-stu-id="a134b-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a134b-107">STime de configuración regional \_</span><span class="sxs-lookup"><span data-stu-id="a134b-107">LOCALE\_STIME</span></span>       | <span data-ttu-id="a134b-108">Carácter (s) para el separador de hora.</span><span class="sxs-lookup"><span data-stu-id="a134b-108">Character(s) for the time separator.</span></span> <span data-ttu-id="a134b-109">El número máximo de caracteres permitido para esta cadena es cuatro, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="a134b-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <br/> <span data-ttu-id="a134b-110">**Windows Vista y versiones posteriores:** Esta constante está en desuso.</span><span class="sxs-lookup"><span data-stu-id="a134b-110">**Windows Vista and later:** This constant is deprecated.</span></span> <span data-ttu-id="a134b-111">Use la configuración regional \_ STIMEFORMAT en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a134b-111">Use LOCALE\_STIMEFORMAT instead.</span></span> <span data-ttu-id="a134b-112">Una configuración regional personalizada no puede tener un único carácter separador uniforme.</span><span class="sxs-lookup"><span data-stu-id="a134b-112">A custom locale might not have a single, uniform separator character.</span></span> <span data-ttu-id="a134b-113">Por ejemplo, un formato como "03:56" 23 "es válido.</span><span class="sxs-lookup"><span data-stu-id="a134b-113">For example, a format such as "03:56'23" is valid.</span></span><br/> |
| <span data-ttu-id="a134b-114">configuración regional \_ STIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="a134b-114">LOCALE\_STIMEFORMAT</span></span> | <span data-ttu-id="a134b-115">Cadenas de formato de hora para la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="a134b-115">Time formatting strings for the locale.</span></span> <span data-ttu-id="a134b-116">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="a134b-116">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="a134b-117">La cadena puede constar de una combinación de [imágenes con formato de hora, minuto y segundo](hour--minute--and-second-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="a134b-117">The string can consist of a combination of [hour, minute, and second format pictures](hour--minute--and-second-format-pictures.md).</span></span>                                                                                                      |



 

 

 




