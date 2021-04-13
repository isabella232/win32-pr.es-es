---
description: Dado que los sockets no están representados por el entero de estilo UNIX, pequeño y no negativo, se ha cambiado la implementación de la función SELECT en Windows Sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Macros Select, FD_SET y FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544862"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a><span data-ttu-id="fdf44-103">Macros Select, FD \_ set y FD \_ XXX</span><span class="sxs-lookup"><span data-stu-id="fdf44-103">Select, FD\_SET, and FD\_XXX Macros</span></span>

<span data-ttu-id="fdf44-104">Dado que los sockets no están representados por el entero de estilo UNIX, pequeño y no negativo, se ha cambiado la implementación de la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) en Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="fdf44-104">Since sockets are not represented by the UNIX-style, small, non-negative integer, the implementation of the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was changed in Windows Sockets.</span></span> <span data-ttu-id="fdf44-105">Cada conjunto de sockets todavía se representa mediante la estructura del **\_ conjunto FD** , pero en lugar de almacenarse como una máscara de máscara, el conjunto se implementa como una matriz de Sockets.</span><span class="sxs-lookup"><span data-stu-id="fdf44-105">Each set of sockets is still represented by the **FD\_SET** structure, but instead of being stored as a bitmask, the set is implemented as an array of sockets.</span></span> <span data-ttu-id="fdf44-106">Para evitar posibles problemas, las aplicaciones deben cumplir el uso de las \_ macros FD XXX para establecer, inicializar, borrar y comprobar las estructuras [**de \_ conjuntos FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .</span><span class="sxs-lookup"><span data-stu-id="fdf44-106">To avoid potential problems, applications must adhere to the use of the FD\_XXX macros to set, initialize, clear, and check the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdf44-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fdf44-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf44-108">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="fdf44-108">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="fdf44-109">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="fdf44-109">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



