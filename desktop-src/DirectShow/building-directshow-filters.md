---
description: Creación de DirectShow filtros
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Creación de DirectShow filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d1983d3bfd42d1a1582ef696b6793acdd0856dde2bd2d589e809acc614314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794334"
---
# <a name="building-directshow-filters"></a>Creación de DirectShow filtros

Las DirectShow base se recomiendan para implementar DirectShow filtros. Para compilar con las clases base, realice los pasos siguientes, además de los pasos enumerados en [Configuración del entorno de compilación](setting-up-the-build-environment.md):

-   Compile la biblioteca de clases base, ubicada en el directorio Ejemplos \\ \\ multimedia DirectShow \\ BaseClasses, en el directorio raíz del SDK. Hay dos versiones de la biblioteca: una versión comercial (Strmbase.lib) y una versión de depuración (Strmbasd.lib).
-   Incluya el archivo de encabezado Secuencias.h.
-   Use la \_ \_ convención de llamada stdcall.
-   Use la biblioteca en tiempo de ejecución de C multiproceso (depuración o venta al por menor, según corresponda).
-   Incluya un archivo de definición (.def) que exporte las funciones DLL. A continuación se muestra un ejemplo de un archivo de definición. Se supone que el archivo de salida se denomina MyFilter.dll.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Vínculo a los siguientes archivos lib.

| Etiqueta | Value |
    |--------------|--------------------------------------|
    | Compilación de depuración  | Strmbasd.lib, Msvcrtd.lib, Winmm.lib |
    | Retail Build | Strmbase.lib, Msvcrt.lib, Winmm.lib  |

    

     

-   Elija la opción "Omitir bibliotecas predeterminadas" en la configuración del vinculador.
-   Declare el punto de entrada dll en el código fuente, como se muestra a continuación:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Versiones anteriores

Para las versiones de la biblioteca de clases base DirectShow 9.0, también debe hacer lo siguiente:

-   Para las compilaciones de depuración, defina la marca de preprocesador DEBUG.

Este paso no es necesario para la versión de la biblioteca de clases base que está disponible en DirectShow 9.0 y versiones posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



