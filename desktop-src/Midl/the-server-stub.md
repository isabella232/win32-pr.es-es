---
title: El código auxiliar del servidor
description: El código auxiliar de servidor proporciona puntos de entrada suplentes en el servidor para cada una de las operaciones definidas en el archivo IDL de entrada.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL del compilador MIDL, MIDL y RPC MIDL, interfaces, código auxiliar de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076156"
---
# <a name="the-server-stub"></a><span data-ttu-id="0c446-104">El código auxiliar del servidor</span><span class="sxs-lookup"><span data-stu-id="0c446-104">The Server Stub</span></span>

<span data-ttu-id="0c446-105">El código auxiliar de servidor proporciona puntos de entrada suplentes en el servidor para cada una de las operaciones definidas en el archivo IDL de entrada.</span><span class="sxs-lookup"><span data-stu-id="0c446-105">The server stub provides surrogate entry points on the server for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="0c446-106">Cuando la biblioteca en tiempo de ejecución de RPC invoca una rutina de código auxiliar de servidor, realiza las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="0c446-106">When a server stub routine is invoked by the RPC run-time library, it performs the following functions:</span></span>

-   <span data-ttu-id="0c446-107">Anula las referencias de los argumentos de entrada (desempaqueta los argumentos de los formatos transmitidos).</span><span class="sxs-lookup"><span data-stu-id="0c446-107">Unmarshals input arguments (unpacks the arguments from their transmitted formats).</span></span>
-   <span data-ttu-id="0c446-108">Llama a la implementación real del procedimiento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="0c446-108">Calls the actual implementation of the procedure on the server.</span></span>
-   <span data-ttu-id="0c446-109">Calcula las referencias de los argumentos de salida (empaqueta los argumentos en los formularios transmitidos).</span><span class="sxs-lookup"><span data-stu-id="0c446-109">Marshals output arguments (packages the arguments into the transmitted forms).</span></span>

<span data-ttu-id="0c446-110">El compilador MIDL cambia [**/Server**](-server.md), [**/sstub**](-sstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="0c446-110">The MIDL compiler switches [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

 

 




