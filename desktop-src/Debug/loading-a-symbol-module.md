---
description: Si una aplicación no llama a la función SymInitialize con el parámetro fInvadeProcess establecido en TRUE, debe cargar los símbolos para un módulo cuando sea necesario.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Cargar un módulo de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152820"
---
# <a name="loading-a-symbol-module"></a><span data-ttu-id="998ae-103">Cargar un módulo de símbolos</span><span class="sxs-lookup"><span data-stu-id="998ae-103">Loading a Symbol Module</span></span>

<span data-ttu-id="998ae-104">Si una aplicación no llama a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con el parámetro *FInvadeProcess* establecido en **true**, debe cargar los símbolos para un módulo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="998ae-104">If an application does not call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function with the *fInvadeProcess* parameter set to **TRUE**, it must load symbols for a module when they are required.</span></span> <span data-ttu-id="998ae-105">Para cargar un módulo de símbolos a petición, la aplicación puede llamar a la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) con una ruta de acceso completa a un nombre de módulo.</span><span class="sxs-lookup"><span data-stu-id="998ae-105">To load a symbol module on demand, the application can call the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function with a full path to a module name.</span></span> <span data-ttu-id="998ae-106">Cuando se carga el módulo, el controlador de símbolos cargará los símbolos inmediatamente o aplazará la carga, dependiendo de las opciones establecidas mediante la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="998ae-106">When the module is loaded, the symbol handler will either load the symbols immediately or defer the load, depending on the options set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span>

<span data-ttu-id="998ae-107">En el código siguiente se carga un módulo de símbolos.</span><span class="sxs-lookup"><span data-stu-id="998ae-107">The following code loads a symbol module.</span></span> <span data-ttu-id="998ae-108">Tenga en cuenta que se supone que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="998ae-108">Note that it assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



<span data-ttu-id="998ae-109">Tenga en cuenta que *szImageName* puede ser una ruta de acceso a cualquier módulo ejecutable que tenga información de depuración (. exe,. dll,. drv,. sys,. SCR,. cpl,. com).</span><span class="sxs-lookup"><span data-stu-id="998ae-109">Note that *szImageName* can be a path to any executable module that has debugging information (.exe, .dll, .drv, .sys, .scr, .cpl, .com).</span></span> <span data-ttu-id="998ae-110">Además, *dwBaseAddr* es la dirección base del módulo de símbolos que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="998ae-110">Also, *dwBaseAddr* is the base address of the symbol module to be loaded.</span></span> <span data-ttu-id="998ae-111">Si este valor es 0, el controlador de símbolos obtendrá la dirección base del módulo de símbolos especificado.</span><span class="sxs-lookup"><span data-stu-id="998ae-111">If this value is 0, the symbol handler will obtain the base address from the specified symbol module.</span></span>

## <a name="related-topics"></a><span data-ttu-id="998ae-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="998ae-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="998ae-113">Descargar un módulo de símbolos</span><span class="sxs-lookup"><span data-stu-id="998ae-113">Unloading a Symbol Module</span></span>](unloading-a-symbol-module.md)
</dt> </dl>

 

 



