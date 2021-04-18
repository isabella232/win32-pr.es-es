---
description: En esta sección se describen las consideraciones de portabilidad de Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Trasladar aplicaciones de socket a Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715115"
---
# <a name="porting-socket-applications-to-winsock"></a><span data-ttu-id="201b4-103">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="201b4-103">Porting Socket Applications to Winsock</span></span>

<span data-ttu-id="201b4-104">En esta sección se describen las consideraciones de portabilidad de Winsock.</span><span class="sxs-lookup"><span data-stu-id="201b4-104">This section describes Winsock porting considerations.</span></span>

<span data-ttu-id="201b4-105">Hay un número limitado de instancias en las que Windows Sockets se desvía del cumplimiento estricto de las convenciones de Berkeley, normalmente debido a las dificultades de implementación en el entorno de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="201b4-105">There are a limited number of instances where Windows Sockets has diverted from strict adherence to the Berkeley conventions, usually due to implementation difficulties in the Microsoft Windows environment.</span></span>

<span data-ttu-id="201b4-106">Cuando se produce una desviación de las convenciones de Berkeley en Windows Sockets, la desviación se indica específicamente y claramente.</span><span class="sxs-lookup"><span data-stu-id="201b4-106">When a deviation from Berkeley conventions occurs in Windows Sockets, the deviation is specifically and clearly noted.</span></span> <span data-ttu-id="201b4-107">Por ejemplo, si una función es específica de Windows Sockets, esa desviación se especifica con una frase en la descripción de la función similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="201b4-107">For example, if a function is specific to Windows Sockets, that deviation is specified with a phrase in the function description similar to the following:</span></span>

<span data-ttu-id="201b4-108">La función **\[ de nombre \] de función** es una extensión específica de Microsoft para la API de Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="201b4-108">The **\[function-name\]** function is a Microsoft-specific extension to the Windows Sockets 2 API.</span></span>

<span data-ttu-id="201b4-109">En esta sección se proporciona información sobre cómo migrar aplicaciones de sockets de UNIX Berkeley (BSD) a Winsock:</span><span class="sxs-lookup"><span data-stu-id="201b4-109">This section provides information about porting Berkeley (BSD) UNIX socket applications to Winsock:</span></span>

-   [<span data-ttu-id="201b4-110">Tipo de datos socket</span><span class="sxs-lookup"><span data-stu-id="201b4-110">Socket Data Type</span></span>](socket-data-type-2.md)
-   [<span data-ttu-id="201b4-111">Macros Select, FD \_ set y FD \_ XXX</span><span class="sxs-lookup"><span data-stu-id="201b4-111">Select, FD\_SET, and FD\_XXX Macros</span></span>](select-and-fd---2.md)
-   [<span data-ttu-id="201b4-112">Códigos de error: errno, h \_ errno y WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="201b4-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [<span data-ttu-id="201b4-113">Punteros</span><span class="sxs-lookup"><span data-stu-id="201b4-113">Pointers</span></span>](pointers-2.md)
-   [<span data-ttu-id="201b4-114">Funciones cuyo nombre ha cambiado</span><span class="sxs-lookup"><span data-stu-id="201b4-114">Renamed Functions</span></span>](renamed-functions-2.md)
-   [<span data-ttu-id="201b4-115">Número máximo de sockets admitidos</span><span class="sxs-lookup"><span data-stu-id="201b4-115">Maximum Number of Sockets Supported</span></span>](maximum-number-of-sockets-supported-2.md)
-   [<span data-ttu-id="201b4-116">Archivos de inclusión</span><span class="sxs-lookup"><span data-stu-id="201b4-116">Include Files</span></span>](include-files-2.md)
-   [<span data-ttu-id="201b4-117">Valores devueltos en un error de función</span><span class="sxs-lookup"><span data-stu-id="201b4-117">Return Values on Function Failure</span></span>](return-values-on-function-failure-2.md)
-   [<span data-ttu-id="201b4-118">Sockets sin formato</span><span class="sxs-lookup"><span data-stu-id="201b4-118">Raw Sockets</span></span>](service-provided-raw-sockets-2.md)
-   [<span data-ttu-id="201b4-119">Ordenación de bytes</span><span class="sxs-lookup"><span data-stu-id="201b4-119">Byte Ordering</span></span>](byte-ordering-2.md)
-   [<span data-ttu-id="201b4-120">Rutinas de conversión extendida Byte-Order</span><span class="sxs-lookup"><span data-stu-id="201b4-120">Extended Byte-Order Conversion Routines</span></span>](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a><span data-ttu-id="201b4-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="201b4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="201b4-122">Control de errores de Winsock</span><span class="sxs-lookup"><span data-stu-id="201b4-122">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="201b4-123">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="201b4-123">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="201b4-124">Códigos de error de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="201b4-124">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="201b4-125">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="201b4-125">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



