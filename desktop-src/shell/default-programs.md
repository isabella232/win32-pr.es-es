---
description: Use programas predeterminados para establecer la experiencia del usuario predeterminada.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programas predeterminados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "103913910"
---
# <a name="default-programs"></a>Programas predeterminados

Use **programas predeterminados** para establecer la experiencia del usuario predeterminada. Los usuarios pueden tener acceso a **programas predeterminados** desde el panel de control o directamente desde el menú **Inicio** . Configurar la herramienta de [acceso a programas y valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md) , la experiencia de valores predeterminados principales para los usuarios de Windows XP, es ahora una parte de los **programas predeterminados**.

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que las asociaciones de archivos predeterminadas funcionan en Windows 10. Para obtener más información, consulte la sección **cambios en la forma en que Windows 10 trata las aplicaciones predeterminadas** en [esta publicación](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Cuando un usuario establece los valores predeterminados del programa mediante **programas predeterminados**, la configuración predeterminada solo se aplica a ese usuario y no a otros usuarios que puedan usar el mismo equipo. **Programas predeterminados** proporciona un conjunto de API (en desuso en Windows 8) que permiten a los fabricantes de software independientes (ISV) incluir sus programas o aplicaciones en el sistema de valores predeterminados. El conjunto de API también ayuda a los ISV a administrar mejor su estado como valores predeterminados.

Este tema se organiza de la siguiente manera:

-   [Introducción a los programas predeterminados y a su conjunto de API relacionado](#introduction-to-default-programs-and-its-related-api-set)
-   [Registro de una aplicación para su uso con programas predeterminados](#registering-an-application-for-use-with-default-programs)
    -   [ProgID](#progids)
    -   [Descripciones de subclave y valor de registro](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Ejemplo de registro completo](#full-registration-example)
-   [Convertirse en el explorador predeterminado](#becoming-the-default-browser)
-   [Interfaz de usuario de programas predeterminados](#default-programs-ui)
-   [Prácticas recomendadas para usar programas predeterminados](#best-practices-for-using-default-programs)
    -   [Durante la instalación](#during-installation)
    -   [Después de la instalación](#after-installation)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Introducción a los programas predeterminados y a su conjunto de API relacionado

Los **programas predeterminados** se han diseñado principalmente para las aplicaciones que usan tipos de archivo estándar, como archivos. mp3 o. jpg o protocolos estándar, como http o mailto. Las aplicaciones que usan sus propios protocolos y asociaciones de archivo propios no suelen usar la funcionalidad **programas predeterminados** .

Después de registrar una aplicación para la funcionalidad de **programas predeterminados** , las siguientes opciones y funcionalidades están disponibles mediante el conjunto de API:

-   Restaurar todos los valores predeterminados registrados de una aplicación. En desuso para Windows 8.
-   Restaurar un único valor predeterminado registrado para una aplicación. En desuso para Windows 8.
-   Consulta el propietario de un valor predeterminado específico en una sola llamada en lugar de buscarlo en el registro. Puede consultar el valor predeterminado de una asociación de archivo, un protocolo o un verbo canónico del menú **Inicio** .
-   Inicia una interfaz de usuario para una aplicación específica en la que un usuario puede establecer valores predeterminados individuales.
-   Quite todas las asociaciones por usuario.

**Programas predeterminados** también proporciona una interfaz de usuario que permite registrar una aplicación con el fin de proporcionar información adicional al usuario. Por ejemplo, una aplicación firmada digitalmente puede incluir una dirección URL a la Página principal del fabricante.

El uso del conjunto de API asociado puede ayudar a que una aplicación funcione correctamente en la característica control de cuentas de usuario (UAC) introducida en Windows Vista. En UAC, un administrador aparece como un usuario estándar en el sistema, por lo que el administrador no suele escribir en el subárbol de la **\_ \_ máquina local HKEY** . Esta restricción es una característica de seguridad que impide que un proceso actúe como administrador sin el conocimiento del administrador.

La instalación de un programa por parte de un usuario se realiza normalmente como un proceso con privilegios elevados. Sin embargo, los intentos de una aplicación para modificar los comportamientos de asociación predeterminados en un nivel de equipo posterior a la instalación no se realizarán correctamente. En su lugar, los valores predeterminados deben registrarse en un nivel por usuario, lo que impide que varios usuarios sobrescriban los valores predeterminados de los demás.

La estructura jerárquica del registro para las asociaciones de archivos y protocolos da prioridad a los valores predeterminados por usuario a través de los valores predeterminados de nivel de equipo. Algunas aplicaciones incluyen puntos en el código que elevan temporalmente sus derechos cuando reclaman valores predeterminados registrados en **HKEY \_ local \_ Machine**. Estas aplicaciones podrían experimentar resultados inesperados si otra aplicación ya está registrada como predeterminada por usuario. El uso de **programas predeterminados** evita esta ambigüedad y garantiza los resultados esperados en un nivel por usuario.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registro de una aplicación para su uso con programas predeterminados

En esta sección se muestran las subclaves del registro y los valores necesarios para registrar una aplicación con **programas predeterminados**. Incluye un ejemplo completo.

Esta sección contiene los siguientes temas:

-   [ProgID](#progids)
-   [Descripciones de subclave y valor de registro](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Ejemplo de registro completo](#full-registration-example)

**Programas predeterminados** requiere que cada aplicación se registre explícitamente las asociaciones de archivo, las asociaciones MIME y los protocolos para los que la aplicación debe aparecer como un valor predeterminado posible. Las asociaciones se registran mediante los siguientes elementos del registro, que se explican en detalle más adelante en este tema, en [descripciones de subclave y valor de registro](#registration-subkey-and-value-descriptions):

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

En el ejemplo siguiente se muestran las entradas del registro para un explorador ficticio de Contoso denominado WebBrowser:

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

Una aplicación debe proporcionar un [ProgID](fa-progids.md)específico. Asegúrese de incluir toda la información que se escribe normalmente en la subclave predeterminada genérica de la extensión. Por ejemplo, el reproductor multimedia ficticio ficticia proporciona las clases de software del **\_ \_ equipo local HKEY** específico de la aplicación \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** subclave. Esa subclave incluye toda la información de la subclave predeterminada genérica **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\ **. mp3** y cualquier información adicional que desee que la aplicación registre. Esto garantiza que si el usuario restaura la asociación. mp3 al reproductor de Litware, la información del jugador de Litware está intacta y no se ha sobrescrito por otra aplicación. (Se puede sobrescribir si la subclave predeterminada es el único origen de esa información).

Cuando se asigna un ProgID a una extensión de nombre de archivo o protocolo, una aplicación puede asignar uno a uno o uno a varios. En el ejemplo de Contoso, ContosoHTML señala a un ProgID único que proporciona información de ShellExecute para las extensiones. htm,. html,. shtml,. XHT y. XHTML. Dado que existe un ProgID diferente para cada protocolo, cuando se utilizan protocolos se habilita cada protocolo para que tenga su propia cadena de ejecución.

Cuando el tipo MIME se puede ver en línea en un explorador, el ProgID del tipo MIME debe contener la subclave **CLSID** que usa el identificador de clase (CLSID) de la aplicación correspondiente. Este CLSID se usa en una búsqueda en el CLSID en la base de datos MIME almacenada en **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\ **MIME** \\ **Database** \\ **Type**. Si el tipo MIME no se ha diseñado para que se vea en línea en un explorador, este paso se puede omitir.

### <a name="registration-subkey-and-value-descriptions"></a>Descripciones de subclave y valor de registro

En esta sección se describen las subclaves individuales del registro y los valores que se usan para registrar una aplicación con **programas predeterminados**, como se muestra anteriormente.

### <a name="capabilities"></a>Funcionalidades

La subclave **Capabilities** contiene toda la información de **programas predeterminados** para una aplicación específica. El marcador de posición% ApplicationCapabilityPath% hace referencia a la ruta de acceso del registro desde **HKEY \_ Current \_ User** o **HKEY \_ local \_ Machine** a la subclave **Capabilities** de la aplicación. Esta subclave contiene los valores significativos que se muestran en la tabla siguiente.



| Value                  | Tipo                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ SZ o REG \_ Expand \_ | **Requerido**. Para permitir que un usuario realice una elección de asignación predeterminada informada, una aplicación debe proporcionar una cadena que describa las capacidades de la aplicación. Aunque el ejemplo de Contoso anterior asigna la descripción directamente al valor de ApplicationDescription, las aplicaciones normalmente proporcionan la descripción como un recurso que se inserta en un archivo. dll para facilitar la localización. Si no se proporciona ApplicationDescription, la aplicación no aparece en las listas de interfaz de usuario de posibles programas predeterminados.                                                            |
| ApplicationName        | REG \_ SZ o REG \_ Expand \_ | **Opcional.** El nombre por el que aparece el programa en la interfaz de usuario de programas predeterminados. Si la aplicación no proporciona estos datos, en la interfaz de usuario se usa el nombre del programa ejecutable que está asociado al primer ProgID registrado para la aplicación. ApplicationName siempre debe coincidir con el nombre registrado en [RegisteredApplications](#registeredapplications). Puede usar ApplicationName si desea diferentes tipos de aplicaciones, como un explorador y un cliente de correo electrónico, para que apunten al mismo archivo ejecutable mientras aparecen como nombres diferentes.<br/> |
| Hidden                 | \_valor DWORD reg                 | **Opcional.** Establezca este valor en 1 para suprimir la aplicación de la lista de programas en el cuadro de diálogo **establecer programas predeterminados** . Si este valor es 0 o no está presente, la aplicación aparece en la lista normalmente.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

La subclave **FileAssociations** contiene asociaciones de archivo específicas que se reclaman por la aplicación. Estas notificaciones se almacenan como valores, con un valor para cada extensión. Las asociaciones apuntan a un ProgID específico de la aplicación en lugar de un ProgID genérico. Sin embargo, no es necesario que todas las asociaciones señalen al mismo ProgID.

### <a name="mimeassociations"></a>MIMEAssociations

La subclave **MIMEAssociations** contiene tipos MIME específicos que se reclaman por la aplicación. Estas notificaciones se almacenan como valores, con un valor para cada tipo MIME. El nombre de valor de cada tipo MIME debe coincidir exactamente con el nombre MIME almacenado en la base de datos MIME. También se debe asignar al valor un ProgID específico de la aplicación que contenga el CLSID correspondiente de la aplicación.

### <a name="startmenu"></a>Inicio

La subclave **Inicio** está asociada a las entradas de **correo electrónico** y de **Internet** asignables por el usuario en el menú **Inicio** . Una aplicación debe registrarse por separado como un contratador para esas entradas. Para obtener más información, consulte [registrar programas con tipos de cliente](reg-middleware-apps.md).

> [!Note]  
> A partir de Windows 7, ya no hay entradas de **Internet** y de **correo electrónico** en el menú **Inicio** . Los datos del registro asociados a la entrada de **correo electrónico** se siguen usando para el cliente MAPI predeterminado, pero Windows no utiliza los datos del registro asociados a la entrada de **Internet** .

 

Al asociar el registro del menú **Inicio** de una aplicación con el registro de sus **programas predeterminados** , la aplicación aparece como valor predeterminado potencial en la interfaz de usuario de **asociaciones de conjunto** . Si el usuario ha elegido la aplicación como predeterminada y, a continuación, elige restaurar todos los valores predeterminados de la aplicación más tarde, la aplicación se restaura en su posición en el menú **Inicio** para ese usuario. Para obtener más información y una ilustración, vea la sección [interfaz de usuario de programas predeterminados](#default-programs-ui) más adelante en este tema.

La subclave **Inicio** tiene dos entradas: StartMenuInternet y mail, que corresponden a las posiciones de **Internet** y **correo electrónico** canónicas en el menú **Inicio** . Una aplicación asigna StartMenuInternet o mail un valor igual al nombre de la subclave registrada de la aplicación en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** o **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** (como se describe en [registrar programas con tipos de cliente](reg-middleware-apps.md)).

En el caso de la posición canónica de **correo electrónico** en el menú **Inicio** , representa el cliente MAPI predeterminado y, por lo tanto, se supone que es capaz de controlar las llamadas MAPI. En Windows 7, aunque ya no existe una posición canónica de **correo electrónico** en el menú **Inicio** , esta subclave se sigue usando para el cliente MAPI predeterminado. Una aplicación que solicite el correo predeterminado debe registrarse como controlador MAPI en la siguiente subclave:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Si un cliente de correo no admite MAPI pero aún desea competir por la posición canónica de **correo electrónico** del menú **Inicio** , puede registrar una línea de comandos en la siguiente subclave:

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

Además, en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** \\ *CanonicalName* , agregue un valor predeterminado con el nombre de la aplicación.

Estas entradas permiten que la aplicación se inicie desde la posición de **correo electrónico** del menú **Inicio** . Tenga en cuenta que las llamadas MAPI todavía se realizan en la aplicación y se llevan a cabo hasta el controlador MAPI anterior, o bien se produce un error si no se ha establecido ningún controlador MAPI. Para obtener más información, consulte [registrar programas con tipos de cliente](reg-middleware-apps.md).

### <a name="urlassociations"></a>UrlAssociations

La subclave **UrlAssociations** contiene los protocolos de dirección URL específicos que solicita la aplicación. Estas notificaciones se almacenan como valores, con un valor para cada protocolo. Cada protocolo debe apuntar a un ProgID específico de la aplicación en lugar de a un ProgID genérico. Como se mencionó en el ejemplo de Contoso, puede usar un ProgID diferente para cada protocolo para que cada uno tenga su propia cadena de ejecución.

### <a name="registeredapplications"></a>RegisteredApplications

La subclave completa de **RegisteredApplications** es:

**HKEY \_ \_** RegisteredApplications de \\ **software** \\  de equipo local

Esta subclave proporciona el sistema operativo con la ubicación del registro de la información de **programas predeterminados** para la aplicación. La ubicación se almacena como un valor cuyo nombre debe coincidir con el nombre de la aplicación.

### <a name="full-registration-example"></a>Ejemplo de registro completo

En este ejemplo se muestran las subclaves y los valores que se usan para registrar el reproductor multimedia ficticio ficticia. En el ejemplo se incluyen las entradas ProgID para mostrar cómo encaja todo.

La siguiente subclave muestra el ProgID específico de la aplicación para el tipo MIME. mp3:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

A continuación se encuentra el ProgID específico de la aplicación que asocia el programa Litware a la extensión de nombre de archivo. mp3.

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

Las entradas siguientes muestran el ProgID combinado para el tipo MIME de. MPEG y la extensión de nombre de archivo.

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

Las siguientes entradas registran el programa Litware en **programas predeterminados** y usan los ProgID previamente registrados

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

Por último, en este ejemplo se registra la ubicación del registro de **programas predeterminados** de Litware.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Convertirse en el explorador predeterminado

El registro del explorador debe seguir las prácticas recomendadas que se describen en este tema. Cuando se instala el explorador, Windows puede presentar al usuario una notificación del sistema a través de la cual el usuario puede seleccionar el explorador como predeterminado del sistema. Esta notificación se muestra cuando se cumplen estas condiciones:

-   El instalador del explorador llama a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con la marca **SHCNE \_ ASSOCCHANGED** para indicar a Windows que se han registrado nuevos controladores de protocolo.
-   Windows detecta que una o varias aplicaciones nuevas se han registrado para controlar los protocolos http://y https://, y el usuario aún no se ha notificado. En otras palabras, no se ha mostrado nada de lo siguiente al usuario: una notificación del sistema que anuncia la aplicación, un control flotante de OpenWith que contiene la aplicación o la página del panel de control establecer valores predeterminados del usuario (SUD) para la aplicación.

En el ejemplo siguiente se muestra el código de registro recomendado que el instalador del explorador debe ejecutar después de escribir sus claves del registro.

[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) primero notifica al sistema que hay disponibles nuevas opciones de asociación. La llamada a **SHChangeNotify** es necesaria para garantizar el correcto funcionamiento de los valores predeterminados del sistema.

Una instrucción [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) permite a los procesos del sistema controlar la notificación.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Si el usuario descarta u omite la notificación o el control flotante resultante sin crear una nueva selección predeterminada del explorador, el explorador predeterminado permanece inalterado. Tenga en cuenta que el usuario también puede cambiar el explorador predeterminado en cualquier momento a través de otros mecanismos, incluidos los valores predeterminados establecidos por el usuario en el panel de control.

## <a name="default-programs-ui"></a>Interfaz de usuario de programas predeterminados

En las ilustraciones de esta sección se muestra la interfaz de usuario de los **programas predeterminados** tal y como se muestra en el usuario.

En la ilustración siguiente se muestra la ventana **programas predeterminados** principales del panel de control.

![captura de pantalla de la página de entrada programas predeterminados](images/defaultprogramsmain.png)

Cuando un usuario elige la opción **establecer programas predeterminados** , aparece la siguiente ventana. Los usuarios pueden usar esta página para asignar un programa predeterminado para todos los tipos de archivos y protocolos para los que el programa sea un valor predeterminado posible. Como se muestra en la siguiente ilustración, todos los programas [registrados](#registering-an-application-for-use-with-default-programs) y el icono del programa aparecen en el cuadro **programas** de la izquierda.

![captura de pantalla de la página establecer programas predeterminados](images/setyourdefaultprograms.png)

Cuando el usuario selecciona un programa de la lista, se muestran el icono del programa y el proveedor. Si la dirección URL está incrustada en el certificado firmado digitalmente del programa, el programa también puede mostrar una dirección URL. Los programas que no están firmados digitalmente no pueden mostrar una dirección URL.

También se muestra el texto descriptivo, proporcionado por el programa durante el registro. Este texto es obligatorio. Debajo del cuadro Descripción se indica el número de valores predeterminados que el programa actualmente tiene asignados fuera del número completo en el que está registrado.

Para asignar o restaurar un programa como valor predeterminado para todos los archivos y protocolos para los que está registrado, el usuario hace clic en la opción **establecer este programa como predeterminado** .

Para asignar tipos de archivos y protocolos individuales a un programa, el usuario hace clic en la opción **elegir valores predeterminados para este programa** , que muestra un **conjunto de asociaciones para una** ventana de programa como la que aparece en la ilustración siguiente.

> [!Note]  
> Se recomienda llamar a las **asociaciones de conjuntos para un programa** mediante [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).

 

![captura de pantalla de la página establecer asociaciones para un programa](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Prácticas recomendadas para usar programas predeterminados

En esta sección se proporcionan instrucciones prácticas recomendadas para usar **programas predeterminados** al registrar aplicaciones. También ofrece sugerencias de diseño para crear una aplicación que proporciona a los usuarios una funcionalidad óptima de **programas predeterminados** .

### <a name="during-installation"></a>Durante la instalación

Además de los procedimientos de instalación que normalmente se usan en Windows XP, una aplicación basada en Windows Vista o posterior debe registrarse con la característica **programas predeterminados** para aprovechar su funcionalidad.

Realice la siguiente secuencia de pasos durante la instalación. Los pasos 1-3 coinciden con los pasos que se usaron en Windows XP; el paso 4 es nuevo en Windows Vista.

1.  Instale los archivos binarios necesarios.
2.  Escriba ProgIDs en el \_ equipo local HKEY \_ . Tenga en cuenta que las aplicaciones deben crear ProgID específicos de la aplicación para sus asociaciones.
3.  Registre la aplicación con los **programas predeterminados** tal como se explicó anteriormente en [el registro de una aplicación para su uso con programas predeterminados](#registering-an-application-for-use-with-default-programs).

### <a name="after-installation"></a>Después de la instalación

En esta sección se describe cómo el mensaje de la aplicación debe presentar primero sus opciones predeterminadas a cada usuario. También se explica cómo una aplicación puede supervisar su estado como valor predeterminado para sus posibles asociaciones y protocolos.

### <a name="first-run-experiences"></a>Experiencias de primera ejecución

Cuando un usuario ejecuta la aplicación por primera vez, se recomienda que la aplicación muestre la interfaz de usuario al usuario que normalmente incluye estas dos opciones:

-   Acepte la configuración predeterminada de la aplicación. Esta opción está seleccionada de forma predeterminada.
-   Personalizar la configuración predeterminada de la aplicación.

Antes de Windows 8, si el usuario acepta la configuración predeterminada, la aplicación llama a [**IApplicationAssociationRegistration:: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), que convierte todas las asociaciones de nivel de equipo que se declaran durante la instalación a la configuración por usuario para ese usuario.

Si el usuario decide personalizar la configuración, la aplicación llama a [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) para mostrar la interfaz de usuario de la Asociación de archivo. En la ilustración siguiente se muestra esta ventana para el reproductor multimedia ficticio ficticia.

![captura de pantalla de la página establecer asociaciones para un programa de Litware](images/setassociationsforaprogramforlitware.png)

La ventana Asociación de archivos muestra los valores predeterminados que ha registrado la aplicación y también muestra el valor predeterminado actual para otras extensiones y protocolos. Una vez que el usuario termina de personalizar sus valores predeterminados, haga clic en el botón **Guardar** para confirmar los cambios. Si el usuario hace clic en **Cancelar**, la ventana se cierra sin guardar los cambios.

Debe usar esta interfaz de usuario para sus aplicaciones en lugar de crear las suyas propias. Al hacerlo, se guardan los recursos necesarios para desarrollar la interfaz de usuario de la Asociación de archivos. También garantiza que las asociaciones se guarden correctamente.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Establecer una aplicación para comprobar si es el valor predeterminado

> [!Note]  
> Ya no se admite en Windows 8.

 

Normalmente, las aplicaciones comprueban si están establecidas como valor predeterminado cuando se ejecutan. Establezca las aplicaciones para realizar esta comprobación mediante una llamada a [**IApplicationAssociationRegistration:: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) o [**IApplicationAssociationRegistration:: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).

Si la aplicación determina que no es el valor predeterminado, puede presentar una interfaz de usuario que pida al usuario que acepte la situación actual o que la aplicación sea la predeterminada. Incluya siempre una casilla en esta interfaz de usuario que esté seleccionada de forma predeterminada y que presente la opción no volver a preguntar.

> [!Note]  
> La elección de default debe estar controlada por el usuario. Una aplicación nunca debe reclamar un valor predeterminado sin preguntar al usuario.

 

En la ilustración siguiente se muestra un cuadro de diálogo de ejemplo.

![captura de pantalla de un cuadro de diálogo de ejemplo](images/notthedefaultui.png)

## <a name="additional-resources"></a>Recursos adicionales

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Establecer los valores predeterminados de acceso a programas y del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
