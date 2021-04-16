---
description: Las aplicaciones pueden depender de una versión específica de un archivo DLL compartido y comenzar a producir un error si se instala otra aplicación con una versión más reciente o anterior del mismo archivo DLL.
ms.assetid: 3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8
title: Redirección de la biblioteca Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d566231058cca13c10a067a3c2e20078073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687146"
---
# <a name="dynamic-link-library-redirection"></a>Redirección de la biblioteca Dynamic-Link

Las aplicaciones pueden depender de una versión específica de un archivo DLL compartido y comenzar a producir un error si se instala otra aplicación con una versión más reciente o anterior del mismo archivo DLL. Hay dos maneras de asegurarse de que la aplicación usa el archivo DLL correcto: redirección de DLL y componentes en paralelo. Los desarrolladores y administradores deben usar el redireccionamiento de DLL para las aplicaciones existentes, ya que no requiere ningún cambio en la aplicación. Si está creando una nueva aplicación o actualizando una aplicación y desea aislar la aplicación de posibles problemas, cree un [componente en paralelo](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Para habilitar la redirección de archivos DLL en todo el equipo, debe crear una nueva clave del registro. Cree una nueva clave DWORD denominada **DevOverrideEnable** en **las opciones de ejecución de archivo HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image** y establézcala en 1. Después, debe reiniciar el equipo para ver los efectos.

Para usar el redireccionamiento de DLL, cree un *archivo de redireccionamiento* para la aplicación. El archivo de redireccionamiento debe tener el nombre siguiente: *\_ nombre* de la aplicación. local. Por ejemplo, si el nombre de la aplicación es Editor.exe, el archivo de redireccionamiento se debe denominar Editor.exe. local. Debe instalar el archivo. local en el directorio de la aplicación. También debe instalar los archivos dll en el directorio de la aplicación.

El contenido de un archivo de redireccionamiento se omite, pero su presencia hace que Windows Compruebe el directorio de la aplicación en primer lugar cada vez que carga un archivo DLL, independientemente de la ruta de acceso especificada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Si el archivo DLL no se encuentra en el directorio de la aplicación, estas funciones usan su orden de búsqueda habitual. Por ejemplo, si la aplicación c: \\ myapp \\myapp.exe llama a **LoadLibrary** mediante la siguiente ruta de acceso:

c: archivos de \\ programa archivos \\ comunes \\ sistema \\mydll.dll

Y, si tanto c: \\ myapp \\myapp.exe. local como c: \\ MyApp \\mydll.dll existen, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) carga c: \\ MyApp \\mydll.dll. De lo contrario, **LoadLibrary** carga c: \\ archivos de programa \\ Common file \\ System \\mydll.dll.

Como alternativa, si un directorio denominado c: \\ myapp \\myapp.exe. local existe y contiene mydll.dll, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) carga c: \\ MyApp \\myapp.exe. local \\mydll.dll.

Si la aplicación tiene un manifiesto, se omiten los archivos. local.

Si usa el redireccionamiento de DLL y la aplicación no tiene acceso a todas las unidades y directorios en el orden de búsqueda, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) dejará de buscar en cuanto se deniegue el acceso. (Si no usa el redireccionamiento de DLL, **LoadLibrary** omite los directorios a los que no puede tener acceso y, a continuación, continúa con la búsqueda).

Es recomendable instalar los archivos dll de la aplicación en el mismo directorio que contiene la aplicación, incluso si no está utilizando el redireccionamiento de DLL. Esto garantiza que al instalar la aplicación no se sobrescriban otras copias del archivo DLL y que se produzca un error en otras aplicaciones. Además, si sigue este procedimiento recomendado, otras aplicaciones no sobrescribirán su copia del archivo DLL y provocarán un error en la aplicación.

 

 
