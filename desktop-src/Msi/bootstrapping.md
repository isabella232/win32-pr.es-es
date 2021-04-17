---
description: Actualmente, cada instalación que intenta utilizar el Windows Installer comienza comprobando si el instalador está presente en el equipo del usuario y, si no está presente, si el usuario y el equipo están preparados para instalar Windows Installer.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Arranque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff743acbcd2dfc81b0e912e5be84c363f34614ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652601"
---
# <a name="bootstrapping"></a>Arranque

Actualmente, cada instalación que intenta utilizar el Windows Installer comienza comprobando si el instalador está presente en el equipo del usuario y, si no está presente, si el usuario y el equipo están preparados para instalar Windows Installer. Hay disponible un [Instmsi.exe](instmsi-exe.md) de aplicación de instalación con el SDK de Windows Installer que contiene toda la lógica y la funcionalidad para instalar Windows Installer. Sin embargo, una aplicación de arranque debe administrar esta instalación.

La aplicación de arranque debe comprobar primero si Windows Installer está instalado actualmente. Las aplicaciones pueden obtener la versión de Windows Installer instalado actualmente mediante [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc). Si Windows Installer no está instalado actualmente, la aplicación de arranque debe consultar al sistema operativo para determinar qué versión de la Instmsi.exe es necesaria. Una vez iniciada la instalación de Windows Installer, la aplicación de arranque debe controlar los códigos de retorno de la aplicación Instmsi.exe y controlar cualquier reinicio que se produzca durante la Windows Installer instalación. Para obtener más información, consulte [determinación de la versión de Windows Installer](determining-the-windows-installer-version.md)

En el ejemplo siguiente se muestra cómo la aplicación de instalación que instala Microsoft Office 2000 comprueba el sistema del usuario y configura el Windows Installer instalación. Este ejemplo está escrito específicamente para instalar Office 2000 y debe usarse solo como referencia general.

Cuando un usuario inserta un CD-ROM de Office 2000 en su equipo, Setup.exe intenta iniciar el modo de mantenimiento, la aplicación de instalación o no hace nada, según las necesidades del usuario. En la siguiente sección se describe cómo la aplicación de instalación de Office 2000, denominada Setup.exe, califica al usuario y su equipo, crea una línea de comandos e instala Windows Installer mediante la aplicación Msiexec.exe.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Cómo Setup.exe arranca el Windows Installer al instalar Office 2000

1.  El usuario inserta un CD-ROM de Office 2000 en su equipo. El sistema operativo Windows inicia Setup.exe mediante el modificador/Autorun y el archivo Autorun. inf. El archivo Autorun. inf se encuentra en la raíz del CD-ROM de Office 2000 y contiene las siguientes secciones:

    \[Ejecución automática\]

     

    \[Características de Office\]

     

    \[Información del producto\]

     

    \[ServicePack \] .

    La \[ sección ejecución automática \] contiene una línea de comandos que ejecuta la aplicación Setup.exe, ejecuta el icono usado para mostrar el disco y contiene información para agregar una opción "instalar" y una opción "configurar" al menú contextual del CD-ROM.

    La \[ sección características \] de Office contiene una lista de características y pares de nombres de características.

    La \[ sección información del producto \] especifica el nombre y la versión de la aplicación.

    La \[ \] sección ServicePack permite a un administrador de red establecer el nivel mínimo de Service Pack necesario. El administrador de red puede utilizar esta sección para crear el texto de un mensaje de alerta que se muestra si el sistema operativo local no tiene los Service Pack necesarios.

    A continuación se muestra un archivo Autorun. inf de ejemplo.

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

