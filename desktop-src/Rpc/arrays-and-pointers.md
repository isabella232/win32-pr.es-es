---
title: Matrices y punteros
description: La llamada a procedimiento remoto (RPC) está diseñada para ser más transparente para los desarrolladores.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Llamada a procedimiento remoto RPC, descrito, matrices y punteros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776872"
---
# <a name="arrays-and-pointers"></a><span data-ttu-id="77945-104">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="77945-104">Arrays and Pointers</span></span>

<span data-ttu-id="77945-105">La llamada a procedimiento remoto (RPC) está diseñada para ser más transparente para los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="77945-105">Remote Procedure Call (RPC) is designed to be mostly transparent to developers.</span></span> <span data-ttu-id="77945-106">Para lograr esta transparencia, el código auxiliar del cliente se transmite al servidor tanto el puntero como el objeto de datos al que señala.</span><span class="sxs-lookup"><span data-stu-id="77945-106">To achieve this transparency, the client stub transmits to the server both the pointer and the data object to which it points.</span></span> <span data-ttu-id="77945-107">Si el procedimiento remoto cambia los datos, el servidor debe devolver los datos nuevos al cliente para que el cliente pueda copiar los datos nuevos en los datos originales.</span><span class="sxs-lookup"><span data-stu-id="77945-107">If the remote procedure changes the data, the server must transmit the new data back to the client so that the client can copy the new data over the original data.</span></span>

<span data-ttu-id="77945-108">En general, una llamada a procedimiento remoto se comporta igual que una llamada a procedimiento local.</span><span class="sxs-lookup"><span data-stu-id="77945-108">In general, a remote procedure call behaves just like a local procedure call.</span></span> <span data-ttu-id="77945-109">Es decir, cuando un puntero es un parámetro, el procedimiento remoto puede tener acceso al objeto de datos al que hace referencia el puntero de la misma manera que un procedimiento local.</span><span class="sxs-lookup"><span data-stu-id="77945-109">That is, when a pointer is a parameter, the remote procedure can access the data object the pointer refers to in the same way that a local procedure can.</span></span>

<span data-ttu-id="77945-110">Dado que los programas de cliente y servidor se ejecutan en espacios de direcciones diferentes, los programadores deben usar los atributos Lenguaje de definición de interfaz de Microsoft (MIDL) para describir cómo se transmiten los datos de puntero y matriz entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="77945-110">Since client and server programs run in different address spaces, developers must use Microsoft Interface Definition Language (MIDL) attributes to describe how array and pointer data is transmitted between the client and the server.</span></span> <span data-ttu-id="77945-111">En esta sección se ofrece información general sobre cómo usar matrices y punteros en aplicaciones distribuidas, en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="77945-111">This section presents an overview of how to use arrays and pointers in distributed applications, in the following topics:</span></span>

-   [<span data-ttu-id="77945-112">Matrices y RPC</span><span class="sxs-lookup"><span data-stu-id="77945-112">Arrays and RPC</span></span>](arrays-and-rpc.md)
-   [<span data-ttu-id="77945-113">Punteros y RPC</span><span class="sxs-lookup"><span data-stu-id="77945-113">Pointers and RPC</span></span>](pointers-and-rpc.md)
-   [<span data-ttu-id="77945-114">Usar matrices, cadenas y punteros</span><span class="sxs-lookup"><span data-stu-id="77945-114">Using Arrays, Strings, and Pointers</span></span>](using-arrays-strings-and-pointers.md)

 

 




