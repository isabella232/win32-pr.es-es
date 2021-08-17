---
title: Uso de los ejemplos de código de cliente drm Windows Media de Microsoft
description: Uso de los ejemplos de código de cliente drm Windows Media de Microsoft
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows SDK de formato multimedia, ejemplos de código
- Windows SDK de formato multimedia, código de ejemplo
- Windows SDK de formato multimedia, ejemplos de código DRM
- administración de derechos digitales (DRM),ejemplos de código
- DRM (administración de derechos digitales),ejemplos de código
- administración de derechos digitales (DRM),código de ejemplo
- DRM (administración de derechos digitales),código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e14ef7e1d003dec8270bb4cfb63d5b4ead7f11751eb94dd09cd771ebd34b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704218"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Uso de los ejemplos de código de cliente drm Windows Media de Microsoft

En esta documentación se incluyen ejemplos de código para ilustrar el uso de componentes. Los ejemplos se escriben para que sean lo más claros y concisos posible. Al leer los ejemplos, debe tener en cuenta las convenciones siguientes.

-   Se supone que todos los ejemplos incluyen windows.h y wmdrmsdk.h. El ejemplo incluirá una nota si requiere otros encabezados para compilar.
-   La comprobación de errores se ha restringido a la separación de la función si se produce un error. En una aplicación, debe buscar códigos de error específicos y proporcionar algún tipo de informe de errores.
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

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas iniciales**](drm-getting-started.md)
</dt> </dl>

 

 




