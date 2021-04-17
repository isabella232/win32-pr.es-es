---
description: Muestra cómo registrar un proveedor de raíz de sincronización e integrar un proveedor de almacenamiento en la nube en el nivel raíz del panel de navegación.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: Integración de un proveedor de almacenamiento en la nube
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21fdc5abfbf9881bfe23b00a924fce989aec7c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569390"
---
# <a name="integrate-a-cloud-storage-provider"></a>Integración de un proveedor de almacenamiento en la nube

Si tiene un proveedor de almacenamiento en la nube, debe realizar un par de pasos para proporcionar una experiencia coherente y preferida para el usuario. Estas dos acciones se registran como un proveedor raíz de sincronización e integran la aplicación en el nivel raíz del panel de navegación.

> [!IMPORTANT]
> La integración del proveedor de almacenamiento en la nube solo se admite a partir de Windows 10.

 

Lo primero es registrarse como proveedor raíz de sincronización. Esto permite que el shell de Windows Conozca la aplicación y que la aplicación sea responsable de sincronizar los archivos en la raíz de sincronización. Esto también permitirá que otras aplicaciones sepan que está sincronizando estos archivos para que puedan responder adecuadamente. Después, otras aplicaciones pueden usar [**StorageFile. Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) para obtener el [**displayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) y el [**identificador**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) de la aplicación.

Para registrarse como proveedor de raíz de sincronización, deberá crear varias entradas del registro. Antes de proporcionar la lista de pares clave-valor, estos son algunos marcadores de posición que debe reemplazar por sus propios datos de aplicación.

-   *\[ identificador \] de proveedor de almacenamiento*: el nombre del proveedor de almacenamiento en la nube. Este nombre debe ser coherente independientemente de la versión de la aplicación. Un ejemplo de esto es OneDrive.
-   *\[ SID \] de Windows*: el SID de Windows único que identifica al usuario. Si la aplicación admite varias instalaciones para varios usuarios en un solo equipo, se requiere esta parte.
-   *\[ ID \]*. de cuenta: el identificador de proveedor de servicios para la cuenta actual de este usuario. Algunos proveedores requieren la capacidad de proporcionar varias raíces de sincronización para un usuario. Un ejemplo de esto es un trabajo y una cuenta personal. El *identificador de cuenta* permite tener varias cuentas registradas para un usuario. Si el proveedor admite varias raíces de sincronización por usuario, esta parte es obligatoria.

Estos marcadores de posición se combinan para formar el identificador raíz de sincronización. Debe colocar un **.** carácter entre cada uno de los marcadores de posición al formar el identificador raíz de sincronización. Estos son los pares clave-valor que se deben crear.

-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ explorador \\ SyncRootManager \\**_\[ ID. \] de proveedor de almacenamiento_** _\[ SID \] de Windows_** _\[ Identificador \] de cuenta_*_\\ DisplayNameResource_* : apunta al recurso en el que el shell de Windows u otras aplicaciones pueden obtener un nombre descriptivo para la raíz de sincronización.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ explorador \\ SyncRootManager \\**_\[ ID. \] de proveedor de almacenamiento_** _\[ SID \] de Windows_** _\[ Identificador \] de cuenta_*_\\ IconResource_* : apunta al recurso en el que el shell de Windows u otras aplicaciones pueden obtener un icono para la raíz de sincronización.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ explorador \\ SyncRootManager \\**_\[ ID. \] de proveedor de almacenamiento_** _\[ SID \] de Windows_** _\[ Identificador \] de cuenta_*_\\ UserSyncRoots \\_*_\[ SID \] de Windows_ : la ubicación en el disco donde se encuentra la raíz de sincronización.

