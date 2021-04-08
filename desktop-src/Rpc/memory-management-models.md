---
title: Modelos de Memory-Management
description: Modelos de Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994611"
---
# <a name="memory-management-models"></a><span data-ttu-id="b433f-103">Modelos de Memory-Management</span><span class="sxs-lookup"><span data-stu-id="b433f-103">Memory-Management Models</span></span>

<span data-ttu-id="b433f-104">Como desarrollador, tiene varias opciones para la asignación y liberación de la memoria.</span><span class="sxs-lookup"><span data-stu-id="b433f-104">As a developer, you have several choices for how memory is allocated and freed.</span></span> <span data-ttu-id="b433f-105">Considere una estructura de datos compleja que consta de nodos conectados con punteros, como una lista vinculada o un árbol.</span><span class="sxs-lookup"><span data-stu-id="b433f-105">Consider a complex data structure that consists of nodes connected with pointers, such as a linked list or a tree.</span></span> <span data-ttu-id="b433f-106">Puede aplicar atributos que seleccionen uno de los siguientes modelos:</span><span class="sxs-lookup"><span data-stu-id="b433f-106">You can apply attributes that select one of the following models:</span></span>

-   <span data-ttu-id="b433f-107">[Asignación y desasignación de nodo por nodo](node-by-node-allocation-and-deallocation.md).</span><span class="sxs-lookup"><span data-stu-id="b433f-107">[Node-by-node allocation and deallocation](node-by-node-allocation-and-deallocation.md).</span></span>
-   <span data-ttu-id="b433f-108">[Un búfer lineal único asignado por el código auxiliar para todo el árbol](stub-allocated-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="b433f-108">[A single linear buffer allocated by the stub for the entire tree](stub-allocated-buffers.md).</span></span>
-   [<span data-ttu-id="b433f-109">Administración de memoria de código auxiliar de servidor</span><span class="sxs-lookup"><span data-stu-id="b433f-109">Server stub memory management</span></span>](server-stub-memory-management.md)
-   <span data-ttu-id="b433f-110">[Un búfer lineal único asignado por la aplicación cliente para todo el árbol](application-allocated-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="b433f-110">[A single linear buffer allocated by the client application for the entire tree](application-allocated-buffer.md).</span></span>
-   <span data-ttu-id="b433f-111">[Almacenamiento persistente en el servidor](persistent-storage-on-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="b433f-111">[Persistent storage on the server](persistent-storage-on-the-server.md).</span></span>

 

 




