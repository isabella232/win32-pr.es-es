---
description: En el caso de una aplicación que acepta escritura a mano mixta y entrada de dibujo, la capacidad de distinguir entre escritura a mano y dibujo y agrupar escritura a mano en subcategorías, como segmentos de reconocimiento, líneas y párrafos, es muy útil.
ms.assetid: 17ce349c-10f3-4d9b-abb0-7af4f40bab32
title: Análisis de la entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021882d8f2de83b4bac9580ae66dd097bfd556db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082006"
---
# <a name="ink-analysis"></a><span data-ttu-id="8ef3b-103">Análisis de la entrada de lápiz</span><span class="sxs-lookup"><span data-stu-id="8ef3b-103">Ink Analysis</span></span>

<span data-ttu-id="8ef3b-104">En el caso de una aplicación que acepta escritura a mano mixta y entrada de dibujo, la capacidad de distinguir entre escritura a mano y dibujo y agrupar escritura a mano en subcategorías, como segmentos de reconocimiento, líneas y párrafos, es muy útil.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-104">For an application that accepts mixed handwriting and drawing input, the ability to distinguish between handwriting and drawing and to group handwriting into subcategories, such as recognition segments, lines, and paragraphs, is very useful.</span></span>

## <a name="ink-analysis-library"></a><span data-ttu-id="8ef3b-105">Biblioteca de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="8ef3b-105">Ink Analysis Library</span></span>

<span data-ttu-id="8ef3b-106">Las API de análisis de tinta combinan eficazmente dos tecnologías distintas pero gratuitas: el reconocimiento de escritura a mano y el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-106">The ink analysis APIs effectively combine two distinct but complimentary technologies: handwriting recognition and ink analyzing.</span></span> <span data-ttu-id="8ef3b-107">La combinación de estas dos tecnologías proporciona resultados más definitivos que las partes tomadas por sí sola.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-107">Combining these two technologies gives definitively greater results than the parts taken alone.</span></span>

<span data-ttu-id="8ef3b-108">El reconocimiento de escritura a mano es el análisis computacional de la tinta digital manuscrita para devolver la interpretación basada en caracteres en un idioma determinado.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-108">Handwriting recognition is the computational analysis of handwritten digital ink to return character-based interpretation in a given language.</span></span> <span data-ttu-id="8ef3b-109">Es decir, el reconocimiento de escritura a mano es el modo en que el equipo "Lee" la escritura a mano de una persona.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-109">That is, handwriting recognition is how the computer "reads" a person's handwriting.</span></span>

<span data-ttu-id="8ef3b-110">El análisis de tintas se puede desglosar aún más en el análisis de diseño y clasificación de tinta.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-110">Ink analyzing can be further broken down into ink classification and layout analysis.</span></span> <span data-ttu-id="8ef3b-111">La clasificación de tinta es la división computacional de la entrada manuscrita en unidades semánticamente significativas como párrafos, líneas, palabras y dibujos.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-111">Ink classification is the computational division of ink into semantically meaningful units such as paragraphs, lines, words, and drawings.</span></span> <span data-ttu-id="8ef3b-112">El análisis de diseño es el examen computacional de la entrada manuscrita para determinar la posición de la tinta en la superficie de entrada manuscrita y cómo se relacionan los trazos entre sí espacialmente e incluso semánticamente.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-112">Layout analysis is the computational examination of ink input to determine the position of the ink on the inking surface and how the strokes relate to each other spatially and even semantically.</span></span>

<span data-ttu-id="8ef3b-113">Para más información sobre cómo usar las API de administrado de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8ef3b-113">For details on how to use the Ink Analyis APIs, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

 

 



