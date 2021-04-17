---
description: Cuando la aplicación llama a las funciones LoadLibrary o LoadLibraryEx, el sistema intenta encontrar el archivo DLL (para obtener más información, vea Dynamic-Link el orden de búsqueda de la biblioteca).
ms.assetid: 81e237a9-3c32-46a5-88d3-c978f43dad54
title: Vinculación dinámica Run-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e215ac83ecdc0615b8030e2e215857c67fe6e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666707"
---
# <a name="run-time-dynamic-linking"></a>Vinculación dinámica Run-Time

Cuando la aplicación llama a las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , el sistema intenta encontrar el archivo DLL (para obtener más información, vea [orden de búsqueda de la biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md)). Si la búsqueda se realiza correctamente, el sistema asigna el módulo DLL en el espacio de direcciones virtuales del proceso e incrementa el recuento de referencias. Si la llamada a **LoadLibrary** o **LoadLibraryEx** especifica un archivo dll cuyo código ya está asignado en el espacio de direcciones virtuales del proceso de llamada, la función devuelve simplemente un identificador a la dll e incrementa el recuento de referencias de dll. Tenga en cuenta que dos archivos DLL que tienen el mismo nombre y extensión de archivo base, pero que se encuentran en directorios diferentes, no se consideran el mismo archivo DLL.

El sistema llama a la función de punto de entrada en el contexto del subproceso que llamó a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). No se llama a la función de punto de entrada si el proceso ya cargó el archivo DLL a través de una llamada a **LoadLibrary** o **LoadLibraryEx** sin una llamada correspondiente a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

Si el sistema no puede encontrar el archivo DLL o si la función de punto de entrada devuelve FALSE, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) devuelve NULL. Si **LoadLibrary** o **LoadLibraryEx** se realiza correctamente, devuelve un identificador al módulo DLL. El proceso puede utilizar este identificador para identificar el archivo DLL en una llamada a la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)o [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) .

La función [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) devuelve un identificador que se usa en [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)o [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). La función **GetModuleHandle** solo se realiza correctamente si el módulo DLL ya está asignado en el espacio de direcciones del proceso mediante la vinculación en tiempo de carga o mediante una llamada anterior a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). A diferencia de **LoadLibrary** o **LoadLibraryEx**, **GetModuleHandle** no incrementa el recuento de referencias del módulo. La función [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) recupera la ruta de acceso completa del módulo asociado a un identificador devuelto por **GetModuleHandle**, **LoadLibrary** o **LoadLibraryEx**.

El proceso puede utilizar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener la dirección de una función exportada en el archivo DLL mediante un identificador de módulo DLL devuelto por [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

Cuando el módulo DLL ya no se necesita, el proceso puede llamar a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) o [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). Estas funciones disminuyen el recuento de referencias del módulo y desasocian el código DLL del espacio de direcciones virtuales del proceso si el recuento de referencias es cero.

La vinculación dinámica en tiempo de ejecución permite que el proceso continúe ejecutándose incluso si un archivo DLL no está disponible. Después, el proceso puede utilizar un método alternativo para lograr su objetivo. Por ejemplo, si un proceso no encuentra un archivo DLL, puede intentar usar otro o puede notificar al usuario de un error. Si el usuario puede proporcionar la ruta de acceso completa del archivo DLL que falta, el proceso puede utilizar esta información para cargar el archivo DLL aunque no esté en la ruta de búsqueda normal. Esta situación contrasta con la vinculación en tiempo de carga, en la que el sistema simplemente finaliza el proceso si no encuentra el archivo DLL.

La vinculación dinámica en tiempo de ejecución puede producir problemas si el archivo DLL utiliza la función [**DllMain**](dllmain.md) para realizar la inicialización de cada subproceso de un proceso, ya que no se llama al punto de entrada para los subprocesos que existían antes de que se llame a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Para ver un ejemplo en el que se muestra cómo solucionar este problema, vea [usar el almacenamiento local para el subproceso en una biblioteca de Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la vinculación dinámica en tiempo de ejecución](using-run-time-dynamic-linking.md)
</dt> </dl>

 

 
