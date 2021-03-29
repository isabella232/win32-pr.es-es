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
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Usar los ejemplos de código de cliente DRM de Microsoft Windows Media

En esta documentación se incluyen ejemplos de código para mostrar el uso de los componentes de. Los ejemplos se escriben para ser tan claros y concisos como sea posible. Al leer los ejemplos, debe tener en cuenta las siguientes convenciones.

-   Se supone que todos los ejemplos incluyen Windows. h y wmdrmsdk. h. El ejemplo incluirá una nota si requiere otros encabezados para compilar.
-   La comprobación de errores se ha restringido a interrumpir la función si se produce un error. En una aplicación, debe comprobar los códigos de error específicos y proporcionar algún tipo de informe de errores.
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

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción**](drm-getting-started.md)
</dt> </dl>

 

 




