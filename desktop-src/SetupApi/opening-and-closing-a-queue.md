---
description: Antes de poder poner en cola las operaciones de archivo, debe abrir una cola de archivos. La llamada a la función SetupOpenFileQueue devuelve un identificador a un archivo de cola. Este identificador lo usan las funciones de cola subsiguientes para hacer referencia a la cola abierta y agregarle operaciones o examinarla.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Abrir y cerrar una cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667989"
---
# <a name="opening-and-closing-a-queue"></a><span data-ttu-id="44582-105">Abrir y cerrar una cola</span><span class="sxs-lookup"><span data-stu-id="44582-105">Opening and Closing a Queue</span></span>

<span data-ttu-id="44582-106">Antes de poder poner en cola las operaciones de archivo, debe abrir una cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="44582-106">Before you can queue file operations, you must open a file queue.</span></span> <span data-ttu-id="44582-107">La llamada a la función [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) devuelve un identificador a un archivo de cola.</span><span class="sxs-lookup"><span data-stu-id="44582-107">Calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function returns a handle to a queue file.</span></span> <span data-ttu-id="44582-108">Este identificador lo usan las funciones de cola subsiguientes para hacer referencia a la cola abierta y agregarle operaciones o examinarla.</span><span class="sxs-lookup"><span data-stu-id="44582-108">This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.</span></span>

<span data-ttu-id="44582-109">Una vez que todas las operaciones de archivo especificadas se han puesto en cola y confirmado, debe llamar a la función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) para liberar los recursos asignados durante la llamada a [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="44582-109">After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span>

> [!Note]  
> <span data-ttu-id="44582-110">La función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) no confirma la cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="44582-110">The [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function does not commit the file queue.</span></span> <span data-ttu-id="44582-111">Las operaciones que no se confirman cuando se llama a **SetupCloseFileQueue** no se realizarán.</span><span class="sxs-lookup"><span data-stu-id="44582-111">Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.</span></span>

 

 

 



