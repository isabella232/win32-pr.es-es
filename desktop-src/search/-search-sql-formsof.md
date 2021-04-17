---
description: El término FORMSOF realiza coincidencias con otras formas lingüísticas de la palabra.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Términos de FORMs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705485"
---
# <a name="formsof-term"></a><span data-ttu-id="9da7e-103">Términos de FORMs</span><span class="sxs-lookup"><span data-stu-id="9da7e-103">FORMSOF Term</span></span>

<span data-ttu-id="9da7e-104">El término FORMSOF realiza coincidencias con otras formas lingüísticas de la palabra.</span><span class="sxs-lookup"><span data-stu-id="9da7e-104">The FORMSOF term performs matches using other linguistic forms of the word.</span></span> <span data-ttu-id="9da7e-105">A continuación se indican las sintaxis de los términos de FORMSOF:</span><span class="sxs-lookup"><span data-stu-id="9da7e-105">The following is the FORMSOF term syntax:</span></span>


```
FORMSOF (<generation_type>,<match_words>)
```



<span data-ttu-id="9da7e-106">El tipo de generación especifica cómo Microsoft Windows Search elige los formularios de Word alternativos.</span><span class="sxs-lookup"><span data-stu-id="9da7e-106">The generation type specifies how Microsoft Windows Search chooses the alternative word forms.</span></span> <span data-ttu-id="9da7e-107">El valor con **inflexión** elige formas de inflexión alternativas para las palabras de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="9da7e-107">The **INFLECTIONAL** value chooses alternative inflection forms for the match words.</span></span> <span data-ttu-id="9da7e-108">Si la palabra es un verbo, se usan decenas alternativos.</span><span class="sxs-lookup"><span data-stu-id="9da7e-108">If the word is a verb, alternative tenses are used.</span></span> <span data-ttu-id="9da7e-109">Si la palabra es un nombre, los formularios singular, plural y Possessive se usan para detectar coincidencias.</span><span class="sxs-lookup"><span data-stu-id="9da7e-109">If the word is a noun, the singular, plural, and possessive forms are used to detect matches.</span></span>

<span data-ttu-id="9da7e-110">El \_ valor buscar palabras es una o varias palabras, separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="9da7e-110">The match\_words value is one or more words, separated by commas.</span></span>

## <a name="examples"></a><span data-ttu-id="9da7e-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9da7e-111">Examples</span></span>

<span data-ttu-id="9da7e-112">En el ejemplo siguiente se buscan coincidencias con inflexión de la palabra "Run".</span><span class="sxs-lookup"><span data-stu-id="9da7e-112">The following example searches for inflectional matches for the word "run".</span></span> <span data-ttu-id="9da7e-113">Este ejemplo encuentra documentos que contienen "Run", "Running" o "Running".</span><span class="sxs-lookup"><span data-stu-id="9da7e-113">This example matches documents containing "run", "running", or "ran".</span></span>


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a><span data-ttu-id="9da7e-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9da7e-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9da7e-115">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9da7e-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9da7e-116">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="9da7e-116">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="9da7e-117">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="9da7e-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



