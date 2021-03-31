---
title: Traducir la sintaxis de objetos COM para lenguajes de programación
description: Traducir la sintaxis de objetos COM para lenguajes de programación
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903401"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a><span data-ttu-id="cbb54-103">Traducir la sintaxis de objetos COM para lenguajes de programación</span><span class="sxs-lookup"><span data-stu-id="cbb54-103">Translating COM Object Syntax for Programming Languages</span></span>

<span data-ttu-id="cbb54-104">Para llamar a un objeto COM desde una aplicación escrita en un lenguaje de programación distinto del usado para escribir el objeto COM, primero debe traducir la sintaxis del objeto al lenguaje de programación.</span><span class="sxs-lookup"><span data-stu-id="cbb54-104">To call a COM object from an application written in a programming language other than the one used to write the COM object, you must first translate the object's syntax to your programming language.</span></span> <span data-ttu-id="cbb54-105">Esta operación se puede completar mediante los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="cbb54-105">This can be done using the following steps:</span></span>

1.  <span data-ttu-id="cbb54-106">Vea la biblioteca de tipos del objeto COM en la sintaxis del lenguaje de programación.</span><span class="sxs-lookup"><span data-stu-id="cbb54-106">View the COM object's type library in your programming language's syntax.</span></span> <span data-ttu-id="cbb54-107">Al hacerlo, se proporcionan descripciones de las clases, interfaces, métodos, propiedades y eventos del objeto en la sintaxis del lenguaje que se usa.</span><span class="sxs-lookup"><span data-stu-id="cbb54-107">Doing this provides you with descriptions of the object's classes, interfaces, methods, properties and events in the language syntax you use.</span></span>

    <span data-ttu-id="cbb54-108">Los productos para desarrolladores de Microsoft proporcionan varias herramientas que le ayudarán a ver y convertir bibliotecas de tipos.</span><span class="sxs-lookup"><span data-stu-id="cbb54-108">Microsoft developer products provide several tools to assist you in viewing and converting type libraries.</span></span> <span data-ttu-id="cbb54-109">Para obtener más información, vea [visores de biblioteca de tipos y herramientas de conversión](type-library-viewers-and-conversion-tools.md) y [Cómo herramientas de desarrollo usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="cbb54-109">For more information, see [Type Library Viewers and Conversion Tools](type-library-viewers-and-conversion-tools.md) and [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

    <span data-ttu-id="cbb54-110">Una vez que pueda ver la biblioteca de tipos del objeto en el lenguaje de programación que prefiera, puede comparar su sintaxis con la de la documentación del objeto.</span><span class="sxs-lookup"><span data-stu-id="cbb54-110">Once you can view the object's type library in your preferred programming language, you can compare its syntax to that in the documentation for the object.</span></span> <span data-ttu-id="cbb54-111">Si el objeto está documentado en un lenguaje de programación distinto del que está utilizando, los tipos de datos y la sintaxis pueden diferir, pero las descripciones de los parámetros, los valores devueltos y la funcionalidad del objeto deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="cbb54-111">If the object is documented in a programming language other than the one you are using, the data types and syntax may differ, but descriptions of parameters, return values, and the object's functionality should be the same.</span></span>

2.  <span data-ttu-id="cbb54-112">Tenga en cuenta las consideraciones especiales para traducir a su lenguaje de programación.</span><span class="sxs-lookup"><span data-stu-id="cbb54-112">Take into account any special considerations for translating to your programming language.</span></span>

    <span data-ttu-id="cbb54-113">Dado que cada lenguaje de programación define conceptos que no pueden tener un equivalente en otros lenguajes, parte de la funcionalidad de un objeto puede funcionar de manera diferente en otro lenguaje o no estar disponible en absoluto.</span><span class="sxs-lookup"><span data-stu-id="cbb54-113">Because each programming language defines concepts that may not have an equivalent in other languages, some of an object's functionality may work differently in another language, or not be available at all.</span></span> <span data-ttu-id="cbb54-114">Por ejemplo, el lenguaje de programación Visual Basic no reconoce los tipos de datos sin signo de C++, como **unsignedÂ Long**.</span><span class="sxs-lookup"><span data-stu-id="cbb54-114">For example, the Visual Basic programming language does not recognize C++ unsigned data types, such as **unsignedÂ long**.</span></span> <span data-ttu-id="cbb54-115">Una aplicación escrita en Visual Basic no puede usar métodos COM que acepten o devuelvan variables de tipo de datos sin firmar.</span><span class="sxs-lookup"><span data-stu-id="cbb54-115">An application written in Visual Basic cannot use COM methods that accept or return unsigned data type variables.</span></span>

3.  <span data-ttu-id="cbb54-116">Agregue el código compilado del objeto COM al proyecto.</span><span class="sxs-lookup"><span data-stu-id="cbb54-116">Add the COM object's compiled code to your project.</span></span> <span data-ttu-id="cbb54-117">Normalmente, el código compilado se incluye en un archivo. dll o. ocx.</span><span class="sxs-lookup"><span data-stu-id="cbb54-117">The compiled code is typically contained in a .dll or .ocx file.</span></span> <span data-ttu-id="cbb54-118">Este paso es necesario para que el compilador reconozca las clases del objeto COM.</span><span class="sxs-lookup"><span data-stu-id="cbb54-118">This step is necessary for the compiler to recognize the COM object's classes.</span></span> <span data-ttu-id="cbb54-119">Después de agregar el objeto COM, la aplicación puede usar sus clases e interfaces.</span><span class="sxs-lookup"><span data-stu-id="cbb54-119">After you add the COM object, your application can use its classes and interfaces.</span></span>

<span data-ttu-id="cbb54-120">En los temas siguientes se describe cómo traducir y usar objetos COM en diversos lenguajes de programación:</span><span class="sxs-lookup"><span data-stu-id="cbb54-120">The following topics describe how to translate and use COM objects in a variety of programming languages:</span></span>

-   [<span data-ttu-id="cbb54-121">Traducir a C++</span><span class="sxs-lookup"><span data-stu-id="cbb54-121">Translating to C++</span></span>](translating-to-c--.md)
-   [<span data-ttu-id="cbb54-122">Trasladar a Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cbb54-122">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
-   [<span data-ttu-id="cbb54-123">Traducir a Java</span><span class="sxs-lookup"><span data-stu-id="cbb54-123">Translating to Java</span></span>](translating-to-java.md)

<span data-ttu-id="cbb54-124">En estos temas se describen los procesos y las herramientas de conversión proporcionados por los productos para desarrolladores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cbb54-124">These topics describe conversion tools and processes provided by Microsoft developer products.</span></span> <span data-ttu-id="cbb54-125">Para obtener instrucciones sobre cómo programar objetos COM mediante herramientas de desarrollo creadas por otras compañías, consulte la documentación de las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="cbb54-125">For instructions on how to program COM objects using development tools created by other companies, see those development tools' documentation.</span></span>

 

 




