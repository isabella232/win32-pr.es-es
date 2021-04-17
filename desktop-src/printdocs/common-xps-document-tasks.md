---
description: En esta página se enumeran algunas de las tareas de programación que se suelen realizar con la API de documentos XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Tareas comunes de programación de documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677785"
---
# <a name="common-xps-document-programming-tasks"></a><span data-ttu-id="0e9a9-103">Tareas comunes de programación de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-103">Common XPS Document Programming Tasks</span></span>

<span data-ttu-id="0e9a9-104">En esta página se enumeran algunas de las tareas de programación que se suelen realizar con la API de documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-104">This page lists some of the programming tasks that are commonly performed with the XPS Document API.</span></span>

## <a name="common-xps-document-tasks"></a><span data-ttu-id="0e9a9-105">Tareas comunes de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-105">Common XPS Document Tasks</span></span>

<span data-ttu-id="0e9a9-106">En los siguientes ejemplos de código se muestran algunas de las tareas de programación que normalmente se realizan cuando se usa la API de documento XPS para trabajar con un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-106">The following code examples illustrate some of the programming tasks that are commonly performed when the XPS Document API is used for working with an XPS OM.</span></span>

<dl>

[<span data-ttu-id="0e9a9-107">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-107">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="0e9a9-108">Crear un OM XPS en blanco</span><span class="sxs-lookup"><span data-stu-id="0e9a9-108">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="0e9a9-109">Leer un documento XPS en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-109">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="0e9a9-110">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-110">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="0e9a9-111">Escribir texto en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-111">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="0e9a9-112">Dibujar gráficos en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-112">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="0e9a9-113">Colocar imágenes en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-113">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="0e9a9-114">Escribir un OM XPS en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-114">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="0e9a9-115">Imprimir un OM XPS</span><span class="sxs-lookup"><span data-stu-id="0e9a9-115">Print an XPS OM</span></span>](print-an-xps-om.md)  
[<span data-ttu-id="0e9a9-116">Trabajar con interfaces de colección de XPS OM</span><span class="sxs-lookup"><span data-stu-id="0e9a9-116">Working with XPS OM Collection Interfaces</span></span>](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a><span data-ttu-id="0e9a9-117">Declinación de responsabilidades</span><span class="sxs-lookup"><span data-stu-id="0e9a9-117">Disclaimer</span></span>

<span data-ttu-id="0e9a9-118">Los ejemplos de código no pretenden ser completos ni programas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-118">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="0e9a9-119">Los ejemplos de código a los que se hace referencia en esta página, por ejemplo, no realizan la comprobación de parámetros, la comprobación de errores ni el control de errores.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-119">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, or error handling.</span></span> <span data-ttu-id="0e9a9-120">Use estos ejemplos como punto de partida y, a continuación, agregue el código necesario para crear una aplicación sólida.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-120">Use these examples as a starting point, and then add the code necessary to create a robust application.</span></span> <span data-ttu-id="0e9a9-121">Para obtener más información sobre los valores devueltos **HRESULT** y las estrategias de control de errores, vea [control de errores en com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="0e9a9-121">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="0e9a9-122">Antes de poder usar las interfaces XPS OM, se debe inicializar COM en el subproceso, tal como se muestra en el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-122">Before XPS OM interfaces can be used, COM must be initialized in the thread, as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="0e9a9-123">Para mayor claridad, en estos ejemplos de código se usa un modelo de objetos de XPS muy sencillo, uno que podría no ser suficientemente complejo para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-123">For clarity, these code examples use a very simple XPS OM, one that might not be complex enough for your application.</span></span> <span data-ttu-id="0e9a9-124">Como punto, en los ejemplos de código que agregan contenido a una página, los elementos visuales de una página se agregan directamente a la lista de objetos visuales de la página. en la práctica, sin embargo, es posible que desee agrupar objetos visuales en objetos de lienzo, de modo que se pueda actuar como grupo en varios objetos.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-124">As a case in point, in the code examples that add content to a page, the visual elements of a page are added directly to the page's list of visual objects; in practice, however, you might want to group visual objects into canvas objects, so that multiple objects could be acted upon as a group.</span></span> <span data-ttu-id="0e9a9-125">Por lo tanto, para habilitar la compatibilidad del mismo contenido con más de un tamaño de página, puede agrupar el contenido visual de una página en un solo objeto Canvas y, a continuación, aplicar una transformación al lienzo para escalarlo al tamaño de página actual.</span><span class="sxs-lookup"><span data-stu-id="0e9a9-125">Thus, to enable support of the same content for more than one page size, you could group the visual content of a page into a single canvas object, and then apply a transform to the canvas to scale it to the current page size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e9a9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e9a9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e9a9-127">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="0e9a9-127">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="0e9a9-128">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="0e9a9-128">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
