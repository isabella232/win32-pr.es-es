---
description: Muestra cómo registrarse como proveedor raíz de sincronización e integrar un proveedor de almacenamiento en la nube en el nivel raíz del panel de navegación.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: Integración de un proveedor de Storage nube
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e218caa292e2b85e13e00374562c172158be8bb2f062f25b47979902046282c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458205"
---
# <a name="integrate-a-cloud-storage-provider"></a>Integración de un proveedor de Storage nube

Cuando tiene un proveedor de almacenamiento en la nube, hay un par de pasos que debe seguir para proporcionar una experiencia coherente y preferida para el usuario. Estos dos elementos se registran como proveedor raíz de sincronización e integran la aplicación en el nivel raíz del panel de navegación.

> [!IMPORTANT]
> La integración del proveedor de almacenamiento en la nube solo se admite a partir de Windows 10.

 

Lo primero es registrarse como proveedor raíz de sincronización. Esto permite que Windows Shell sepa sobre la aplicación y que la aplicación será responsable de sincronizar los archivos en la raíz de sincronización. Esto también permitirá que otras aplicaciones sepan que está sincronizando estos archivos para que puedan responder correctamente. A continuación, otras aplicaciones [**pueden usar StorageFile.Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) para obtener el [**displayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) y el [**identificador**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) de la aplicación.

Para registrarse como proveedor raíz de sincronización, deberá crear varias entradas del Registro. Antes de proporcionar la lista de pares clave-valor, estos son algunos marcadores de posición que debe reemplazar por sus propios datos de aplicación.

-   *\[ identificador del \] proveedor de* almacenamiento: el nombre del proveedor de almacenamiento en la nube. Este nombre debe ser coherente independientemente de la versión de la aplicación. Un ejemplo de esto es OneDrive.
-   *\[ Windows SID: \]* identificador único Windows SID que identifica al usuario. Si la aplicación admite varias instalaciones para varios usuarios en un solo equipo, esta pieza es necesaria.
-   *\[ Id. \] de* cuenta: identificador del proveedor de servicios de la cuenta actual de este usuario. Algunos proveedores requieren la capacidad de proporcionar varias raíces de sincronización para un usuario. Un ejemplo de esto es un trabajo y una cuenta personal. El *identificador de* cuenta le permite tener varias cuentas registradas para un usuario. Si el proveedor admite varias raíces de sincronización por usuario, se requiere esta parte.

Estos marcadores de posición se combinan para formar el identificador raíz de sincronización. Debe colocar un **.** carácter entre cada uno de los marcadores de posición al formar el identificador raíz de sincronización. Estos son los pares clave-valor que deben crearse.

-   **HKLM \\ Software \\ Microsoft Windows El explorador de \\ \\ \\ \\ currentVersion SyncRootManager \\** identificador del proveedor de _\[ almacenamiento \]_*_!_* _\[ Windows SID \]_*_!_* _\[ Id. \] de_*_\\ cuenta DisplayNameResource:_* apunta al recurso donde Windows Shell u otras aplicaciones pueden obtener un nombre descriptivo para la raíz de sincronización.
-   **HKLM \\ Software \\ Microsoft Windows El explorador de \\ \\ \\ \\ currentVersion SyncRootManager \\** identificador del proveedor de _\[ almacenamiento \]_*_!_* _\[ Windows SID \]_*_!_* _\[ Icono \] de id._*_\\ de cuentaResource:_* apunta al recurso donde Windows Shell u otras aplicaciones pueden obtener un icono para la raíz de sincronización.
-   **HKLM \\ Software \\ Microsoft Windows El explorador de \\ \\ \\ \\ currentVersion SyncRootManager \\** identificador del proveedor de _\[ almacenamiento \]_*_!_* _\[ Windows SID \]_*_!_* _\[ Id. \] de_*_\\ cuenta \\ UserSyncRoots_*_\[ Windows SID: \]_ la ubicación en el disco donde se encuentra la raíz de sincronización.

