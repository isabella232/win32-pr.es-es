---
description: Compilar filtros de DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Compilar filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806452"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="e1813-103">Compilar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1813-103">Building DirectShow Filters</span></span>

<span data-ttu-id="e1813-104">Se recomiendan las clases base de DirectShow para implementar filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e1813-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="e1813-105">Para compilar con las clases base, realice los pasos siguientes, además de los pasos que se indican en [configuración del entorno de compilación](setting-up-the-build-environment.md):</span><span class="sxs-lookup"><span data-stu-id="e1813-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="e1813-106">Compile la biblioteca de clases base, que se encuentra en el directorio Samples \\ multimedia \\ DirectShow \\ BaseClasses, en el directorio raíz del SDK.</span><span class="sxs-lookup"><span data-stu-id="e1813-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="e1813-107">Hay dos versiones de la biblioteca: una versión comercial (Strmbase. lib) y una versión de depuración (Strmbasd. lib).</span><span class="sxs-lookup"><span data-stu-id="e1813-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="e1813-108">Incluya el archivo de encabezado streams. h.</span><span class="sxs-lookup"><span data-stu-id="e1813-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="e1813-109">Utilice la \_ \_ Convención de llamada Stdcall.</span><span class="sxs-lookup"><span data-stu-id="e1813-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="e1813-110">Use la biblioteca en tiempo de ejecución de C multiproceso (depuración o comercial, según corresponda).</span><span class="sxs-lookup"><span data-stu-id="e1813-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="e1813-111">Incluya un archivo de definición (. def) que exporte las funciones DLL.</span><span class="sxs-lookup"><span data-stu-id="e1813-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="e1813-112">El siguiente es un ejemplo de un archivo de definición.</span><span class="sxs-lookup"><span data-stu-id="e1813-112">The following is an example of a definition file.</span></span> <span data-ttu-id="e1813-113">Se supone que el archivo de salida se denomina MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="e1813-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="e1813-114">Vincule a los siguientes archivos lib.</span><span class="sxs-lookup"><span data-stu-id="e1813-114">Link to the following lib files.</span></span>

    |              |                                      |
    |--------------|--------------------------------------|
    | <span data-ttu-id="e1813-115">Depurar compilación</span><span class="sxs-lookup"><span data-stu-id="e1813-115">Debug Build</span></span>  | <span data-ttu-id="e1813-116">Strmbasd. lib, msvcrtd. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="e1813-116">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="e1813-117">Compilación comercial</span><span class="sxs-lookup"><span data-stu-id="e1813-117">Retail Build</span></span> | <span data-ttu-id="e1813-118">Strmbase. lib, msvcrt. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="e1813-118">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="e1813-119">Elija la opción "omitir bibliotecas predeterminadas" en la configuración del vinculador.</span><span class="sxs-lookup"><span data-stu-id="e1813-119">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="e1813-120">Declare el punto de entrada de DLL en el código fuente, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e1813-120">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="e1813-121">Versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="e1813-121">Previous Versions</span></span>

<span data-ttu-id="e1813-122">En el caso de las versiones de la biblioteca de clases base anteriores a DirectShow 9,0, también debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e1813-122">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="e1813-123">Para las compilaciones de depuración, defina la marca de preprocesador DEBUG.</span><span class="sxs-lookup"><span data-stu-id="e1813-123">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="e1813-124">Este paso no es necesario para la versión de la biblioteca de clases base que está disponible en DirectShow 9,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e1813-124">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1813-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1813-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1813-126">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1813-126">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="e1813-127">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1813-127">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



