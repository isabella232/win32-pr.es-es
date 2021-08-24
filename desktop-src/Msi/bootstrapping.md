---
description: Actualmente, cada instalación que intenta usar el instalador de Windows comienza comprobando si el instalador está presente en el equipo del usuario y, si no está presente, si el usuario y el equipo están listos para instalar Windows Installer.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Arranque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c590d00fa9d6ac63f93caa287f34b9f2bf25357bd36ab9ea3fb9ce87e81291d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145718"
---
# <a name="bootstrapping"></a>Arranque

Actualmente, cada instalación que intenta usar el instalador de Windows comienza comprobando si el instalador está presente en el equipo del usuario y, si no está presente, si el usuario y el equipo están listos para instalar Windows Installer. Hay una aplicación [deInstmsi.exe](instmsi-exe.md) disponible con el SDK del instalador de Windows que contiene toda la lógica y la funcionalidad para instalar Windows Instalador. Sin embargo, una aplicación de arranque debe administrar esta instalación.

La aplicación de arranque debe comprobar primero si Windows instalador está instalado actualmente. Las aplicaciones pueden obtener la versión de Windows Instalador instalado actualmente mediante [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc). Si Windows instalador no está instalado actualmente, la aplicación de arranque debe consultar el sistema operativo para determinar qué versión del Instmsi.exe es necesaria. Una vez iniciada la instalación de Windows Installer, la aplicación de arranque debe controlar los códigos de retorno de la aplicación Instmsi.exe y controlar los reinicios que se producen durante la instalación del instalador de Windows. Para obtener más información, vea [Determinar la versión Windows instalador](determining-the-windows-installer-version.md)

En el ejemplo siguiente se muestra cómo la aplicación de instalación que instala Microsoft Office 2000 comprueba el sistema del usuario y configura la instalación Windows Installer. Este ejemplo se escribe específicamente para instalar Office 2000 y solo debe usarse como referencia general.

Cuando un usuario inserta un CD-ROM de Office 2000 en su equipo, Setup.exe intenta iniciar el modo de mantenimiento, la aplicación de instalación o no hace nada, según las necesidades del usuario. En la sección siguiente se describe cómo la aplicación de instalación de Office 2000, denominada Setup.exe, califica al usuario y a su equipo, crea una línea de comandos e instala Windows Installer mediante la aplicación Msiexec.exe.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>How Setup.exe Bootstraps the Windows Installer when Installing Office 2000

1.  El usuario inserta una Office CD-ROM 2000 en su equipo. El Windows operativo inicia Setup.exe mediante el modificador /autorun y el archivo Autorun.inf. El archivo Autorun.inf se encuentra en la raíz del cd-ROM Office 2000 y contiene las secciones siguientes:

    \[Ejecución automática\]

     

    \[Office Funciones\]

     

    \[Información del producto\]

     

    \[ServicePack \] .

    La sección Ejecución automática contiene una línea de comandos que ejecuta la aplicación Setup.exe, ejecuta el icono usado para mostrar el disco y contiene información para agregar una opción "Instalar" y una opción "Configurar" al menú contextual del \[ \] CD-ROM.

    La Office características contiene una lista de características y pares de \[ \] nombres de características.

    La \[ sección Información del producto especifica el nombre y la versión de la \] aplicación.

    La \[ sección ServicePack \] permite a un administrador de red establecer el nivel mínimo necesario de Service Pack. El administrador de red puede usar esta sección para crear el texto de un mensaje de alerta que se muestra si el sistema operativo local no tiene el Service Pack necesario.

    A continuación se muestra un archivo Autorun.inf de ejemplo.

    ``` syntax
    [autorun] 
    OPEN=setup.EXE /AUTORUN /KEY:Software\Microsoft\Office\9.0\Common\General\InstallProductID
    ICON=setup.EXE,1
    shell\configure=&Configure
    shell\configure\command=setup.EXE
    shell\install=&Install
    shell\install\command=setup.EXE
    [OfficeFeatures]
    Feature1=ACCESSFiles
    Feature2=OfficeFiles
    Feature3=WORDFiles
    Feature4=EXCELFiles
    Feature5=PPTFiles
    [ProductInformation]
    DisplayName=Microsoft Office 9
    Version=9.0
    ProductCode={product guid}
    [ServicePack]
    MessageText="The operating system does not have a required service pack. Please download and install this from www.microsoft.com."
    SPLevel=3
    ```