Además de registrarse como proveedor raíz de sincronización, también quiere que los usuarios tengan un acceso sencillo a los datos que proporcione. El Explorador de archivos de nombres está diseñado para proporcionar un método para ese acceso sencillo. La creación de una extensión de espacio de nombres para el proveedor y su incorporación a la ventana de Explorador de archivos permitirá a los usuarios interactuar con el nivel raíz de los servicios tal como están acostumbrados a hacerlo con otros Explorador de archivos elementos. En este tema se explica cómo extender el espacio Explorador de archivos de nombres para que el proveedor aparezca en el nivel raíz en el panel de navegación.

El panel de navegación de Explorador de archivos ventana es la parte de la ventana que se muestra en el lado izquierdo. En la imagen siguiente, puede ver la estructura del espacio de nombres para este usuario. El nivel raíz del panel de navegación incluye los **objetos para OneDrive**, Este **equipo** y **Red.** Si sigue estos pasos, agregará la extensión al mismo nivel.

![Panel de navegación](images/navigationpane.png)

Para agregar la extensión al panel de navegación, debe tener lo siguiente antes de editar el Registro:

-   Una carpeta del sistema de archivos que contiene los datos que se mostrarán al usuario.

-   Nombre del servicio en la nube que aparecerá en el panel de navegación. También podría ser el nombre de la instancia si el servicio admite varias cuentas.

-   Icono de identificación de la aplicación.

-   UN CLSID para la aplicación. Una manera de generar un CLSID para la aplicación es usar el Uuidgen.exe. Vea [CLSID Key (Clave CLSID)](../com/clsid-key-hklm.md) para obtener más información sobre CLSID.

Los pasos siguientes modifican el Registro para obtener la información necesaria en el espacio de nombres Explorador de archivos datos. Los pasos específicos hacen tres cosas.

-   Cree claves en el Registro para el CLSID que incluyan valores para el nombre y el icono de la extensión, así como otra información que defina su comportamiento.

-   Configure la extensión para que se integre en el panel de navegación en la ubicación adecuada y con la visibilidad adecuada.

-   Configure la extensión para que tenga el comportamiento esperado de un elemento en el panel de navegación.

Estas instrucciones usan específicamente el **reg.exe,** pero puede usar cualquier herramienta de edición del Registro de su elección. Incluso puede integrar estos pasos en un instalador que actualice el Registro mediante programación.

## <a name="instructions"></a>Instructions

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Paso 1: Agregar el CLSID y dar nombre a la extensión

Agregue el nombre de la extensión al Registro en HKEY \_ CURRENT \_ USER. También agregará el identificador único para esta extensión. Es posible agregar más de una extensión por usuario, pero en ese caso necesitará un nombre y un identificador únicos para cada extensión. Este nombre y el identificador deben ser coherentes en el resto de estos pasos. En este ejemplo, el nombre es *MyCloudStorageApp.*

> [!IMPORTANT]
> El identificador proporcionado (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) en estos pasos solo se usa como ejemplo. Tendrá que cambiarlo a su CLSID único.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d "MyCloudStorageApp" /f**

### <a name="step-2-set-the-image-for-your-icon"></a>Paso 2: Establecer la imagen del icono

Proporcione la ruta de acceso al icono que debe mostrarse en el panel de navegación. En el ejemplo siguiente, *1043* hace referencia al identificador de recurso para el icono en el archivo DLL indicado.

> [!IMPORTANT]
> Debe actualizar la ruta de acceso de la imagen. Debe apuntar a una ruta de acceso genérica donde la aplicación instaló una imagen.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon /ve /t REG \_ EXPAND SZ \_ /d %SystemRoot%% \\ \\ system32imageres.dll,-1043 /f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Paso 3: Agregar la extensión al panel de navegación y hacer que sea visible

