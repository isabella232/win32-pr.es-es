---
description: Los mecanismos de control estructurado de excepciones y de terminación son partes integrales del sistema; permiten que el sistema sea sólido. Puede usar estos mecanismos para crear aplicaciones sólidas y confiables coherentes.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: Acerca del control estructurado de excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274879"
---
# <a name="about-structured-exception-handling"></a><span data-ttu-id="58abf-104">Acerca del control estructurado de excepciones</span><span class="sxs-lookup"><span data-stu-id="58abf-104">About Structured Exception Handling</span></span>

<span data-ttu-id="58abf-105">Los mecanismos de control estructurado de excepciones y de terminación son partes integrales del sistema; permiten que el sistema sea sólido.</span><span class="sxs-lookup"><span data-stu-id="58abf-105">The structured exception handling and termination handling mechanisms are integral parts of the system; they enable the system to be robust.</span></span> <span data-ttu-id="58abf-106">Puede usar estos mecanismos para crear aplicaciones sólidas y confiables coherentes.</span><span class="sxs-lookup"><span data-stu-id="58abf-106">You can use these mechanisms to create consistently robust and reliable applications.</span></span>

<span data-ttu-id="58abf-107">El control estructurado de excepciones está disponible principalmente a través de la compatibilidad del compilador.</span><span class="sxs-lookup"><span data-stu-id="58abf-107">Structured exception handling is made available primarily through compiler support.</span></span> <span data-ttu-id="58abf-108">Por ejemplo, el compilador de optimización de C/C++ de Microsoft admite la palabra clave **\_ \_ try** que identifica un cuerpo protegido de código, la palabra clave **\_ \_ Except** que identifica un controlador de excepciones y la palabra clave **\_ \_ Finally** que identifica un controlador de terminación.</span><span class="sxs-lookup"><span data-stu-id="58abf-108">For example, the Microsoft C/C++ Optimizing Compiler supports the **\_\_try** keyword that identifies a guarded body of code, the **\_\_except** keyword that identifies an exception handler, and the **\_\_finally** keyword that identifies a termination handler.</span></span> <span data-ttu-id="58abf-109">Aunque esta información general usa ejemplos específicos del compilador de C/C++ de Microsoft, otros compiladores también proporcionan esta compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="58abf-109">Although this overview uses examples specific to the Microsoft C/C++ compiler, other compilers provide this support as well.</span></span>

-   [<span data-ttu-id="58abf-110">Control de excepciones</span><span class="sxs-lookup"><span data-stu-id="58abf-110">Exception Handling</span></span>](exception-handling.md)
-   [<span data-ttu-id="58abf-111">Control de excepciones basado en marcos</span><span class="sxs-lookup"><span data-stu-id="58abf-111">Frame-based Exception Handling</span></span>](frame-based-exception-handling.md)
-   [<span data-ttu-id="58abf-112">Control de excepciones vectoriales</span><span class="sxs-lookup"><span data-stu-id="58abf-112">Vectored Exception Handling</span></span>](vectored-exception-handling.md)
-   [<span data-ttu-id="58abf-113">Control de terminación</span><span class="sxs-lookup"><span data-stu-id="58abf-113">Termination Handling</span></span>](termination-handling.md)
-   [<span data-ttu-id="58abf-114">Sintaxis del controlador</span><span class="sxs-lookup"><span data-stu-id="58abf-114">Handler Syntax</span></span>](handler-syntax.md)

 

 



