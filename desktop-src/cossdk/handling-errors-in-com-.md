---
description: La parte más problemática de la escritura de componentes consiste en tratar con posibles errores.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Control de errores en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153584"
---
# <a name="handling-errors-in-com"></a><span data-ttu-id="cedc4-103">Control de errores en COM+</span><span class="sxs-lookup"><span data-stu-id="cedc4-103">Handling Errors in COM+</span></span>

<span data-ttu-id="cedc4-104">La parte más problemática de la escritura de componentes consiste en tratar con posibles errores.</span><span class="sxs-lookup"><span data-stu-id="cedc4-104">The most problematic part of writing components is dealing with possible errors.</span></span> <span data-ttu-id="cedc4-105">Intentar determinar lo que puede ir mal y lo que debe hacer sobre él puede ser complicado en las mejores condiciones.</span><span class="sxs-lookup"><span data-stu-id="cedc4-105">Trying to determine what can go wrong and what to do about it can be challenging under the best conditions.</span></span> <span data-ttu-id="cedc4-106">Los errores comunes que el componente puede buscar y controlar son las conexiones de red con errores, los errores de seguridad y los errores asociados a los objetos inalcanzables.</span><span class="sxs-lookup"><span data-stu-id="cedc4-106">Common errors that your component might check for and handle are failed network connections, security errors, and failures associated with unreachable objects.</span></span>

<span data-ttu-id="cedc4-107">Además, puede desarrollar sus propios códigos de error para informar sobre errores específicos de la interfaz, como cuando se ha infringido una regla de negocios.</span><span class="sxs-lookup"><span data-stu-id="cedc4-107">Additionally, you can develop your own error codes to report interface-specific errors such as when a business rule has been violated.</span></span>

<span data-ttu-id="cedc4-108">En consonancia con el modelo de programación COM+, un objeto puede (y con frecuencia) llamar a métodos de interfaz en otros objetos para realizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="cedc4-108">In keeping with the COM+ programming model, an object can (and often does) call interface methods on other objects to perform work.</span></span> <span data-ttu-id="cedc4-109">Dado que los programadores pueden escribir componentes en diferentes lenguajes de programación, COM+ requiere que todos los mecanismos de control de errores sean independientes del idioma, por ejemplo: HRESULTs y colecciones [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="cedc4-109">Because programmers can write components in different programming languages, COM+ requires that all error-handling mechanisms be language-neutral, for example: HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span>

<span data-ttu-id="cedc4-110">En esta sección se incluyen temas, que se describen en la tabla siguiente, en los que se explican técnicas para controlar errores en aplicaciones COM+, características de COM+ que afectan al comportamiento de errores y sugerencias para diagnosticar errores de COM+.</span><span class="sxs-lookup"><span data-stu-id="cedc4-110">This section includes topics, described in the following table, that discuss techniques for handling errors in COM+ applications, features in COM+ that affect failure behavior, and suggestions for diagnosing COM+ errors.</span></span>



| <span data-ttu-id="cedc4-111">Tema</span><span class="sxs-lookup"><span data-stu-id="cedc4-111">Topic</span></span>                                                                                           | <span data-ttu-id="cedc4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cedc4-112">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cedc4-113">Estrategias para controlar errores en COM+</span><span class="sxs-lookup"><span data-stu-id="cedc4-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)<br/> | <span data-ttu-id="cedc4-114">Enumera y describe las directrices básicas para controlar los errores en COM+, incluido Cuándo usar valores HRESULT y colecciones de [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="cedc4-114">Lists and describes basic guidelines for handling errors in COM+, including when to use HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span><br/> |
| [<span data-ttu-id="cedc4-115">Cómo modifica COM+ los valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cedc4-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)<br/>               | <span data-ttu-id="cedc4-116">Identifica la única condición en la que COM+ convierte un valor HRESULT estándar en un código de error de COM+ antes de devolverlo al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="cedc4-116">Identifies the single condition in which COM+ converts a standard HRESULT to a COM+ error code before passing it back to the caller.</span></span><br/>             |
| [<span data-ttu-id="cedc4-117">Aislamiento de errores y Directiva FailFast</span><span class="sxs-lookup"><span data-stu-id="cedc4-117">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)<br/>       | <span data-ttu-id="cedc4-118">Muestra cómo el aislamiento de errores y la Directiva FailFast afectan al comportamiento de COM+.</span><span class="sxs-lookup"><span data-stu-id="cedc4-118">Shows how fault isolation and the failfast policy affect COM+ behavior.</span></span><br/>                                                                          |
| [<span data-ttu-id="cedc4-119">Buscar el origen de un error</span><span class="sxs-lookup"><span data-stu-id="cedc4-119">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)<br/>                 | <span data-ttu-id="cedc4-120">Describe cómo diagnosticar el origen y obtener una descripción de los errores de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cedc4-120">Describes how you can diagnose the source and obtain a description of application errors.</span></span> <br/>                                                       |
| [<span data-ttu-id="cedc4-121">Interpretar códigos de error</span><span class="sxs-lookup"><span data-stu-id="cedc4-121">Interpreting Error Codes</span></span>](interpreting-error-codes.md)<br/>                             | <span data-ttu-id="cedc4-122">Identifica el mecanismo de control de errores predominante para Microsoft Visual C++, el lenguaje Java y Visual Basic de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cedc4-122">Identifies the predominant error-handling mechanism for Microsoft Visual C++, the Java language, and Microsoft Visual Basic.</span></span> <br/>                    |
| [<span data-ttu-id="cedc4-123">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="cedc4-123">Troubleshooting</span></span>](troubleshooting.md)<br/>                                               | <span data-ttu-id="cedc4-124">Proporciona ayuda adicional para diagnosticar errores.</span><span class="sxs-lookup"><span data-stu-id="cedc4-124">Provides additional assistance in diagnosing errors.</span></span><br/>                                                                                             |
| [<span data-ttu-id="cedc4-125">Ponerse en contacto con soporte técnico</span><span class="sxs-lookup"><span data-stu-id="cedc4-125">Contacting Support</span></span>](contacting-support.md)<br/>                                         | <span data-ttu-id="cedc4-126">Identifica información importante sobre la solución de problemas que debe proporcionar al ponerse en contacto con el servicio de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="cedc4-126">Identifies important problem-solving information you should provide when contacting support.</span></span><br/>                                                     |



 

<span data-ttu-id="cedc4-127">Para obtener información detallada sobre el control de errores asociados a varios servicios COM+, vea las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="cedc4-127">For detailed information on handling errors associated with various COM+ services, see the following sections:</span></span>

-   [<span data-ttu-id="cedc4-128">Acelerar las transacciones mediante la notificación del objeto raíz</span><span class="sxs-lookup"><span data-stu-id="cedc4-128">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
-   <span data-ttu-id="cedc4-129">[Control de errores](handling-errors-in-queued-components.md) (para componentes en cola)</span><span class="sxs-lookup"><span data-stu-id="cedc4-129">[Handling Errors](handling-errors-in-queued-components.md) (for queued components)</span></span>

## <a name="related-topics"></a><span data-ttu-id="cedc4-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cedc4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cedc4-131">Depurar aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="cedc4-131">Debugging COM+ Applications</span></span>](debugging-com--applications.md)
</dt> </dl>

 

 




