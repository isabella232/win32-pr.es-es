---
title: El código auxiliar del cliente
description: El módulo de código auxiliar de cliente proporciona puntos de entrada suplentes en el cliente para cada una de las operaciones definidas en el archivo IDL de entrada.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL y RPC MIDL, interfaces, código auxiliar de cliente
- interfaces MIDL
- interfaces MIDL, MIDL y RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357447"
---
# <a name="the-client-stub"></a><span data-ttu-id="d2a5d-106">El código auxiliar del cliente</span><span class="sxs-lookup"><span data-stu-id="d2a5d-106">The Client Stub</span></span>

<span data-ttu-id="d2a5d-107">El módulo de código auxiliar de cliente proporciona puntos de entrada suplentes en el cliente para cada una de las operaciones definidas en el archivo IDL de entrada.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-107">The client stub module provides surrogate entry points on the client for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="d2a5d-108">Cuando la aplicación cliente realiza una llamada al procedimiento remoto, su llamada pasa primero a la rutina suplente en el archivo de código auxiliar de cliente.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-108">When the client application makes a call to the remote procedure, its call first goes to the surrogate routine in the client stub file.</span></span> <span data-ttu-id="d2a5d-109">La rutina de código auxiliar de cliente realiza las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="d2a5d-109">The client stub routine performs the following functions:</span></span>

-   <span data-ttu-id="d2a5d-110">Calcula las referencias de los argumentos.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-110">Marshals arguments.</span></span> <span data-ttu-id="d2a5d-111">El código auxiliar de cliente empaqueta los argumentos de entrada en un formulario que se puede transmitir al servidor.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-111">The client stub packages input arguments into a form that can be transmitted to the server.</span></span>
-   <span data-ttu-id="d2a5d-112">Llama a la biblioteca en tiempo de ejecución del cliente para transmitir argumentos al espacio de direcciones remoto e invoca el procedimiento remoto en el espacio de direcciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-112">Calls the client run-time library to transmit arguments to the remote address space and invokes the remote procedure in the server address space.</span></span>
-   <span data-ttu-id="d2a5d-113">Anula las referencias de los argumentos de salida.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-113">Unmarshals output arguments.</span></span> <span data-ttu-id="d2a5d-114">El código auxiliar del cliente desempaqueta los argumentos de salida y vuelve al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-114">The client stub unpacks output arguments and returns to the caller.</span></span>

<span data-ttu-id="d2a5d-115">El compilador MIDL cambia [**/Client**](-client.md), [**/cstub**](-cstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-115">The MIDL compiler switches [**/client**](-client.md), [**/cstub**](-cstub.md), and [**/out**](-out.md) affect the client stub file.</span></span>

 

 




