---
description: El léxico, o la lista de palabras posibles utilizadas por un modelo de lenguaje del reconocedor determinado, se encuentra en uno o varios diccionarios.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Diccionarios y listas de frases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697564"
---
# <a name="dictionaries-and-phrase-lists"></a><span data-ttu-id="420d4-103">Diccionarios y listas de frases</span><span class="sxs-lookup"><span data-stu-id="420d4-103">Dictionaries and Phrase lists</span></span>

<span data-ttu-id="420d4-104">El léxico, o la lista de palabras posibles utilizadas por un modelo de lenguaje del reconocedor determinado, se encuentra en uno o varios diccionarios.</span><span class="sxs-lookup"><span data-stu-id="420d4-104">The lexicon, or list of possible words used by a particular recognizer's language model, is contained in one or more dictionaries.</span></span> <span data-ttu-id="420d4-105">El reconocedor busca en todos los diccionarios disponibles en el sistema al compilar las coincidencias de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="420d4-105">The recognizer searches all dictionaries available on the system when compiling recognition matches.</span></span> <span data-ttu-id="420d4-106">Puede usar las API de Microsoft Speech (SAPI) para modificar algunos de estos diccionarios.</span><span class="sxs-lookup"><span data-stu-id="420d4-106">You can use the Microsoft Speech APIs (SAPI) to modify some of these dictionaries.</span></span>

<span data-ttu-id="420d4-107">Una lista de frases proporciona otro medio para modificar el vocabulario del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="420d4-107">A phrase list provides another means of modifying the recognizer's vocabulary.</span></span> <span data-ttu-id="420d4-108">Al agregar palabras a una lista de frases se amplía el vocabulario; al agregar palabras y restringir el reconocedor para que use solo la lista de frases (en lugar de la lista de frases y los diccionarios) se restringe el vocabulario.</span><span class="sxs-lookup"><span data-stu-id="420d4-108">Adding words to a phrase list extends the vocabulary; adding words and then constraining the recognizer to use only the phrase list (as opposed to the phrase list and the dictionaries) restricts the vocabulary.</span></span>

<span data-ttu-id="420d4-109">Las versiones anteriores de las API de tecnología de Tablet PC se basaban en el concepto de listas de palabras.</span><span class="sxs-lookup"><span data-stu-id="420d4-109">Previous releases of the Tablet PC Technology APIs relied on the concept of word lists.</span></span> <span data-ttu-id="420d4-110">Las listas de palabras son casi idénticas a las listas de frases y se usan para el mismo propósito cuando se trabaja directamente con un objeto [**RecognizerContext**](inkrecognizercontext-class.md) en una aplicación que tiene habilitada la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="420d4-110">Word lists are almost identical to phrase lists and are used for the same purpose when working directly with a [**RecognizerContext**](inkrecognizercontext-class.md) object in an application that is ink enabled.</span></span> <span data-ttu-id="420d4-111">Para obtener más información sobre dónde y Cuándo usar las listas de palabras, vea [establecer el contexto para los controles de Ink-Enabled](setting-context-for-ink-enabled-controls.md).</span><span class="sxs-lookup"><span data-stu-id="420d4-111">For more details about where and when to use word lists, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="420d4-112">Cuando el tamaño de la lista con la que desea extender el léxico supera las 100.000 palabras, se recomienda usar un diccionario en lugar de una lista de palabras o una lista de frases.</span><span class="sxs-lookup"><span data-stu-id="420d4-112">When the size of the list with which you want to extend the lexicon exceeds 100,000 words, we recommend that you use a dictionary instead of a word list or phrase list.</span></span>

 

 



