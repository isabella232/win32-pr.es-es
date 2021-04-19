---
description: Aislamiento de errores y Directiva FailFast
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Aislamiento de errores y Directiva FailFast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538727"
---
# <a name="fault-isolation-and-failfast-policy"></a><span data-ttu-id="4955e-103">Aislamiento de errores y Directiva FailFast</span><span class="sxs-lookup"><span data-stu-id="4955e-103">Fault Isolation and Failfast Policy</span></span>

<span data-ttu-id="4955e-104">COM+ realiza comprobaciones de coherencia e integridad interna extensas.</span><span class="sxs-lookup"><span data-stu-id="4955e-104">COM+ performs extensive internal integrity and consistency checks.</span></span> <span data-ttu-id="4955e-105">Si COM+ encuentra una condición de error interno inesperada, finaliza inmediatamente el proceso.</span><span class="sxs-lookup"><span data-stu-id="4955e-105">If COM+ encounters an unexpected internal error condition, it immediately terminates the process.</span></span> <span data-ttu-id="4955e-106">Esta Directiva, denominada *FailFast*, facilita la contención de errores y da como resultado sistemas más confiables y sólidos.</span><span class="sxs-lookup"><span data-stu-id="4955e-106">This policy, called *failfast*, facilitates fault containment and results in more reliable and robust systems.</span></span>

<span data-ttu-id="4955e-107">Considere un caso en el que COM+ detecta que una de sus estructuras de datos está en un estado dañado.</span><span class="sxs-lookup"><span data-stu-id="4955e-107">Consider a case in which COM+ detects that one of its data structures is in a corrupted state.</span></span> <span data-ttu-id="4955e-108">En este momento, la causa y la magnitud de los daños son desconocidos y, desafortunadamente, COM+ no puede saber hasta qué punto se han distribuido los daños.</span><span class="sxs-lookup"><span data-stu-id="4955e-108">At this point, both the cause and the magnitude of the corruption are unknown and, unfortunately, COM+ cannot tell how far the damage has spread.</span></span> <span data-ttu-id="4955e-109">Sin embargo, aunque COM+ se encuentra en un estado indeterminado, no se ejecuta de forma aislada.</span><span class="sxs-lookup"><span data-stu-id="4955e-109">However, even though COM+ is in an indeterminate state, it does not run in isolation.</span></span> <span data-ttu-id="4955e-110">Al igual que otros archivos dll, se hospeda en un entorno de proceso y comparte un solo espacio de direcciones con el archivo ejecutable del programa principal y muchos otros archivos dll.</span><span class="sxs-lookup"><span data-stu-id="4955e-110">Like other DLLs, it is hosted in a process environment and shares a single address space with the main program executable and many other DLLs.</span></span> <span data-ttu-id="4955e-111">Por lo tanto, COM+ supone que se ha dañado todo el proceso y el proceso se termina inmediatamente para impedir que se propague información potencialmente dañada a otros procesos o, peor aún, que permita la confirmación y la permanencia de los datos dañados.</span><span class="sxs-lookup"><span data-stu-id="4955e-111">Therefore, COM+ assumes that the entire process has been corrupted, and the process is immediately terminated to prevent it from spreading potentially corrupted information to other processes or, worse yet, from allowing corrupted data to be committed and made durable.</span></span>

<span data-ttu-id="4955e-112">COM+ no permite que las excepciones se propaguen fuera de un contexto.</span><span class="sxs-lookup"><span data-stu-id="4955e-112">COM+ does not allow exceptions to propagate outside of a context.</span></span> <span data-ttu-id="4955e-113">Si se produce una excepción mientras se ejecuta dentro de un contexto de COM+ y la aplicación no detecta la excepción antes de volver del contexto, COM+ detecta la excepción y finaliza el proceso.</span><span class="sxs-lookup"><span data-stu-id="4955e-113">If an exception occurs while executing within a COM+ context and the application doesn't catch the exception before returning from the context, COM+ catches the exception and terminates the process.</span></span> <span data-ttu-id="4955e-114">En este caso, el uso de la Directiva FailFast se basa en la suposición de que la excepción ha puesto el proceso en un estado indeterminado. no es seguro continuar el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="4955e-114">Using the failfast policy in this case is based on the assumption that the exception has put the process into an indeterminate state; it is not safe to continue processing.</span></span>

<span data-ttu-id="4955e-115">Como desarrollador o administrador, debe inspeccionar el registro de la aplicación Visor de eventos para obtener más información sobre cualquier acción de FailFast o errores de aplicación graves.</span><span class="sxs-lookup"><span data-stu-id="4955e-115">As a developer or administrator, you should inspect the Event Viewer application log for details on any failfast action or serious application errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4955e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4955e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4955e-117">Buscar el origen de un error</span><span class="sxs-lookup"><span data-stu-id="4955e-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="4955e-118">Cómo modifica COM+ los valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4955e-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="4955e-119">Interpretar códigos de error</span><span class="sxs-lookup"><span data-stu-id="4955e-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="4955e-120">Estrategias para controlar errores en COM+</span><span class="sxs-lookup"><span data-stu-id="4955e-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="4955e-121">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="4955e-121">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



