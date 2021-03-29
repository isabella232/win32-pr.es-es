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
# <a name="using-the-windows-media-format-sdk-code-examples"></a><span data-ttu-id="6132c-105">Usar los ejemplos de código del SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="6132c-105">Using the Windows Media Format SDK Code Examples</span></span>

<span data-ttu-id="6132c-106">Muchas de las secciones explicativas de este SDK incluyen ejemplos de código.</span><span class="sxs-lookup"><span data-stu-id="6132c-106">Many of the explanatory sections of this SDK include code examples.</span></span> <span data-ttu-id="6132c-107">Los ejemplos se escriben para ser tan claros y concisos como sea posible.</span><span class="sxs-lookup"><span data-stu-id="6132c-107">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="6132c-108">Al leer los ejemplos, debe tener en cuenta las siguientes convenciones.</span><span class="sxs-lookup"><span data-stu-id="6132c-108">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="6132c-109">Se supone que todos los ejemplos incluyen Windows. h y wmsdk. h.</span><span class="sxs-lookup"><span data-stu-id="6132c-109">All examples are assumed to include windows.h and wmsdk.h.</span></span> <span data-ttu-id="6132c-110">Cualquier otro archivo de encabezado necesario se menciona en el texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="6132c-110">Any other required header files are mentioned in the explanatory text.</span></span>
-   <span data-ttu-id="6132c-111">La comprobación de errores se ha restringido a interrumpir la función si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="6132c-111">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="6132c-112">En una aplicación, debe comprobar los códigos de error específicos y proporcionar algún tipo de informe de errores.</span><span class="sxs-lookup"><span data-stu-id="6132c-112">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>

    <span data-ttu-id="6132c-113">Al comprobar los valores devueltos de métodos o funciones que devuelven un valor **HRESULT** , debe usar la macro **failed** para detectar si el valor devuelto indica error.</span><span class="sxs-lookup"><span data-stu-id="6132c-113">When checking return values from methods or functions that return an **HRESULT** value, you should use the **FAILED** macro to discover whether the return value indicates failure.</span></span>

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    <span data-ttu-id="6132c-114">Muchos de los ejemplos de esta documentación usan una macro denominada GOTO \_ Exit \_ si \_ se produce un error, que se define en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="6132c-114">Many of the examples in this documentation use a macro named GOTO\_EXIT\_IF\_FAILED, which is defined in the following code.</span></span>

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    <span data-ttu-id="6132c-115">Cada una de estas funciones de ejemplo tiene una etiqueta denominada "EXIT:", después de la cual se liberan todas las interfaces y la memoria asignadas en la función y se devuelve el código de error, si existe.</span><span class="sxs-lookup"><span data-stu-id="6132c-115">These example functions each have a tag named "Exit:", after which all interfaces and memory allocated in the function are released and the error code, if any, is returned.</span></span>

-   <span data-ttu-id="6132c-116">Las interfaces y la memoria se liberan en los ejemplos de código mediante macros denominadas \_ versión segura y \_ matriz segura \_ eliminar.</span><span class="sxs-lookup"><span data-stu-id="6132c-116">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="6132c-117">Estas macros se definen en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="6132c-117">These macros are defined in the following code:</span></span>
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

    

-   <span data-ttu-id="6132c-118">A menudo, tendrá que incluir la lógica de un ejemplo en otro ejemplo para que el ejemplo sea significativo.</span><span class="sxs-lookup"><span data-stu-id="6132c-118">Often, you will need to include the logic of one example in another example for the example to be meaningful.</span></span> <span data-ttu-id="6132c-119">En esos casos, se incluye un comentario TODO, con una referencia al ejemplo de código adecuado.</span><span class="sxs-lookup"><span data-stu-id="6132c-119">In those instances, a TODO comment is included, with a reference to the appropriate code example.</span></span>
-   <span data-ttu-id="6132c-120">Para que el código sea más fácil de leer, ninguna de las funciones de ejemplo de esta documentación valida sus parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="6132c-120">To make the code easier to read, none of the example functions in this documentation validate their input parameters.</span></span> <span data-ttu-id="6132c-121">Si copia cualquiera de estas funciones en el código, debe validar cualquier parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="6132c-121">If you copy any of these functions into your code, you should validate any input parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6132c-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6132c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6132c-123">**Introducción**</span><span class="sxs-lookup"><span data-stu-id="6132c-123">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 




