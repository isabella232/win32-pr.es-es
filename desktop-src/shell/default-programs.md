---
description: Use Programas predeterminados para establecer la experiencia del usuario predeterminada.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programas predeterminados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1cd54afe23291c191fdd045ca3cb42b68361aa8f7f3d8ef431042cfe9f5c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861362"
---
# <a name="default-programs"></a>Programas predeterminados

Use **Programas predeterminados para** establecer la experiencia del usuario predeterminada. Los usuarios pueden **acceder a los** programas predeterminados Panel de control o directamente desde el **menú** Inicio. Establezca la herramienta Acceso a programas y valores predeterminados del equipo [(SPAD),](cpl-setprogramaccess.md) la experiencia de valores predeterminados principal para los usuarios de Windows XP, ahora es una parte de **programas predeterminados.**

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que funcionan las asociaciones de archivos predeterminadas en Windows 10. Para obtener más información, vea la sección Cambios en la **forma en que Windows 10 las aplicaciones predeterminadas** en esta [entrada](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Cuando un usuario establece los valores predeterminados del programa mediante Programas predeterminados **,** la configuración predeterminada solo se aplica a ese usuario y no a otros usuarios que puedan usar el mismo equipo. **Programas predeterminados** proporciona un conjunto de API (en desuso en Windows 8) que permiten a los proveedores de software independientes (ISV) incluir sus programas o aplicaciones en el sistema predeterminado. El conjunto de API también ayuda a los ISV a administrar mejor su estado como valores predeterminados.

Este tema se organiza de la siguiente manera:

-   [Introducción a los programas predeterminados y su conjunto de API relacionado](#introduction-to-default-programs-and-its-related-api-set)
-   [Registro de una aplicación para su uso con programas predeterminados](#registering-an-application-for-use-with-default-programs)
    -   [ProgID](#progids)
    -   [Subclave de registro y descripciones de valores](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Ejemplo de registro completo](#full-registration-example)
-   [Convertirse en el explorador predeterminado](#becoming-the-default-browser)
-   [Interfaz de usuario de programas predeterminada](#default-programs-ui)
-   [Procedimientos recomendados para usar programas predeterminados](#best-practices-for-using-default-programs)
    -   [Durante la instalación](#during-installation)
    -   [Después de la instalación](#after-installation)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Introducción a los programas predeterminados y a su conjunto de API relacionado

**Programas predeterminados** está diseñado principalmente para aplicaciones que usan tipos de archivo estándar, como archivos .mp3 o .jpg o protocolos estándar, como HTTP o mailto. Las aplicaciones que usan sus propios protocolos propietarios y asociaciones de archivos no suelen usar la **funcionalidad Programas predeterminados.**

Después de registrar una aplicación para la **funcionalidad programas** predeterminados, las siguientes opciones y funcionalidades están disponibles mediante el conjunto de API:

-   Restaure todos los valores predeterminados registrados para una aplicación. En desuso para Windows 8.
-   Restaurar un único valor predeterminado registrado para una aplicación. En desuso para Windows 8.
-   Consulte el propietario de un valor predeterminado específico en una sola llamada en lugar de buscar en el Registro. Puede consultar el valor predeterminado de una asociación de archivos, un protocolo o un verbo canónico **del** menú Inicio.
-   Inicie una interfaz de usuario para una aplicación específica en la que un usuario pueda establecer valores predeterminados individuales.
-   Quite todas las asociaciones por usuario.

**Programas predeterminados** también proporciona una interfaz de usuario que permite registrar una aplicación para proporcionar información adicional al usuario. Por ejemplo, una aplicación firmada digitalmente puede incluir una dirección URL a la página principal del fabricante.

El uso del conjunto de API asociado puede ayudar a que una aplicación funcione correctamente en la característica de control de cuentas de usuario (UAC) introducida en Windows Vista. En UAC, un administrador aparece en el sistema como un usuario estándar, por lo que el administrador no puede escribir normalmente en el subárbol **HKEY \_ LOCAL \_ MACHINE.** Esta restricción es una característica de seguridad que impide que un proceso actúe como administrador sin el conocimiento del administrador.

La instalación de un programa por parte de un usuario normalmente se realiza como un proceso con privilegios elevados. Sin embargo, los intentos de una aplicación de modificar los comportamientos de asociación predeterminados en un nivel de equipo posterior a la instalación no se realizarán correctamente. En su lugar, los valores predeterminados deben registrarse en un nivel por usuario, lo que impide que varios usuarios sobrescriban los valores predeterminados entre sí.

La estructura jerárquica del Registro para las asociaciones de archivos y protocolos da prioridad a los valores predeterminados por usuario sobre los valores predeterminados de nivel de equipo. Algunas aplicaciones incluyen puntos en su código que elevan temporalmente sus derechos cuando reclaman valores predeterminados registrados en **HKEY \_ LOCAL \_ MACHINE**. Estas aplicaciones pueden experimentar resultados inesperados si otra aplicación ya está registrada como valor predeterminado por usuario. El uso **de programas predeterminados** evita esta ambigüedad y garantiza los resultados esperados en un nivel por usuario.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registro de una aplicación para su uso con programas predeterminados

En esta sección se muestran las subclaves del Registro y los valores necesarios para registrar una aplicación con **programas predeterminados.** Incluye un ejemplo completo.

Esta sección contiene los siguientes temas:

-   [ProgID](#progids)
-   [Subclave de registro y descripciones de valores](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Ejemplo de registro completo](#full-registration-example)

**Los programas predeterminados** requieren que cada aplicación registre explícitamente las asociaciones de archivo, las asociaciones MIME y los protocolos para los que la aplicación debe aparecer como un posible valor predeterminado. Las asociaciones se registran mediante los siguientes elementos del Registro, que se explican con detalle más adelante en este tema en Subclave de registro y Descripciones [de valores](#registration-subkey-and-value-descriptions):

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

En el ejemplo siguiente se muestran las entradas del Registro para un explorador Ficticio de Contoso denominado WebBrowser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a>ProgID

Una aplicación debe proporcionar un [ProgID específico.](fa-progids.md) Asegúrese de incluir toda la información que normalmente se escribe en la subclave predeterminada genérica para la extensión. Por ejemplo, el reproductor multimedia ficticio litware proporciona las clases **HKEY \_ LOCAL \_ MACHINE** SOFTWARE específicas de \\  \\  \\ **la aplicaciónLitwarePlayer11.AssocFile.MP3** subclave. Esa subclave incluye toda la información de la subclave predeterminada genérica **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Classes.mp3además de cualquier información adicional que desee que \\  \\  \\ **** la aplicación registre. Esto garantiza que si el usuario restaura la asociación .mp3 al reproductor de Litware, la información del reproductor de Litware está intacta y no se ha sobrescrito por otra aplicación. (La sobrescritura puede producirse si la subclave predeterminada es el único origen de esa información).

Al asignar un ProgID a una extensión o protocolo de nombre de archivo, una aplicación puede asignar uno a uno o uno a varios. En el ejemplo de Contoso, ContosoHTML apunta a un solo ProgID que proporciona información de shellexecute para las extensiones .htm, .html, .shtml, .xht y .xhtml. Dado que existe un ProgID diferente para cada protocolo, cuando se usan protocolos, se habilita cada protocolo para que tenga su propia cadena de ejecución.

Cuando el tipo MIME se puede ver en línea en un explorador, el ProgID del tipo MIME debe contener la subclave **CLSID** que usa el identificador de clase (CLSID) de la aplicación correspondiente. Este CLSID se usa en una búsqueda en el CLSID de la base de datos MIME que se almacena en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Classes** \\ **MIME** \\ **Database** \\ **Content Type**. Si el tipo MIME no está pensado para que se vea en línea en un explorador, se puede omitir este paso.

### <a name="registration-subkey-and-value-descriptions"></a>Subclave de registro y descripciones de valores

En esta sección se describen las subclaves individuales del Registro y los valores usados para registrar una aplicación con programas **predeterminados,** como se ha ilustrado anteriormente.

### <a name="capabilities"></a>Funcionalidades

La  subclave Capabilities contiene toda la **información de programas** predeterminados para una aplicación específica. El marcador de posición %ApplicationCapabilityPath% hace referencia a la ruta de acceso del Registro de **HKEY \_ CURRENT \_ USER** o **HKEY \_ LOCAL \_ MACHINE** a la subclave **Capabilities de la** aplicación. Esta subclave contiene los valores significativos que se muestran en la tabla siguiente.



| Valor                  | Tipo                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ SZ o REG EXPAND \_ \_ SZ | **Requerido**. Para permitir que un usuario realice una opción de asignación predeterminada informada, una aplicación debe proporcionar una cadena que describa las funcionalidades de la aplicación. Aunque en el ejemplo anterior de Contoso se asigna la descripción directamente al valor ApplicationDescription, las aplicaciones suelen proporcionar la descripción como un recurso insertado en un archivo .dll para facilitar la localización. Si no se proporciona ApplicationDescription, la aplicación no aparece en las listas de interfaz de usuario de los programas predeterminados potenciales.                                                            |
| ApplicationName        | REG \_ SZ o REG EXPAND \_ \_ SZ | **Opcional.** Nombre por el que el programa aparece en la interfaz de usuario Programas predeterminados. Si la aplicación no proporciona estos datos, en la interfaz de usuario se usa el nombre del programa ejecutable asociado al primer ProgID registrado para la aplicación. ApplicationName siempre debe coincidir con el nombre registrado en [RegisteredApplications.](#registeredapplications) Puede usar ApplicationName si desea que distintos tipos de aplicación, como un explorador y un cliente de correo electrónico, apunten al mismo archivo ejecutable mientras aparecen como nombres diferentes.<br/> |
| Hidden                 | REG \_ DWORD                 | **Opcional.** Establezca este valor en 1 para suprimir la aplicación de la lista de programas del cuadro de **diálogo Establecer los programas** predeterminados. Si este valor es 0 o no está presente, la aplicación aparece normalmente en la lista.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

La **subclave FileAssociations** contiene asociaciones de archivo específicas que la aplicación reclama. Estas notificaciones se almacenan como valores, con un valor para cada extensión. Las asociaciones apuntan a un ProgID específico de la aplicación en lugar de a un ProgID genérico. Sin embargo, no es necesario que todas las asociaciones apunten al mismo ProgID.

### <a name="mimeassociations"></a>MIMEAssociations

La **subclave MIMEAssociations** contiene tipos MIME específicos que la aplicación reclama. Estas notificaciones se almacenan como valores, con un valor para cada tipo MIME. El nombre de valor de cada tipo MIME debe coincidir exactamente con el nombre MIME que se almacena en la base de datos MIME. Al valor también se le debe asignar un ProgID específico de la aplicación que contenga el CLSID correspondiente de la aplicación.

### <a name="startmenu"></a>Startmenu

La **subclave Startmenu** está asociada a las entradas de **Internet** y **correo** electrónico asignables por el usuario en el **menú** Inicio. Una aplicación debe registrarse por separado como contendiente para esas entradas. Para obtener más información, [vea Registrar programas con tipos de cliente.](reg-middleware-apps.md)

> [!Note]  
> A partir Windows 7, ya no hay entradas de **Internet** y **correo** electrónico en el **menú** Inicio. Los datos del  Registro asociados a la entrada de correo electrónico se siguen utilizando para el cliente PREDETERMINADO de LDAP, pero los datos del Registro asociados a la entrada de **Internet** no se usan Windows en absoluto.

 

Al asociar el registro **del** menú Inicio de una aplicación a su registro de **programas** predeterminados, la aplicación aparece como un posible valor predeterminado en la interfaz de usuario **Establecer asociaciones.** Si el usuario ha elegido la aplicación como predeterminada y, a continuación, elige  restaurar todos los valores predeterminados de la aplicación más adelante, la aplicación se restaura a su posición de menú Inicio para ese usuario. Para obtener más información e ilustración, vea la sección Interfaz de usuario [de programas](#default-programs-ui) predeterminados más adelante en este tema.

La **subclave Startmenu** tiene dos entradas: StartMenuInternet y Mail,  que corresponden a las posiciones canónicas de **Internet** y Correo electrónico en el **menú** Inicio. Una aplicación asigna a StartMenuInternet o Mail un valor igual al nombre de la subclave registrada de la aplicación en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet** o **HKEY LOCAL \_ \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **Mail** (como [](reg-middleware-apps.md)se describe en Registro de programas con tipos de cliente).

En el caso  de la posición canónica del correo electrónico en el menú Inicio, representa el cliente PREDETERMINADO de LAN Y, por lo tanto, se supone que es capaz de entregar llamadas DE LAN.  En Windows 7, aunque ya no  hay una posición canónica de correo electrónico en el menú Inicio, esta subclave se sigue utilizando para el cliente PREDETERMINADO DE LA RUTA DE ACCESO.  Una aplicación que reclame el valor predeterminado de correo debe registrarse como un controlador DE PROTOCOLO DE SEGURIDAD en la subclave siguiente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Si un cliente de correo no es  compatible  con MAPI pero todavía desea contender por la posición canónica del correo electrónico del menú Inicio, puede registrar una línea de comandos en la subclave siguiente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

Además, en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **Mail** \\ *CanonicalName* agregue un valor predeterminado con el nombre de la aplicación.

Estas entradas permiten iniciar la aplicación desde la **posición** **de correo** electrónico del menú Inicio. Tenga en cuenta que todavía se realizan llamadas DE LAN a la aplicación y que pasan al controlador DE LAN anterior, o bien se producirá un error si no se ha establecido ningún controlador DE LAE. Para obtener más información, [vea Registrar programas con tipos de cliente.](reg-middleware-apps.md)

### <a name="urlassociations"></a>UrlAssociations

La **subclave UrlAssociations** contiene los protocolos de dirección URL específicos que reclama la aplicación. Estas notificaciones se almacenan como valores, con un valor para cada protocolo. Cada protocolo debe apuntar a un ProgID específico de la aplicación en lugar de a un ProgID genérico. Como se mencionó en el ejemplo de Contoso, puede usar un ProgID diferente para cada protocolo para que cada uno tenga su propia cadena de ejecución.

### <a name="registeredapplications"></a>RegisteredApplications

La subclave completa **para RegisteredApplications** es:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **RegisteredApplications**

Esta subclave proporciona al sistema operativo la ubicación del Registro de la **información de programas predeterminados** de la aplicación. La ubicación se almacena como un valor cuyo nombre debe coincidir con el nombre de la aplicación.

### <a name="full-registration-example"></a>Ejemplo de registro completo

En este ejemplo se muestran las subclaves y los valores que se usan para registrar el reproductor multimedia ficticio de Litware. En el ejemplo se incluyen las entradas progID para mostrar cómo encaja todo.

La subclave siguiente muestra el ProgID específico de la aplicación para el .mp3 MIME:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

A continuación, se encuentra el ProgID específico de la aplicación que asocia el programa Litware con la .mp3 de nombre de archivo.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

En las entradas siguientes se muestra el ProgID combinado para el .mpeg tipo MIME y la extensión de nombre de archivo.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

Las entradas siguientes registran el programa Litware en **Programas predeterminados** y usan los ProgID registrados anteriormente.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

Por último, en este ejemplo se registra la ubicación del registro **de programas predeterminados de** Litware.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Convertirse en el explorador predeterminado

El registro del explorador debe seguir los procedimientos recomendados descritos en este tema. Cuando se instala el explorador, Windows puede presentar al usuario una notificación del sistema a través de la cual el usuario puede seleccionar el explorador como valor predeterminado del sistema. Esta notificación se muestra cuando se cumplen estas condiciones:

-   El instalador del explorador llama a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con la marca **\_ ASSOCCHANGED de SHCNE** para indicar Windows que se han registrado nuevos controladores de protocolo.
-   Windows detecta que una o varias aplicaciones nuevas se han registrado para controlar los protocolos http:// y https://, y el usuario aún no ha recibido una notificación. En otras palabras, no se ha mostrado nada de lo siguiente al usuario: una notificación del sistema que anuncia la aplicación, un control flyout OpenWith que contiene la aplicación o la página Establecer valores predeterminados de usuario (SUD) Panel de control la aplicación.

En el ejemplo siguiente se muestra el código de registro recomendado que el instalador del explorador debe ejecutar después de escribir sus claves del Registro.

[**SHChangeNotify notifica**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) primero al sistema que hay nuevas opciones de asociación disponibles. La **llamada SHChangeNotify** es necesaria para garantizar el funcionamiento correcto de los valores predeterminados del sistema.

A [**continuación,**](/windows/win32/api/synchapi/nf-synchapi-sleep) una instrucción Sleep permite que los procesos del sistema controle la notificación.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Si el usuario descarta o omite la notificación o el control flyout resultantes sin realizar una nueva selección predeterminada del explorador, el explorador predeterminado permanece sin cambios. Tenga en cuenta que el usuario también puede cambiar el explorador predeterminado en cualquier momento a través de otros mecanismos, incluido Establecer valores predeterminados de usuario en el Panel de control.

## <a name="default-programs-ui"></a>Interfaz de usuario de programas predeterminada

En las ilustraciones de esta sección se muestra la interfaz de usuario **de los programas predeterminados** tal como lo ve el usuario.

En la ilustración siguiente se muestra la **ventana programas predeterminados** principal de Panel de control.

![captura de pantalla de la página de entrada de programas predeterminada](images/defaultprogramsmain.png)

Cuando un usuario elige la opción **Establecer los programas predeterminados,** aparece la siguiente ventana. Los usuarios pueden usar esta página para asignar un programa predeterminado para todos los tipos de archivo y protocolos para los que el programa es un posible valor predeterminado. Como se muestra en la ilustración siguiente, todos los [programas registrados](#registering-an-application-for-use-with-default-programs) y el icono de programa aparecen en el **cuadro Programas** de la izquierda.

![captura de pantalla de la página establecer los programas predeterminados](images/setyourdefaultprograms.png)

Cuando el usuario selecciona un programa de la lista, se muestran el icono del programa y el proveedor. Si la dirección URL está incrustada en el certificado firmado digitalmente del programa, el programa también puede mostrar una dirección URL. Los programas que no están firmados digitalmente no pueden mostrar una dirección URL.

También se muestra el texto descriptivo proporcionado por el programa durante el registro. Este texto es obligatorio. Debajo del cuadro de descripción hay una indicación de cuántos valores predeterminados está asignado actualmente el programa del número completo que se registra para controlar.

Para asignar o restaurar un programa como predeterminado para todos los archivos y protocolos para los que está registrado, el usuario hace clic en la opción Establecer este programa **como** predeterminado.

Para asignar tipos de archivo y protocolos individuales  a un programa, el usuario  hace clic en la opción Elegir valores predeterminados para este programa, que muestra una ventana Establecer asociaciones para un programa como la de la ilustración siguiente.

> [!Note]  
> Se recomienda llamar a las asociaciones **Set** de un programa mediante [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).

 

![captura de pantalla del conjunto de asociaciones de una página del programa](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Procedimientos recomendados para usar programas predeterminados

En esta sección se proporcionan instrucciones de procedimientos recomendados para **usar programas predeterminados** al registrar aplicaciones. También ofrece sugerencias de diseño para crear una aplicación que proporciona a los usuarios una **funcionalidad óptima de programas predeterminados.**

### <a name="during-installation"></a>Durante la instalación

Además de los procedimientos de instalación que se suelen practicar en Windows XP, una  aplicación basada en Windows Vista o posterior debe registrarse con la característica Programas predeterminados para aprovechar su funcionalidad.

Realice la siguiente secuencia de pasos durante la instalación. Los pasos del 1 al 3 coinciden con los pasos que se usaron en Windows XP; El paso 4 era nuevo en Windows Vista.

1.  Instale los archivos binarios necesarios.
2.  Escriba ProgID en HKEY \_ LOCAL \_ MACHINE. Tenga en cuenta que las aplicaciones deben crear progID específicos de la aplicación para sus asociaciones.
3.  Registre la aplicación con **programas predeterminados como** se explicó anteriormente en Registro de una aplicación para su uso con programas [predeterminados.](#registering-an-application-for-use-with-default-programs)

### <a name="after-installation"></a>Después de la instalación

En esta sección se describe cómo el símbolo del sistema de la aplicación debe presentar primero sus opciones predeterminadas a cada usuario. También se describe cómo una aplicación puede supervisar su estado como valor predeterminado para sus posibles asociaciones y protocolos.

### <a name="first-run-experiences"></a>Experiencias de primera ejecución

Cuando un usuario ejecuta la aplicación por primera vez, se recomienda que la aplicación muestre la interfaz de usuario al usuario que normalmente incluye estas dos opciones:

-   Acepte la configuración predeterminada de la aplicación. Esta opción está seleccionada de forma predeterminada.
-   Personalice la configuración predeterminada de la aplicación.

Antes de Windows 8, si el usuario acepta la configuración predeterminada, la aplicación llama a [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), que convierte todas las asociaciones de nivel de equipo declaradas durante la instalación en la configuración por usuario para ese usuario.

Si el usuario decide personalizar la configuración, la aplicación llama a [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) para mostrar la interfaz de usuario de asociación de archivos. En la ilustración siguiente se muestra esta ventana para el reproductor multimedia ficticio litware.

![captura de pantalla de las asociaciones de conjunto para una página de programa para litware](images/setassociationsforaprogramforlitware.png)

La ventana de asociación de archivos muestra los valores predeterminados que registró la aplicación y también muestra el valor predeterminado actual para otras extensiones y protocolos. Una vez que el usuario termina de personalizar sus valores predeterminados, hace clic **en** el botón Guardar para confirmar los cambios. Si el usuario hace clic **en Cancelar**, la ventana se cierra sin guardar los cambios.

Debe usar esta interfaz de usuario para las aplicaciones en lugar de crear la suya propia. Al hacerlo, guarda los recursos que anteriormente eran necesarios para desarrollar la interfaz de usuario de asociación de archivos. También garantiza que las asociaciones se guardan correctamente.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Establecer una aplicación para comprobar si es el valor predeterminado

> [!Note]  
> Esto ya no se admite a Windows 8.

 

Las aplicaciones suelen comprobar si se establecen como valor predeterminado cuando se ejecutan. Establezca las aplicaciones para realizar esta comprobación mediante una llamada a [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) o [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).

Si la aplicación determina que no es el valor predeterminado, puede presentar una interfaz de usuario que pregunte al usuario si debe aceptar la situación actual o si quiere que la aplicación sea el valor predeterminado. Incluya siempre una casilla en esta interfaz de usuario que esté seleccionada de forma predeterminada y que presente la opción para no volver a solicitarla.

> [!Note]  
> La opción predeterminada debe estar controlada por el usuario. Una aplicación nunca debe reclamar un valor predeterminado sin preguntar al usuario.

 

En la ilustración siguiente se muestra un cuadro de diálogo de ejemplo.

![captura de pantalla de un cuadro de diálogo de ejemplo](images/notthedefaultui.png)

## <a name="additional-resources"></a>Recursos adicionales

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Escenario de ejemplo de asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Establecer el acceso a programas y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
