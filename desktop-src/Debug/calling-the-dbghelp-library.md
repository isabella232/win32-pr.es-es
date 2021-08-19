---
description: Aunque DbgHelp.dll se incluye con todas las versiones de Windows, los autores de la llamada deben considerar el uso de una de las versiones más recientes de este archivo DLL, como se encuentra en el paquete Debugging Tools For Windows . Para más información sobre la distribución de DbgHelp, consulte Versiones de DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Llamada a la biblioteca DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d6a111da8b0874a0c66fa08840e1ea4edeabf539afab2e9decf0eb19372db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957164"
---
# <a name="calling-the-dbghelp-library"></a>Llamada a la biblioteca DbgHelp

Aunque DbgHelp.dll se incluye con todas las versiones de Windows, los autores de la llamada deben considerar la posibilidad de usar una de las versiones más recientes de este archivo DLL, como se encuentra en el paquete [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) . Para obtener más información sobre la distribución de DbgHelp, vea [Versiones de DbgHelp.](dbghelp-versions.md)

Cuando se usa DbgHelp, la mejor estrategia es instalar una copia de la biblioteca desde el paquete Herramientas de depuración para Windows en el directorio de la aplicación adyacente lógicamente [al](https://www.microsoft.com/?ref=go) software que la llama. Si también se necesitan servidor de símbolos y servidor de origen, tanto SymSrv.dll como SrcSrv.dll deben instalarse en el mismo directorio que DbgHelp.dll, ya que DbgHelp solo llamará a estos archivos DLL si comparten el mismo directorio con él. (Tenga en cuenta que DbgHelp no llamará a estos dos archivos DLL desde la ruta de acceso de búsqueda estándar). Esto ayuda a evitar el uso de archivos DLL no coincidentes; Del mismo modo, también mejora la seguridad general.

El código siguiente se extrae del origen DbgHelp. Muestra cómo DbgHelp solo carga versiones de SymSrv.dll y SrcSrv.dll desde el mismo directorio en el que DbgHelp.dll reside.


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



Después de cargar estos dos archivos DLL, DbgHelp llama a [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener las funciones que necesita de ellos.

Normalmente, el código que llama a DbgHelp.dll garantiza que se carga la versión correcta instalando DbgHelp.dll en el mismo directorio que la aplicación que inició el proceso actual. Si el código de llamada está en un archivo DLL y no tiene acceso ni conocimiento de la ubicación del proceso inicial, se debe instalar DbgHelp.dll junto con el archivo DLL que realiza la llamada y se debe usar un código similar al LoadDLL de DbgHelp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones de DbgHelp](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
