---
title: El estado de la canalización
description: En el servidor, el compilador MIDL crea una variable de estado que coordina los procedimientos de inserción, extracción y asignación.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149426"
---
# <a name="the-pipe-state"></a><span data-ttu-id="529e5-103">El estado de la canalización</span><span class="sxs-lookup"><span data-stu-id="529e5-103">The Pipe State</span></span>

<span data-ttu-id="529e5-104">En el servidor, el compilador MIDL crea una variable de *Estado* que coordina los procedimientos de inserción, extracción y asignación.</span><span class="sxs-lookup"><span data-stu-id="529e5-104">On the server, the MIDL compiler creates a *state* variable that coordinates push, pull, and alloc procedures.</span></span> <span data-ttu-id="529e5-105">En el lado del cliente, el desarrollador debe crear la variable de *Estado* .</span><span class="sxs-lookup"><span data-stu-id="529e5-105">On the client side, the developer must create the *state* variable.</span></span> <span data-ttu-id="529e5-106">Por lo tanto, la variable de *Estado* es local en ambos lados, es decir, cada cliente y servidor mantienen su propio estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="529e5-106">Therefore, the *state* variable is local to both sides—that is, the client and server each maintain their own pipe state.</span></span> <span data-ttu-id="529e5-107">El código auxiliar del servidor mantiene la variable de estado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="529e5-107">The server stub code maintains the state variable on the server.</span></span> <span data-ttu-id="529e5-108">No debe intentar modificar su contenido directamente.</span><span class="sxs-lookup"><span data-stu-id="529e5-108">You should not attempt to modify its contents directly.</span></span> <span data-ttu-id="529e5-109">El cliente debe inicializar los campos de la estructura de control de canalización y mantener su variable de *Estado* .</span><span class="sxs-lookup"><span data-stu-id="529e5-109">The client must initialize the fields in the pipe control structure and maintain its *state* variable.</span></span> <span data-ttu-id="529e5-110">Utiliza la variable de *Estado* para identificar dónde ubicar o colocar los datos.</span><span class="sxs-lookup"><span data-stu-id="529e5-110">It uses the *state* variable to identify where to locate or place data.</span></span>

<span data-ttu-id="529e5-111">La variable de *Estado* de cliente puede ser tan simple como un identificador de archivo, si va a transferir datos de un archivo a otro.</span><span class="sxs-lookup"><span data-stu-id="529e5-111">The client *state* variable can be as simple as a file handle, if you are transferring data from one file to another.</span></span> <span data-ttu-id="529e5-112">También puede ser un entero que apunte a un elemento de una matriz.</span><span class="sxs-lookup"><span data-stu-id="529e5-112">It can also be an integer that points to an element in an array.</span></span> <span data-ttu-id="529e5-113">O bien, puede definir una estructura de estado bastante compleja para realizar tareas adicionales, como coordinar las rutinas de inserción y extracción en un \[ parámetro [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="529e5-113">Or you can define a fairly complex state structure to perform additional tasks, such as coordinating the push and pull routines on an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl)\] parameter.</span></span>

 

 