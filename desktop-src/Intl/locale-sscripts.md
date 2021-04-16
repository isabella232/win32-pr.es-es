---
description: configuración regional \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666592"
---
# <a name="locale_sscripts"></a><span data-ttu-id="7e38c-103">configuración regional \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="7e38c-103">LOCALE\_SSCRIPTS</span></span>

<span data-ttu-id="7e38c-104">**Windows Vista y versiones posteriores:** Una cadena que representa una lista de scripts, con la notación de 4 caracteres utilizada en [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="7e38c-104">**Windows Vista and later:** A string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="7e38c-105">Cada nombre de script consta de cuatro caracteres latinos y la lista se organiza en orden alfabético con cada nombre, incluido el último, seguido de un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="7e38c-105">Each script name consists of four Latin characters and the list is arranged in alphabetical order with each name, including the last, followed by a semicolon.</span></span>

<span data-ttu-id="7e38c-106">Se puede llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCTYPE* establecido en la configuración regional \_ SSCRIPTS como parte de una estrategia para mitigar los problemas de seguridad relacionados con los nombres de dominio internacionalizados (IDN).</span><span class="sxs-lookup"><span data-stu-id="7e38c-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can be called with *LCType* set to LOCALE\_SSCRIPTS as part of a strategy to mitigate security issues related to Internationalized Domain Names (IDNs).</span></span> <span data-ttu-id="7e38c-107">Estos son algunos valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7e38c-107">Here are some example values:</span></span>



| <span data-ttu-id="7e38c-108">Configuración regional</span><span class="sxs-lookup"><span data-stu-id="7e38c-108">Locale</span></span>                  | <span data-ttu-id="7e38c-109">Nombre de idioma o configuración regional</span><span class="sxs-lookup"><span data-stu-id="7e38c-109">Locale/language name</span></span> | <span data-ttu-id="7e38c-110">Value</span><span class="sxs-lookup"><span data-stu-id="7e38c-110">Value</span></span>                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e38c-111">Spanish (Traditional Sort) - Spain</span><span class="sxs-lookup"><span data-stu-id="7e38c-111">English (United States)</span></span> | <span data-ttu-id="7e38c-112">es-ES</span><span class="sxs-lookup"><span data-stu-id="7e38c-112">en-US</span></span>                | <span data-ttu-id="7e38c-113">LATN</span><span class="sxs-lookup"><span data-stu-id="7e38c-113">Latn;</span></span>                                                                                                  |
| <span data-ttu-id="7e38c-114">Hindi (India)</span><span class="sxs-lookup"><span data-stu-id="7e38c-114">Hindi (India)</span></span>           | <span data-ttu-id="7e38c-115">hi-IN</span><span class="sxs-lookup"><span data-stu-id="7e38c-115">hi-IN</span></span>                | <span data-ttu-id="7e38c-116">Deva</span><span class="sxs-lookup"><span data-stu-id="7e38c-116">Deva;</span></span>                                                                                                  |
| <span data-ttu-id="7e38c-117">Japonés (Japón)</span><span class="sxs-lookup"><span data-stu-id="7e38c-117">Japanese (Japan)</span></span>        | <span data-ttu-id="7e38c-118">ja-JP</span><span class="sxs-lookup"><span data-stu-id="7e38c-118">ja-JP</span></span>                | <span data-ttu-id="7e38c-119">**Windows 7 y versiones posteriores:** Hani; Hira; Jpan; Kana</span><span class="sxs-lookup"><span data-stu-id="7e38c-119">**Windows 7 and later:** Hani;Hira;Jpan;Kana;</span></span><br/> <span data-ttu-id="7e38c-120">**Windows Vista:** Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="7e38c-120">**Windows Vista:** Hani;Hira;Kana;</span></span><br/> |



 

<span data-ttu-id="7e38c-121">Un valor de script compuesto no incluye el script Latino a menos que sea una parte esencial del sistema de escritura que se usa para la configuración regional concreta.</span><span class="sxs-lookup"><span data-stu-id="7e38c-121">A compound script value does not include the Latin script unless it is an essential part of the writing system used for the particular locale.</span></span> <span data-ttu-id="7e38c-122">Los caracteres latinos se suelen usar en el contexto de las configuraciones regionales para las que no son nativas, por ejemplo, para un nombre empresarial extranjero.</span><span class="sxs-lookup"><span data-stu-id="7e38c-122">Latin characters are often used in the context of locales for which they are not native, for example, for a foreign business name.</span></span> <span data-ttu-id="7e38c-123">En el ejemplo anterior de Hindi en India, el único valor de script es "Deva" (para "Devanagari"), aunque los caracteres latinos también pueden aparecer en texto Hindi.</span><span class="sxs-lookup"><span data-stu-id="7e38c-123">In the example above for Hindi in India, the only script value is "Deva" (for "Devanagari"), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="7e38c-124">La función [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) tiene una marca especial para abordar este caso.</span><span class="sxs-lookup"><span data-stu-id="7e38c-124">The [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) function has a special flag to address this case.</span></span>

 

 