Aparte de registrarlo como un proveedor raíz de sincronización, también desea que los usuarios tengan fácil acceso a los datos proporcionados. El espacio de nombres del explorador de archivos está diseñado para proporcionar un método para facilitar el acceso. La creación de una extensión de espacio de nombres para el proveedor y su incorporación en la ventana del explorador de archivos permitirá a los usuarios interactuar con el nivel raíz de los servicios de la misma manera que se usan con otros elementos del explorador de archivos. En este tema se explica cómo extender el espacio de nombres del explorador de archivos para que el proveedor aparezca en el nivel raíz en el panel de navegación.

El panel de navegación de la ventana Explorador de archivos es la parte de la ventana que se muestra en el lado izquierdo. En la imagen siguiente, puede ver la estructura del espacio de nombres para este usuario. El nivel raíz del panel de navegación incluye los objetos para **OneDrive**, **este equipo** y la **red**. Al seguir estos pasos, se agregará la extensión al mismo nivel.

![Panel de navegación](images/navigationpane.png)

Para agregar la extensión al panel de navegación, debe tener lo siguiente antes de editar el registro:

-   Carpeta del sistema de archivos que contiene los datos que se van a mostrar al usuario.

-   Nombre del servicio en la nube que aparecerá en el panel de navegación. También podría ser el nombre de la instancia si el servicio admite varias cuentas.

-   Icono de identificación de la aplicación.

-   Un CLSID para la aplicación. Una manera de generar un CLSID para la aplicación es usar el Uuidgen.exe. Consulte [clave CLSID](../com/clsid-key-hklm.md) para obtener más información acerca de CLSID.

En los pasos siguientes se modifica el registro para obtener la información necesaria en el espacio de nombres del explorador de archivos. Los pasos específicos hacen tres cosas.

-   Cree claves en el registro para el CLSID que incluya valores para el nombre y el icono de la extensión, así como otra información que defina su comportamiento.

-   Configure la extensión para que se integre en el panel de navegación en la ubicación adecuada y con la visibilidad adecuada.

-   Configure la extensión para que tenga el comportamiento esperado para un elemento en el panel de navegación.

Estas instrucciones usan específicamente el comando **reg.exe** , pero puede usar cualquier herramienta de edición del registro que prefiera. Incluso puede integrar estos pasos en un instalador que actualice el registro mediante programación.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Paso 1: agregar el CLSID y asignar un nombre a la extensión

Agregue el nombre de la extensión al registro en HKEY \_ Current \_ User. También agregará el identificador único para esta extensión. Es posible agregar más de una extensión por usuario, pero en ese caso necesitará un nombre y un identificador únicos para cada extensión. Este nombre e identificador deben ser coherentes en el resto de estos pasos. En este ejemplo, el nombre es *MyCloudStorageApp*.

> [!IMPORTANT]
> El identificador proporcionado (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) en estos pasos se usa simplemente como ejemplo. Tendrá que cambiar esto por el CLSID único.

 

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t reg \_ SZ/d "MyCloudStorageApp"/f**

### <a name="step-2-set-the-image-for-your-icon"></a>Paso 2: establecer la imagen para el icono

Proporcione la ruta de acceso al icono que debe mostrarse en el panel de navegación. En el ejemplo siguiente, *1043* hace referencia al identificador de recurso del icono de la dll indicada.

> [!IMPORTANT]
> Debe actualizar la ruta de acceso de la imagen. Debe apuntar a una ruta de acceso genérica donde la aplicación ha instalado una imagen.

 

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon/ve/t reg \_ Expand \_ SZ/d%% SystemRoot%% \\ system32 \\imageres.dll,-1043/f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Paso 3: agregar la extensión al panel de navegación y hacer que esté visible

Establecer este valor en 0x1 indica que se debe anclar la extensión. Esto garantizará que se muestre a los usuarios de forma predeterminada. La configuración predeterminada de un usuario es que solo se mostrarán los elementos anclados en el panel de navegación. Un usuario puede cambiar esa configuración si hace clic con el botón secundario en el panel de navegación y selecciona **Mostrar todas las carpetas**. Si no desea anclar la extensión, puede establecer este valor en 0X0. Esto no quitará la extensión, pero simplemente impedirá que se muestre al usuario de forma predeterminada.

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/v System. IsPinnedToNameSpaceTree/t reg \_ DWORD/d 0x1/f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Paso 4: establecer la ubicación de la extensión en el panel de navegación

