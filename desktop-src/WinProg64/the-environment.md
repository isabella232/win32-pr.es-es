---
title: El entorno
description: Los desarrolladores que trabajan en aplicaciones para Windows de 64 bits encontrarán el entorno de desarrollo prácticamente idéntico al entorno de desarrollo de Windows de 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- entorno de desarrollo de 64 programación de Windows de bits
- 'entorno de 64: programación de Windows de bits'
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, entorno de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075391"
---
# <a name="the-environment"></a><span data-ttu-id="c40b1-106">El entorno</span><span class="sxs-lookup"><span data-stu-id="c40b1-106">The Environment</span></span>

<span data-ttu-id="c40b1-107">Los desarrolladores que trabajan en aplicaciones para Windows de 64 bits encontrarán el entorno de desarrollo prácticamente idéntico al entorno de desarrollo de Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c40b1-107">Developers working on applications for 64-bit Windows will find the development environment virtually identical to the development environment for 32-bit Windows.</span></span> <span data-ttu-id="c40b1-108">Las API existentes se han modificado cuando sea necesario para que reflejen la precisión de la plataforma en la que se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="c40b1-108">The existing APIs have been modified where necessary to allow them to reflect the precision of the platform on which they are running.</span></span> <span data-ttu-id="c40b1-109">El resultado es una simplicidad y una curva de aprendizaje breve para el desarrollador; escribir código para Windows de 64 bits es igual que escribir código para Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c40b1-109">The result is simplicity and a short learning curve for the developer—writing code for 64-bit Windows is just like writing code for 32-bit Windows.</span></span>

<span data-ttu-id="c40b1-110">Los archivos de encabezado de Windows admiten nuevos tipos de datos que permiten que los punteros y las variables asociadas a puntero reflejen la precisión de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c40b1-110">The Windows header files support new data types that allow pointers and pointer-associated variables to reflect the precision of the platform.</span></span> <span data-ttu-id="c40b1-111">Esto significa que los desarrolladores pueden compilar una base de origen única para ejecutarse de forma nativa en Windows de 32 bits o en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c40b1-111">This means that developers can compile a single source base to run natively on either 32-bit Windows or 64-bit Windows.</span></span> <span data-ttu-id="c40b1-112">Esta estrategia reduce el costo del desarrollo de aplicaciones que aprovechan el hardware de 64 bits, como procesadores AMD Opteron o Athlon64 o procesadores Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="c40b1-112">This strategy reduces the cost of developing applications that leverage 64-bit hardware such as AMD Opteron or Athlon64 processors or Intel Itanium processors.</span></span>

<span data-ttu-id="c40b1-113">Tendrá más tiempo para que las aplicaciones 64 de bits estén listas si adopta las nuevas convenciones de tipos de datos lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="c40b1-113">You will have more time to make your applications 64-bit ready if you adopt the new data-type conventions as soon as possible.</span></span> <span data-ttu-id="c40b1-114">Si va a cambiar el código, debe cambiar las definiciones de datos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c40b1-114">If you are changing your code, you should change the data definitions at the same time.</span></span> <span data-ttu-id="c40b1-115">Pruebe la aplicación en Windows de 32 bits, ejecútela a través del compilador de 64 bits (descrito en [las herramientas](the-tools.md)) y la aplicación estará lista para probarse cuando tenga el hardware de 64 bits adecuado.</span><span class="sxs-lookup"><span data-stu-id="c40b1-115">Test the application on 32-bit Windows, run it through the 64-bit compiler (described in [The Tools](the-tools.md)), and the application will be ready to test when you have the appropriate 64-bit hardware.</span></span>

 

 




