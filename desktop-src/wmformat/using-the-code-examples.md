---
title: Uso de los ejemplos de código Windows SDK de formato multimedia
description: Uso de los ejemplos de código Windows SDK de formato multimedia
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows SDK de formato multimedia, ejemplos de código
- Windows SDK de formato multimedia, código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a5b6718bf7665d04fedb5d5a0bad473a632cbeeabdfd756a52877ccdc84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963944"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>Uso de los ejemplos de código Windows SDK de formato multimedia

Muchas de las secciones explicativas de este SDK incluyen ejemplos de código. Los ejemplos se escriben para que sean lo más claros y concisos posibles. Al leer los ejemplos, debe tener en cuenta las convenciones siguientes.

-   Se supone que todos los ejemplos incluyen windows.h y wmsdk.h. Los demás archivos de encabezado necesarios se mencionan en el texto explicativo.
-   La comprobación de errores se ha restringido a la separación de la función si se produce un error. En una aplicación, debe buscar códigos de error específicos y proporcionar algún tipo de informe de errores.

    Al comprobar los valores devueltos de métodos o funciones que devuelven un valor **HRESULT,** debe usar la macro **FAILED** para detectar si el valor devuelto indica un error.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    Muchos de los ejemplos de esta documentación usan una macro denominada GOTO EXIT IF FAILED, que \_ se define en el código \_ \_ siguiente.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Cada una de estas funciones de ejemplo tiene una etiqueta denominada "Exit:", después de la cual se liberan todas las interfaces y memoria asignadas en la función y se devuelve el código de error, si existe.

-   Las interfaces y la memoria se liberan en los ejemplos de código mediante macros denominadas SAFE \_ RELEASE y SAFE ARRAY \_ \_ DELETE. Estas macros se definen en el código siguiente:
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   A menudo, tendrá que incluir la lógica de un ejemplo en otro ejemplo para que el ejemplo sea significativo. En esos casos, se incluye un comentario TODO, con una referencia al ejemplo de código adecuado.
-   Para facilitar la lectura del código, ninguna de las funciones de ejemplo de esta documentación valida sus parámetros de entrada. Si copia cualquiera de estas funciones en el código, debe validar los parámetros de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas iniciales**](getting-started.md)
</dt> </dl>

 

 




