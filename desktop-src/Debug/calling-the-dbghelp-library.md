---
description: Aunque DbgHelp.dll se incluye con todas las versiones de Windows, los autores de la llamada deben considerar el uso de una de las versiones más recientes de este archivo DLL, tal como se encuentra en el paquete de herramientas de depuración para Windows. Para obtener más información sobre la distribución de DbgHelp, consulte las versiones de DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Llamar a la biblioteca DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc06f6a0e28f163d80490647ee8f33754c249b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495815"
---
# <a name="calling-the-dbghelp-library"></a><span data-ttu-id="a225c-104">Llamar a la biblioteca DbgHelp</span><span class="sxs-lookup"><span data-stu-id="a225c-104">Calling the DbgHelp Library</span></span>

<span data-ttu-id="a225c-105">Aunque DbgHelp.dll se incluye con todas las versiones de Windows, los autores de la llamada deben considerar el uso de una de las versiones más recientes de este archivo DLL, tal como se encuentra en el paquete de [herramientas de depuración para Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="a225c-105">Although DbgHelp.dll ships with all versions of Windows, callers should consider using one of the more recent versions of this DLL as found in the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package.</span></span> <span data-ttu-id="a225c-106">Para obtener más información sobre la distribución de DbgHelp, consulte [las versiones de DbgHelp](dbghelp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a225c-106">For details on distribution of DbgHelp, see [DbgHelp Versions](dbghelp-versions.md).</span></span>

<span data-ttu-id="a225c-107">Cuando se usa DbgHelp, la mejor estrategia es instalar una copia de la biblioteca desde el paquete de [herramientas de depuración para Windows](https://www.microsoft.com/?ref=go) en el directorio de la aplicación, de forma lógica adyacente al software que lo llama.</span><span class="sxs-lookup"><span data-stu-id="a225c-107">When using DbgHelp, the best strategy is to install a copy of the library from the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package in the application directory logically adjacent to the software that calls it.</span></span> <span data-ttu-id="a225c-108">Si también se necesitan el servidor de símbolos y el servidor de origen, tanto SymSrv.dll como SrcSrv.dll deben instalarse en el mismo directorio que DbgHelp.dll, ya que DbgHelp solo llamará a estos archivos dll si comparten el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="a225c-108">If Symbol Server and Source Server are also needed, then both SymSrv.dll and SrcSrv.dll must be installed in the same directory as DbgHelp.dll, as DbgHelp will only call these DLLs if they share the same directory with it.</span></span> <span data-ttu-id="a225c-109">(Tenga en cuenta que DbgHelp no llamará a estos dos archivos dll desde la ruta de acceso de búsqueda estándar). Esto ayuda a evitar el uso de archivos dll no coincidentes. del mismo modo, también mejora la seguridad en general.</span><span class="sxs-lookup"><span data-stu-id="a225c-109">(Note that DbgHelp will not call these two DLLs from the standard search path.) This helps prevent the usage of mismatched DLLs; likewise, it also improves security overall.</span></span>

<span data-ttu-id="a225c-110">El código siguiente se extrae del origen de DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="a225c-110">The following code is extracted from the DbgHelp source.</span></span> <span data-ttu-id="a225c-111">Muestra cómo DbgHelp solo carga las versiones de SymSrv.dll y SrcSrv.dll desde el mismo directorio en el que reside DbgHelp.dll.</span><span class="sxs-lookup"><span data-stu-id="a225c-111">It shows how DbgHelp only loads versions of SymSrv.dll and SrcSrv.dll from the same directory that DbgHelp.dll resides in.</span></span>


```C++
HINSTANCE ghinst;

// For calculating the size of arrays for safe string functions.

#ifndef cch
 #define ccht(Array, EltType) (sizeof(Array) / sizeof(EltType))
 #define cch(Array) ccht(Array, (Array)[0])
#endif

//
// LoadLibrary() a DLL, using the same directory as dbghelp.dll.
//

HMODULE 
LoadDLL(
    __in PCWSTR filename
    )
{
    WCHAR drive[10] = L"";
    WCHAR dir[MAX_PATH + 1] = L"";
    WCHAR file[MAX_PATH + 1] = L"";
    WCHAR ext[MAX_PATH + 1] = L"";
    WCHAR path[MAX_PATH + 1] = L"";
    HMODULE hm;
    
    // Chop up 'filename' into its elements.
    
    _wsplitpath_s(filename, drive, cch(drive), dir, cch(dir), file, cch(file), ext, cch(ext));

    // If 'filename' contains no path information, then get the path to our module and 
    // use it to create a fully qualified path to the module we are loading.  Then load it.
    
    if (!*drive && !*dir) 
    {
        // ghinst is the HINSTANCE of this module, initialized in DllMain or WinMain
         
        if (GetModuleFileNameW(ghinst, path, MAX_PATH)) 
        {
            _wsplitpath_s(path, drive, cch(drive), dir, cch(dir), NULL, 0, NULL, 0);
            if (*drive || *dir) 
            {
                swprintf_s(path, cch(path), L"%s%s%s%s", drive, dir, file, ext);
                hm = LoadLibrary(path);
                if (hm)
                    return hm;
            }
        }
    }
    else
    {
        // If we wanted to, we could have LoadDLL also support directories being specified
        // in 'filename'.  We could pass the path here.  The result is if no path is specified,
        // the module path is used as above, otherwise the path in 'filename' is specified.
        // But the standard search logic of LoadLibrary is still avoided.
        
        /*
        hm = LoadLibrary(path);
        if (hm)
            return hm;
        */
    }
    
    return 0;
}
```



<span data-ttu-id="a225c-112">Después de cargar estos dos archivos dll, DbgHelp llama a [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener las funciones que necesita de ellos.</span><span class="sxs-lookup"><span data-stu-id="a225c-112">After loading these two DLLs, DbgHelp calls [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain the functions it needs from them.</span></span>

<span data-ttu-id="a225c-113">Normalmente, el código que llama a DbgHelp.dll garantiza que se cargue la versión correcta instalando DbgHelp.dll en el mismo directorio que la aplicación que inició el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="a225c-113">Normally, code that calls DbgHelp.dll ensures that the correct version is loaded by installing DbgHelp.dll in the same directory as the application that initiated the current process.</span></span> <span data-ttu-id="a225c-114">Si el código de llamada está en un archivo DLL y no tiene acceso a la ubicación del proceso inicial o lo conoce, se debe instalar DbgHelp.dll junto con el archivo DLL de llamada y se debe usar el código similar al LoadDLL de DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="a225c-114">If the calling code is in a DLL and does not have access to or knowledge of the location of the initial process, then DbgHelp.dll must be installed alongside the calling DLL and code similar to DbgHelp's LoadDLL should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a225c-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a225c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a225c-116">Versiones de DbgHelp</span><span class="sxs-lookup"><span data-stu-id="a225c-116">DbgHelp Versions</span></span>](dbghelp-versions.md)
</dt> <dt>

[<span data-ttu-id="a225c-117">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="a225c-117">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="a225c-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="a225c-118">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="a225c-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="a225c-119">**GetModuleFileName**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