Establecer este valor en 0x1 indica que se debe anclar la extensión. Esto garantizará que se muestra a los usuarios de forma predeterminada. La configuración predeterminada para un usuario es que solo se mostrarán los elementos anclados en el panel de navegación. Un usuario puede cambiar esa configuración haciendo clic con el botón derecho en el panel de navegación y **seleccionando Mostrar todas las carpetas.** Si no desea anclar la extensión, puede establecer este valor en 0x0. Esto no quitará la extensión, sino que simplemente impedirá que se muestre al usuario de forma predeterminada.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v System.IsPinnedToNameSpaceTree /t REG \_ DWORD /d 0x1 /f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Paso 4: Establecer la ubicación de la extensión en el panel de navegación

Esto es fundamental para asegurarse de que el panel de navegación proporciona una experiencia coherente para el usuario.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v SortOrderIndex /t REG \_ DWORD /d 0x42 /f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Paso 5: Proporcione el archivo DLL que hospeda la extensión.

Use el shell32.dll para emular las carpetas predeterminadas de Windows. Cambie esto solo si tiene una razón específica para hacerlo y está familiarizado con las extensiones de espacio de nombres.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InProcServer32 /ve /t REG \_ EXPAND SZ \_ /d %systemroot%% \\ system32 \\shell32.dll /f**

### <a name="step-6-define-the-instance-object"></a>Paso 6: Definición del objeto de instancia

Indique que la extensión de espacio de nombres debe funcionar como otras estructuras de carpetas de archivos Explorador de archivos. Para obtener más información sobre los objetos de instancia de shell, vea [Creating Shell Extensions with Shell Instance Objects](/previous-versions/ms997573(v=msdn.10)).

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance /v CLSID /t REG \_ SZ /d {0E5AAE11-A475-4c5b-AB00-C66DE400274E} /f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Paso 7: Proporcionar los atributos del sistema de archivos de la carpeta de destino

Esto es necesario para asegurarse de que el Explorador de archivos proporciona una experiencia coherente y esperada para los usuarios. Este comando establece **FILE \_ ATTRIBUTE DIRECTORY \_ y** **FILE ATTRIBUTE \_ \_ READONLY,** que son [**constantes de atributo de archivo.**](../fileio/file-attribute-constants.md)

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v Attributes /t REG \_ DWORD /d 0x11 /f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Paso 8: Establecer la ruta de acceso de la raíz de sincronización

Establezca la ruta de acceso de la raíz de sincronización.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v TargetFolderPath /t REG \_ EXPAND SZ \_ /d %%USERPROFILE%% \\ MyCloudStorageApp /f**

### <a name="step-9-set-appropriate-shell-flags"></a>Paso 9: Establecer las marcas de shell adecuadas

Establezca algunas marcas necesarias para anclar la extensión de espacio de nombres al Explorador de archivos de nombres.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v FolderValueFlags /t REG \_ DWORD /d 0x28 /f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Paso 10: Establecer las marcas adecuadas para controlar el comportamiento del shell

Establezca las marcas [**SFGAO**](sfgao.md) adecuadas. Las marcas pertinentes son SFGAO \_ CANCOPY, SFGAO \_ CANLINK, SFGAO \_ STORAGE, SFGAO \_ HASPROPSHEET, SFGAO \_ STORAGEANCESTOR, SFGAO \_ FILESYSANCESTOR, SFGAO \_ FOLDER, SFGAO FILESYSTEM y \_ SFGAO \_ HASSUBFOLDER.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v Attributes /t REG \_ DWORD /d 0xF080004D /f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Paso 11: Registro de la extensión en la raíz del espacio de nombres

Configure la extensión de espacio de nombres para que sea un elemento secundario de la carpeta desktop.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer Desktop \\ \\ \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d MyCloudStorageApp /f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Paso 12: Ocultar la extensión del escritorio

Es importante que la extensión solo aparezca en el panel de navegación de la Explorador de archivos. Una extensión de espacio de nombres no funciona como un acceso directo normal. Por lo tanto, no debe usar este método para crear un acceso directo de escritorio.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer \\ \\ HideDesktopIcons \\ NewStartPanel /v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /t REG \_ DWORD /d 0x1 /f**

 

 