Esto es crítico para asegurarse de que el panel de navegación proporciona una experiencia coherente para el usuario.

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/V SortOrderIndex/t reg \_ DWORD/d 0x42/f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Paso 5: proporcione el archivo DLL que hospeda la extensión.

Use el shell32.dll para emular las carpetas predeterminadas de Windows. Cámbielo solo si tiene una razón concreta para hacerlo y está familiarizado con las extensiones de espacio de nombres.

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InProcServer32/ve/t reg \_ Expand \_ SZ/d%% SystemRoot%% \\ system32 \\shell32.dll/f**

### <a name="step-6-define-the-instance-object"></a>Paso 6: definir el objeto de instancia

Indique que la extensión de espacio de nombres debe funcionar como otras estructuras de carpetas de archivos en el explorador de archivos. Para obtener más información sobre los objetos de instancia de Shell, vea [crear extensiones de Shell con objetos de instancia de Shell](/previous-versions/ms997573(v=msdn.10)).

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance/v CLSID/T reg \_ SZ/d {0E5AAE11-A475-4c5b-AB00-C66DE400274E}/f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Paso 7: proporcionar los atributos del sistema de archivos de la carpeta de destino

Esto es necesario para asegurarse de que el explorador de archivos proporciona una experiencia coherente y esperada a los usuarios. Este comando establece **el \_ \_ Directorio de atributos de archivo** y el atributo de **archivo \_ \_ ReadOnly**, y ambos son [**constantes de atributo de archivo**](../fileio/file-attribute-constants.md).

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag/v Attributes/t reg \_ DWORD/d 0x11/f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Paso 8: establecer la ruta de acceso de la raíz de sincronización

Establezca la ruta de acceso de la raíz de sincronización.

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag/v TargetFolderPath/t reg \_ Expand \_ SZ/d%% userprofile%% \\ MyCloudStorageApp/f**

### <a name="step-9-set-appropriate-shell-flags"></a>Paso 9: establecimiento de las marcas de Shell adecuadas

Establezca algunas marcas necesarias para anclar la extensión de espacio de nombres al árbol del explorador de archivos.

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder/v FolderValueFlags/t reg \_ DWORD/d 0x28/f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Paso 10: establecimiento de las marcas adecuadas para controlar el comportamiento del shell

Establezca las marcas [**SFGAO**](sfgao.md) adecuadas. Las marcas pertinentes son SFGAO \_ CANCOPY, SFGAO \_ CANLINK, SFGAO \_ Storage, SFGAO \_ HASPROPSHEET, SFGAO \_ STORAGEANCESTOR, SFGAO \_ FILESYSANCESTOR, SFGAO \_ Folder, SFGAO \_ FILESYSTEM y SFGAO \_ HASSUBFOLDER.

**REG Add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ SHELLFOLDER/V Attributes/t reg \_ DWORD/d 0xF080004D/f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Paso 11: registro de la extensión en la raíz del espacio de nombres

Configure la extensión de espacio de nombres para que sea un elemento secundario de la carpeta escritorio.

**REG Add HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ Desktop \\ namespace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t reg \_ SZ/d MyCloudStorageApp/f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Paso 12: ocultar la extensión del escritorio

Es importante que la extensión solo aparezca en el panel de navegación del explorador de archivos. Una extensión de espacio de nombres no funciona como un método abreviado normal. Por lo tanto, no debe utilizar este método para crear un acceso directo de escritorio.

**REG Add HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ HideDesktopIcons \\ NewStartPanel/v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/t reg \_ DWORD/d 0x1/f**

 

 
