---
description: Las siguientes funciones se usan en la vinculación dinámica.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Dynamic-Link library functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521c9200b3fa6585ec2804d76ac385845dcd6fb56ef4e7b70a7a3d9bd59150c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070585"
---
# <a name="dynamic-link-library-functions"></a>Dynamic-Link library functions

Las siguientes funciones se usan en la vinculación dinámica.



| Función                                                       | Descripción                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Agrega un directorio a la ruta de acceso de búsqueda dll del proceso.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Deshabilita las notificaciones de asociación de subprocesos y desasociadas para el archivo DLL especificado.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Punto de entrada opcional en un archivo DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Disminuye el recuento de referencias del archivo DLL cargado. Cuando el recuento de referencias alcanza cero, el módulo se desaconsja del espacio de direcciones del proceso de llamada. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Disminuye el recuento de referencias de un archivo DLL cargado en uno y, a continuación, llama a [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) para finalizar el subproceso que realiza la llamada.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Recupera la parte específica de la aplicación de la ruta de búsqueda que se usa para buscar archivos DLL para la aplicación.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Recupera la ruta de acceso completa para el archivo que contiene el módulo especificado.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Recupera la ruta de acceso completa para el archivo que contiene el módulo especificado.                                                                               |
| [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Recupera un identificador de módulo para el módulo especificado.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Recupera un identificador de módulo para el módulo especificado.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Recupera la dirección de una función o variable exportada del archivo DLL especificado.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Mapas el módulo ejecutable especificado en el espacio de direcciones del proceso de llamada.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Mapas el módulo ejecutable especificado en el espacio de direcciones del proceso de llamada.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Mapas el módulo empaquetado especificado y sus dependencias en el espacio de direcciones del proceso de llamada. Solo Windows aplicaciones de store pueden llamar a esta función.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Quita un directorio que se agregó a la ruta de acceso de búsqueda del archivo DLL de proceso mediante [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Especifica un conjunto predeterminado de directorios que se buscarán cuando el proceso de llamada cargue un archivo DLL.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Modifica la ruta de acceso de búsqueda utilizada para buscar archivos DLL para la aplicación.                                                                                              |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Estas funciones solo se proporcionan por compatibilidad con versiones de 16 bits de Windows.

[**Loadmodule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
