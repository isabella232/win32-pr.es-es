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
# <a name="building-directshow-filters"></a>Compilar filtros de DirectShow

Se recomiendan las clases base de DirectShow para implementar filtros de DirectShow. Para compilar con las clases base, realice los pasos siguientes, además de los pasos que se indican en [configuración del entorno de compilación](setting-up-the-build-environment.md):

-   Compile la biblioteca de clases base, que se encuentra en el directorio Samples \\ multimedia \\ DirectShow \\ BaseClasses, en el directorio raíz del SDK. Hay dos versiones de la biblioteca: una versión comercial (Strmbase. lib) y una versión de depuración (Strmbasd. lib).
-   Incluya el archivo de encabezado streams. h.
-   Utilice la \_ \_ Convención de llamada Stdcall.
-   Use la biblioteca en tiempo de ejecución de C multiproceso (depuración o comercial, según corresponda).
-   Incluya un archivo de definición (. def) que exporte las funciones DLL. El siguiente es un ejemplo de un archivo de definición. Se supone que el archivo de salida se denomina MyFilter.dll.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Vincule a los siguientes archivos lib.

    |              |                                      |
    |--------------|--------------------------------------|
    | Depurar compilación  | Strmbasd. lib, msvcrtd. lib, winmm. lib |
    | Compilación comercial | Strmbase. lib, msvcrt. lib, winmm. lib  |

    

     

-   Elija la opción "omitir bibliotecas predeterminadas" en la configuración del vinculador.
-   Declare el punto de entrada de DLL en el código fuente, como se indica a continuación:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Versiones anteriores

En el caso de las versiones de la biblioteca de clases base anteriores a DirectShow 9,0, también debe hacer lo siguiente:

-   Para las compilaciones de depuración, defina la marca de preprocesador DEBUG.

Este paso no es necesario para la versión de la biblioteca de clases base que está disponible en DirectShow 9,0 y versiones posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



