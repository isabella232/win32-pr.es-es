---
description: Una alternativa es una coincidencia de palabras posible para un segmento de reconocimiento. Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada manuscrita o de audio en un diccionario o Factoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666201"
---
# <a name="alternates"></a><span data-ttu-id="49b7f-104">Alternativas</span><span class="sxs-lookup"><span data-stu-id="49b7f-104">Alternates</span></span>

<span data-ttu-id="49b7f-105">Una alternativa es una coincidencia de palabras posible para un segmento de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="49b7f-105">An alternate is a potential word match for a recognition segment.</span></span> <span data-ttu-id="49b7f-106">Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada manuscrita o de audio en un diccionario o Factoid.</span><span class="sxs-lookup"><span data-stu-id="49b7f-106">A recognizer generates alternates and bases them on acceptable matches of the ink or audio input against a dictionary or factoid.</span></span>

> [!Note]  
> <span data-ttu-id="49b7f-107">Actualmente, la evaluación de confianza solo está disponible para los reconocedores de Microsoft English (Estados Unidos) y gestos.</span><span class="sxs-lookup"><span data-stu-id="49b7f-107">Confidence evaluation is currently available only for the Microsoft English (United States) and gesture recognizers.</span></span>

 

<span data-ttu-id="49b7f-108">A veces, la tinta puede tener distinciones ambiguas entre segmentos.</span><span class="sxs-lookup"><span data-stu-id="49b7f-108">Sometimes the ink may have ambiguous distinctions between segments.</span></span> <span data-ttu-id="49b7f-109">El reconocedor compara estos segmentos con un diccionario de reconocedor para determinar las posibles coincidencias.</span><span class="sxs-lookup"><span data-stu-id="49b7f-109">The recognizer compares these segments to a recognizer dictionary to determine possible matches.</span></span> <span data-ttu-id="49b7f-110">Cuando el reconocedor compara los segmentos, mantiene una lista de posibles coincidencias alternativas y asigna un nivel de confianza a cada una de ellas, seleccionando una opción superior.</span><span class="sxs-lookup"><span data-stu-id="49b7f-110">When the recognizer compares the segments, it maintains a list of possible alternate matches and assigns a confidence level to each one, picking a top choice.</span></span>

> [!Note]  
> <span data-ttu-id="49b7f-111">El Reconocedor no puede proporcionar alternativas para una parte de la tinta menor que un segmento de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="49b7f-111">The recognizer cannot provide alternates for a portion of ink that is smaller than a recognition segment.</span></span>

 

 

 



