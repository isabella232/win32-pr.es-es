---
description: Tablet PC incluye tecnología para reconocer la entrada manuscrita que suele tener la forma de escritura a mano.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Acerca del reconocimiento de escritura a mano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717220"
---
# <a name="about-handwriting-recognition"></a><span data-ttu-id="3dc69-103">Acerca del reconocimiento de escritura a mano</span><span class="sxs-lookup"><span data-stu-id="3dc69-103">About Handwriting Recognition</span></span>

<span data-ttu-id="3dc69-104">Tablet PC incluye tecnología para reconocer la entrada manuscrita que suele tener la forma de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="3dc69-104">Tablet PC includes technology for recognizing ink input that is most commonly in the form of handwriting.</span></span> <span data-ttu-id="3dc69-105">El módulo de software que proporciona el reconocimiento se denomina reconocedor.</span><span class="sxs-lookup"><span data-stu-id="3dc69-105">The software module that provides the recognition is called a recognizer.</span></span> <span data-ttu-id="3dc69-106">Un reconocedor reconoce un idioma, un grupo de idiomas relacionados o una clase de objetos relacionados, como notas musicales, gestos del sistema o formas geométricas.</span><span class="sxs-lookup"><span data-stu-id="3dc69-106">A recognizer recognizes one language, a group of related languages, or a class of related objects such as musical notes, system gestures, or geometric shapes.</span></span> <span data-ttu-id="3dc69-107">Puede Agregar reconocedores al sistema de servicios de tinta de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="3dc69-107">You can dynamically add recognizers to the ink services system.</span></span>

## <a name="recognition-steps"></a><span data-ttu-id="3dc69-108">Pasos de reconocimiento</span><span class="sxs-lookup"><span data-stu-id="3dc69-108">Recognition Steps</span></span>

<span data-ttu-id="3dc69-109">El reconocimiento se controla mediante el uso de un contexto de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="3dc69-109">Recognition is handled through the use of a recognizer context.</span></span> <span data-ttu-id="3dc69-110">El reconocimiento consta de cuatro pasos básicos:</span><span class="sxs-lookup"><span data-stu-id="3dc69-110">Recognition consists of four basic steps:</span></span>

1.  <span data-ttu-id="3dc69-111">Configurar las restricciones de reconocimiento mediante:</span><span class="sxs-lookup"><span data-stu-id="3dc69-111">Setting up the recognition constraints by:</span></span>
    -   <span data-ttu-id="3dc69-112">Seleccionar el reconocedor y el modo de entrada (restricciones geométricas).</span><span class="sxs-lookup"><span data-stu-id="3dc69-112">Selecting the recognizer and input mode (geometric constraints).</span></span>
    -   <span data-ttu-id="3dc69-113">Establecer las restricciones de idioma.</span><span class="sxs-lookup"><span data-stu-id="3dc69-113">Setting the language constraints.</span></span> <span data-ttu-id="3dc69-114">Por ejemplo, puede restringir la entrada a caracteres alfanuméricos o puede pasar esquemas para ayudar al reconocedor.</span><span class="sxs-lookup"><span data-stu-id="3dc69-114">For example, you can restrict input to alphanumeric characters or you can pass schemas to assist the recognizer.</span></span>
2.  <span data-ttu-id="3dc69-115">Enviar entradas manuscritas al reconocedor.</span><span class="sxs-lookup"><span data-stu-id="3dc69-115">Sending ink to the recognizer.</span></span>
3.  <span data-ttu-id="3dc69-116">Procesar la entrada (reconociendo).</span><span class="sxs-lookup"><span data-stu-id="3dc69-116">Processing the input (recognizing).</span></span>
4.  <span data-ttu-id="3dc69-117">Devolver los resultados del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="3dc69-117">Returning the results of the recognition.</span></span>

<span data-ttu-id="3dc69-118">Los pasos 2 y 3 pueden repetirse en un bucle, o bien se pueden agregar todos los trazos de lápiz a la tinta antes de que se intente el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="3dc69-118">Steps 2 and 3 may be repeated in a loop, or all of the ink strokes may be added to the ink before recognition is attempted.</span></span>

## <a name="samples-and-related-topics"></a><span data-ttu-id="3dc69-119">Ejemplos y temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3dc69-119">Samples and Related Topics</span></span>

