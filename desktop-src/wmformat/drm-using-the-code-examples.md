---
title: Usar los ejemplos de código de cliente DRM de Microsoft Windows Media
description: Usar los ejemplos de código de cliente DRM de Microsoft Windows Media
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- SDK de Windows Media Format, ejemplos de código
- SDK de Windows Media Format, código de ejemplo
- SDK de Windows Media Format, ejemplos de código DRM
- Administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- Administración de derechos digitales (DRM), código de ejemplo
- DRM (administración de derechos digitales), código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421756"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a><span data-ttu-id="923ae-110">Usar los ejemplos de código de cliente DRM de Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="923ae-110">Using the Microsoft Windows Media DRM Client Code Examples</span></span>

<span data-ttu-id="923ae-111">En esta documentación se incluyen ejemplos de código para mostrar el uso de los componentes de.</span><span class="sxs-lookup"><span data-stu-id="923ae-111">Code examples are included in this documentation to illustrate the use of components.</span></span> <span data-ttu-id="923ae-112">Los ejemplos se escriben para ser tan claros y concisos como sea posible.</span><span class="sxs-lookup"><span data-stu-id="923ae-112">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="923ae-113">Al leer los ejemplos, debe tener en cuenta las siguientes convenciones.</span><span class="sxs-lookup"><span data-stu-id="923ae-113">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="923ae-114">Se supone que todos los ejemplos incluyen Windows. h y wmdrmsdk. h.</span><span class="sxs-lookup"><span data-stu-id="923ae-114">All examples are assumed to include windows.h and wmdrmsdk.h.</span></span> <span data-ttu-id="923ae-115">El ejemplo incluirá una nota si requiere otros encabezados para compilar.</span><span class="sxs-lookup"><span data-stu-id="923ae-115">The example will include a note if it requires other headers in order to compile.</span></span>
-   <span data-ttu-id="923ae-116">La comprobación de errores se ha restringido a interrumpir la función si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="923ae-116">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="923ae-117">En una aplicación, debe comprobar los códigos de error específicos y proporcionar algún tipo de informe de errores.</span><span class="sxs-lookup"><span data-stu-id="923ae-117">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>
-   <span data-ttu-id="923ae-118">Las interfaces y la memoria se liberan en los ejemplos de código mediante macros denominadas \_ versión segura y \_ matriz segura \_ eliminar.</span><span class="sxs-lookup"><span data-stu-id="923ae-118">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="923ae-119">Estas macros se definen en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="923ae-119">These macros are defined in the following code:</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="923ae-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="923ae-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="923ae-121">**Introducción**</span><span class="sxs-lookup"><span data-stu-id="923ae-121">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