2.  La Setup.exe busca la \_ exclusión mutua MsiPromptForCD. Windows El instalador crea esta exclusión mutua cuando solicita al usuario que inserte el CD-ROM. La presencia de la exclusión mutua indica que Windows instalador está ejecutando una instalación que ha solicitado la Office 2000 CD-ROM. En este caso, la Setup.exe se cierra inmediatamente y permite que Office la instalación de 2000. Si la exclusión mutua no existe, la aplicación Setup.exe continúa en el paso 3, donde se evalúa una clave del Registro para determinar si Office 2000 está instalado.
3.  La Setup.exe comprueba la presencia de la clave del Registro de Office9:

    **HKCU/Software/Microsoft/Office/9.0/Common/General/InstallProductID**

    Si esta clave del Registro no existe, la aplicación Setup.exe continúa en el paso 6, donde se comprueba el sistema operativo para determinar si cumple los requisitos para la instalación de Office 2000.

4.  Si existe Office clave del Registro 2000, la aplicación Setup.exe comprueba el estado de instalación actual mediante una llamada a [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea). Un estado devuelto de InstallState Default indica que Office 2000 ya está instalado y la aplicación de Setup.exe continúa en el paso 5, donde se comprueba si Office 2000 se ejecuta desde el \_ origen.

    Si Office 2000 no está instalado, la aplicación de Setup.exe continúa en el paso 6, donde se comprueba el sistema operativo para determinar si es adecuado para la instalación de Office 2000.

