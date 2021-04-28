---
title: Control de errores en COM (Introducción a Win32 y C++)
description: Control de errores en COM (Introducción a Win32 y C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103923"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>Control de errores en COM (Introducción a Win32 y C++)

COM usa **valores HRESULT** para indicar el éxito o error de una llamada de método o función. Varios encabezados sdk definen varias **constantes HRESULT.** En WinError.h se define un conjunto común de códigos para todo el sistema. En la tabla siguiente se muestran algunos de esos códigos de retorno de todo el sistema.



| Constante            | Valor numérico | Descripción                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ ACCESSDENIED** | 0x80070005    | Acceso denegado.                                       |
| **E \_ FAIL**         | 0x80004005    | Error no especificado.                                   |
| **E \_ INVALIDARG**   | 0x80070057    | Valor de parámetro no válido.                             |
| **E \_ OUTOFMEMORY**  | 0x8007000E    | Memoria insuficiente                                       |
| **PUNTERO \_ E**      | 0x80004003    | **Null** se pasó incorrectamente para un valor de puntero. |
| **E \_ UNEXPECTED**   | 0x8000FFFF    | Condición inesperada.                                |
| **S \_ OK**           | 0x0           | Correcto.                                             |
| **S \_ FALSE**        | 0x1           | Correcto.                                             |



 

Todas las constantes con el prefijo \_ "E" son códigos de error. Las constantes **S \_ OK y** S FALSE **\_ son** códigos de éxito. Es probable que el 99 % de los métodos COM **devuelvaN S \_ OK** cuando se realicen correctamente, pero no permita que este hecho le desconfie. Un método puede devolver otros códigos de operación correcta, por lo que siempre debe probar si hay errores mediante la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) o [**FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) En el código de ejemplo siguiente se muestra la manera incorrecta y la manera correcta de probar el éxito de una llamada de función.


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



El código de éxito **S \_ FALSE** merece mención. Algunos métodos **usan S \_ FALSE** para significar, aproximadamente, una condición negativa que no es un error. También puede indicar un "no-op": el método se ha hecho correctamente, pero no ha tenido ningún efecto. Por ejemplo, la [**función CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) devuelve **S \_ FALSE** si la llama una segunda vez desde el mismo subproceso. Si necesita diferenciar entre **S \_ OK** y **S \_ FALSE** en el código, debe probar el valor directamente, pero seguir utilizando [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) o [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) para controlar los casos restantes, como se muestra en el código de ejemplo siguiente.


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



Algunos **valores HRESULT** son específicos de una determinada característica o subsistema de Windows. Por ejemplo, la API de gráficos de Direct2D define el código de error **D2DERR \_ UNSUPPORTED \_ PIXEL \_ FORMAT**, lo que significa que el programa usó un formato de píxel no admitido. La documentación de MSDN a menudo proporciona una lista de códigos de error específicos que un método podría devolver. Sin embargo, no debe considerar estas listas como definitivas. Un método siempre puede devolver un **valor HRESULT** que no aparece en la documentación. De nuevo, use las macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) [**y FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) Si prueba un código de error específico, incluya también un caso predeterminado.


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a>Patrones para el control de errores

En esta sección se examinan algunos patrones para controlar los errores COM de forma estructurada. Cada patrón tiene ventajas y desventajas. Hasta cierto punto, la elección es una cuestión de buen gusto. Si trabaja en un proyecto existente, es posible que ya tenga directrices de codificación que proscriben un estilo determinado. Independientemente del patrón que adopte, el código sólido cumplirá las reglas siguientes.

-   Para cada método o función que devuelve un **valor HRESULT,** compruebe el valor devuelto antes de continuar.
-   Liberar recursos después de su uso.
-   No intente acceder a recursos no válidos o no inicializados, como punteros **NULL.**
-   No intente usar un recurso después de liberarlo.

Con estas reglas en mente, estos son cuatro patrones para controlar los errores.

