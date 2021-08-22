---
description: Cuando una aplicación carga dinámicamente una biblioteca de vínculos dinámicos sin especificar un nombre de ruta de acceso completo, Windows intenta buscar el archivo DLL buscando un conjunto bien definido de directorios en un orden determinado, tal como se describe en el orden de búsqueda de la biblioteca de Dynamic-Link. Si un atacante obtiene el control de uno de los directorios en la ruta de búsqueda de dll, puede colocar una copia malintencionada del archivo DLL en ese directorio. Esto se denomina a veces un ataque de precarga de DLL o un ataque de plantación binaria.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Dynamic-Link seguridad de la biblioteca de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582122debce68ade593c007e431e62a91a7fa07f395f148b7eaa05cac13bc56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290405"
---
# <a name="dynamic-link-library-security"></a>Dynamic-Link seguridad de la biblioteca de recursos

Cuando una aplicación carga dinámicamente una biblioteca de vínculos dinámicos sin especificar un nombre de ruta de acceso completo, Windows intenta localizar el archivo DLL buscando un conjunto bien definido de directorios en un orden determinado, como se describe en Orden de búsqueda de la biblioteca de vínculos [dinámicos](dynamic-link-library-search-order.md). Si un atacante obtiene el control de uno de los directorios en la ruta de búsqueda de dll, puede colocar una copia malintencionada del archivo DLL en ese directorio. Esto se denomina a veces un *ataque de precarga de DLL* o un ataque de *plantación binaria.* Si el sistema no encuentra una copia legítima del archivo DLL antes de buscar en el directorio en peligro, carga el archivo DLL malintencionado. Si la aplicación se ejecuta con privilegios de administrador, el atacante puede tener éxito en la elevación de privilegios local.

