---
description: La vinculación dinámica presenta las siguientes ventajas con respecto a la vinculación estática.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Ventajas de la vinculación dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667633"
---
# <a name="advantages-of-dynamic-linking"></a><span data-ttu-id="63a8b-103">Ventajas de la vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="63a8b-103">Advantages of Dynamic Linking</span></span>

<span data-ttu-id="63a8b-104">La vinculación dinámica presenta las siguientes ventajas con respecto a la vinculación estática:</span><span class="sxs-lookup"><span data-stu-id="63a8b-104">Dynamic linking has the following advantages over static linking:</span></span>

-   <span data-ttu-id="63a8b-105">Varios procesos que cargan el mismo archivo DLL en la misma dirección base comparten una única copia de la DLL en la memoria física.</span><span class="sxs-lookup"><span data-stu-id="63a8b-105">Multiple processes that load the same DLL at the same base address share a single copy of the DLL in physical memory.</span></span> <span data-ttu-id="63a8b-106">Esto ahorra memoria del sistema y reduce el intercambio.</span><span class="sxs-lookup"><span data-stu-id="63a8b-106">Doing this saves system memory and reduces swapping.</span></span>
-   <span data-ttu-id="63a8b-107">Cuando cambian las funciones de un archivo DLL, no es necesario volver a compilar o volver a vincular las aplicaciones que las usan, siempre y cuando no cambien los argumentos de la función, las convenciones de llamada y los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="63a8b-107">When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments, calling conventions, and return values do not change.</span></span> <span data-ttu-id="63a8b-108">En cambio, el código de un objeto vinculado estáticamente requiere que se vuelva a vincular la aplicación cuando cambien las funciones.</span><span class="sxs-lookup"><span data-stu-id="63a8b-108">In contrast, statically linked object code requires that the application be relinked when the functions change.</span></span>
-   <span data-ttu-id="63a8b-109">Un archivo DLL puede proporcionar soporte técnico después del mercado.</span><span class="sxs-lookup"><span data-stu-id="63a8b-109">A DLL can provide after-market support.</span></span> <span data-ttu-id="63a8b-110">Por ejemplo, se puede modificar una DLL de controlador de pantalla para que admita una pantalla que no estaba disponible cuando la aplicación se envió inicialmente.</span><span class="sxs-lookup"><span data-stu-id="63a8b-110">For example, a display driver DLL can be modified to support a display that was not available when the application was initially shipped.</span></span>
-   <span data-ttu-id="63a8b-111">Los programas escritos en lenguajes de programación diferentes pueden llamar a la misma función DLL siempre que los programas sigan la misma Convención de llamada que usa la función.</span><span class="sxs-lookup"><span data-stu-id="63a8b-111">Programs written in different programming languages can call the same DLL function as long as the programs follow the same calling convention that the function uses.</span></span> <span data-ttu-id="63a8b-112">La Convención de llamada (como C, Pascal o llamada estándar) controla el orden en el que la función de llamada debe introducir los argumentos en la pila, tanto si la función como la función de llamada es responsable de limpiar la pila y de si se pasan argumentos en los registros.</span><span class="sxs-lookup"><span data-stu-id="63a8b-112">The calling convention (such as C, Pascal, or standard call) controls the order in which the calling function must push the arguments onto the stack, whether the function or the calling function is responsible for cleaning up the stack, and whether any arguments are passed in registers.</span></span> <span data-ttu-id="63a8b-113">Para obtener más información, vea la documentación que se incluye con el compilador.</span><span class="sxs-lookup"><span data-stu-id="63a8b-113">For more information, see the documentation included with your compiler.</span></span>

<span data-ttu-id="63a8b-114">Una posible desventaja de utilizar archivos DLL es que la aplicación no es independiente; depende de la existencia de un módulo de archivo DLL separado.</span><span class="sxs-lookup"><span data-stu-id="63a8b-114">A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.</span></span> <span data-ttu-id="63a8b-115">El sistema termina los procesos mediante la vinculación dinámica en tiempo de carga si requieren un archivo DLL que no se encuentra en el inicio del proceso y proporciona un mensaje de error al usuario.</span><span class="sxs-lookup"><span data-stu-id="63a8b-115">The system terminates processes using load-time dynamic linking if they require a DLL that is not found at process startup and gives an error message to the user.</span></span> <span data-ttu-id="63a8b-116">El sistema no finaliza un proceso que usa la vinculación dinámica en tiempo de ejecución en esta situación, pero las funciones exportadas por el archivo DLL que faltan no están disponibles para el programa.</span><span class="sxs-lookup"><span data-stu-id="63a8b-116">The system does not terminate a process using run-time dynamic linking in this situation, but functions exported by the missing DLL are not available to the program.</span></span>

 

 



