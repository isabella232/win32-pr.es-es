---
title: Control de errores en COM (introducción a Win32 y C++)
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685810"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>Control de errores en COM (introducción a Win32 y C++)

COM utiliza valores **HRESULT** para indicar si la llamada a un método o una función se ha realizado correctamente o no. Varios encabezados de SDK definen varias constantes de **HRESULT** . En WinError. h se define un conjunto común de códigos para todo el sistema. En la tabla siguiente se muestran algunos de los códigos de retorno para todo el sistema.



| Constante            | Valor numérico | Descripción                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ ACCESSDENIED** | 0x80070005    | Acceso denegado.                                       |
| **E \_ FAIL**         | 0x80004005    | Error no especificado.                                   |
| **E \_ INVALIDARG**   | 0x80070057    | Valor de parámetro no válido.                             |
| **E \_ OUTOFMEMORY**  | 0x8007000E    | Memoria insuficiente                                       |
| **\_puntero E**      | 0x80004003    | Se pasó incorrectamente **null** para un valor de puntero. |
| **E \_ inesperado**   | 0x8000FFFF    | Condición inesperada.                                |
| **S \_ correcto**           | 0x0           | Correcto.                                             |
| **S \_ false**        | 0x1           | Correcto.                                             |



 

Todas las constantes con el prefijo "E \_ " son códigos de error. Las constantes **S \_ OK** y **s \_ false** son códigos correctos. Probablemente, el 99% de los métodos COM devuelven los elementos **\_ correctos** cuando se ejecutan correctamente, pero no le informan de este hecho. Un método puede devolver otros códigos correctos, por lo que siempre se comprueba si hay errores mediante la macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) o [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) . En el ejemplo de código siguiente se muestra la manera equivocada y la manera correcta de comprobar si la llamada a una función se ha realizado correctamente.


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



El código de operación correcta **S \_ false** merece mención. Algunos métodos usan **S \_ false** para indicar, aproximadamente, una condición negativa que no es un error. También puede indicar un "no operativo": el método se realizó correctamente, pero no tenía ningún efecto. Por ejemplo, la función [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) devuelve **S \_ false** si se llama por segunda vez desde el mismo subproceso. Si necesita diferenciar entre **s \_ OK** y **s \_ false** en el código, debe probar el valor directamente, pero seguir usando [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) o [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) para administrar los casos restantes, tal como se muestra en el código de ejemplo siguiente.


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



Algunos valores **HRESULT** son específicos de una determinada característica o subsistema de Windows. Por ejemplo, la API de gráficos de Direct2D define el código de error **D2DERR \_ \_ \_ formato de píxel no admitido**, lo que significa que el programa usó un formato de píxel no admitido. La documentación de MSDN suele proporcionar una lista de códigos de error específicos que un método puede devolver. Sin embargo, no debe considerar que estas listas sean definitivas. Un método siempre puede devolver un valor **HRESULT** que no aparece en la documentación. De nuevo, use las macros [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) y [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) . Si comprueba un código de error específico, incluya también un caso predeterminado.


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

En esta sección se examinan algunos patrones para controlar los errores de COM de una manera estructurada. Cada patrón tiene ventajas y desventajas. En cierta medida, la elección es una cuestión de sabor. Si trabaja en un proyecto existente, es posible que ya tenga instrucciones de codificación que propongan un estilo determinado. Independientemente del modelo que adopte, el código sólido obedecerá las siguientes reglas.

-   Para cada método o función que devuelva un **HRESULT**, compruebe el valor devuelto antes de continuar.
-   Libere recursos después de usarlos.
-   No intente obtener acceso a recursos no válidos o no inicializados, como punteros **nulos** .
-   No intente usar un recurso después de liberarlo.

Teniendo en cuenta estas reglas, aquí hay cuatro patrones para controlar los errores.

