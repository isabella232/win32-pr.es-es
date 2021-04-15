---
description: Cuando una aplicación carga dinámicamente una biblioteca de vínculos dinámicos sin especificar un nombre de ruta de acceso completo, Windows intenta localizar el archivo DLL buscando un conjunto de directorios bien definido en un orden determinado, como se describe en Dynamic-Link el orden de búsqueda de la biblioteca. Si un atacante obtiene el control de uno de los directorios de la ruta de búsqueda de DLL, puede colocar una copia malintencionada del archivo DLL en ese directorio. Esto se denomina a veces un ataque de carga previa de DLL o un ataque de Binary Planting.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Seguridad de biblioteca Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4016139762461784702ac0190c1ee65d8bc6e72d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669703"
---
# <a name="dynamic-link-library-security"></a>Seguridad de biblioteca Dynamic-Link

Cuando una aplicación carga dinámicamente una biblioteca de vínculos dinámicos sin especificar un nombre de ruta de acceso completo, Windows intenta localizar el archivo DLL buscando un conjunto de directorios bien definido en un orden determinado, tal como se describe en el orden de búsqueda de la [biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md). Si un atacante obtiene el control de uno de los directorios de la ruta de búsqueda de DLL, puede colocar una copia malintencionada del archivo DLL en ese directorio. Esto se denomina a veces un *ataque de carga previa de dll* o un ataque de *Binary planting*. Si el sistema no encuentra una copia legítima de la DLL antes de buscar en el directorio en peligro, carga la DLL malintencionada. Si la aplicación se ejecuta con privilegios de administrador, el atacante puede tener éxito en la elevación de privilegios local.

Por ejemplo, supongamos que una aplicación está diseñada para cargar un archivo DLL desde el directorio actual del usuario y se produce un error si no se encuentra el archivo DLL. La aplicación llama a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con solo el nombre del archivo dll, lo que hace que el sistema busque el archivo dll. Suponiendo que el modo de búsqueda de archivos DLL seguro está habilitado y la aplicación no usa un orden de búsqueda alternativo, el sistema busca en los directorios en el siguiente orden:

1.  Directorio desde el que se cargó la aplicación.
2.  Directorio del sistema.
3.  Directorio del sistema de 16 bits.
4.  El directorio de Windows.
5.  El directorio actual.
6.  Los directorios que aparecen en la variable de entorno PATH.

Continuando con el ejemplo, un atacante con conocimiento de la aplicación gana el control del directorio actual y coloca una copia malintencionada del archivo DLL en ese directorio. Cuando la aplicación emite la llamada **LoadLibrary** , el sistema busca el archivo dll, encuentra la copia malintencionada del archivo dll en el directorio actual y lo carga. La copia malintencionada del archivo DLL se ejecuta dentro de la aplicación y obtiene los privilegios del usuario.

Los desarrolladores pueden ayudar a proteger sus aplicaciones contra los ataques de carga previa de DLL siguiendo estas instrucciones:

