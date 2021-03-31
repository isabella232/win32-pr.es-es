---
description: Un nombre de símbolo representativo incluye caracteres que distinguen el modo en que se ha declarado un símbolo público.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nombres de símbolos representativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495802"
---
# <a name="decorated-symbol-names"></a><span data-ttu-id="c49d8-103">Nombres de símbolos representativos</span><span class="sxs-lookup"><span data-stu-id="c49d8-103">Decorated Symbol Names</span></span>

<span data-ttu-id="c49d8-104">Un nombre de símbolo representativo incluye caracteres que distinguen el modo en que se ha declarado un símbolo público.</span><span class="sxs-lookup"><span data-stu-id="c49d8-104">A decorated symbol name includes characters that distinguish how a public symbol has been declared.</span></span> <span data-ttu-id="c49d8-105">En el caso de \_ \_ las funciones Stdcall, los nombres incluyen el carácter "@" y un número decimal que especifica el número de bytes en sus parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="c49d8-105">For \_\_stdcall functions, names include the "@" character and a decimal number that specifies the number of bytes in its function parameters.</span></span> <span data-ttu-id="c49d8-106">Por ejemplo, el nombre representativo de la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) es LoadLibrary@4 .</span><span class="sxs-lookup"><span data-stu-id="c49d8-106">For example, the decorated name of the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is LoadLibrary@4.</span></span> <span data-ttu-id="c49d8-107">En las funciones de C++, la decoración del nombre es más compleja y varía de un compilador a un compilador.</span><span class="sxs-lookup"><span data-stu-id="c49d8-107">For C++ functions the name decoration is more complex and varies from compiler to compiler.</span></span>

<span data-ttu-id="c49d8-108">Para recuperar el nombre de símbolo no representativo, utilice la función [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .</span><span class="sxs-lookup"><span data-stu-id="c49d8-108">To retrieve the undecorated symbol name, use the [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) function.</span></span> <span data-ttu-id="c49d8-109">Como alternativa, puede llamar a la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para solicitar que el controlador de símbolos presente siempre símbolos con nombres no representativos.</span><span class="sxs-lookup"><span data-stu-id="c49d8-109">Alternatively, you can call the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to request that the symbol handler always present symbols with undecorated names.</span></span> <span data-ttu-id="c49d8-110">Debe establecer esta opción antes de cargar los símbolos, ya que el controlador de símbolos crea las tablas de nombres de símbolos en el momento de la carga.</span><span class="sxs-lookup"><span data-stu-id="c49d8-110">You must set this option before loading the symbols because the symbol handler creates the symbol name tables at load time.</span></span>

 

 
