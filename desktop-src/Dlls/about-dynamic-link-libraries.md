---
description: La vinculación dinámica permite a un módulo incluir solo la información necesaria para buscar una función de DLL exportada en tiempo de carga o en tiempo de ejecución.
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: Acerca de las bibliotecas de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdb24048e17e9164aaf39d0ab337aea33576c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908353"
---
# <a name="about-dynamic-link-libraries"></a>Acerca de las bibliotecas de Dynamic-Link

La vinculación dinámica permite a un módulo incluir solo la información necesaria para buscar una función de DLL exportada en tiempo de carga o en tiempo de ejecución. La vinculación dinámica difiere de la vinculación estática más familiar, en la que el vinculador copia el código de una función de biblioteca en cada módulo que lo llama.

## <a name="types-of-dynamic-linking"></a>Tipos de vinculación dinámica

Hay dos métodos para llamar a una función en un archivo DLL:

-   En la *vinculación dinámica en tiempo de carga*, un módulo realiza llamadas explícitas a las funciones de dll exportadas como si fueran funciones locales. Esto requiere vincular el módulo con la biblioteca de importación del archivo DLL que contiene las funciones. Una biblioteca de importación proporciona al sistema la información necesaria para cargar el archivo DLL y ubicar las funciones DLL exportadas cuando se carga la aplicación.
-   En la *vinculación dinámica en tiempo de ejecución*, un módulo utiliza la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) para cargar el archivo dll en tiempo de ejecución. Una vez cargado el archivo DLL, el módulo llama a la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener las direcciones de las funciones DLL exportadas. El módulo llama a las funciones DLL exportadas con los punteros de función devueltos por **GetProcAddress**. Esto elimina la necesidad de una biblioteca de importación.

## <a name="dlls-and-memory-management"></a>Archivos dll y administración de memoria

Cada proceso que carga el archivo DLL lo asigna a su espacio de direcciones virtuales. Una vez que el proceso carga el archivo DLL en su dirección virtual, puede llamar a las funciones de DLL exportadas.

El sistema mantiene un recuento de referencias por proceso para cada archivo DLL. Cuando un subproceso carga el archivo DLL, el recuento de referencias se incrementa en uno. Cuando finaliza el proceso, o cuando el recuento de referencias se convierte en cero (solo vinculación dinámica en tiempo de ejecución), el archivo DLL se descarga del espacio de direcciones virtuales del proceso.

Al igual que cualquier otra función, una función de DLL exportada se ejecuta en el contexto del subproceso que la llama. Por lo tanto, se aplican las condiciones siguientes:

-   Los subprocesos del proceso que llamó a la DLL pueden usar los identificadores abiertos por una función DLL. De forma similar, los identificadores abiertos por cualquier subproceso del proceso de llamada se pueden usar en la función DLL.
-   El archivo DLL utiliza la pila del subproceso que realiza la llamada y el espacio de direcciones virtuales del proceso que realiza la llamada.
-   El archivo DLL asigna memoria del espacio de direcciones virtuales del proceso que realiza la llamada.

Para obtener más información acerca de los archivos dll, vea los temas siguientes:

-   [Ventajas de la vinculación dinámica](advantages-of-dynamic-linking.md)
-   [Creación de biblioteca de vínculos dinámicos](dynamic-link-library-creation.md)
-   [Función Entry-Point de la biblioteca de vínculos dinámicos](dynamic-link-library-entry-point-function.md)
-   [Vinculación dinámica en tiempo de carga](load-time-dynamic-linking.md)
-   [Vinculación dinámica en tiempo de ejecución](run-time-dynamic-linking.md)
-   [Orden de búsqueda de la biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md)
-   [Datos de biblioteca de vínculos dinámicos](dynamic-link-library-data.md)
-   [Redirección de biblioteca de vínculos dinámicos](dynamic-link-library-redirection.md)
-   [Actualizaciones de la biblioteca de vínculos dinámicos](dynamic-link-library-updates.md)
-   [Seguridad de la biblioteca de vínculos dinámicos](dynamic-link-library-security.md)
-   [Archivos dll de AppInit y arranque seguro](secure-boot-and-appinit-dlls.md)

 

 
