---
description: El servicio de detección de lenguaje ELS se llama Microsoft Detección de idioma. Este servicio usa tecnología Microsoft-patentada para permitir que las aplicaciones detecten el idioma en el que se escribe el texto específico.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft Detección de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687089"
---
# <a name="microsoft-language-detection"></a><span data-ttu-id="6d4e3-104">Microsoft Detección de idioma</span><span class="sxs-lookup"><span data-stu-id="6d4e3-104">Microsoft Language Detection</span></span>

<span data-ttu-id="6d4e3-105">El servicio de detección de lenguaje ELS se llama Microsoft Detección de idioma.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-105">The ELS language detection service is called Microsoft Language Detection.</span></span> <span data-ttu-id="6d4e3-106">Este servicio usa tecnología Microsoft-patentada para permitir que las aplicaciones detecten el idioma en el que se escribe el texto específico.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-106">This service uses Microsoft-patented technology to allow applications to detect the language in which specific text is written.</span></span>

## <a name="input-to-microsoft-language-detection"></a><span data-ttu-id="6d4e3-107">Entrada a Microsoft Detección de idioma</span><span class="sxs-lookup"><span data-stu-id="6d4e3-107">Input to Microsoft Language Detection</span></span>

<span data-ttu-id="6d4e3-108">La entrada del servicio Microsoft Detección de idioma es UTF-16 (formato normalizado C).</span><span class="sxs-lookup"><span data-stu-id="6d4e3-108">The input to the Microsoft Language Detection service is UTF-16 (normalized form C) text.</span></span> <span data-ttu-id="6d4e3-109">El servicio tiene que determinar el idioma de este texto.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-109">The service has to determine the language for this text.</span></span>

## <a name="output-of-microsoft-language-detection"></a><span data-ttu-id="6d4e3-110">Salida de Microsoft Detección de idioma</span><span class="sxs-lookup"><span data-stu-id="6d4e3-110">Output of Microsoft Language Detection</span></span>

<span data-ttu-id="6d4e3-111">El servicio Microsoft Detección de idioma recupera los lenguajes de lista de cadenas UTF-16 con formato del registro y terminadas en null, representados por sus nombres, separados por delimitadores de caracteres null.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-111">The Microsoft Language Detection service retrieves a double-null-terminated, registry-formatted UTF-16 string listing languages, represented by their names, separated by null character delimiters.</span></span> <span data-ttu-id="6d4e3-112">La lista se ordena por relevancia.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-112">The list is sorted by relevance.</span></span> <span data-ttu-id="6d4e3-113">Para la mayoría de los idiomas, se usan nombres neutros.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-113">For most languages, neutral names are used.</span></span> <span data-ttu-id="6d4e3-114">Sin embargo, para algunos, por ejemplo, Sr-Cyrl, Sr-Latn, ZH-hant y ZH-Hans, se usan nombres completos.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-114">However, for some, for example, sr-Cyrl, sr-Latn, zh-Hant, and zh-Hans, full names are used.</span></span>

## <a name="microsoft-language-detection-operation"></a><span data-ttu-id="6d4e3-115">Operación de Microsoft Detección de idioma</span><span class="sxs-lookup"><span data-stu-id="6d4e3-115">Microsoft Language Detection Operation</span></span>

<span data-ttu-id="6d4e3-116">El servicio Microsoft Detección de idioma comprueba el script Unicode del texto proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-116">The Microsoft Language Detection service checks the Unicode script of the text provided by the application.</span></span> <span data-ttu-id="6d4e3-117">Segmenta el texto en función de los scripts que detecta y, a continuación, determina el idioma en el que se escribe cada segmento.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-117">It segments the text based on the scripts that it detects, and then determines the language in which each segment is written.</span></span> <span data-ttu-id="6d4e3-118">Si un script indica un solo idioma, se garantiza que el idioma está presente en la lista de resultados de los idiomas.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-118">If a script indicates a single language, the language is guaranteed to be present in the output list of languages.</span></span> <span data-ttu-id="6d4e3-119">El servicio utiliza un algoritmo patentado para determinar la relevancia de cada idioma admitido.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-119">The service uses a patented algorithm to determine the relevance of each supported language.</span></span>

## <a name="microsoft-language-detection-guid"></a><span data-ttu-id="6d4e3-120">GUID de Microsoft Detección de idioma</span><span class="sxs-lookup"><span data-stu-id="6d4e3-120">Microsoft Language Detection GUID</span></span>

<span data-ttu-id="6d4e3-121">El GUID del servicio Microsoft Detección de idioma se declara en Elssrvc. h, tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-121">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a><span data-ttu-id="6d4e3-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d4e3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d4e3-123">Acerca de los servicios lingüísticos extendidos</span><span class="sxs-lookup"><span data-stu-id="6d4e3-123">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