-   Siempre que sea posible, especifique una ruta de acceso completa al utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)o [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) .
-   Use las marcas de búsqueda de la \_ biblioteca de carga \_ con la función [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) o use estas marcas con la función [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) para establecer un orden de búsqueda de dll para un proceso y, a continuación, use las funciones [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) para modificar la lista. Para obtener más información, vea [orden de búsqueda en la biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md).

    **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Estas marcas y funciones están disponibles en los sistemas con [KB2533623](https://support.microsoft.com/kb/2533623) instalado.

-   En los sistemas con [KB2533623](https://support.microsoft.com/kb/2533623) instalado, use las marcas de búsqueda de la biblioteca de carga \_ \_ con la función [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , o bien use estas marcas con la función [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) para establecer un orden de búsqueda de dll para un proceso y, a continuación, use las funciones [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) para modificar la lista. Para obtener más información, vea [orden de búsqueda en la biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md).
-   Considere la posibilidad de usar el [redireccionamiento de dll](dynamic-link-library-redirection.md) o un [manifiesto](/windows/desktop/SbsCs/manifests) para asegurarse de que la aplicación usa el archivo dll correcto.
-   Al usar el orden de búsqueda estándar, asegúrese de que está habilitado el modo de búsqueda segura de DLL. Esto coloca el directorio actual del usuario más adelante en el orden de búsqueda, lo que aumenta las posibilidades de que Windows encuentre una copia legítima del archivo DLL antes de una copia malintencionada. El modo de búsqueda segura de archivos dll está habilitado de forma predeterminada a partir de Windows XP con Service Pack 2 (SP2) y se controla mediante el valor del registro **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Session Manager** \\ **SafeDllSearchMode** . Para obtener más información, vea [orden de búsqueda en la biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md).
-   Considere la posibilidad de quitar el directorio actual de la ruta de acceso de búsqueda estándar mediante una llamada a [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) con una cadena vacía (""). Esto debe realizarse una vez al principio de la inicialización del proceso, no antes ni después de las llamadas a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Tenga en cuenta que **SetDllDirectory** afecta a todo el proceso y que varios subprocesos que llaman a **SetDllDirectory** con distintos valores pueden provocar un comportamiento indefinido. Si la aplicación carga archivos dll de terceros, realice una prueba detenidamente para identificar las incompatibilidades.
-   No utilice la función [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para recuperar una ruta de acceso a un archivo DLL para una llamada [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) subsiguiente a menos que esté habilitado el modo de búsqueda de procesos seguros. Cuando el modo de búsqueda de procesos seguro no está habilitado, la función **SearchPath** usa un orden de búsqueda diferente que **LoadLibrary** y es probable que busque primero en el directorio actual del usuario la dll especificada. Para habilitar el modo de búsqueda segura de procesos para la función **SearchPath** , use la función [**SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) con la \_ ruta de búsqueda base \_ \_ habilitar \_ \_ SEARCHMODE segura. Esto mueve el directorio actual al final de la lista de búsqueda de **SearchPath** mientras dure el proceso. Tenga en cuenta que el directorio actual no se quita de la ruta de acceso de búsqueda, por lo que si el sistema no encuentra una copia legítima del archivo DLL antes de que llegue al directorio actual, la aplicación seguirá siendo vulnerable. Al igual que con [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya), la llamada a **SetSearchPathMode** se debe realizar en el principio de la inicialización del proceso y afecta a todo el proceso. Si la aplicación carga archivos dll de terceros, realice una prueba detenidamente para identificar las incompatibilidades.
-   No realice suposiciones sobre la versión del sistema operativo basada en una llamada [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) que busque un archivo dll. Si la aplicación se ejecuta en un entorno en el que el archivo DLL no está presente legítimamente pero hay una copia malintencionada de la DLL en la ruta de búsqueda, se puede cargar la copia malintencionada del archivo DLL. En su lugar, use las técnicas recomendadas que se describen en [obtener la versión del sistema](/windows/desktop/SysInfo/getting-the-system-version).

La herramienta Monitor de procesos se puede usar para ayudar a identificar las operaciones de carga de archivos DLL que podrían ser vulnerables. La herramienta Monitor de procesos se puede descargar desde <https://technet.microsoft.com/sysinternals/bb896645.aspx> .

En el procedimiento siguiente se describe cómo usar el monitor de procesos para examinar las operaciones de carga de archivos DLL en la aplicación.

**Para usar el monitor de procesos para examinar las operaciones de carga de archivos DLL en la aplicación**

1.  Inicie el monitor de proceso.
2.  En el monitor de procesos, incluya los siguientes filtros:
    -   La operación es CreateFile
    -   La operación es LoadImage
    -   Path contiene. cpl
    -   La ruta de acceso contiene. dll
    -   La ruta de acceso contiene. drv
    -   La ruta de acceso contiene. exe
    -   La ruta de acceso contiene. ocx
    -   La ruta de acceso contiene. SCR
    -   La ruta de acceso contiene. sys
3.  Excluya los siguientes filtros:
    -   El nombre del proceso es procmon.exe
    -   El nombre del proceso es Procmon64.exe
    -   El nombre del proceso es sistema
    -   La operación comienza con IRP \_ MJ\_
    -   La operación comienza con FASTIO\_
    -   El resultado es SUCCEss
    -   La ruta de acceso finaliza con pagefile.sys
4.  Intente iniciar la aplicación con el directorio actual establecido en un directorio específico. Por ejemplo, haga doble clic en un archivo con una extensión cuyo controlador de archivos esté asignado a la aplicación.
5.  Compruebe la salida del monitor de procesos para las rutas de acceso que parezcan sospechosas, como una llamada al directorio actual para cargar un archivo DLL. Este tipo de llamada puede indicar una vulnerabilidad en la aplicación.

 

 
