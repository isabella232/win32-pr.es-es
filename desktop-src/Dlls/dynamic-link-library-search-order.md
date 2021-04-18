---
description: Las aplicaciones pueden controlar la ubicación desde la que se carga un archivo DLL mediante la especificación de una ruta de acceso completa o mediante otro mecanismo, como un manifiesto. Si no se utilizan estos métodos, el sistema busca el archivo DLL en tiempo de carga como se describe en este tema.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Orden de búsqueda de la biblioteca de vínculos dinámicos
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 928cf9030e24c91145ae95e1eed680017bf68533
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/04/2021
ms.locfileid: "104536400"
---
# <a name="dynamic-link-library-search-order"></a>Orden de búsqueda de la biblioteca de vínculos dinámicos

Un sistema puede contener varias versiones de la misma biblioteca de vínculos dinámicos (DLL). Las aplicaciones pueden controlar la ubicación desde la que se carga un archivo DLL mediante la especificación de una ruta de acceso completa o mediante otro mecanismo, como un manifiesto. Si no se utilizan estos métodos, el sistema busca el archivo DLL en tiempo de carga como se describe en este tema.

-   [Factores que afectan a la búsqueda](#factors-that-affect-searching)
-   [Buscar el orden de las aplicaciones para UWP](#search-order-for-uwp-apps)
    -   [Orden de búsqueda estándar para aplicaciones para UWP](#standard-search-order-for-uwp-apps)
    -   [Orden de búsqueda alternativo para aplicaciones para UWP](#alternate-search-order-for-uwp-apps)
-   [Orden de búsqueda de aplicaciones de escritorio](#search-order-for-desktop-applications)
    -   [Orden de búsqueda estándar para aplicaciones de escritorio](#standard-search-order-for-desktop-applications)
    -   [Orden de búsqueda alternativo para aplicaciones de escritorio](#alternate-search-order-for-desktop-applications)
    -   [Buscar el orden usando las marcas de **\_ \_ búsqueda** de la biblioteca de carga](/windows)
-   [Temas relacionados](#related-topics)

## <a name="factors-that-affect-searching"></a>Factores que afectan a la búsqueda

Los siguientes factores influyen en si el sistema busca un archivo DLL:

-   Si un archivo DLL con el mismo nombre de módulo ya está cargado en la memoria, el sistema comprueba solo la redirección y un manifiesto antes de resolver el archivo DLL cargado, con independencia del directorio en el que se encuentre. El sistema no busca el archivo DLL.
-   Si el archivo DLL está en la lista de archivos dll conocidos para la versión de Windows en la que se está ejecutando la aplicación, el sistema utiliza su copia del archivo DLL conocido (y los archivos DLL dependientes del archivo DLL conocido, si existen) en lugar de buscar el archivo DLL. Para obtener una lista de los archivos dll conocidos en el sistema actual, consulte la siguiente clave del registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Session Manager \\ KnownDLLs**.
-   Si un archivo DLL tiene dependencias, el sistema busca los archivos DLL dependientes como si estuvieran cargados con solo los nombres de los módulos. Esto es así incluso si el primer archivo DLL se cargó especificando una ruta de acceso completa.

## <a name="search-order-for-uwp-apps"></a>Buscar el orden de las aplicaciones para UWP

Cuando una aplicación de UWP para Windows 10 (o una aplicación de la tienda para Windows 8. x) carga un módulo empaquetado mediante una llamada a la función [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) , el archivo DLL debe estar en el gráfico de dependencias del paquete del proceso. Para obtener más información, vea **LoadPackagedLibrary**. Cuando una aplicación para UWP carga un módulo por otros medios y no especifica una ruta de acceso completa, el sistema busca el archivo DLL y sus dependencias en tiempo de carga, tal y como se describe en esta sección.

Antes de que el sistema busque un archivo DLL, comprueba lo siguiente:

-   Si un archivo DLL con el mismo nombre de módulo ya está cargado en la memoria, el sistema utiliza el archivo DLL cargado, con independencia del directorio en el que se encuentre. El sistema no busca el archivo DLL.
-   Si el archivo DLL está en la lista de archivos dll conocidos para la versión de Windows en la que se está ejecutando la aplicación, el sistema utiliza su copia del archivo DLL conocido (y los archivos DLL dependientes del archivo DLL conocido, si existen). El sistema no busca el archivo DLL. Para obtener una lista de los archivos dll conocidos en el sistema actual, consulte la siguiente clave del registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Session Manager \\ KnownDLLs**.

Si el sistema debe buscar un módulo o sus dependencias, siempre usa el orden de búsqueda de las aplicaciones para UWP incluso si una dependencia no es código de aplicación de UWP.

### <a name="standard-search-order-for-uwp-apps"></a>Orden de búsqueda estándar para aplicaciones para UWP

Si el módulo no está ya cargado o en la lista de archivos dll conocidos, el sistema busca en estas ubicaciones en este orden:

1.  Gráfico de dependencias del paquete del proceso. Este es el paquete de la aplicación más las dependencias especificadas como `<PackageDependency>` en la `<Dependencies>` sección del manifiesto del paquete de la aplicación. Las dependencias se buscan en el orden en el que aparecen en el manifiesto.
2.  Directorio desde el que se cargó el proceso de llamada.
3.  Directorio del sistema (% SystemRoot% \\ system32).

Si un archivo DLL tiene dependencias, el sistema busca los archivos DLL dependientes como si estuvieran cargados con solo los nombres de los módulos. Esto es así incluso si el primer archivo DLL se cargó especificando una ruta de acceso completa.

### <a name="alternate-search-order-for-uwp-apps"></a>Orden de búsqueda alternativo para aplicaciones para UWP

Si un módulo cambia el orden de búsqueda estándar mediante una llamada a la función [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con la **carga \_ con la \_ \_ \_ ruta de búsqueda modificada**, el sistema busca en el directorio en el que se cargó el módulo especificado, en lugar del directorio del proceso de llamada. El sistema busca en estas ubicaciones en este orden:

1.  Gráfico de dependencias del paquete del proceso. Este es el paquete de la aplicación más las dependencias especificadas como `<PackageDependency>` en la `<Dependencies>` sección del manifiesto del paquete de la aplicación. Las dependencias se buscan en el orden en el que aparecen en el manifiesto.
2.  Directorio desde el que se cargó el módulo especificado.
3.  Directorio del sistema (% SystemRoot% \\ system32).

## <a name="search-order-for-desktop-applications"></a>Orden de búsqueda de aplicaciones de escritorio

Las aplicaciones de escritorio pueden controlar la ubicación desde la que se carga un archivo DLL mediante la especificación de una ruta de acceso completa, el uso de la [redirección de dll](dynamic-link-library-redirection.md)o el uso de un [manifiesto](/windows/desktop/SbsCs/manifests). Si no se usa ninguno de estos métodos, el sistema busca el archivo DLL en tiempo de carga tal y como se describe en esta sección.

Antes de que el sistema busque un archivo DLL, comprueba lo siguiente:

-   Si un archivo DLL con el mismo nombre de módulo ya está cargado en la memoria, el sistema utiliza el archivo DLL cargado, con independencia del directorio en el que se encuentre. El sistema no busca el archivo DLL.
-   Si el archivo DLL está en la lista de archivos dll conocidos para la versión de Windows en la que se está ejecutando la aplicación, el sistema utiliza su copia del archivo DLL conocido (y los archivos DLL dependientes del archivo DLL conocido, si existen). El sistema no busca el archivo DLL. Para obtener una lista de los archivos dll conocidos en el sistema actual, consulte la siguiente clave del registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Session Manager \\ KnownDLLs**.

Si un archivo DLL tiene dependencias, el sistema busca los archivos DLL dependientes como si estuvieran cargados con solo los nombres de los módulos. Esto es así incluso si el primer archivo DLL se cargó especificando una ruta de acceso completa.

> [!IMPORTANT]
> Si un atacante obtiene el control de uno de los directorios en los que se realiza la búsqueda, puede colocar una copia malintencionada del archivo DLL en ese directorio. Para obtener más formas de evitar estos ataques, consulte [seguridad de la biblioteca de vínculos dinámicos](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Orden de búsqueda estándar para aplicaciones de escritorio

El orden de búsqueda de DLL estándar que usa el sistema depende de si está habilitado o deshabilitado el modo de búsqueda de archivos DLL seguros. El modo de búsqueda segura de DLL coloca el directorio actual del usuario más adelante en el orden de búsqueda.

El modo de búsqueda segura de DLL está habilitado de forma predeterminada. Para deshabilitar esta característica, cree el valor del registro **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Session Manager** \\ **SafeDllSearchMode** y establézcalo en 0. La llamada a la función [**SetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) deshabilita **SafeDllSearchMode** de forma eficaz mientras el directorio especificado se encuentra en la ruta de búsqueda y cambia el orden de búsqueda tal y como se describe en este tema.

Si **SafeDllSearchMode** está habilitado, el orden de búsqueda es el siguiente:

1.  Directorio desde el que se cargó la aplicación.
2.  Directorio del sistema. Utilice la función [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
3.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
4.  El directorio de Windows. Utilice la función [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
5.  El directorio actual.
6.  Los directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del registro de **rutas** de acceso de la aplicación. La clave de rutas de acceso de la **aplicación** no se usa al calcular la ruta de búsqueda de dll.

Si **SafeDllSearchMode** está deshabilitado, el orden de búsqueda es el siguiente:

1.  Directorio desde el que se cargó la aplicación.
2.  El directorio actual.
3.  Directorio del sistema. Utilice la función [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
4.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
5.  El directorio de Windows. Utilice la función [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
6.  Los directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del registro de **rutas** de acceso de la aplicación. La clave de rutas de acceso de la **aplicación** no se usa al calcular la ruta de búsqueda de dll.

### <a name="alternate-search-order-for-desktop-applications"></a>Orden de búsqueda alternativo para aplicaciones de escritorio

Se puede cambiar el orden de búsqueda estándar que usa el sistema mediante una llamada a la función [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con la **carga \_ con la \_ \_ \_ ruta de búsqueda modificada**. El orden de búsqueda estándar también se puede cambiar mediante una llamada a la función [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

> [!NOTE]
> El orden de búsqueda estándar del proceso también se verá afectado por la llamada a la función [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) en el proceso primario antes del inicio del proceso actual.

Si especifica una estrategia de búsqueda alternativa, su comportamiento continúa hasta que se hayan encontrado todos los módulos ejecutables asociados. Una vez que el sistema inicia el procesamiento de rutinas de inicialización de DLL, el sistema vuelve a la estrategia de búsqueda estándar.

La función [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) admite un orden de búsqueda alternativo si la llamada especifica la **carga con la \_ \_ \_ \_ ruta de búsqueda modificada** y el parámetro *lpFileName* especifica una ruta de acceso absoluta.

Tenga en cuenta que la estrategia de búsqueda estándar y la estrategia de búsqueda alternativa especificada por [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con la **\_ \_ \_ \_ ruta de búsqueda modificada** difieren solo en una manera: la búsqueda estándar comienza en el directorio de la aplicación que realiza la llamada y la búsqueda alternativa comienza en el directorio del módulo ejecutable que se está cargando en **loadlibraryex** .

Si **SafeDllSearchMode** está habilitado, el orden de búsqueda alternativo es el siguiente:

1.  El directorio especificado por *lpFileName*.
2.  Directorio del sistema. Utilice la función [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
3.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
4.  El directorio de Windows. Utilice la función [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
5.  El directorio actual.
6.  Los directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del registro de **rutas** de acceso de la aplicación. La clave de rutas de acceso de la **aplicación** no se usa al calcular la ruta de búsqueda de dll.

Si **SafeDllSearchMode** está deshabilitado, el orden de búsqueda alternativo es el siguiente:

1.  El directorio especificado por *lpFileName*.
2.  El directorio actual.
3.  Directorio del sistema. Utilice la función [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio.
4.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca.
5.  El directorio de Windows. Utilice la función [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
6.  Los directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del registro de **rutas** de acceso de la aplicación. La clave de rutas de acceso de la **aplicación** no se usa al calcular la ruta de búsqueda de dll.

La función [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) admite un orden de búsqueda alternativo si el parámetro *lpPathName* especifica una ruta de acceso. El orden de búsqueda alternativo es el siguiente:

1.  Directorio desde el que se cargó la aplicación.
2.  El directorio especificado por el parámetro *lpPathName* de [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya).
3.  Directorio del sistema. Utilice la función [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obtener la ruta de acceso de este directorio. El nombre de este directorio es system32.
4.  Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de acceso de este directorio, pero se busca. El nombre de este directorio es System.
5.  El directorio de Windows. Utilice la función [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obtener la ruta de acceso de este directorio.
6.  Los directorios que aparecen en la variable de entorno PATH. Tenga en cuenta que esto no incluye la ruta de acceso por aplicación especificada por la clave del registro de **rutas** de acceso de la aplicación. La clave de rutas de acceso de la **aplicación** no se usa al calcular la ruta de búsqueda de dll.

Si el parámetro *lpPathName* es una cadena vacía, la llamada quita el directorio actual del orden de búsqueda.

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) deshabilita de forma eficaz el modo de búsqueda de dll segura mientras el directorio especificado está en la ruta de búsqueda. Para restaurar el modo de búsqueda de DLL segura según el valor del registro **SafeDllSearchMode** y restaurar el directorio actual en el orden de búsqueda, llame a **SetDllDirectory** con *lpPathName* como null.

### <a name="search-order-using-load_library_search-flags"></a>Buscar el orden usando las marcas de **\_ \_ búsqueda** de la biblioteca de carga

Una aplicación puede especificar un orden de búsqueda mediante el uso de una o más marcas de **\_ \_ búsqueda** de la biblioteca de carga con la función [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Una aplicación también puede utilizar las marcas de **\_ \_ búsqueda** de la biblioteca de carga con la función [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) para establecer un orden de búsqueda de dll para un proceso. La aplicación puede especificar directorios adicionales para el orden de búsqueda de DLL de proceso mediante las funciones [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

Los directorios en los que se realiza la búsqueda dependen de las marcas especificadas con [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Si se usa más de una marca, se busca en los directorios correspondientes en el orden siguiente:

1.  Directorio que contiene el archivo DLL (**cargar \_ \_ Directorio de \_ \_ carga de \_ dll de búsqueda de biblioteca**). Solo se busca en este directorio las dependencias de la DLL que se va a cargar.
2.  Directorio de la aplicación (carga de la **\_ aplicación de \_ búsqueda de \_ \_ biblioteca**).
3.  Las rutas de acceso se agregan explícitamente con la función [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) (**cargar \_ directorios de usuario de \_ búsqueda \_ \_ de biblioteca**) o la función [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) . Si se ha agregado más de una ruta, no se especifica el orden en el que se buscan las rutas de acceso.
4.  Directorio del sistema (**Load \_ Library \_ Search \_ system32**).

Si la aplicación no llama a [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con ninguna marca de **\_ \_ búsqueda** de la biblioteca de carga o establece un orden de búsqueda de dll para el proceso, el sistema busca los archivos DLL mediante el orden de búsqueda estándar o el orden de búsqueda alternativo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[Registro de aplicaciones](/windows/desktop/shell/app-registration)
</dt> <dt>

[Redirección de biblioteca de vínculos dinámicos](dynamic-link-library-redirection.md)
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

 

 