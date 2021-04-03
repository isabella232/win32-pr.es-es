---
description: En esta sección se describe la sintaxis y el uso del control de excepciones estructurado tal y como se implementa en el compilador de optimización de C/C++ de Microsoft. El compilador interpreta las siguientes palabras clave como parte del mecanismo de control de excepciones estructurado.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintaxis del controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907006"
---
# <a name="handler-syntax"></a><span data-ttu-id="22b7c-104">Sintaxis del controlador</span><span class="sxs-lookup"><span data-stu-id="22b7c-104">Handler Syntax</span></span>

<span data-ttu-id="22b7c-105">En esta sección se describe la sintaxis y el uso del control de excepciones estructurado tal y como se implementa en el compilador de optimización de C/C++ de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="22b7c-105">This section describes the syntax and usage of structured exception handling as implemented in the Microsoft C/C++ Optimizing Compiler.</span></span> <span data-ttu-id="22b7c-106">El compilador interpreta las siguientes palabras clave como parte del mecanismo de control de excepciones estructurado.</span><span class="sxs-lookup"><span data-stu-id="22b7c-106">The following keywords are interpreted by the compiler as part of the structured exception-handling mechanism.</span></span>



| <span data-ttu-id="22b7c-107">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="22b7c-107">Keyword</span></span>         | <span data-ttu-id="22b7c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b7c-108">Description</span></span>                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b7c-109">**\_\_try**</span><span class="sxs-lookup"><span data-stu-id="22b7c-109">**\_\_try**</span></span>     | <span data-ttu-id="22b7c-110">Comienza un cuerpo protegido del código.</span><span class="sxs-lookup"><span data-stu-id="22b7c-110">Begins a guarded body of code.</span></span> <span data-ttu-id="22b7c-111">Se usa con la palabra clave **\_ \_ Except** para construir un [controlador de excepciones](exception-handler-syntax.md)o con la palabra clave **\_ \_ Finally** para construir un [controlador de finalización](termination-handler-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="22b7c-111">Used with the **\_\_except** keyword to construct an [exception handler](exception-handler-syntax.md), or with the **\_\_finally** keyword to construct a [termination handler](termination-handler-syntax.md).</span></span> |
| <span data-ttu-id="22b7c-112">**\_\_CEPT**</span><span class="sxs-lookup"><span data-stu-id="22b7c-112">**\_\_except**</span></span>  | <span data-ttu-id="22b7c-113">Comienza un bloque de código que se ejecuta solo cuando se produce una excepción dentro de su bloque **\_ \_ try** asociado.</span><span class="sxs-lookup"><span data-stu-id="22b7c-113">Begins a block of code that is executed only when an exception occurs within its associated **\_\_try** block.</span></span>                                                                                                                                   |
| <span data-ttu-id="22b7c-114">**\_\_finally**</span><span class="sxs-lookup"><span data-stu-id="22b7c-114">**\_\_finally**</span></span> | <span data-ttu-id="22b7c-115">Comienza un bloque de código que se ejecuta cada vez que el flujo de control abandona su bloque **\_ \_ try** asociado.</span><span class="sxs-lookup"><span data-stu-id="22b7c-115">Begins a block of code that is executed whenever the flow of control leaves its associated **\_\_try** block.</span></span>                                                                                                                                    |
| <span data-ttu-id="22b7c-116">**\_\_omiti**</span><span class="sxs-lookup"><span data-stu-id="22b7c-116">**\_\_leave**</span></span>   | <span data-ttu-id="22b7c-117">Permite la terminación inmediata del bloque **\_ \_ try** sin causar una terminación anómala y su penalización en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="22b7c-117">Allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span>                                                                                                                      |



 

<span data-ttu-id="22b7c-118">El compilador también interpreta las funciones [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)y [**AbnormalTermination**](abnormaltermination.md) como palabras clave, y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.</span><span class="sxs-lookup"><span data-stu-id="22b7c-118">The compiler also interprets the [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md), and [**AbnormalTermination**](abnormaltermination.md) functions as keywords, and their use outside the appropriate exception-handling syntax generates a compiler error.</span></span> <span data-ttu-id="22b7c-119">A continuación se muestran breves descripciones de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="22b7c-119">The following are brief descriptions of these functions.</span></span>



| <span data-ttu-id="22b7c-120">Función</span><span class="sxs-lookup"><span data-stu-id="22b7c-120">Function</span></span>                                                   | <span data-ttu-id="22b7c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b7c-121">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22b7c-122">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="22b7c-122">**GetExceptionCode**</span></span>](getexceptioncode.md)               | <span data-ttu-id="22b7c-123">Devuelve un código que identifica el tipo de excepción.</span><span class="sxs-lookup"><span data-stu-id="22b7c-123">Returns a code that identifies the type of exception.</span></span> <span data-ttu-id="22b7c-124">Solo se puede llamar a esta función desde dentro de la expresión de filtro o el bloque de controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="22b7c-124">This function can be called only from within the filter expression or the exception-handler block.</span></span>                                                                                                |
| [<span data-ttu-id="22b7c-125">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="22b7c-125">**GetExceptionInformation**</span></span>](getexceptioninformation.md) | <span data-ttu-id="22b7c-126">Devuelve un puntero a una estructura de [**\_ punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros al registro de contexto y al registro de excepción.</span><span class="sxs-lookup"><span data-stu-id="22b7c-126">Returns a pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure containing pointers to the context record and the exception record.</span></span> <span data-ttu-id="22b7c-127">Solo se puede llamar a esta función desde dentro de la expresión de filtro de un controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="22b7c-127">This function can be called only from within the filter expression of an exception handler.</span></span> |
| [<span data-ttu-id="22b7c-128">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="22b7c-128">**AbnormalTermination**</span></span>](abnormaltermination.md)         | <span data-ttu-id="22b7c-129">Indica si el flujo de control dejó el bloque **\_ \_ try** asociado secuencialmente después de ejecutar la última instrucción del bloque.</span><span class="sxs-lookup"><span data-stu-id="22b7c-129">Indicates whether the flow of control left the associated **\_\_try** block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="22b7c-130">Solo se puede llamar a esta función desde dentro del bloque **\_ \_ Finally** de un controlador de finalización.</span><span class="sxs-lookup"><span data-stu-id="22b7c-130">This function can be called only from within the **\_\_finally** block of a termination handler.</span></span>              |



 

 

 