-   [Ifs anidados](#nested-ifs)
-   [Ifs en cascada](#cascading-ifs)
-   [Salto al producir un error](#jump-on-fail)
-   [Iniciar al producir un error](#throw-on-fail)

### <a name="nested-ifs"></a>Ifs anidados

Después de cada llamada que devuelve **un valor HRESULT,** use una **instrucción if** para comprobar si la ejecución se ha hecho correctamente. A continuación, coloque la siguiente llamada al método dentro del ámbito de la **instrucción if.** Más **si las** instrucciones se pueden anidar tan profundamente como sea necesario. Los ejemplos de código anteriores de este módulo han usado este patrón, pero aquí es de nuevo:


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



Ventajas

-   Las variables se pueden declarar con un ámbito mínimo. Por ejemplo, *pItem* no se declara hasta que se usa.
-   Dentro de **cada instrucción if,** ciertas invariables son verdaderas: todas las llamadas anteriores se han hecho correctamente y todos los recursos adquiridos siguen siendo válidos. En el ejemplo anterior, cuando el programa alcanza la instrucción **if** más interna, se sabe que *tanto pItem* como *pFileOpen* son válidos.
-   Está claro cuándo liberar punteros de interfaz y otros recursos. Liberará un recurso al final de la **instrucción if** que sigue inmediatamente a la llamada que adquirió el recurso.

Inconvenientes

-   A algunas personas le resulta difícil leer el anidamiento profundo.
-   El control de errores se mezcla con otras instrucciones de bifurcación y bucle. Esto puede dificultar el seguimiento de la lógica general del programa.

### <a name="cascading-ifs"></a>Ifs en cascada

Después de cada llamada al método, use una **instrucción if** para comprobar si la ejecución se ha hecho correctamente. Si el método se realiza correctamente, coloque la siguiente llamada al método dentro del **bloque if.** Pero en lugar de anidar más **instrucciones if,** coloque cada prueba [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) posterior al bloque **if** anterior. Si se produce un error en cualquier método, todas las pruebas **SUCCEEDED** restantes simplemente producirán un error hasta que se alcance la parte inferior de la función.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



En este patrón, los recursos se liberan al final de la función. Si se produce un error, es posible que algunos punteros no sean válidos cuando se cierra la función. Llamar [**a Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en un puntero no válido bloqueará el programa (o peor), por lo que debe inicializar todos los punteros en **NULL** y comprobar si son **NULL** antes de liberarlos. En este ejemplo se `SafeRelease` usa la función ; los punteros inteligentes también son una buena opción.

Si usa este patrón, debe tener cuidado con las construcciones de bucle. Dentro de un bucle, se interrumpirá del bucle si se produce un error en alguna llamada.

Ventajas

-   Este patrón crea menos anidamiento que el patrón "ifs anidado".
-   El flujo de control general es más fácil de ver.
-   Los recursos se liberan en un punto del código.

Inconvenientes

-   Todas las variables se deben declarar e inicializar en la parte superior de la función.
-   Si se produce un error en una llamada, la función realiza varias comprobaciones de errores innecesarios, en lugar de salir inmediatamente de la función.
-   Dado que el flujo de control continúa a través de la función después de un error, debe tener cuidado en todo el cuerpo de la función para no tener acceso a recursos no válidos.
-   Los errores dentro de un bucle requieren un caso especial.

### <a name="jump-on-fail"></a>Salto al producir un error

Después de cada llamada de método, pruebe si hay errores (no correctos). En caso de error, vaya a una etiqueta cerca de la parte inferior de la función. Después de la etiqueta, pero antes de salir de la función, libere los recursos.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



Ventajas

-   El flujo de control general es fácil de ver.
-   En cada punto del código después de una comprobación FAILED, si no ha saltado [**a**](/windows/desktop/api/winerror/nf-winerror-failed) la etiqueta, se garantiza que todas las llamadas anteriores se han hecho correctamente.
-   Los recursos se liberan en un lugar del código.

Inconvenientes

-   Todas las variables se deben declarar e inicializar en la parte superior de la función.
-   A algunos programadores no les gusta usar **goto** en su código. (Sin embargo, debe tenerse en cuenta que este uso de **goto** está muy estructurado; el código nunca salta fuera de la llamada de función actual).
-   **Las instrucciones goto** omiten los inicializadores.

### <a name="throw-on-fail"></a>Iniciar al producir un error

En lugar de saltar a una etiqueta, puede producir una excepción cuando se produce un error en un método. Esto puede generar un estilo más idiomático de C++ si se usa para escribir código seguro para excepciones.


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



Observe que en este ejemplo se usa **la clase CComPtr** para administrar punteros de interfaz. Por lo general, si el código produce excepciones, debe seguir el patrón RAII (Adquisición de recursos es inicialización). Es decir, cada recurso debe administrarse mediante un objeto cuyo destructor garantiza que el recurso se libera correctamente. Si se produce una excepción, se garantiza que se invocará al destructor. De lo contrario, el programa podría filtrar recursos.

Ventajas

-   Compatible con el código existente que usa el control de excepciones.
-   Compatible con las bibliotecas de C++ que inician excepciones, como la Biblioteca de plantillas estándar (STL).

Inconvenientes

-   Requiere objetos de C++ para administrar recursos como identificadores de archivos o memoria.
-   Requiere una buena comprensión de cómo escribir código seguro para excepciones.

## <a name="next"></a>Siguientes

[Módulo 3. Gráficos de Windows](module-3---windows-graphics.md)

 

 
