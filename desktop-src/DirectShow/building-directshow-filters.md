---
description: Creación de filtros de DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Creación de filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7090eed702b1abe8ee863d5fa3ac9c1fd413690e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908623"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="63bae-103">Creación de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="63bae-103">Building DirectShow Filters</span></span>

<span data-ttu-id="63bae-104">Las clases base de DirectShow se recomiendan para implementar filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="63bae-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="63bae-105">Para compilar con las clases base, realice los pasos siguientes, además de los pasos enumerados en [Configuración del entorno de compilación](setting-up-the-build-environment.md):</span><span class="sxs-lookup"><span data-stu-id="63bae-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="63bae-106">Compile la biblioteca de clases base, ubicada en el directorio Samples \\ Multimedia \\ DirectShow \\ BaseClasses, en el directorio raíz del SDK.</span><span class="sxs-lookup"><span data-stu-id="63bae-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="63bae-107">Hay dos versiones de la biblioteca: una versión comercial (Strmbase.lib) y una versión de depuración (Strmbasd.lib).</span><span class="sxs-lookup"><span data-stu-id="63bae-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="63bae-108">Incluya el archivo de encabezado Streams.h.</span><span class="sxs-lookup"><span data-stu-id="63bae-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="63bae-109">Use la \_ \_ convención de llamada stdcall.</span><span class="sxs-lookup"><span data-stu-id="63bae-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="63bae-110">Use la biblioteca en tiempo de ejecución de C multiproceso (depuración o venta al por menor, según corresponda).</span><span class="sxs-lookup"><span data-stu-id="63bae-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="63bae-111">Incluya un archivo de definición (.def) que exporte las funciones DLL.</span><span class="sxs-lookup"><span data-stu-id="63bae-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="63bae-112">A continuación se muestra un ejemplo de un archivo de definición.</span><span class="sxs-lookup"><span data-stu-id="63bae-112">The following is an example of a definition file.</span></span> <span data-ttu-id="63bae-113">Se supone que el archivo de salida se denomina MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="63bae-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="63bae-114">Vínculo a los siguientes archivos lib.</span><span class="sxs-lookup"><span data-stu-id="63bae-114">Link to the following lib files.</span></span>

| <span data-ttu-id="63bae-115">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="63bae-115">Label</span></span> | <span data-ttu-id="63bae-116">Value</span><span class="sxs-lookup"><span data-stu-id="63bae-116">Value</span></span> |
    |--------------|--------------------------------------|
    | <span data-ttu-id="63bae-117">Compilación de depuración</span><span class="sxs-lookup"><span data-stu-id="63bae-117">Debug Build</span></span>  | <span data-ttu-id="63bae-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span><span class="sxs-lookup"><span data-stu-id="63bae-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="63bae-119">Compilación de venta al por menor</span><span class="sxs-lookup"><span data-stu-id="63bae-119">Retail Build</span></span> | <span data-ttu-id="63bae-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span><span class="sxs-lookup"><span data-stu-id="63bae-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="63bae-121">Elija la opción "Omitir bibliotecas predeterminadas" en la configuración del vinculador.</span><span class="sxs-lookup"><span data-stu-id="63bae-121">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="63bae-122">Declare el punto de entrada de DLL en el código fuente, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="63bae-122">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="63bae-123">Versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="63bae-123">Previous Versions</span></span>

<span data-ttu-id="63bae-124">Para las versiones de la biblioteca de clases base anteriores a DirectShow 9.0, también debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="63bae-124">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="63bae-125">Para las compilaciones de depuración, defina la marca de preprocesador DEBUG.</span><span class="sxs-lookup"><span data-stu-id="63bae-125">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="63bae-126">Este paso no es necesario para la versión de la biblioteca de clases base que está disponible en DirectShow 9.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="63bae-126">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63bae-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63bae-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63bae-128">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="63bae-128">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="63bae-129">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="63bae-129">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



