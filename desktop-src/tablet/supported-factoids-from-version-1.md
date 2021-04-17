---
description: La plataforma de Tablet PC admite una serie de Factoids que se usan para aumentar la precisión del reconocimiento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids admitido de la versión 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678493"
---
# <a name="supported-factoids-from-version-1"></a><span data-ttu-id="ec1b9-103">Factoids admitido de la versión 1</span><span class="sxs-lookup"><span data-stu-id="ec1b9-103">Supported Factoids from Version 1</span></span>

<span data-ttu-id="ec1b9-104">\[Tenga en cuenta que la siguiente descripción de Factoids admitida en la versión 1 del kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition todavía es compatible con los reconocedores, pero se recomienda que todos los nuevos desarrollos (para los reconocedores de scripts latinos) usen los valores definidos en la enumeración [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]</span><span class="sxs-lookup"><span data-stu-id="ec1b9-104">\[Note the following description of the factoids supported in version 1 of the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) are still supported by recognizers, but it is recommended that all new development (for recognizers of Latin script) use the values defined in the [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration.\]</span></span>

<span data-ttu-id="ec1b9-105">La plataforma de Tablet PC admite una serie de Factoids que se usan para aumentar la precisión del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-105">The Tablet PC Platform supports a number of factoids that are used to increase recognition accuracy.</span></span> <span data-ttu-id="ec1b9-106">Cuando se usa Factoids, es importante que la entrada esperada coincida exactamente con la definición de Factoid.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-106">When using factoids, it is important that the expected input exactly match the definition of the factoid.</span></span> <span data-ttu-id="ec1b9-107">Si la entrada no coincide con la definición de Factoid, la precisión del reconocimiento se ve afectada.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-107">If the input does not match the definition of the factoid, recognition accuracy suffers.</span></span> <span data-ttu-id="ec1b9-108">Por ejemplo, si se establece el **número** Factoid y el usuario escribe letras, la precisión del reconocimiento de las letras es deficiente.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-108">For example, if the **Number** factoid is set and the user enters letters, the recognition accuracy for letters is poor.</span></span>

<span data-ttu-id="ec1b9-109">Ciertos Factoids, como el **correo electrónico** y el **dígito**, son casi idénticos en todos los idiomas.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-109">Certain factoids, such as **Email** and **Digit**, are almost identical across languages.</span></span> <span data-ttu-id="ec1b9-110">Otros Factoids, como **teléfono** y **CódigoPostal**, varían según el idioma.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-110">Other factoids, such as **Telephone** and **PostalCode**, vary by language.</span></span> <span data-ttu-id="ec1b9-111">Examine el formato de cada Factoid para el idioma que está usando.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-111">Examine the format of each factoid for the language that you are using.</span></span> <span data-ttu-id="ec1b9-112">Puede encontrar una lista de formatos para cada Factoid en cada idioma en las tablas de los temas que se indican a continuación de este tema.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-112">A list of formats for each factoid in each language can be found in the tables in the topics following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="ec1b9-113">Existe una diferencia sutil pero importante entre Factoids para los idiomas occidentales y Factoids para los idiomas de Asia oriental.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-113">There is a subtle but important distinction between factoids for western languages and factoids for East Asian languages.</span></span> <span data-ttu-id="ec1b9-114">Factoids para idiomas occidentales se implementa mediante expresiones que describen el resultado deseado.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-114">Factoids for western languages are implemented by using expressions that describe the desired result.</span></span> <span data-ttu-id="ec1b9-115">Después, el reconocedor se sesga para generar resultados que coincidan con esta expresión.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-115">The recognizer is then biased to produce results that match this expression.</span></span> <span data-ttu-id="ec1b9-116">Factoids para idiomas de Asia oriental se implementan mediante la especificación de un intervalo aceptable de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-116">Factoids for East Asian languages are implemented by specifying an acceptable range of Unicode characters.</span></span> <span data-ttu-id="ec1b9-117">Por ejemplo, la **fecha** Factoid para los idiomas de Asia oriental solo acepta caracteres Unicode dentro de un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-117">For example, the **Date** factoid for East Asian languages accepts only Unicode characters within a certain range.</span></span>

 

<span data-ttu-id="ec1b9-118">Factoids para idiomas occidentales incluyen Factoids para inglés (Reino Unido), Inglés (Estados Unidos), Francés, alemán y español.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-118">Factoids for western languages include factoids for English (United Kingdom), English (United States), French, German, and Spanish.</span></span> <span data-ttu-id="ec1b9-119">Factoids para idiomas de Asia oriental son Factoids para chino (simplificado), Chino (tradicional), Japonés y coreano.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-119">Factoids for East Asian languages include factoids for Chinese (Simplified), Chinese (Traditional), Japanese, and Korean.</span></span>

<span data-ttu-id="ec1b9-120">En las secciones siguientes se muestran los formatos admitidos para cada Factoid en cada idioma:</span><span class="sxs-lookup"><span data-stu-id="ec1b9-120">The following sections show the formats supported for each factoid in each language:</span></span>

-   [<span data-ttu-id="ec1b9-121">Factoids común entre idiomas</span><span class="sxs-lookup"><span data-stu-id="ec1b9-121">Factoids Common Across Languages</span></span>](factoids-common-across-languages.md)
-   [<span data-ttu-id="ec1b9-122">Factoids para idiomas occidentales</span><span class="sxs-lookup"><span data-stu-id="ec1b9-122">Factoids for Western Languages</span></span>](factoids-for-western-languages.md)
-   [<span data-ttu-id="ec1b9-123">Factoids para idiomas de Asia oriental</span><span class="sxs-lookup"><span data-stu-id="ec1b9-123">Factoids for East Asian Languages</span></span>](factoids-for-east-asian-languages.md)

<span data-ttu-id="ec1b9-124">Si espera que la entrada sea diferente de los formatos enumerados en las tablas de estas secciones, no use un Factoid.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-124">If you expect input that is different from the formats listed in the tables in these sections, do not use a factoid.</span></span> <span data-ttu-id="ec1b9-125">Además, los Factoids están integrados en el reconocedor para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-125">In addition, factoids are built into the recognizer for each language.</span></span> <span data-ttu-id="ec1b9-126">No se puede usar Factoids desde un idioma con un reconocedor de otro idioma.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-126">You cannot use factoids from one language with a recognizer from another language.</span></span> <span data-ttu-id="ec1b9-127">Por ejemplo, no puede usar el **teléfono** francés Factoid con un reconocedor japonés.</span><span class="sxs-lookup"><span data-stu-id="ec1b9-127">For example, you cannot use the French **Telephone** factoid with a Japanese recognizer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec1b9-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec1b9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec1b9-129">**Constantes de Factoid**</span><span class="sxs-lookup"><span data-stu-id="ec1b9-129">**Factoid Constants**</span></span>](factoid-constants.md)
</dt> <dt>

<span data-ttu-id="ec1b9-130">[Clase Microsoft. Ink. Factoid](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ec1b9-130">[Microsoft.Ink.Factoid Class](/previous-versions/ms583657(v=vs.100))</span></span>
</dt> </dl>

 

 