Por ejemplo, suponga que una aplicación está diseñada para cargar un archivo DLL desde el directorio actual del usuario y se producirá un error correctamente si no se encuentra el archivo DLL. La aplicación llama [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con solo el nombre del archivo DLL, lo que hace que el sistema busque el archivo DLL. Suponiendo que el modo de búsqueda de DLL seguro está habilitado y la aplicación no usa un orden de búsqueda alternativo, el sistema busca directorios en el orden siguiente:

1.  Directorio desde el que se cargó la aplicación.
2.  Directorio del sistema.
3.  Directorio del sistema de 16 bits.
4.  El directorio de Windows.
5.  El directorio actual.
6.  Directorios que aparecen en la variable de entorno PATH.

Continuando con el ejemplo, un atacante con conocimiento de la aplicación obtiene el control del directorio actual y coloca una copia malintencionada del archivo DLL en ese directorio. Cuando la aplicación emite la **llamada LoadLibrary,** el sistema busca el archivo DLL, busca la copia malintencionada del archivo DLL en el directorio actual y la carga. A continuación, la copia malintencionada del archivo DLL se ejecuta dentro de la aplicación y obtiene los privilegios del usuario.

Los desarrolladores pueden ayudar a proteger sus aplicaciones frente a ataques de carga previa de DLL siguiendo estas directrices:

-   Siempre que sea posible, especifique una ruta de acceso completa al usar las funciones [**LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**LoadLibraryEx,**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)o [**ShellExecute.**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea)
-   Use las marcas LOAD LIBRARY SEARCH con la función LoadLibraryEx o use estas marcas con la función \_ \_ [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) [](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) para establecer un orden de búsqueda de DLL para un proceso y, a continuación, use las funciones [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory para**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) modificar la lista. Para obtener más información, vea [Orden de búsqueda de la biblioteca de vínculos dinámicos.](dynamic-link-library-search-order.md)

    **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Estas marcas y funciones están disponibles en sistemas con [KB2533623](https://support.microsoft.com/kb/2533623) instalado.

-   En sistemas con [KB2533623](https://support.microsoft.com/kb/2533623) instalado, use las marcas LOAD LIBRARY SEARCH con la función LoadLibraryEx o use estas marcas con la función \_ \_ [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) [](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) para establecer un orden de búsqueda de DLL para un proceso y, a continuación, use las funciones [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) para modificar la lista. Para obtener más información, vea [Orden de búsqueda de la biblioteca de vínculos dinámicos.](dynamic-link-library-search-order.md)
-   Considere la posibilidad [de usar el redireccionamiento](dynamic-link-library-redirection.md) de DLL [o un manifiesto](/windows/desktop/SbsCs/manifests) para asegurarse de que la aplicación usa el archivo DLL correcto.
-   Cuando use el orden de búsqueda estándar, asegúrese de que el modo de búsqueda de DLL seguro está habilitado. Esto coloca el directorio actual del usuario más adelante en el orden de búsqueda, lo que aumenta las posibilidades de Windows encontrar una copia legítima del archivo DLL antes de una copia malintencionada. Caja fuerte El modo de búsqueda dll está habilitado de forma predeterminada a partir de Windows XP con Service Pack 2 (SP2) y se controla mediante el valor del Registro SafeDllSearchMode del Administrador de sesiones de control **\_ \_ \\ \\ HKEY \\ \\ LOCAL MACHINE.** \\  Para obtener más información, vea [Orden de búsqueda de la biblioteca de vínculos dinámicos.](dynamic-link-library-search-order.md)
-   Considere la posibilidad de quitar el directorio actual de la ruta de acceso de búsqueda estándar mediante una llamada a [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) con una cadena vacía (""). Esto debe hacerse una vez al principio del proceso de inicialización, no antes y después de las llamadas [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Tenga en cuenta **que SetDllDirectory afecta** a todo el proceso y que varios subprocesos que llaman a **SetDllDirectory** con valores diferentes pueden provocar un comportamiento indefinido. Si la aplicación carga archivos DLL de terceros, pruebe detenidamente para identificar las incompatibilidades.
-   No use la función [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para recuperar una ruta de acceso a un archivo DLL para una llamada [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) posterior a menos que el modo de búsqueda de procesos seguros esté habilitado. Cuando el modo de búsqueda de procesos seguros no está habilitado, la función **SearchPath** usa un orden de búsqueda diferente al de **LoadLibrary** y es probable que primero busque en el directorio actual del usuario el archivo DLL especificado. Para habilitar el modo de búsqueda de procesos seguros para la función **SearchPath,** use la función [**SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) con BASE \_ SEARCH PATH ENABLE SAFE \_ \_ \_ \_ SEARCHMODE. Esto mueve el directorio actual al final de la lista de búsqueda **searchPath** durante la vida del proceso. Tenga en cuenta que el directorio actual no se quita de la ruta de acceso de búsqueda, por lo que si el sistema no encuentra una copia legítima del archivo DLL antes de llegar al directorio actual, la aplicación sigue siendo vulnerable. Al igual [**que con SetDllDirectory,**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)la llamada **a SetSearchPathMode** debe realizarse al principio de la inicialización del proceso y afecta a todo el proceso. Si la aplicación carga archivos DLL de terceros, pruebe detenidamente para identificar las incompatibilidades.
-   No realice suposiciones sobre la versión del sistema operativo en función de una [**llamada LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) que busque un archivo DLL. Si la aplicación se ejecuta en un entorno donde el archivo DLL no está legítimamente presente, pero hay una copia malintencionada del archivo DLL en la ruta de búsqueda, se puede cargar la copia malintencionada del archivo DLL. En su lugar, use las técnicas recomendadas descritas [en Obtención de la versión del sistema](/windows/desktop/SysInfo/getting-the-system-version).

La herramienta Monitor de procesos se puede usar para ayudar a identificar las operaciones de carga de DLL que podrían ser vulnerables. La herramienta Monitor de procesos se puede descargar desde <https://technet.microsoft.com/sysinternals/bb896645.aspx> .

En el procedimiento siguiente se describe cómo usar el Monitor de procesos para examinar las operaciones de carga de DLL en la aplicación.

**Para usar el Monitor de procesos para examinar las operaciones de carga de DLL en la aplicación**

1.  Inicie el Monitor de procesos.
2.  En el Monitor de procesos, incluya los siguientes filtros:
    -   La operación es CreateFile
    -   La operación es LoadImage
    -   La ruta de acceso contiene .cpl
    -   La ruta de acceso contiene .dll
    -   La ruta de acceso contiene .drv
    -   La ruta de acceso contiene .exe
    -   La ruta de acceso contiene .ocx
    -   La ruta de acceso contiene .scr
    -   La ruta de acceso contiene .sys
3.  Excluya los filtros siguientes:
    -   Nombre del proceso procmon.exe
    -   Nombre del proceso Procmon64.exe
    -   El nombre del proceso es System
    -   La operación comienza con IRP \_ MJ\_
    -   La operación comienza con FASTIO\_
    -   El resultado es SUCCESS
    -   La ruta de acceso termina con pagefile.sys
4.  Intente iniciar la aplicación con el directorio actual establecido en un directorio específico. Por ejemplo, haga doble clic en un archivo con una extensión cuyo controlador de archivos esté asignado a la aplicación.
5.  Compruebe la salida del Monitor de procesos para ver las rutas de acceso que parecen sospechosas, como una llamada al directorio actual para cargar un archivo DLL. Este tipo de llamada puede indicar una vulnerabilidad en la aplicación.

 

 
