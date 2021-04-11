---
description: La configuración correcta de los símbolos para la depuración puede ser una tarea desafiante, especialmente para la depuración del kernel.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Servidor de símbolos y almacenes de símbolos"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274909"
---
# <a name="symbol-server-and-symbol-stores"></a><span data-ttu-id="20657-103">  Servidor de símbolos y almacenes de símbolos</span><span class="sxs-lookup"><span data-stu-id="20657-103">Symbol Server and Symbol Stores</span></span>

<span data-ttu-id="20657-104">La configuración correcta de los símbolos para la depuración puede ser una tarea desafiante, especialmente para la depuración del kernel.</span><span class="sxs-lookup"><span data-stu-id="20657-104">Setting up symbols correctly for debugging can be a challenging task, particularly for kernel debugging.</span></span> <span data-ttu-id="20657-105">A menudo, es necesario conocer los nombres y las versiones de todos los productos del equipo.</span><span class="sxs-lookup"><span data-stu-id="20657-105">It often requires that you know the names and releases of all products on your computer.</span></span> <span data-ttu-id="20657-106">El depurador debe ser capaz de encontrar los archivos de símbolos que corresponden a cada versión de producto y Service Pack.</span><span class="sxs-lookup"><span data-stu-id="20657-106">The debugger must be able to locate the symbol files that correspond to each product release and service pack.</span></span> <span data-ttu-id="20657-107">Esto puede dar lugar a una ruta de acceso de símbolos extremadamente larga formada por una larga lista de directorios.</span><span class="sxs-lookup"><span data-stu-id="20657-107">This can result in an extremely long symbol path consisting of a long list of directories.</span></span>

<span data-ttu-id="20657-108">Para simplificar estas dificultades en la coordinación de archivos de símbolos, use el *servidor de símbolos*.</span><span class="sxs-lookup"><span data-stu-id="20657-108">To simplify these difficulties in coordinating symbol files, use the *symbol server*.</span></span> <span data-ttu-id="20657-109">El servidor de símbolos permite que los depuradores recuperen automáticamente los archivos de símbolos correctos sin los nombres de producto, las versiones o los números de compilación.</span><span class="sxs-lookup"><span data-stu-id="20657-109">The symbol server enables the debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="20657-110">Herramientas de depuración para Windows contiene el servidor de símbolos SymSrv.</span><span class="sxs-lookup"><span data-stu-id="20657-110">Debugging Tools for Windows contains the SymSrv symbol server.</span></span>

<span data-ttu-id="20657-111">El servidor de símbolos se activa mediante la inclusión de una cadena de texto determinada en la ruta de acceso de símbolos.</span><span class="sxs-lookup"><span data-stu-id="20657-111">The symbol server is activated by including a certain text string in the symbol path.</span></span> <span data-ttu-id="20657-112">Cada vez que el depurador necesita cargar símbolos para un módulo recién cargado, llama al servidor de símbolos para buscar los archivos de símbolos adecuados.</span><span class="sxs-lookup"><span data-stu-id="20657-112">Each time the debugger needs to load symbols for a newly loaded module, it calls the symbol server to locate the appropriate symbol files.</span></span> <span data-ttu-id="20657-113">El servidor de símbolos ubica los archivos en un *almacén de símbolos*.</span><span class="sxs-lookup"><span data-stu-id="20657-113">The symbol server locates the files in a *symbol store*.</span></span> <span data-ttu-id="20657-114">Se trata de una colección de archivos de símbolos, un índice y una herramienta que un administrador puede usar para agregar y eliminar archivos.</span><span class="sxs-lookup"><span data-stu-id="20657-114">This is a collection of symbol files, an index, and a tool that can be used by an administrator to add and delete files.</span></span> <span data-ttu-id="20657-115">Los archivos se indexan según parámetros únicos, como la marca de tiempo y el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="20657-115">The files are indexed according to unique parameters such as the time stamp and image size.</span></span> <span data-ttu-id="20657-116">Herramientas de depuración para Windows contiene una herramienta de almacén de símbolos denominada SymStore.</span><span class="sxs-lookup"><span data-stu-id="20657-116">Debugging Tools for Windows contains a symbol store tool called SymStore.</span></span>

<span data-ttu-id="20657-117">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="20657-117">For more information, see:</span></span>

-   [<span data-ttu-id="20657-118">Usar SymSrv</span><span class="sxs-lookup"><span data-stu-id="20657-118">Using SymSrv</span></span>](using-symsrv.md)
-   [<span data-ttu-id="20657-119">Usar SymStore</span><span class="sxs-lookup"><span data-stu-id="20657-119">Using SymStore</span></span>](using-symstore.md)
-   [<span data-ttu-id="20657-120">Usar otros almacenes de símbolos</span><span class="sxs-lookup"><span data-stu-id="20657-120">Using Other Symbol Stores</span></span>](using-other-symbol-stores.md)
-   [<span data-ttu-id="20657-121">Opciones de Command-Line de SymStore</span><span class="sxs-lookup"><span data-stu-id="20657-121">SymStore Command-Line Options</span></span>](symstore-command-line-options.md)
-   [<span data-ttu-id="20657-122">Servidor de símbolos y firewalls de Internet</span><span class="sxs-lookup"><span data-stu-id="20657-122">Symbol Server and Internet Firewalls</span></span>](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a><span data-ttu-id="20657-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20657-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20657-124">Archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="20657-124">Symbol Files</span></span>](symbol-files.md)
</dt> </dl>

 

 