5.  La Setup.exe llama a [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para cada una de las características de la sección **\[ OfficeFeatures \]** del archivo Autorun.inf. Si alguna de estas características devuelve INSTALLSTATE SOURCE, esto indica que la característica se ejecuta desde el origen y el Setup.exe \_ aplicación se cierra inmediatamente.

    Si ninguna de las características devuelve INSTALLSTATE SOURCE, la aplicación Setup.exe inicia la aplicación instalador, Msiexec.exe, y presenta el modo de mantenimiento Windows Installer antes de \_ salir.

6.  La Setup.exe determina si el sistema operativo cumple los requisitos para una instalación de Office 2000. Windows Xp es necesario para instalar Office 2000. Si el sistema operativo requiere una actualización de Service Pack para calificar para Office 2000, la aplicación Setup.exe muestra el texto especificado en el archivo Autorun.inf. Si el sistema operativo no es apto para Office 2000 o una actualización de Office 2000, la aplicación Setup.exe muestra un mensaje que impide que el usuario continúe.

    Si el sistema operativo cumple los requisitos para Office 2000, la aplicación Setup.exe continúa en el paso 7, que determina si Windows Installer está instalado en el equipo del usuario.

7.  Si Windows Installer existe en el equipo del usuario, la aplicación Setup.exe inicia la aplicación Msiexec.exe y le pasa el archivo .msi Office 2000.

    Si Windows Installer no está instalado en el equipo local, la aplicación Setup.exe continúa en el paso 8, que determina si el sistema operativo cumple los requisitos para tener instalado Windows Installer.

8.  Si el equipo local es apto para tener instalado Windows Installer, la aplicación Setup.exe ejecuta la versión correcta de la aplicación instalador de Instmsi.exe para la plataforma. Setup.exe pasar el modificador de línea de comandos "/q" para suprimir la interfaz de usuario e impedir que el usuario cambie las opciones de configuración de instalación.
9.  La Setup.exe carga el archivo Msi.dll recién instalado y realiza una llamada a la función [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para instalar la aplicación del usuario.

## <a name="setupexe-command-line-parameters"></a>Setup.exe de línea de comandos

La Setup.exe permite a los administradores y usuarios pasar opciones de línea de comandos a la Msiexec.exe aplicación. Para obtener más información, vea [Opciones de línea de comandos](command-line-options.md). En la tabla siguiente se enumeran las opciones de comando que se pueden usar con Setup.exe.



| Opción                       | Uso                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe /autorun                                                                                                                           | Ejecuta el archivo Autorun.inf descrito anteriormente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Inicia una instalación administrativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[u \| m \] *Package o* <br/> \[u \| m \] *Package* /t *Transform List*<br/> o <br/> \[u \| m \] *Package* /g *LanguageID*<br/> | Anuncia un producto. Esta opción omite los valores de propiedad especificados en la línea de comandos. u Anunciar al usuario actual.<br/> m Anunciar a todos los usuarios de la máquina.<br/> g Identificador de idioma<br/> t Aplica la transformación al paquete anunciado.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe /I Office9.msi /t ProgramMgmt.mst                                                                                                  | Especifica el archivo .msi que Setup.exe se va a instalar. Si no se incluye la opción /I, Setup.exe usa el Office9.msi archivo.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o<*valor de* = *propiedad*> | setup.exe /o CDKEY=111111-1111                                                                                                               | Establece las propiedades del .msi archivo. Setup.exe los pasa a msiexec tal como están escritos.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe /q                                                                                                                                 | Establezca el nivel de la interfaz de usuario de la instalación. /q no UI (/qn para msiexec).) /qb basic UI<br/> Interfaz de usuario reducida /qr.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe /m4                                                                                                                                | Admite varias licencias de acuerdo con los contratos Select. Esta propiedad se usa en la acción personalizada Comprobación de licencia para escribir el certificado LV. La opción /m debe ir seguida del número de desbloqueos permitidos. El valor especificado por la opción /m debe establecerse como la propiedad "M" en el Office9.msi archivo. Si no se especifica ningún valor, pero la opción /m se usa con el programa de instalación, se debe establecer el valor 0. La opción /m es necesaria para admitir Seleccionar clientes mediante un CD o una red. |
| /settings                    | setup.exe /settings mysettings.ini                                                                                                           | Permite a los administradores especificar un .ini que contiene toda la configuración personalizada que se pasará durante la Office 2000. Consulte la descripción del archivo .ini siguiente.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Uso de un .ini archivo

Crear un archivo de inicialización puede ser más fácil que crear una línea de comandos larga. Con la opción /settings, la aplicación Setup.exe lee el archivo .ini especificado y construye una línea de comandos para pasarla a la Msiexec.exe especificada. Solo se admiten las propiedades admitidas en la línea de comandos en .ini archivo. Si se encuentra una propiedad o un valor en el archivo .ini y en la línea de comandos, la configuración de la línea de comandos invalida la configuración del .ini de archivos.

El formato del archivo .ini es:

\[Msi\]

 

\[Mst\]

 

\[options\]

 

\[Pantalla\]

La \[ sección msi del archivo .ini especifica la ruta de acceso al paquete de instalación para la \] instalación. Esto corresponde a la opción /I en la línea de comandos.

La sección mst del archivo .ini especifica la ruta de acceso \[ \] a las transformaciones usadas con esta instalación. Esto corresponde a la opción /j en la línea de comandos. Se indican varias transformaciones en una línea diferente, mediante MST1 MST(N). Cuando se analiza en la línea de comandos, la lista del archivo .ini se convierte de izquierda a derecha. Tenga en cuenta que el número asociado al título MST(N) solo está presente para mantener identificadores únicos y no tiene ningún significado mediante programación.

La sección de opciones permite a los administradores de red establecer e invalidar propiedades en \[ los archivos .msi o \] .mst. Las opciones establecidas en .ini archivo se agregan a la línea de comandos mediante la opción /o. Cada opción de la sección option debe tener un nombre de propiedad y un valor.

La \[ sección Mostrar se usa para establecer el nivel de interfaz de usuario utilizado durante la \] instalación. Esto corresponde a la opción /q en la línea de comandos. Los valores válidos son none, basic, reduced y full.

Archivo de .ini ejemplo

\[MSI\]

 

MSI= \\ \\ sourceshare \\ Office2000 \\Office2000.msi

 

\[Mst\]

 

MST1= \\ \\ sourceshare \\ Office2000 \\ trns1.mst

 

MST2= \\ \\ sourceshare \\ Office2000 \\ trns2.mst

 

\[Opciones\]

 

PUBLICPROPERTY=su valor

\[Pantalla\]

 

Display=None

 

