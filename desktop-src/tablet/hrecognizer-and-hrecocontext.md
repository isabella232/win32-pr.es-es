---
description: Se hace referencia a un reconocedor de tinta con un identificador de HRECOGNIZER y un contexto de reconocedor como identificador de HRECOCONTEXT. Una biblioteca de vínculos dinámicos (DLL) del reconocedor puede implementar reconocedores para más de un idioma.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER y HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715247"
---
# <a name="hrecognizer-and-hrecocontext"></a><span data-ttu-id="c30fe-103">HRECOGNIZER y HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="c30fe-103">HRECOGNIZER and HRECOCONTEXT</span></span>

<span data-ttu-id="c30fe-104">Se hace referencia a un reconocedor de tinta con un identificador de [HRECOGNIZER](hrecognizer-handle.md) y un contexto de reconocedor como identificador de [HRECOCONTEXT](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="c30fe-104">You reference an ink recognizer with an [HRECOGNIZER](hrecognizer-handle.md) handle and a recognizer context as an [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="c30fe-105">Una biblioteca de vínculos dinámicos (DLL) del reconocedor puede implementar reconocedores para más de un idioma.</span><span class="sxs-lookup"><span data-stu-id="c30fe-105">A recognizer dynamic-link library (DLL) can implement recognizers for more than one language.</span></span> <span data-ttu-id="c30fe-106">Si es así, cada idioma se selecciona mediante un CLSID que se pasa al crear el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c30fe-106">If so, each language is selected by a CLSID that is passed in when creating the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object in the application.</span></span> <span data-ttu-id="c30fe-107">Además, una DLL de reconocedor puede crear varios identificadores de reconocedor cuando se carga, uno o varios de los lenguajes reconocidos.</span><span class="sxs-lookup"><span data-stu-id="c30fe-107">In addition, a recognizer DLL can create multiple recognizer handles when it is loaded, one or more for each language recognized.</span></span>

<span data-ttu-id="c30fe-108">Se crea un contexto de reconocedor que representa el evento de reconocimiento de una parte específica de la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c30fe-108">A recognizer context is created to represent the event of recognizing a specific piece of ink.</span></span> <span data-ttu-id="c30fe-109">Cuando se crea el contexto, se pasa el identificador de objetos del reconocedor asociado a la función [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .</span><span class="sxs-lookup"><span data-stu-id="c30fe-109">When the context is created, the associated recognizer objects handle is passed to the [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) function.</span></span> <span data-ttu-id="c30fe-110">Esto asocia el idioma con el contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="c30fe-110">This associates the language with the recognizer context.</span></span>

<span data-ttu-id="c30fe-111">Un contexto de reconocedor puede representar el reconocimiento de toda la tinta en el cuerpo de un correo electrónico, la tinta de un solo campo dentro de una aplicación o una sola línea de texto escrita en el panel de entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="c30fe-111">A recognizer context may represent the recognition of all the ink in the body of an email, the ink of a single field within an application, or a single line of text written in the Tablet PC Input Panel.</span></span> <span data-ttu-id="c30fe-112">El volumen de tinta de un único contexto de reconocedor puede variar de un solo trazo a una página completa o más.</span><span class="sxs-lookup"><span data-stu-id="c30fe-112">The volume of ink in a single recognizer context may vary from a single stroke to a whole page or more.</span></span>

<span data-ttu-id="c30fe-113">El contexto del reconocedor se define mediante la configuración de:</span><span class="sxs-lookup"><span data-stu-id="c30fe-113">The recognizer context is defined by the settings of:</span></span>

-   <span data-ttu-id="c30fe-114">La guía de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="c30fe-114">The recognition guide.</span></span>
-   <span data-ttu-id="c30fe-115">Cualquier Factoids.</span><span class="sxs-lookup"><span data-stu-id="c30fe-115">Any factoids.</span></span>
-   <span data-ttu-id="c30fe-116">Cualquier marcador.</span><span class="sxs-lookup"><span data-stu-id="c30fe-116">Any flags.</span></span>
-   <span data-ttu-id="c30fe-117">Contexto del texto.</span><span class="sxs-lookup"><span data-stu-id="c30fe-117">The text context.</span></span>
-   <span data-ttu-id="c30fe-118">Cualquier lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="c30fe-118">Any word list.</span></span>
-   <span data-ttu-id="c30fe-119">El modo de autocompletar caracteres.</span><span class="sxs-lookup"><span data-stu-id="c30fe-119">The character Autocomplete mode.</span></span>

<span data-ttu-id="c30fe-120">El identificador del contexto del reconocedor se pasa a todas las funciones que usan esta configuración.</span><span class="sxs-lookup"><span data-stu-id="c30fe-120">The handle for the recognizer context is passed to all functions that use these settings.</span></span> <span data-ttu-id="c30fe-121">Cambiar un valor de configuración cambia el contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="c30fe-121">Changing a setting changes the recognizer context.</span></span>

<span data-ttu-id="c30fe-122">La aplicación puede usar varios contextos para reconocer la tinta de diferentes partes de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c30fe-122">The application may use several contexts to recognize ink from different parts of the screen.</span></span> <span data-ttu-id="c30fe-123">Un contexto individual puede reconocer varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="c30fe-123">An individual context can recognize multiple lines of text.</span></span> <span data-ttu-id="c30fe-124">Sin embargo, un contexto individual no puede procesar dos párrafos escritos en paralelo, como varias columnas en un artículo de un periódico.</span><span class="sxs-lookup"><span data-stu-id="c30fe-124">However, an individual context cannot process two paragraphs written side by side, such as multiple columns in a newspaper article.</span></span>

<span data-ttu-id="c30fe-125">Para reconocer nuevas entradas manuscritas, cree un nuevo contexto.</span><span class="sxs-lookup"><span data-stu-id="c30fe-125">To recognize new ink, create a new context.</span></span> <span data-ttu-id="c30fe-126">Como alternativa, utilice la función [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) para realizar una copia de un contexto que no tenga la tinta y los resultados, o la función [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) para borrar un contexto de su tinta y resultados.</span><span class="sxs-lookup"><span data-stu-id="c30fe-126">As an alternative, use the [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) function to make a copy of a context that does not have the ink and results, or the [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) function to clear a context of its ink and results.</span></span> <span data-ttu-id="c30fe-127">Con estos enfoques, una aplicación de entrada manuscrita puede reutilizar un contexto.</span><span class="sxs-lookup"><span data-stu-id="c30fe-127">With these approaches, an ink application can reuse a context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c30fe-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c30fe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c30fe-129">**SetGuide función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-129">**SetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[<span data-ttu-id="c30fe-130">**GetGuide función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-130">**GetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[<span data-ttu-id="c30fe-131">**SetFactoid función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-131">**SetFactoid Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[<span data-ttu-id="c30fe-132">**Función SetFlags**</span><span class="sxs-lookup"><span data-stu-id="c30fe-132">**SetFlags Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[<span data-ttu-id="c30fe-133">**SetEnabledUnicodeRanges función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-133">**SetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="c30fe-134">**GetEnabledUnicodeRanges función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-134">**GetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="c30fe-135">**SetCACMode función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-135">**SetCACMode Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[<span data-ttu-id="c30fe-136">**SetTextContext función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-136">**SetTextContext Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[<span data-ttu-id="c30fe-137">**SetWordList función)**</span><span class="sxs-lookup"><span data-stu-id="c30fe-137">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



