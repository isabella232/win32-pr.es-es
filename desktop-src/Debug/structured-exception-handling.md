---
description: Una excepción es un evento que se produce durante la ejecución de un programa y requiere la ejecución de código fuera del flujo de control normal.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Control de excepciones estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907003"
---
# <a name="structured-exception-handling"></a><span data-ttu-id="61d2f-103">Control de excepciones estructurado</span><span class="sxs-lookup"><span data-stu-id="61d2f-103">Structured Exception Handling</span></span>

<span data-ttu-id="61d2f-104">Una *excepción* es un evento que se produce durante la ejecución de un programa y requiere la ejecución de código fuera del flujo de control normal.</span><span class="sxs-lookup"><span data-stu-id="61d2f-104">An *exception* is an event that occurs during the execution of a program, and requires the execution of code outside the normal flow of control.</span></span> <span data-ttu-id="61d2f-105">Hay dos tipos de excepciones: excepciones de hardware y de software.</span><span class="sxs-lookup"><span data-stu-id="61d2f-105">There are two kinds of exceptions: hardware exceptions and software exceptions.</span></span> <span data-ttu-id="61d2f-106">La CPU inicia las *excepciones de hardware* .</span><span class="sxs-lookup"><span data-stu-id="61d2f-106">*Hardware exceptions* are initiated by the CPU.</span></span> <span data-ttu-id="61d2f-107">Pueden ser el resultado de la ejecución de ciertas secuencias de instrucciones, como la división por cero o un intento de obtener acceso a una dirección de memoria no válida.</span><span class="sxs-lookup"><span data-stu-id="61d2f-107">They can result from the execution of certain instruction sequences, such as division by zero or an attempt to access an invalid memory address.</span></span> <span data-ttu-id="61d2f-108">Las aplicaciones o el sistema operativo inician explícitamente las *excepciones de software* .</span><span class="sxs-lookup"><span data-stu-id="61d2f-108">*Software exceptions* are initiated explicitly by applications or the operating system.</span></span> <span data-ttu-id="61d2f-109">Por ejemplo, el sistema puede detectar cuándo se especifica un valor de parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="61d2f-109">For example, the system can detect when an invalid parameter value is specified.</span></span>

<span data-ttu-id="61d2f-110">El *control estructurado de excepciones* es un mecanismo para controlar las excepciones de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="61d2f-110">*Structured exception handling* is a mechanism for handling both hardware and software exceptions.</span></span> <span data-ttu-id="61d2f-111">Por lo tanto, el código controlará las excepciones de hardware y software de forma idéntica.</span><span class="sxs-lookup"><span data-stu-id="61d2f-111">Therefore, your code will handle hardware and software exceptions identically.</span></span> <span data-ttu-id="61d2f-112">El control de excepciones estructurado permite tener un control completo sobre el control de excepciones, proporciona compatibilidad con los depuradores y se puede usar en todos los lenguajes de programación y máquinas.</span><span class="sxs-lookup"><span data-stu-id="61d2f-112">Structured exception handling enables you to have complete control over the handling of exceptions, provides support for debuggers, and is usable across all programming languages and machines.</span></span> <span data-ttu-id="61d2f-113">El *control de excepciones vectoriales* es una extensión del control estructurado de excepciones.</span><span class="sxs-lookup"><span data-stu-id="61d2f-113">*Vectored exception handling* is an extension to structured exception handling.</span></span>

<span data-ttu-id="61d2f-114">El sistema también admite el *control de terminación*, lo que le permite asegurarse de que, siempre que se ejecute un cuerpo protegido de código, también se ejecute un bloque de código de terminación especificado.</span><span class="sxs-lookup"><span data-stu-id="61d2f-114">The system also supports *termination handling*, which enables you to ensure that whenever a guarded body of code is executed, a specified block of termination code is also executed.</span></span> <span data-ttu-id="61d2f-115">El código de finalización se ejecuta independientemente de cómo el flujo de control abandone el cuerpo protegido.</span><span class="sxs-lookup"><span data-stu-id="61d2f-115">The termination code is executed regardless of how the flow of control leaves the guarded body.</span></span> <span data-ttu-id="61d2f-116">Por ejemplo, un controlador de terminación puede garantizar que las tareas de limpieza se realicen incluso si se produce una excepción o algún otro error mientras se ejecuta el cuerpo protegido del código.</span><span class="sxs-lookup"><span data-stu-id="61d2f-116">For example, a termination handler can guarantee that clean-up tasks are performed even if an exception or some other error occurs while the guarded body of code is being executed.</span></span>

-   [<span data-ttu-id="61d2f-117">Acerca del control estructurado de excepciones</span><span class="sxs-lookup"><span data-stu-id="61d2f-117">About Structured Exception Handling</span></span>](about-structured-exception-handling.md)
-   [<span data-ttu-id="61d2f-118">Usar el control de excepciones estructurado</span><span class="sxs-lookup"><span data-stu-id="61d2f-118">Using Structured Exception Handling</span></span>](using-structured-exception-handling.md)
-   [<span data-ttu-id="61d2f-119">Referencia de control de excepciones estructurado</span><span class="sxs-lookup"><span data-stu-id="61d2f-119">Structured Exception Handling Reference</span></span>](structured-exception-handling-reference.md)

 

 