2.  La aplicación Setup.exe comprueba la \_ exclusión mutua MsiPromptForCD. Windows Installer crea esta exclusión mutua cuando solicita al usuario que inserte el CD-ROM. La presencia de la exclusión mutua indica que Windows Installer está ejecutando una instalación que ha solicitado el CD-ROM de Office 2000. En este caso, la aplicación Setup.exe se cierra inmediatamente y permite que continúe la instalación de Office 2000. Si la exclusión mutua está ausente, la aplicación Setup.exe continúa en el paso 3, donde se evalúa una clave del registro para determinar si Office 2000 está instalado.
3.  La aplicación Setup.exe comprueba la presencia de la clave del registro Office9:

    **HKCU/Software/Microsoft/Office/9.0/Common/general/InstallProductID**

    Si esta clave del registro no existe, la aplicación Setup.exe continúa en el paso 6, donde se comprueba el sistema operativo para determinar si es apta para la instalación de Office 2000.

4.  Si existe la clave del registro Office 2000, la aplicación Setup.exe comprueba el estado de instalación actual mediante una llamada a [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea). Un estado devuelto de InstallState \_ default indica que office 2000 ya está instalado y la aplicación Setup.exe continúa en el paso 5, donde se comprueba la ejecución del origen de office 2000.

    Si Office 2000 no está instalado, la aplicación Setup.exe continúa en el paso 6, donde se comprueba el sistema operativo para determinar si es apta para la instalación de Office 2000.

