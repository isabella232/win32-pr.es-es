---
title: Introducción a Win32 y C++
description: El objetivo de esta serie de introducción es enseñarle a escribir un programa de escritorio en C++ mediante Win32 y las API de COM.
ms.assetid: a9470cb9-a1e7-4d6d-a4be-61b81d209ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b1ad80530877e9502d158a16295013e3f4a05e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779681"
---
# <a name="get-started-with-win32-and-c"></a><span data-ttu-id="4f60e-103">Introducción a Win32 y C++</span><span class="sxs-lookup"><span data-stu-id="4f60e-103">Get Started with Win32 and C++</span></span>

<span data-ttu-id="4f60e-104">El objetivo de esta serie de introducción es enseñarle a escribir un programa de escritorio en C++ mediante Win32 y las API de COM.</span><span class="sxs-lookup"><span data-stu-id="4f60e-104">The aim of this Get Started series is to teach you how to write a desktop program in C++ using Win32 and COM APIs.</span></span>

<span data-ttu-id="4f60e-105">En el primer módulo, aprenderá paso a paso cómo crear y mostrar una ventana.</span><span class="sxs-lookup"><span data-stu-id="4f60e-105">In the first module, you'll learn step-by-step how to create and show a window.</span></span> <span data-ttu-id="4f60e-106">Los módulos posteriores introducirán el modelo de objetos componentes (COM), los gráficos y el texto, y los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="4f60e-106">Later modules will introduce the Component Object Model (COM), graphics and text, and user input.</span></span>

<span data-ttu-id="4f60e-107">En esta serie, se supone que tiene un buen conocimiento práctico de la programación de C++.</span><span class="sxs-lookup"><span data-stu-id="4f60e-107">For this series, it is assumed that you have a good working knowledge of C++ programming.</span></span> <span data-ttu-id="4f60e-108">No se presupone ninguna experiencia anterior con la programación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4f60e-108">No previous experience with Windows programming is assumed.</span></span> <span data-ttu-id="4f60e-109">Si no está familiarizado con C++, puede encontrar material de aprendizaje en el [Centro para desarrolladores de Visual C++](https://msdn.microsoft.com/vstudio//default.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f60e-109">If you are new to C++, you can find learning material at the [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx).</span></span> <span data-ttu-id="4f60e-110">(Es posible que este recurso no esté disponible en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="4f60e-110">(This resource may not be available in some languages and countries.)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4f60e-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4f60e-111">In this section</span></span>



| <span data-ttu-id="4f60e-112">Tema</span><span class="sxs-lookup"><span data-stu-id="4f60e-112">Topic</span></span>                                                                                                     | <span data-ttu-id="4f60e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f60e-113">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f60e-114">Introducción a la programación de Windows en C++</span><span class="sxs-lookup"><span data-stu-id="4f60e-114">Introduction to Windows Programming in C++</span></span>](introduction-to-windows-programming-in-c--.md)<br/>   | <span data-ttu-id="4f60e-115">En esta sección se describen algunas de las convenciones básicas de codificación y terminología que se usan en la programación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4f60e-115">This section describes some of the basic terminology and coding conventions used in Windows programming.</span></span><br/>  |
| [<span data-ttu-id="4f60e-116">Módulo 1. Su primer programa de Windows</span><span class="sxs-lookup"><span data-stu-id="4f60e-116">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)<br/>                         | <span data-ttu-id="4f60e-117">En este módulo, creará un sencillo programa de Windows que muestra una ventana en blanco.</span><span class="sxs-lookup"><span data-stu-id="4f60e-117">In this module, you will create a simple Windows program that shows a blank window.</span></span><br/>                       |
| [<span data-ttu-id="4f60e-118">Módulo 2. Usar COM en el programa de Windows</span><span class="sxs-lookup"><span data-stu-id="4f60e-118">Module 2. Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)<br/> | <span data-ttu-id="4f60e-119">Este módulo presenta el modelo de objetos componentes (COM), que subyace a muchas de las API modernas de Windows.</span><span class="sxs-lookup"><span data-stu-id="4f60e-119">This module introduces the Component Object Model (COM), which underlies many of the modern Windows APIs.</span></span><br/> |
| [<span data-ttu-id="4f60e-120">Módulo 3. Gráficos de Windows</span><span class="sxs-lookup"><span data-stu-id="4f60e-120">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)<br/>                                  | <span data-ttu-id="4f60e-121">Este módulo presenta la arquitectura de gráficos de Windows, centrándose en Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4f60e-121">This module introduces the Windows graphics architecture, with a focus on Direct2D.</span></span><br/>                       |
| [<span data-ttu-id="4f60e-122">Módulo 4. Datos proporcionados por el usuario</span><span class="sxs-lookup"><span data-stu-id="4f60e-122">Module 4. User Input</span></span>](module-4--user-input.md)<br/>                                               | <span data-ttu-id="4f60e-123">Este módulo describe la entrada del mouse y del teclado.</span><span class="sxs-lookup"><span data-stu-id="4f60e-123">This module describes mouse and keyboard input.</span></span><br/>                                                           |
| [<span data-ttu-id="4f60e-124">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f60e-124">Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)<br/>                                   | <span data-ttu-id="4f60e-125">Contiene vínculos para descargar el código de ejemplo de esta serie.</span><span class="sxs-lookup"><span data-stu-id="4f60e-125">Contains links to download the sample code for this series.</span></span><br/>                                               |



 

 

 