-   [IFS anidado](#nested-ifs)
-   [IFS en cascada](#cascading-ifs)
-   [Error de salto](#jump-on-fail)
-   [Iniciar en error](#throw-on-fail)

### <a name="nested-ifs"></a>IFS anidado

Después de cada llamada que devuelve un **valor HRESULT**, use una instrucción **If** para comprobar si se ha realizado correctamente. A continuación, coloque la siguiente llamada al método en el ámbito de la instrucción **If** . Más instrucciones **If** se pueden anidar tan profundamente como sea necesario. Todos los ejemplos de código anteriores de este módulo usan este patrón, pero aquí lo están:


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

-   Las variables se pueden declarar con el ámbito mínimo. Por ejemplo, *pItem* no se declara hasta que se utiliza.
-   Dentro de cada instrucción **If** , se cumplen ciertas condiciones invariables: todas las llamadas anteriores se han realizado correctamente y todos los recursos adquiridos siguen siendo válidos. En el ejemplo anterior, cuando el programa alcanza la instrucción **If** más interna, se sabe que *pItem* y *pFileOpen* son válidos.
-   Está claro Cuándo se deben liberar los punteros de interfaz y otros recursos. Libera un recurso al final de la instrucción **If** que sigue inmediatamente a la llamada que adquirió el recurso.

Inconvenientes

-   Algunas personas buscan un anidamiento profundo difícil de leer.
-   El control de errores se mezcla con otras instrucciones de bifurcación y bucle. Esto puede hacer que la lógica general del programa sea más difícil de seguir.

### <a name="cascading-ifs"></a>IFS en cascada

Después de cada llamada al método, use una instrucción **If** para comprobar si la operación se ha realizado correctamente. Si el método se ejecuta correctamente, coloque la siguiente llamada de método dentro del bloque **If** . Pero en lugar de anidar más instrucciones **If** , coloque cada prueba [**correcta**](/windows/desktop/api/winerror/nf-winerror-succeeded) subsiguiente después del bloque **If** anterior. Si se produce un error en algún método, todas las pruebas **correctas** restantes simplemente producirán un error hasta que se alcance la parte inferior de la función.


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



En este patrón, libera recursos al final de la función. Si se produce un error, es posible que algunos punteros no sean válidos cuando la función termina. La llamada a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en un puntero no válido bloqueará el programa (o peor), por lo que debe inicializar todos los punteros en **null** y comprobar si son **null** antes de liberarlos. En este ejemplo se utiliza la `SafeRelease` función; los punteros inteligentes también son una buena opción.

Si usa este patrón, debe tener cuidado con las construcciones de bucle. Dentro de un bucle, interrumpa el bucle si se produce un error en cualquier llamada.

Ventajas

-   Este patrón crea menos anidamiento que el patrón "IFS anidado".
-   El flujo de control general es más fácil de ver.
-   Los recursos se liberan en un punto del código.

Inconvenientes

-   Todas las variables deben declararse e inicializarse en la parte superior de la función.
-   Si se produce un error en una llamada, la función realiza varias comprobaciones de errores innecesarias, en lugar de salir inmediatamente de la función.
-   Dado que el flujo de control continúa a través de la función después de un error, debe tener cuidado en todo el cuerpo de la función para no tener acceso a recursos no válidos.
-   Los errores dentro de un bucle requieren un caso especial.

### <a name="jump-on-fail"></a>Error de salto

Después de cada llamada al método, pruebe si hay un error (no correcto). En caso de error, saltar a una etiqueta cerca de la parte inferior de la función. Después de la etiqueta, pero antes de salir de la función, libere recursos.


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
-   En cada punto del código después de una comprobación con [**errores**](/windows/desktop/api/winerror/nf-winerror-failed) , si no ha saltado a la etiqueta, se garantiza que todas las llamadas anteriores se han realizado correctamente.
-   Los recursos se liberan en un lugar del código.

Inconvenientes

-   Todas las variables deben declararse e inicializarse en la parte superior de la función.
-   Algunos programadores no desean usar **goto** en su código. (Sin embargo, se debe observar que este uso de **goto** está muy estructurado; el código nunca salta fuera de la llamada de función actual).
-   las instrucciones **goto** omiten los inicializadores.

### <a name="throw-on-fail"></a>Iniciar en error

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



Observe que en este ejemplo se usa la clase **CComPtr** para administrar punteros de interfaz. Por lo general, si el código produce excepciones, debe seguir el patrón RAII (la adquisición de recursos es inicialización). Es decir, cada recurso debe ser administrado por un objeto cuyo destructor garantiza que el recurso se libera correctamente. Si se produce una excepción, se garantiza la invocación del destructor. De lo contrario, el programa podría perder recursos.

Ventajas

-   Compatible con el código existente que usa el control de excepciones.
-   Es compatible con las bibliotecas de C++ que producen excepciones, como la biblioteca de plantillas estándar (STL).

Inconvenientes

-   Requiere objetos de C++ para administrar recursos como la memoria o los identificadores de archivo.
-   Requiere una buena comprensión de cómo escribir código seguro para excepciones.

## <a name="next"></a>Siguientes

[Módulo 3. Gráficos de Windows](module-3---windows-graphics.md)

 

 