<span data-ttu-id="3dc69-120">El [ejemplo de reconocimiento avanzado](advanced-recognition-sample.md) muestra cómo utilizar los reconocedores con objetos de [**tinta**](inkdisp-class.md) para realizar el reconocimiento de tinta.</span><span class="sxs-lookup"><span data-stu-id="3dc69-120">[Advanced Recognition Sample](advanced-recognition-sample.md) demonstrates how to use recognizers with [**Ink**](inkdisp-class.md) objects to perform ink recognition.</span></span>

<span data-ttu-id="3dc69-121">La [plantilla de ejemplo de dll de reconocedor](recognizer-dll-sample-template.md) contiene una plantilla para crear un archivo dll de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="3dc69-121">[Recognizer DLL Sample Template](recognizer-dll-sample-template.md) contains a template for creating a recognizer DLL.</span></span> <span data-ttu-id="3dc69-122">La plantilla contiene funciones para registrar y anular el registro del servidor, así como esqueletos para las funciones principales del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="3dc69-122">The template contains functions for registering and unregistering the server, as well as skeletons for primary recognizer functions.</span></span>

<span data-ttu-id="3dc69-123">En las secciones siguientes se describen los conceptos básicos de la tecnología de reconocimiento de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3dc69-123">The following sections describe the basic concepts behind the Tablet PC recognition technology.</span></span> <span data-ttu-id="3dc69-124">Para obtener información detallada acerca de cómo crear reconocedores personalizados, consulte [crear un reconocedor](creating-a-recognizer.md).</span><span class="sxs-lookup"><span data-stu-id="3dc69-124">For detailed information about creating custom recognizers, see [Creating a Recognizer](creating-a-recognizer.md).</span></span>

-   [<span data-ttu-id="3dc69-125">Reconocedores de texto</span><span class="sxs-lookup"><span data-stu-id="3dc69-125">Text Recognizers</span></span>](text-recognizers.md)
-   [<span data-ttu-id="3dc69-126">Reconocedores de objetos</span><span class="sxs-lookup"><span data-stu-id="3dc69-126">Object Recognizers</span></span>](object-recognizers.md)
-   [<span data-ttu-id="3dc69-127">Usar la colección Recognizers</span><span class="sxs-lookup"><span data-stu-id="3dc69-127">Using the Recognizers Collection</span></span>](using-the-recognizers-collection.md)
-   [<span data-ttu-id="3dc69-128">Contexto del reconocedor</span><span class="sxs-lookup"><span data-stu-id="3dc69-128">Recognizer Context</span></span>](recognizer-context.md)
-   [<span data-ttu-id="3dc69-129">Segmentos de reconocimiento</span><span class="sxs-lookup"><span data-stu-id="3dc69-129">Recognition Segments</span></span>](recognition-segments.md)
-   [<span data-ttu-id="3dc69-130">Reconocimiento de texto angulado</span><span class="sxs-lookup"><span data-stu-id="3dc69-130">Recognition of Angled Text</span></span>](recognition-of-angled-text.md)
-   [<span data-ttu-id="3dc69-131">Compatibilidad de reordenación de trazos de reconocedor</span><span class="sxs-lookup"><span data-stu-id="3dc69-131">Recognizer Stroke Reordering Support</span></span>](recognizer-stroke-reordering-support.md)
-   [<span data-ttu-id="3dc69-132">Diccionarios y Factoids</span><span class="sxs-lookup"><span data-stu-id="3dc69-132">Dictionaries and Factoids</span></span>](dictionaries-and-factoids.md)
-   <span data-ttu-id="3dc69-133">[Propiedad Confidence \[ sobre el reconocimiento\]](confidence-property--about-recognition.md)</span><span class="sxs-lookup"><span data-stu-id="3dc69-133">[Confidence Property \[About Recognition\]](confidence-property--about-recognition.md)</span></span>
-   [<span data-ttu-id="3dc69-134">Alternativas</span><span class="sxs-lookup"><span data-stu-id="3dc69-134">Alternates</span></span>](alternates.md)
-   [<span data-ttu-id="3dc69-135">Segmentos de tinta y alternativas</span><span class="sxs-lookup"><span data-stu-id="3dc69-135">Ink Segments and Alternates</span></span>](ink-segments-and-alternates.md)

 

 