5.  La aplicación Setup.exe llama a [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para cada una de las características de la sección **\[ OfficeFeatures \]** del archivo Autorun. inf. Si alguna de estas características devuelve \_ el origen INSTALLSTATE, esto indica que la característica se ejecuta desde el origen y la aplicación Setup.exe se cierra inmediatamente.

    Si ninguna de las características devuelve el \_ origen INSTALLSTATE, la aplicación Setup.exe inicia la aplicación del instalador, Msiexec.exe y presenta el modo de mantenimiento Windows Installer antes de salir.

6.  La aplicación Setup.exe determina si el sistema operativo es apto para una instalación de Office 2000. Se requiere Windows XP para instalar Office 2000. Si el sistema operativo requiere una actualización de Service Pack para calificar para Office 2000, la aplicación de Setup.exe muestra el texto especificado en el archivo Autorun. inf. Si el sistema operativo no es apto para Office 2000 o una actualización de Office 2000, la aplicación Setup.exe muestra un mensaje que impide que el usuario continúe.

    Si el sistema operativo es apto para Office 2000, la aplicación Setup.exe continúa en el paso 7, que determina si Windows Installer está instalado en el equipo del usuario.

7.  Si Windows Installer existe en el equipo del usuario, la aplicación Setup.exe inicia la aplicación Msiexec.exe y le pasa el archivo Office 2000. msi.

    Si Windows Installer no está instalado en el equipo local, la aplicación de Setup.exe continúa en el paso 8, que determina si el sistema operativo es apto para tener Windows Installer instalado.

8.  Si el equipo local es válido para tener Windows Installer instalado, la aplicación de Setup.exe ejecuta la versión correcta de la aplicación de instalador de Instmsi.exe para la plataforma. Setup.exe puede pasar el modificador de la línea de comandos "/q" para suprimir la interfaz de usuario e impedir que el usuario cambie las opciones de configuración de instalación.
9.  La aplicación Setup.exe carga el archivo de Msi.dll recién instalado y realiza una llamada a la función [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para instalar la aplicación del usuario.

## <a name="setupexe-command-line-parameters"></a>Parámetros de la línea de comandos Setup.exe

La aplicación Setup.exe permite a los administradores y usuarios pasar opciones de línea de comandos a la aplicación Msiexec.exe. Para obtener más información, vea opciones de la [línea de comandos](command-line-options.md). En la tabla siguiente se enumeran las opciones de comando que se pueden usar con Setup.exe.



| Opción                       | Uso                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /Autorun                     | setup.exe/Autorun                                                                                                                           | Ejecuta el archivo Autorun. inf descrito anteriormente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Inicia una instalación administrativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[\| \] *paquete* u m o <br/> \[\| \] *paquete* u m/T ( *lista de transformación* )<br/> or <br/> \[\| \] *paquete* u m/g *ididioma*<br/> | Anuncia un producto. Esta opción omite los valores de propiedad especificados en la línea de comandos. u anuncie al usuario actual.<br/> m anunciar a todos los usuarios de la máquina.<br/> identificador de idioma g<br/> t aplica la transformación al paquete anunciado.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe/I Office9.msi/t ProgramMgmt. MST                                                                                                  | Especifica el archivo. msi que Setup.exe va a instalar. Si no se incluye la opción/I, Setup.exe utiliza el archivo Office9.msi.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o< = *valor* de propiedad> | setup.exe/o CDKEY = 111111-1111                                                                                                               | Establece las propiedades en el archivo. msi. Setup.exe los pasa a msiexec como escrito.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe/q                                                                                                                                 | Establezca el nivel de la interfaz de usuario para la instalación. /q sin interfaz de usuario (/QN para msiexec.)/QB IU básica<br/> /QR interfaz de usuario reducida.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe/M4                                                                                                                                | Admite varias licencias de acuerdo con los contratos seleccionados. Esta propiedad se usa en mediante la acción personalizada de comprobación de licencias para escribir el certificado LV. La opción/m debe ir seguida del número de desbloqueos permitidos. El valor especificado por la opción/m debe establecerse como la propiedad "M" en el archivo de Office9.msi. Si no se especifica ningún valor, pero se usa la opción/m con el programa de instalación, se debe establecer el valor 0. La opción/m es necesaria para admitir clientes seleccionados mediante un CD o una red. |
| /settings                    | setup.exe/Settings mysettings.ini                                                                                                           | Permite a los administradores especificar un archivo. ini que contenga todas las configuraciones personalizadas que se pasarán durante el programa de instalación de Office 2000. Vea la descripción del archivo. ini que aparece a continuación.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Uso de un archivo. ini

Crear un archivo de inicialización puede ser más fácil que crear una línea de comandos larga. Con la opción/Settings, la aplicación Setup.exe lee el archivo. ini especificado y crea una línea de comandos que se pasa a la aplicación Msiexec.exe. En el archivo. ini solo se admiten las propiedades admitidas en la línea de comandos. Si se encuentra una propiedad o un valor en el archivo. ini y en la línea de comandos, la configuración de la línea de comandos invalidará la configuración del archivo. ini.

El formato del archivo. ini es:

\[MS\]

 

\[MSI\]

 

\[options\]

 

\[Pantalla\]

La \[ \] sección MSI del archivo. ini especifica la ruta de acceso al paquete de instalación de para la instalación. Esto corresponde a la opción/I en la línea de comandos.

La \[ \] sección MST del archivo. ini especifica la ruta de acceso a las transformaciones que se usan con esta instalación. Esto corresponde a la opción/j en la línea de comandos. Cada una de las transformaciones se indica en una línea diferente, mediante MST1 MST (N). Cuando se analiza en la línea de comandos, la lista del archivo. ini se convierte de izquierda a derecha. Tenga en cuenta que el número asociado al título MST (N) solo está presente para mantener identificadores únicos y no tiene ningún significado de programación.

La \[ \] sección Opciones permite a los administradores de red establecer e invalidar propiedades en los archivos. msi o. MST. Las opciones establecidas en el archivo. ini se agregan a la línea de comandos mediante la opción/o. Cada opción de la sección de la opción debe tener un nombre de propiedad y un valor.

La \[ sección de presentación \] se usa para establecer el nivel de interfaz de usuario que se usa durante la instalación. Esto corresponde a la opción/q en la línea de comandos. Los valores válidos son none, Basic, Reduced y Full.

Archivo. ini de ejemplo

\[MSI\]

 

MSI = \\ \\ sourceshare \\ office2000 \\Office2000.msi

 

\[MSI\]

 

MST1 = \\ \\ sourceshare \\ office2000 \\ trns1. MST

 

MST2 = \\ \\ sourceshare \\ office2000 \\ trns2. MST

 

\[Opciones\]

 

PUBLICPROPERTY = su valor

\[Pantalla\]

 

Display = ninguno

 

