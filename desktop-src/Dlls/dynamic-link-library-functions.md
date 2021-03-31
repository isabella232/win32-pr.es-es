---
description: Las siguientes funciones se usan en la vinculación dinámica.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Funciones de la biblioteca Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47ce37b6f91570ce9f3314fc329b5e85cde310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912877"
---
# <a name="dynamic-link-library-functions"></a>Funciones de la biblioteca Dynamic-Link

Las siguientes funciones se usan en la vinculación dinámica.



| Función                                                       | Descripción                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Agrega un directorio a la ruta de búsqueda de DLL de proceso.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Deshabilita las notificaciones de Asociación de subprocesos y desasociación de subprocesos para el archivo DLL especificado.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Un punto de entrada opcional en un archivo DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Disminuye el recuento de referencias de la DLL cargada. Cuando el recuento de referencias llega a cero, el módulo se desasigna del espacio de direcciones del proceso de llamada. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Disminuye el recuento de referencias de un archivo DLL cargado en uno y, a continuación, llama a [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) para terminar el subproceso que realiza la llamada.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Recupera la parte específica de la aplicación de la ruta de acceso de búsqueda utilizada para localizar los archivos dll de la aplicación.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Recupera la ruta de acceso completa del archivo que contiene el módulo especificado.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Recupera la ruta de acceso completa del archivo que contiene el módulo especificado.                                                                               |
| [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Recupera un identificador de módulo para el módulo especificado.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Recupera un identificador de módulo para el módulo especificado.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Recupera la dirección de una función o variable exportada de la DLL especificada.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Asigna el módulo ejecutable especificado en el espacio de direcciones del proceso de llamada.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Asigna el módulo ejecutable especificado en el espacio de direcciones del proceso de llamada.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Asigna el módulo empaquetado especificado y sus dependencias en el espacio de direcciones del proceso de llamada. Solo las aplicaciones de la tienda Windows pueden llamar a esta función.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Quita un directorio que se ha agregado a la ruta de búsqueda de DLL de proceso mediante [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Especifica un conjunto predeterminado de directorios para buscar cuando el proceso de llamada carga un archivo DLL.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Modifica la ruta de búsqueda que se usa para buscar los archivos dll de la aplicación.                                                                                              |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Estas funciones solo se proporcionan por compatibilidad con las versiones de 16 bits de Windows.

[**LoadModule (**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
