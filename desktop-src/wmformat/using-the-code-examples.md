---
title: Usar los ejemplos de código del SDK de Windows Media Format
description: Usar los ejemplos de código del SDK de Windows Media Format
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- SDK de Windows Media Format, ejemplos de código
- SDK de Windows Media Format, código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421876"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>Usar los ejemplos de código del SDK de Windows Media Format

Muchas de las secciones explicativas de este SDK incluyen ejemplos de código. Los ejemplos se escriben para ser tan claros y concisos como sea posible. Al leer los ejemplos, debe tener en cuenta las siguientes convenciones.

-   Se supone que todos los ejemplos incluyen Windows. h y wmsdk. h. Cualquier otro archivo de encabezado necesario se menciona en el texto explicativo.
-   La comprobación de errores se ha restringido a interrumpir la función si se produce un error. En una aplicación, debe comprobar los códigos de error específicos y proporcionar algún tipo de informe de errores.

    Al comprobar los valores devueltos de métodos o funciones que devuelven un valor **HRESULT** , debe usar la macro **failed** para detectar si el valor devuelto indica error.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    Muchos de los ejemplos de esta documentación usan una macro denominada GOTO \_ Exit \_ si \_ se produce un error, que se define en el código siguiente.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Cada una de estas funciones de ejemplo tiene una etiqueta denominada "EXIT:", después de la cual se liberan todas las interfaces y la memoria asignadas en la función y se devuelve el código de error, si existe.

-   Las interfaces y la memoria se liberan en los ejemplos de código mediante macros denominadas \_ versión segura y \_ matriz segura \_ eliminar. Estas macros se definen en el código siguiente:
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
-   Para que el código sea más fácil de leer, ninguna de las funciones de ejemplo de esta documentación valida sus parámetros de entrada. Si copia cualquiera de estas funciones en el código, debe validar cualquier parámetro de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción**](getting-started.md)
</dt> </dl>

 

 




