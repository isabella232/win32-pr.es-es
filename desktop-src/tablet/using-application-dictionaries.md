---
description: De forma predeterminada, el reconocedor utiliza un diccionario del sistema que contiene todas las palabras escritas normalmente en un idioma.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Uso de diccionarios de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497344"
---
# <a name="using-application-dictionaries"></a><span data-ttu-id="58e29-103">Uso de diccionarios de aplicación</span><span class="sxs-lookup"><span data-stu-id="58e29-103">Using Application Dictionaries</span></span>

<span data-ttu-id="58e29-104">De forma predeterminada, el reconocedor utiliza un diccionario del sistema que contiene todas las palabras escritas normalmente en un idioma.</span><span class="sxs-lookup"><span data-stu-id="58e29-104">By default, the recognizer uses a system dictionary that contains all of the commonly written words in a language.</span></span> <span data-ttu-id="58e29-105">Además, el reconocedor tiene un diccionario de usuario que contiene palabras que el usuario ha agregado al diccionario.</span><span class="sxs-lookup"><span data-stu-id="58e29-105">In addition, the recognizer has a user dictionary that contains words that the user has added to the dictionary.</span></span> <span data-ttu-id="58e29-106">Los usuarios agregan una palabra al Diccionario de usuarios a través del panel de entrada de Tablet PC a través de selecciones en:</span><span class="sxs-lookup"><span data-stu-id="58e29-106">Users add a word to the user dictionary through Tablet PC Input Panel through selections in:</span></span>

-   <span data-ttu-id="58e29-107">La lista alternativa (al escribir).</span><span class="sxs-lookup"><span data-stu-id="58e29-107">The alternate list (when writing).</span></span>
-   <span data-ttu-id="58e29-108">Menú de herramientas de voz (al hablar).</span><span class="sxs-lookup"><span data-stu-id="58e29-108">The Speech Tools menu (when speaking).</span></span>

<span data-ttu-id="58e29-109">Si diseña una aplicación en la que espera que el usuario escriba palabras que no se encuentran en el Diccionario del sistema o en el Diccionario del usuario, cree un diccionario de aplicación.</span><span class="sxs-lookup"><span data-stu-id="58e29-109">If you are designing an application into which you anticipate the user will write words that are not found in either the system dictionary or the user dictionary, create an application dictionary.</span></span> <span data-ttu-id="58e29-110">Un diccionario de aplicación mejora aún más la precisión del reconocimiento al proporcionar al reconocedor una lista personalizada adicional de palabras que se pueden escribir como escritura a mano en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="58e29-110">An application dictionary further improves recognition accuracy by providing the recognizer with an additional customized list of words likely to be entered as handwriting into an application.</span></span>

<span data-ttu-id="58e29-111">Puede crear un diccionario de aplicación mediante el objeto de la información de [**palabras**](inkwordlist-class.md) .</span><span class="sxs-lookup"><span data-stu-id="58e29-111">You create an application dictionary by using the [**WordList**](inkwordlist-class.md) object.</span></span> <span data-ttu-id="58e29-112">El Diccionario de aplicación subsiguiente aumenta la precisión del reconocimiento al proporcionar al reconocedor una lista de palabras previstas.</span><span class="sxs-lookup"><span data-stu-id="58e29-112">The ensuing application dictionary increases recognition accuracy by providing the recognizer with a list of expected words.</span></span> <span data-ttu-id="58e29-113">Por ejemplo, un diccionario de aplicación que contiene la terminología médica aumenta la precisión del reconocimiento en una aplicación desarrollada para el sector médico en el que es probable que se escriban los términos.</span><span class="sxs-lookup"><span data-stu-id="58e29-113">For example, an application dictionary that contains medical terminology increases recognition accuracy within an application developed for the medical industry into which the terms are likely to be written.</span></span>

<span data-ttu-id="58e29-114">Otro ejemplo: al diseñar un formulario para que alguien pida instrumentos musicales, cree un objeto de una nueva de [**palabras**](inkwordlist-class.md) que contenga los nombres de los fabricantes de instrumentos más comunes.</span><span class="sxs-lookup"><span data-stu-id="58e29-114">As another example, when designing a form for someone to order musical instruments, create a [**WordList**](inkwordlist-class.md) object that contains the names of the most common instrument manufacturers.</span></span> <span data-ttu-id="58e29-115">Establezca la propiedad de la definición de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) en el objeto de la de **palabras** que creó.</span><span class="sxs-lookup"><span data-stu-id="58e29-115">Set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object to the **WordList** object you created.</span></span> <span data-ttu-id="58e29-116">A continuación, el objeto **RecognizerContext** pasa esta lista de palabras al reconocedor.</span><span class="sxs-lookup"><span data-stu-id="58e29-116">This list of words is then passed to the recognizer by the **RecognizerContext** object.</span></span> <span data-ttu-id="58e29-117">El Diccionario de aplicación aumenta la precisión del reconocimiento cuando estos nombres se escriben en un campo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="58e29-117">The application dictionary increases recognition accuracy when those names are written in a field in the application.</span></span>

<span data-ttu-id="58e29-118">En los temas siguientes se describe cómo usar los diccionarios de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="58e29-118">The following topics describe how to use application dictionaries.</span></span>

-   [<span data-ttu-id="58e29-119">Descripción de las listas de palabras, el contexto del reconocedor y Factoids</span><span class="sxs-lookup"><span data-stu-id="58e29-119">Understanding Word Lists, Recognizer Context, and Factoids</span></span>](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [<span data-ttu-id="58e29-120">Uso de diccionarios de aplicación con las API de la plataforma de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="58e29-120">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [<span data-ttu-id="58e29-121">Crear diccionarios personalizados para el reconocimiento de escritura a mano</span><span class="sxs-lookup"><span data-stu-id="58e29-121">Creating Custom Dictionaries for Handwriting Recognition</span></span>](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



