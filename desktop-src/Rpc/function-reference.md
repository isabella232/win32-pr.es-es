---
title: Referencia de funciones
description: En esta sección se documentan las funciones de tiempo de ejecución de llamada a procedimiento remoto (RPC) admitidas en Microsoft RPC.
ms.assetid: 135bef8d-1794-420e-a111-604d02dbcc06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163c68f56a483d3eb7f62596c4a3d78ba2b5774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486822"
---
# <a name="function-reference"></a><span data-ttu-id="23fc6-103">Referencia de funciones</span><span class="sxs-lookup"><span data-stu-id="23fc6-103">Function Reference</span></span>

<span data-ttu-id="23fc6-104">En esta sección se documentan las funciones de tiempo de ejecución de llamada a procedimiento remoto (RPC) admitidas en Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="23fc6-104">This section documents the Remote Procedure Call (RPC) run-time functions supported in Microsoft RPC.</span></span> <span data-ttu-id="23fc6-105">En esta sección se describe el propósito, la sintaxis, los parámetros de entrada y los valores devueltos de cada función.</span><span class="sxs-lookup"><span data-stu-id="23fc6-105">This section describes each function's purpose, syntax, input parameters, and return values.</span></span> <span data-ttu-id="23fc6-106">También se proporciona información adicional para ayudarle a usar las funciones RPC en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="23fc6-106">It also provides additional information to help you use RPC functions in an application.</span></span>

<span data-ttu-id="23fc6-107">Todos los punteros pasados a funciones RPC deben incluir el atributo **\_ \_ RPC \_ Far** .</span><span class="sxs-lookup"><span data-stu-id="23fc6-107">All pointers passed to RPC functions must include the **\_ \_RPC\_FAR** attribute.</span></span> <span data-ttu-id="23fc6-108">Por ejemplo, el **\_ \_ identificador \* de enlace RPC** del puntero se convierte en el identificador de enlace RPC el **\_ \_ punto \_ \_ \_ \*** y el **carácter \* \*** *ptr* pasa a ser un carácter RPC lejano **\_ \_ \_ \* \_ \_ RPC \_ \*** Far.</span><span class="sxs-lookup"><span data-stu-id="23fc6-108">For example, the pointer **RPC\_BINDING\_HANDLE \*** becomes **RPC\_BINDING\_HANDLE \_ \_RPC\_FAR \*** and **char \* \*** *Ptr* becomes **char \_ \_RPC\_FAR \* \_ \_RPC\_FAR \*** *Ptr*.</span></span>

<span data-ttu-id="23fc6-109">En esta sección se presentan las referencias de funciones de los siguientes grupos:</span><span class="sxs-lookup"><span data-stu-id="23fc6-109">This section presents the function references in the following groups:</span></span>

-   [<span data-ttu-id="23fc6-110">Funciones RPC</span><span class="sxs-lookup"><span data-stu-id="23fc6-110">RPC Functions</span></span>](rpc-functions.md)
-   [<span data-ttu-id="23fc6-111">Devolución de llamada RPC y funciones de notificación</span><span class="sxs-lookup"><span data-stu-id="23fc6-111">RPC Callback and Notification Functions</span></span>](rpc-callback-and-notification-functions.md)

 

 




