---
description: Las aplicaciones pueden controlar la ubicación desde la que se carga un archivo DLL especificando una ruta de acceso completa o usando otro mecanismo, como un manifiesto. Si no se usan estos métodos, el sistema busca el archivo DLL en tiempo de carga, como se describe en este tema.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Orden de búsqueda de la biblioteca de vínculos dinámicos
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: e2abe21e0283adab4fbc3c17db6503772e20c217cf3019ea775812b0f45e5145
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083445"
---
# <a name="dynamic-link-library-search-order"></a>Orden de búsqueda de la biblioteca de vínculos dinámicos

Un sistema puede contener varias versiones de la misma biblioteca de vínculos dinámicos (DLL). Las aplicaciones pueden controlar la ubicación desde la que se carga un archivo DLL especificando una ruta de acceso completa o usando otro mecanismo, como un manifiesto. Si no se usan estos métodos, el sistema busca el archivo DLL en tiempo de carga, como se describe en este tema.

-   [Factores que afectan a la búsqueda](#factors-that-affect-searching)
-   [Orden de búsqueda de aplicaciones para UWP](#search-order-for-uwp-apps)
    -   [Orden de búsqueda estándar para aplicaciones para UWP](#standard-search-order-for-uwp-apps)
    -   [Orden de búsqueda alternativo para aplicaciones para UWP](#alternate-search-order-for-uwp-apps)
-   [Orden de búsqueda para aplicaciones de escritorio](#search-order-for-desktop-applications)
    -   [Orden de búsqueda estándar para aplicaciones de escritorio](#standard-search-order-for-desktop-applications)
    -   [Orden de búsqueda alternativo para aplicaciones de escritorio](#alternate-search-order-for-desktop-applications)
    -   [Orden de búsqueda mediante **marcas DE BÚSQUEDA DE \_ \_ LOAD LIBRARY**](#search-order-using-load_library_search-flags)
-   [Temas relacionados](#related-topics)

## <a name="factors-that-affect-searching"></a>Factores que afectan a la búsqueda

Los siguientes factores afectan a si el sistema busca un archivo DLL:

-   Si un archivo DLL con el mismo nombre de módulo ya está cargado en memoria, el sistema solo comprueba si hay redireccionamiento y un manifiesto antes de resolver en el archivo DLL cargado, independientemente del directorio en el que se encuentra. El sistema no busca el archivo DLL.
-   Si el archivo DLL está en la lista de archivos DLL conocidos de la versión de Windows en la que se ejecuta la aplicación, el sistema usa su copia del archivo DLL conocido (y los archivos DLL dependientes del archivo DLL conocidos, si los hay) en lugar de buscar el archivo DLL. Para obtener una lista de archivos DLL conocidos en el sistema actual, vea la siguiente clave del Registro: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.
-   Si un archivo DLL tiene dependencias, el sistema busca los archivos DLL dependientes como si se hubieran cargado solo con sus nombres de módulo. Esto es así incluso si el primer archivo DLL se cargó especificando una ruta de acceso completa.

## <a name="search-order-for-uwp-apps"></a>Orden de búsqueda de aplicaciones para UWP

Cuando una aplicación para UWP para Windows 10 (o una aplicación de la Tienda para Windows 8.x) carga un módulo empaquetado llamando a la [**función LoadPackagedLibrary,**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) el archivo DLL debe estar en el gráfico de dependencias del paquete del proceso. Para obtener más información, **vea LoadPackagedLibrary**. Cuando una aplicación para UWP carga un módulo por otros medios y no especifica una ruta de acceso completa, el sistema busca el archivo DLL y sus dependencias en tiempo de carga, como se describe en esta sección.

Antes de que el sistema busque un archivo DLL, comprueba lo siguiente:

-   Si un archivo DLL con el mismo nombre de módulo ya está cargado en memoria, el sistema usa el archivo DLL cargado, independientemente del directorio en el que se encuentra. El sistema no busca el archivo DLL.
-   Si el archivo DLL está en la lista de archivos DLL conocidos de la versión de Windows en la que se ejecuta la aplicación, el sistema usa su copia del archivo DLL conocido (y los archivos DLL dependientes del archivo DLL conocidos, si los hay). El sistema no busca el archivo DLL. Para obtener una lista de archivos DLL conocidos en el sistema actual, vea la siguiente clave del Registro: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Si el sistema debe buscar un módulo o sus dependencias, siempre usa el orden de búsqueda para las aplicaciones para UWP incluso si una dependencia no es código de aplicación para UWP.

### <a name="standard-search-order-for-uwp-apps"></a>Orden de búsqueda estándar para aplicaciones para UWP

Si el módulo aún no está cargado o está en la lista de archivos DLL conocidos, el sistema busca estas ubicaciones en este orden:

1.  Gráfico de dependencias del paquete del proceso. Este es el paquete de la aplicación más las dependencias especificadas como en la sección del manifiesto `<PackageDependency>` del paquete de la `<Dependencies>` aplicación. Las dependencias se buscan en el orden en que aparecen en el manifiesto.
2.  Directorio desde el que se cargó el proceso de llamada.
3.  Directorio del sistema (%SystemRoot% \\ system32).

Si un archivo DLL tiene dependencias, el sistema busca los archivos DLL dependientes como si se hubieran cargado solo con sus nombres de módulo. Esto es así incluso si el primer archivo DLL se cargó especificando una ruta de acceso completa.

### <a name="alternate-search-order-for-uwp-apps"></a>Orden de búsqueda alternativo para aplicaciones para UWP

Si un módulo cambia el orden de búsqueda estándar mediante una llamada a la función [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH**, el sistema busca en el directorio desde el que se cargó el módulo especificado en lugar del directorio del proceso de llamada. El sistema busca estas ubicaciones en este orden:

1.  Gráfico de dependencias del paquete del proceso. Este es el paquete de la aplicación más las dependencias especificadas como en la sección del manifiesto `<PackageDependency>` del paquete de la `<Dependencies>` aplicación. Las dependencias se buscan en el orden en que aparecen en el manifiesto.
2.  Directorio desde el que se cargó el módulo especificado.
3.  Directorio del sistema (%SystemRoot% \\ system32).

## <a name="search-order-for-desktop-applications"></a>Orden de búsqueda para aplicaciones de escritorio

Las aplicaciones de escritorio pueden controlar la ubicación desde la que se carga un archivo DLL especificando una ruta de acceso completa, mediante el redireccionamiento [de DLL](dynamic-link-library-redirection.md)o mediante un [manifiesto](/windows/desktop/SbsCs/manifests). Si no se usa ninguno de estos métodos, el sistema busca el archivo DLL en tiempo de carga, como se describe en esta sección.

Antes de que el sistema busque un archivo DLL, comprueba lo siguiente:

-   Si un archivo DLL con el mismo nombre de módulo ya está cargado en memoria, el sistema usa el archivo DLL cargado, independientemente del directorio en el que se encuentra. El sistema no busca el archivo DLL.
-   Si el archivo DLL está en la lista de archivos DLL conocidos de la versión de Windows en la que se ejecuta la aplicación, el sistema usa su copia del archivo DLL conocido (y los archivos DLL dependientes del archivo DLL conocidos, si los hay). El sistema no busca el archivo DLL. Para obtener una lista de archivos DLL conocidos en el sistema actual, vea la siguiente clave del Registro: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Si un archivo DLL tiene dependencias, el sistema busca los archivos DLL dependientes como si se hubieran cargado solo con sus nombres de módulo. Esto es así incluso si el primer archivo DLL se cargó especificando una ruta de acceso completa.

> [!IMPORTANT]
> Si un atacante obtiene el control de uno de los directorios en los que se busca, puede colocar una copia malintencionada del archivo DLL en ese directorio. Para obtener maneras de ayudar a evitar estos ataques, vea [Seguridad de la biblioteca de vínculos dinámicos](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Orden de búsqueda estándar para aplicaciones de escritorio

El orden de búsqueda de DLL estándar utilizado por el sistema depende de si el modo de búsqueda dll seguro está habilitado o deshabilitado. Caja fuerte El modo de búsqueda dll coloca el directorio actual del usuario más adelante en el orden de búsqueda.

Caja fuerte El modo de búsqueda dll está habilitado de forma predeterminada. Para deshabilitar esta característica, cree el valor del Registro SafeDllSearchMode del **HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Control Session \\ Manager** y establézcalo \\  en 0. Al llamar a la función [**SetDllDirectory,**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) se deshabilita de forma eficaz **SafeDllSearchMode** mientras el directorio especificado está en la ruta de acceso de búsqueda y cambia el orden de búsqueda, tal como se describe en este tema.

Si **SafeDllSearchMode** está habilitado, el orden de búsqueda es el siguiente:

1.  Directorio desde el que se cargó la aplicación.
2.  Directorio del sistema. Use la [**función GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
3.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
4.  El directorio de Windows. Use la [**función GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
5.  El directorio actual.
6.  Directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del Registro **rutas de** acceso de la aplicación. La **clave Rutas de acceso** de la aplicación no se usa al calcular la ruta de búsqueda dll.

Si **SafeDllSearchMode** está deshabilitado, el orden de búsqueda es el siguiente:

1.  Directorio desde el que se cargó la aplicación.
2.  El directorio actual.
3.  Directorio del sistema. Use la [**función GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
4.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
5.  El directorio de Windows. Use la [**función GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
6.  Directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del Registro **rutas de** acceso de la aplicación. La **clave Rutas de acceso** de la aplicación no se usa al calcular la ruta de búsqueda dll.

### <a name="alternate-search-order-for-desktop-applications"></a>Orden de búsqueda alternativo para aplicaciones de escritorio

El orden de búsqueda estándar utilizado por el sistema se puede cambiar llamando a la [**función LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) **con LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH**. El orden de búsqueda estándar también se puede cambiar llamando a la [**función SetDllDirectory.**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)

> [!NOTE]
> El orden de búsqueda estándar del proceso también se verá afectado al llamar a la función [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) en el proceso primario antes del inicio del proceso actual.

Si especifica una estrategia de búsqueda alternativa, su comportamiento continúa hasta que se han ubicado todos los módulos ejecutables asociados. Una vez que el sistema inicia el procesamiento de rutinas de inicialización de DLL, el sistema vuelve a la estrategia de búsqueda estándar.

La [**función LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) admite un orden de búsqueda alternativo si la llamada especifica **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH** y el parámetro *lpFileName* especifica una ruta de acceso absoluta.

Tenga en cuenta que la estrategia de búsqueda estándar y la estrategia de búsqueda alternativa especificada por [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH** difieren de una sola manera: la búsqueda estándar comienza en el directorio de la aplicación que realiza la llamada y la búsqueda alternativa comienza en el directorio del módulo ejecutable que **carga LoadLibraryEx.**

Si **SafeDllSearchMode** está habilitado, el orden de búsqueda alternativo es el siguiente:

1.  Directorio especificado por *lpFileName*.
2.  Directorio del sistema. Use la [**función GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
3.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
4.  El directorio de Windows. Use la [**función GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
5.  El directorio actual.
6.  Directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del Registro **Rutas de acceso** de la aplicación. La **clave Rutas de** acceso de la aplicación no se usa al calcular la ruta de acceso de búsqueda dll.

Si **SafeDllSearchMode** está deshabilitado, el orden de búsqueda alternativo es el siguiente:

1.  Directorio especificado por *lpFileName*.
2.  El directorio actual.
3.  Directorio del sistema. Use la [**función GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
4.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
5.  El directorio de Windows. Use la [**función GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
6.  Directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del Registro **Rutas de acceso** de la aplicación. La **clave Rutas de** acceso de la aplicación no se usa al calcular la ruta de acceso de búsqueda dll.

La [**función SetDllDirectory admite**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) un orden de búsqueda alternativo si el parámetro *lpPathName* especifica una ruta de acceso. El orden de búsqueda alternativo es el siguiente:

1.  Directorio desde el que se cargó la aplicación.
2.  Directorio especificado por el parámetro *lpPathName* [**de SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya).
3.  Directorio del sistema. Use la [**función GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio. El nombre de este directorio es System32.
4.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca. El nombre de este directorio es System.
5.  El directorio de Windows. Use la [**función GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
6.  Directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del Registro **Rutas de acceso** de la aplicación. La **clave Rutas de** acceso de la aplicación no se usa al calcular la ruta de acceso de búsqueda dll.

Si el *parámetro lpPathName* es una cadena vacía, la llamada quita el directorio actual del orden de búsqueda.

[**SetDllDirectory deshabilita eficazmente**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) el modo de búsqueda de ARCHIVOS DLL seguros mientras el directorio especificado está en la ruta de búsqueda. Para restaurar el modo de búsqueda de ARCHIVOS DLL seguros en función del valor del Registro **SafeDllSearchMode** y restaurar el directorio actual en el orden de búsqueda, llame a **SetDllDirectory** con *lpPathName* como NULL.

### <a name="search-order-using-load_library_search-flags"></a>Orden de búsqueda mediante **marcas DE BÚSQUEDA DE BIBLIOTECA \_ \_ DE** CARGA

Una aplicación puede especificar un orden de búsqueda mediante una o varias marcas **DE BÚSQUEDA DE LOAD \_ \_ LIBRARY** con la función [**LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) Una aplicación también puede usar marcas **DE BÚSQUEDA DE LOAD \_ \_ LIBRARY** con la función [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) para establecer un orden de búsqueda dll para un proceso. La aplicación puede especificar directorios adicionales para el orden de búsqueda de dll de proceso mediante las [**funciones AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) [**o SetDllDirectory.**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)

Los directorios en los que se busca dependen de las marcas especificadas [**con SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) o [**LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) Si se usa más de una marca, se busca en los directorios correspondientes en el orden siguiente:

1.  Directorio que contiene el archivo DLL (**LOAD LIBRARY SEARCH DLL LOAD \_ \_ \_ \_ \_ DIR**). Solo se busca en este directorio las dependencias del archivo DLL que se va a cargar.
2.  El directorio de la aplicación (**LOAD LIBRARY SEARCH APPLICATION \_ \_ \_ \_ DIR**).
3.  Rutas de acceso agregadas explícitamente con la [**función AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) **(LOAD \_ LIBRARY SEARCH \_ USER \_ \_ DIRS)** o [**la función SetDllDirectory.**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) Si se ha agregado más de una ruta de acceso, no se especifica el orden en el que se buscan las rutas de acceso.
4.  Directorio del sistema (**LOAD \_ LIBRARY SEARCH \_ \_ SYSTEM32**).

Si la aplicación no llama a [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con ninguna marca DE BÚSQUEDA DE **LOAD \_ LIBRARY \_** ni establece un orden de búsqueda dll para el proceso, el sistema busca archivos DLL mediante el orden de búsqueda estándar o el orden de búsqueda alternativo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[Registro de aplicaciones](/windows/desktop/shell/app-registration)
</dt> <dt>

[Redireccionamiento de la biblioteca de vínculos dinámicos](dynamic-link-library-redirection.md)
</dt> <dt>

[Seguridad de la biblioteca de vínculos dinámicos](dynamic-link-library-security.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
</dt> <dt>

[**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)
</dt> <dt>

[**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)
</dt> <dt>

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
</dt> <dt>

[Componentes en paralelo](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 
