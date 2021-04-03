---
title: Usar COM en la aplicación de Windows
description: En el módulo 1 de esta serie se ha mostrado cómo crear una ventana y responder a mensajes de ventana, como WM \_ Paint y el cierre de WM \_ . El módulo 2 presenta el modelo de objetos componentes (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791362"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a><span data-ttu-id="221ec-104">Módulo 2.</span><span class="sxs-lookup"><span data-stu-id="221ec-104">Module 2.</span></span> <span data-ttu-id="221ec-105">Usar COM en el programa Windows-Based</span><span class="sxs-lookup"><span data-stu-id="221ec-105">Using COM in Your Windows-Based Program</span></span>

<span data-ttu-id="221ec-106">En el [módulo 1](your-first-windows-program.md) de esta serie se ha mostrado cómo crear una ventana y responder a mensajes de ventana, como [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) y el [**\_ cierre de WM**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="221ec-106">[Module 1](your-first-windows-program.md) of this series showed how to create a window and respond to window messages such as [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span> <span data-ttu-id="221ec-107">El módulo 2 presenta el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="221ec-107">Module 2 introduces the Component Object Model (COM).</span></span>

<span data-ttu-id="221ec-108">COM es una especificación para crear componentes de software reutilizables.</span><span class="sxs-lookup"><span data-stu-id="221ec-108">COM is a specification for creating reusable software components.</span></span> <span data-ttu-id="221ec-109">Muchas de las características que usará en un programa moderno basado en Windows se basan en COM, como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="221ec-109">Many of the features that you will use in a modern Windows-based program rely on COM, such as the following:</span></span>

-   <span data-ttu-id="221ec-110">Gráficos (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="221ec-110">Graphics (Direct2D)</span></span>
-   <span data-ttu-id="221ec-111">Texto (DirectWrite)</span><span class="sxs-lookup"><span data-stu-id="221ec-111">Text (DirectWrite)</span></span>
-   <span data-ttu-id="221ec-112">Shell de Windows</span><span class="sxs-lookup"><span data-stu-id="221ec-112">The Windows Shell</span></span>
-   <span data-ttu-id="221ec-113">Control Ribbon</span><span class="sxs-lookup"><span data-stu-id="221ec-113">The Ribbon control</span></span>
-   <span data-ttu-id="221ec-114">Animación de IU</span><span class="sxs-lookup"><span data-stu-id="221ec-114">UI animation</span></span>

<span data-ttu-id="221ec-115">(Algunas tecnologías de esta lista usan un subconjunto de COM y, por lo tanto, no son "puras" COM).</span><span class="sxs-lookup"><span data-stu-id="221ec-115">(Some technologies on this list use a subset of COM and are therefore not "pure" COM.)</span></span>

<span data-ttu-id="221ec-116">COM tiene una reputación por ser difícil de aprender.</span><span class="sxs-lookup"><span data-stu-id="221ec-116">COM has a reputation for being difficult to learn.</span></span> <span data-ttu-id="221ec-117">Y es cierto que escribir un nuevo módulo de software para admitir COM puede ser complicado.</span><span class="sxs-lookup"><span data-stu-id="221ec-117">And it is true that writing a new software module to support COM can be tricky.</span></span> <span data-ttu-id="221ec-118">Pero si el programa es estrictamente un *consumidor* de com, puede encontrar que com es más fácil de entender de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="221ec-118">But if your program is strictly a *consumer* of COM, you may find that COM is easier to understand than you expect.</span></span>

<span data-ttu-id="221ec-119">En este módulo se muestra cómo llamar a las API basadas en COM en el programa.</span><span class="sxs-lookup"><span data-stu-id="221ec-119">This module shows how to call COM-based APIs in your program.</span></span> <span data-ttu-id="221ec-120">También describe algunas de las razones por las que se basa el diseño de COM.</span><span class="sxs-lookup"><span data-stu-id="221ec-120">It also describes some of the reasoning behind the design of COM.</span></span> <span data-ttu-id="221ec-121">Si entiende por qué COM está diseñado tal cual, puede programar con más eficacia.</span><span class="sxs-lookup"><span data-stu-id="221ec-121">If you understand why COM is designed as it is, you can program with it more effectively.</span></span> <span data-ttu-id="221ec-122">En la segunda parte del módulo se describen algunos procedimientos recomendados de programación para COM.</span><span class="sxs-lookup"><span data-stu-id="221ec-122">The second part of the module describes some recommended programming practices for COM.</span></span>

<span data-ttu-id="221ec-123">COM se presentó en 1993 para admitir la vinculación e incrustación de objetos (OLE) 2,0.</span><span class="sxs-lookup"><span data-stu-id="221ec-123">COM was introduced in 1993 to support Object Linking and Embedding (OLE) 2.0.</span></span> <span data-ttu-id="221ec-124">A veces, los usuarios piensan que COM y OLE son lo mismo.</span><span class="sxs-lookup"><span data-stu-id="221ec-124">People sometimes think that COM and OLE are the same thing.</span></span> <span data-ttu-id="221ec-125">Esto puede ser otro motivo para la percepción de que COM es difícil de aprender.</span><span class="sxs-lookup"><span data-stu-id="221ec-125">This may be another reason for the perception that COM is difficult to learn.</span></span> <span data-ttu-id="221ec-126">OLE 2,0 se basa en COM, pero no es necesario conocer OLE para comprender COM.</span><span class="sxs-lookup"><span data-stu-id="221ec-126">OLE 2.0 is built on COM, but you do not have to know OLE to understand COM.</span></span>

<span data-ttu-id="221ec-127">COM es un *estándar binario*, no un estándar de lenguaje: define la interfaz binaria entre una aplicación y un componente de software.</span><span class="sxs-lookup"><span data-stu-id="221ec-127">COM is a *binary standard*, not a language standard: It defines the binary interface between an application and a software component.</span></span> <span data-ttu-id="221ec-128">Como estándar binario, COM es independiente del lenguaje, aunque se asigna de forma natural a ciertas construcciones de C++.</span><span class="sxs-lookup"><span data-stu-id="221ec-128">As a binary standard, COM is language-neutral, although it maps naturally to certain C++ constructs.</span></span> <span data-ttu-id="221ec-129">Este módulo se centrará en tres objetivos principales de COM:</span><span class="sxs-lookup"><span data-stu-id="221ec-129">This module will focus on three major goals of COM:</span></span>

-   <span data-ttu-id="221ec-130">Separar la implementación de un objeto de su interfaz.</span><span class="sxs-lookup"><span data-stu-id="221ec-130">Separating the implementation of an object from its interface.</span></span>
-   <span data-ttu-id="221ec-131">Administrar la duración de un objeto.</span><span class="sxs-lookup"><span data-stu-id="221ec-131">Managing the lifetime of an object.</span></span>
-   <span data-ttu-id="221ec-132">Detectar las capacidades de un objeto en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="221ec-132">Discovering the capabilities of an object at run time.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="221ec-133">En esta sección</span><span class="sxs-lookup"><span data-stu-id="221ec-133">In this section</span></span>

-   [<span data-ttu-id="221ec-134">¿Qué es una interfaz COM?</span><span class="sxs-lookup"><span data-stu-id="221ec-134">What Is a COM Interface?</span></span>](what-is-a-com-interface-.md)
-   [<span data-ttu-id="221ec-135">Inicializar la biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="221ec-135">Initializing the COM Library</span></span>](initializing-the-com-library.md)
-   [<span data-ttu-id="221ec-136">Códigos de error en COM</span><span class="sxs-lookup"><span data-stu-id="221ec-136">Error Codes in COM</span></span>](error-codes-in-com.md)
-   [<span data-ttu-id="221ec-137">Crear un objeto en COM</span><span class="sxs-lookup"><span data-stu-id="221ec-137">Creating an Object in COM</span></span>](creating-an-object-in-com.md)
-   [<span data-ttu-id="221ec-138">Ejemplo: el cuadro de diálogo abrir</span><span class="sxs-lookup"><span data-stu-id="221ec-138">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)
-   [<span data-ttu-id="221ec-139">Administrar la duración de un objeto</span><span class="sxs-lookup"><span data-stu-id="221ec-139">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)
-   [<span data-ttu-id="221ec-140">Solicitar un objeto para una interfaz</span><span class="sxs-lookup"><span data-stu-id="221ec-140">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)
-   [<span data-ttu-id="221ec-141">Asignación de memoria en COM</span><span class="sxs-lookup"><span data-stu-id="221ec-141">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)
-   [<span data-ttu-id="221ec-142">Prácticas de codificación COM</span><span class="sxs-lookup"><span data-stu-id="221ec-142">COM Coding Practices</span></span>](com-coding-practices.md)
-   [<span data-ttu-id="221ec-143">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="221ec-143">Error Handling in COM</span></span>](error-handling-in-com.md)

## <a name="related-topics"></a><span data-ttu-id="221ec-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="221ec-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="221ec-145">Aprender a programar para Windows en C++</span><span class="sxs-lookup"><span data-stu-id="221ec-145">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 