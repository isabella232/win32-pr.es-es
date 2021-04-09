---
description: En los temas siguientes se describen los archivos de símbolos y la funcionalidad proporcionada por las funciones DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Acerca de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152911"
---
# <a name="about-dbghelp"></a><span data-ttu-id="b5dda-103">Acerca de DbgHelp</span><span class="sxs-lookup"><span data-stu-id="b5dda-103">About DbgHelp</span></span>

<span data-ttu-id="b5dda-104">En los temas siguientes se describen los archivos de símbolos y la funcionalidad proporcionada por las [funciones DbgHelp](dbghelp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b5dda-104">The following topics describe symbol files and the functionality provided by the [DbgHelp functions](dbghelp-functions.md).</span></span>

-   [<span data-ttu-id="b5dda-105">Versiones de DbgHelp</span><span class="sxs-lookup"><span data-stu-id="b5dda-105">DbgHelp Versions</span></span>](dbghelp-versions.md)
-   [<span data-ttu-id="b5dda-106">Archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="b5dda-106">Symbol Files</span></span>](symbol-files.md)
-   [<span data-ttu-id="b5dda-107">Control de símbolos</span><span class="sxs-lookup"><span data-stu-id="b5dda-107">Symbol Handling</span></span>](symbol-handling.md)
-   [<span data-ttu-id="b5dda-108">Servidores de símbolos y almacenes de símbolos</span><span class="sxs-lookup"><span data-stu-id="b5dda-108">Symbol Servers and Symbol Stores</span></span>](symbol-servers-and-symbol-stores.md)
-   [<span data-ttu-id="b5dda-109">Archivos de minivolcado</span><span class="sxs-lookup"><span data-stu-id="b5dda-109">Minidump Files</span></span>](minidump-files.md)
-   [<span data-ttu-id="b5dda-110">Servidor de origen</span><span class="sxs-lookup"><span data-stu-id="b5dda-110">Source Server</span></span>](source-server-and-source-indexing.md)
-   [<span data-ttu-id="b5dda-111">Actualización de la compatibilidad para plataformas</span><span class="sxs-lookup"><span data-stu-id="b5dda-111">Updated Platform Support</span></span>](updated-platform-support.md)

<span data-ttu-id="b5dda-112">Tenga en cuenta que todas [las funciones DbgHelp](dbghelp-functions.md) tienen un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="b5dda-112">Note that all [DbgHelp functions](dbghelp-functions.md) are single threaded.</span></span> <span data-ttu-id="b5dda-113">Por lo tanto, las llamadas desde más de un subproceso a esta función probablemente producirán un comportamiento inesperado o daños en la memoria.</span><span class="sxs-lookup"><span data-stu-id="b5dda-113">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="b5dda-114">Para evitar esto, debe sincronizar todas las llamadas simultáneas de más de un subproceso a esta función.</span><span class="sxs-lookup"><span data-stu-id="b5dda-114">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

 

 



