---
description: 'En este tema se explica cómo registrar un programa en el registro de Windows como uno de los siguientes tipos de cliente: explorador, correo electrónico, reproducción multimedia, mensajería instantánea o máquina virtual para Java.'
title: Registrar programas con tipos de cliente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914245"
---
# <a name="registering-programs-with-client-types"></a>Registrar programas con tipos de cliente

En este tema se explica cómo registrar un programa en el registro de Windows como uno de los siguientes tipos de cliente: explorador, correo electrónico, reproducción multimedia, mensajería instantánea o máquina virtual para Java.

> [!Note]  
> Esta información se aplica a los siguientes sistemas operativos:
> 
> -   Windows 2000 Service Pack 3 (SP3)
> -   Windows 2000 Service Pack 4 (SP4)
> -   Windows XP Service Pack 1 (SP1)
> -   Windows XP Service Pack 2 (SP2)
> -   Windows XP Service Pack 3 (SP3)
> -   Windows Server 2003
> -   Windows Vista
> -   Windows Vista Service Pack 1 (SP1)
> -   Windows 8

 

En este tema se incluyen las secciones siguientes.

-   [Elementos comunes de registro para todos los tipos de cliente](#common-registration-elements-for-all-client-types)
    -   [Seleccionar un nombre canónico](#selecting-a-canonical-name)
    -   [Registrar el nombre para mostrar de un programa](#registering-a-programs-display-name)
    -   [Registrar el icono de un programa](#registering-a-programs-icon)
    -   [Registrar un verbo abierto](#registering-an-open-verb)
    -   [Registrar información de instalación](#registering-installation-information)
-   [Elementos de registro para tipos de cliente específicos](#registration-elements-for-specific-client-types)
    -   [Registro del menú Inicio](#start-menu-registration)
    -   [Registro del cliente de correo](#mail-client-registration)
-   [Completar registros de ejemplo](#complete-sample-registrations)
    -   [Un explorador de ejemplo](#a-sample-browser)
    -   [Un explorador de correo de ejemplo](#a-sample-mail-browser)
    -   [Media Player de ejemplo](#a-sample-media-player)
    -   [Un programa de mensajería instantánea de ejemplo](#a-sample-instant-messenger-program)
    -   [Una máquina virtual de ejemplo para Java](#a-sample-virtual-machine-for-java)
-   [Temas relacionados](#related-topics)

En este tema se amplía la documentación existente sobre el registro de un programa como un tipo de cliente determinado. Para obtener vínculos a esa documentación, consulte la sección temas relacionados.

## <a name="common-registration-elements-for-all-client-types"></a>Elementos comunes de registro para todos los tipos de cliente

Al registrar un programa como un tipo de cliente, la mayoría de las entradas del registro son las mismas independientemente del tipo de cliente. Sin embargo, algunas entradas del registro son específicas del tipo de cliente y se indican en la sección [elementos de registro para tipos de cliente específicos](#registration-elements-for-specific-client-types) .

En esta sección se tratan los temas siguientes:

-   [Seleccionar un nombre canónico](#selecting-a-canonical-name)
-   [Registrar el nombre para mostrar de un programa](#registering-a-programs-display-name)
-   [Registrar el icono de un programa](#registering-a-programs-icon)
-   [Registrar un verbo abierto](#registering-an-open-verb)
-   [Registrar información de instalación](#registering-installation-information)

> [!Note]  
> Los nombres de subclaves que se indican en cursiva en este tema son marcadores de posición para nombres de subclaves definidos por el usuario o un conjunto de valores posibles. En la sección [registros de ejemplo completos](#complete-sample-registrations) se proporcionan ejemplos completos con nombres de ejemplo.

 

Toda la información de registro de tipos de cliente se almacena en la subclave siguiente:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* es uno de los siguientes nombres de subclave:

-   StartMenuInternet (para exploradores)
-   Correo (por correo electrónico)
-   Medios (para la reproducción multimedia)
-   IM (para mensajería instantánea)
-   JavaVM (para la máquina virtual para Java)

En este tema, se anotarán las referencias a un programa de equipo ficticio denominado "Lit View" de Litware Inc., con un archivo ejecutable denominado Litview.exe. Este programa hipotético se usa indistintamente como una mensajería instantánea, un explorador u otro tipo de programa cliente según sea necesario con fines ilustrativos.

### <a name="selecting-a-canonical-name"></a>Seleccionar un nombre canónico

El proveedor debe elegir un *nombre canónico* para el programa. El nombre canónico nunca se muestra al usuario, por lo que no es necesario localizarlo. Su única finalidad es proporcionar una cadena única que se pueda usar para identificar el programa. Normalmente es el mismo que el nombre en inglés del programa, pero esto es simplemente una Convención.

En el caso de tipos de cliente distintos de los exploradores, el nombre canónico puede ser cualquier cadena. Elija un nombre único, uno que no es probable que sea utilizado por otro proveedor.

En el caso de los clientes del explorador, el nombre canónico debe ser el nombre, incluida la extensión, del ejecutable asociado; por ejemplo, "Litview.exe".

Estos son algunos ejemplos de nombres canónicos.

-   Iexplore.exe (explorador)
-   Correo de Windows (correo electrónico)
-   Windows Media Player (multimedia)
-   Windows Messenger (mensajería instantánea)

Registre el nombre canónico mediante la creación de una subclave, como se muestra aquí. El nombre de la subclave es el nombre canónico. Toda la información relacionada con el registro de ese programa existirá en esta subclave.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Registrar el nombre para mostrar de un programa

El siguiente paso del registro consiste en especificar el nombre para mostrar del programa. Se proporciona como un valor en la clave de nombre canónico, como se muestra aquí. Tenga en cuenta de nuevo que *CanonicalName* y *ClientTypeName* no son los nombres reales de las claves, sino solo los marcadores de posición para los nombres verdaderos, como *Lit View*.

> [!Note]  
> A partir de Windows 8, el nombre que se usa para registrar para [configurar el acceso a programas y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md) y para los [programas predeterminados](default-programs.md) debe coincidir para que los cambios de SPAD desencadenen los registros de programas predeterminados.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

El valor de **LocalizedString** es una \_ cadena de reg SZ y consta de un signo de arroba (@), la ruta de acceso completa a un archivo. dll o. exe, una coma, un signo menos y un entero decimal. El entero decimal es el identificador de un recurso de cadena, incluido en el archivo. dll o. exe, cuyo valor se va a mostrar al usuario como el nombre de este cliente. Tenga en cuenta que la ruta de acceso del archivo no requiere comillas, aunque contenga espacios.

El registro de la cadena del nombre para mostrar de esta manera permite usar el mismo registro para varios idiomas. Cada instalación de idioma proporciona un archivo de recursos diferente con el nombre para mostrar almacenado en el mismo identificador de recurso.

En el ejemplo siguiente se muestra el registro de un programa de mensajería instantánea de la vista ficticia Lit. Dado que se trata de un programa de mensajería instantánea, la subclave *CanonicalName* (en este caso, la *vista Lit*) se almacena en la subclave **im** .

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Tenga en cuenta el uso de la entrada (valor predeterminado) como una declaración secundaria del nombre para mostrar del cliente. Si **LocalizedString** no está presente, se utiliza en su lugar el valor (predeterminado). Esto funciona con todos los tipos de cliente (exploradores de Internet, exploradores de correo electrónico, mensajería instantánea y reproductores multimedia). Para mantener la compatibilidad con el [diseño del registro del cliente de Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), los programas de correo electrónico deben establecer el valor (predeterminado) de la subclave *CanonicalName* en el nombre para mostrar del cliente en el idioma instalado actualmente.

### <a name="registering-a-programs-icon"></a>Registrar el icono de un programa

> [!Note]  
> Esta sección no se aplica a Windows 2000.

 

De forma predeterminada, la sección superior del menú **Inicio** de Windows XP y Windows vista contiene iconos de **Internet** y **correo electrónico** . Estos iconos no están presentes en Windows 7 y versiones posteriores. En el caso de los clientes de explorador y de correo electrónico, cuando se asigna un programa como valor predeterminado para su tipo de cliente, se muestra el icono registrado de ese programa para dichas entradas en el menú **Inicio** .

El registro del icono de un programa es obligatorio para los clientes de explorador y de correo electrónico. El registro de un icono para la reproducción multimedia, mensajería instantánea o máquina virtual para tipos de cliente Java es opcional, y los iconos registrados para esos tipos de cliente no se usan actualmente en Windows y no se muestran en la sección superior de los menús **Inicio** de Windows XP o Windows Vista.

Para registrar un icono para un programa cliente, agregue una subclave **DefaultIcon** con un valor predeterminado, como se muestra aquí.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

El valor **filePath** es la ruta de acceso completa al archivo que contiene el icono. Esta ruta de acceso no requiere comillas, aunque contenga espacios.

El valor de **IconIndex** se interpreta de la siguiente manera:

-   Si **IconIndex** es un número positivo, el número se utiliza como el índice de la matriz de los iconos de *base cero* que se almacena en el archivo. Por ejemplo, si **IconIndex** es 1, el segundo icono se carga desde el archivo.
-   Si **IconIndex** es un número negativo, el valor absoluto de **iconindex** se utiliza como identificador de recursos (en lugar del índice) para el icono. Por ejemplo, si **IconIndex** es-3, el icono cuyo identificador de recurso es 3 se carga desde el archivo.

En el ejemplo siguiente se muestra el registro de un explorador hipotético de lit View. El segundo icono almacenado en el archivo Litview.exe se utiliza como valor predeterminado.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Registrar un verbo abierto

> [!Note]  
> Esta sección no se aplica a Windows 2000. El siguiente paso solo es necesario para los clientes del explorador y de correo electrónico.

 

Supongamos que un usuario ha seleccionado el programa como el programa de Internet o de correo electrónico predeterminado. Ese usuario hace clic en el icono de **Internet** o **correo electrónico** en el menú **Inicio** de Windows XP o Windows Vista para abrir el programa. En ese momento, se ejecuta la línea de comandos registrada tal y como se muestra aquí.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

La línea de comandos debe especificar una ruta de acceso absoluta completa al archivo, seguida de opciones de línea de comandos opcionales. Si el tipo de entrada es REG \_ Expand \_ SZ, se pueden usar variables de entorno en la ruta de acceso. Use las comillas correctamente para asegurarse de que no se interpreten erróneamente los espacios de la línea de comandos. La línea de comandos debe ejecutar el programa con los valores predeterminados adecuados. Los exploradores suelen tener como valor predeterminado la Página principal del usuario. Los programas de correo electrónico suelen abrir la **bandeja de entrada** del usuario.

En el ejemplo siguiente se muestra el registro de un `open` verbo para un explorador hipotético de lit View. No especifica ninguna opción de línea de comandos.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

Tenga en cuenta que, en este valor, las comillas se colocan alrededor de la ruta de acceso porque contiene espacios incrustados. Si se omiten estas comillas, puede que la línea de comandos se interprete erróneamente.

### <a name="registering-installation-information"></a>Registrar información de instalación

> [!Note]  
> Esta sección no se aplica a Windows Server 2003.

 

-   [El comando REINSTALL](#the-reinstall-command)
-   [Comando Ocultar iconos](#the-hide-icons-command)
-   [Comando Mostrar iconos](#the-show-icons-command)
-   [Configuración del programa de grupo](#group-program-configuration)
-   [Ejemplo de registro del explorador](#browser-registration-example)

La característica por la que el usuario selecciona programas predeterminados por equipo se denomina y se obtiene acceso a ella, tal y como se muestra en la tabla siguiente. (Windows Vista presentó una nueva característica, **establece los programas predeterminados**, mediante los cuales un usuario puede establecer los valores predeterminados por usuario).



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operativo</th>
<th>Title</th>
<th>Ubicación de acceso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows 7</td>
<td>Establecer los valores predeterminados de acceso a programas y del equipo</td>
<td><ul>
<li>Opción <strong>programas predeterminados</strong> del menú <strong>Inicio</strong></li>
<li><strong>Programas predeterminados</strong> Elemento del panel de control</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista</td>
<td>Establecer los valores predeterminados de acceso a programas y del equipo</td>
<td><ul>
<li>Opción <strong>programas predeterminados</strong> del menú <strong>Inicio</strong></li>
<li><strong>Programas predeterminados</strong> Elemento del panel de control</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows XP SP2</td>
<td>Establecer acceso y valores predeterminados de programas</td>
<td><ul>
<li>Menú <strong>Inicio</strong></li>
<li><strong>Agregar o quitar programas</strong> Elemento del panel de control</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows XP SP1</td>
<td>Configurar programas</td>
<td><ul>
<li><strong>Agregar o quitar programas</strong> Elemento del panel de control</li>
</ul></td>
</tr>
</tbody>
</table>



 

Para simplificar, en este tema se usa el título de Windows 7 de la característica. A todas las versiones de la característica se les conoce comúnmente como SPAD.

> [!Note]  
> Si ejecuta Windows 2000 o Windows XP, debe tener al menos Windows 2000 SP3 o Windows XP SP1 instalado para ver la página **establecer acceso y valores predeterminados del programa** . En Windows Vista y versiones posteriores, el acceso a la página **establecer los valores predeterminados de acceso a programas y equipos** requiere privilegios de administrador. Por esta razón, se recomienda que los desarrolladores se registren en el elemento configurar el panel de control [programas predeterminados](default-programs.md) para que cualquier usuario pueda administrar los valores predeterminados de la aplicación.

 

En el árbol del Registro siguiente se muestra la variedad de información que se debe registrar en la clave **InstallInfo** del programa para que el programa aparezca en la página **establecer los valores predeterminados de acceso a programas y del equipo** como opción para su tipo de cliente. Cada uno de estos valores se describe en detalle en las secciones siguientes.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

La línea de comandos debe especificar una ruta de acceso absoluta completa al archivo, seguida de opciones de línea de comandos opcionales. Use las comillas correctamente para asegurarse de que no se interpreten erróneamente los espacios de la línea de comandos.

### <a name="the-reinstall-command"></a>El comando REINSTALL

La línea de comandos de reinstalación declarada en el valor ReinstallCommand se ejecuta cuando el usuario utiliza la página **establecer los valores predeterminados de acceso a programas y del equipo** para seleccionar el programa como predeterminado para su tipo de cliente. En Windows Vista y versiones posteriores, el acceso a esta página requiere un nivel de privilegios de administrador. En Windows 8, si ha registrado la aplicación con el mismo nombre para establecer el **acceso a programas y los valores** predeterminados del equipo y **programas predeterminados**, los valores predeterminados especificados en **programas** predeterminados para esa aplicación se aplicarán para el usuario actual, así como para ejecutar el comando reinstalar.

El programa iniciado por la línea de comandos de reinstalación debe asociar la aplicación con el conjunto completo de tipos de [archivos](fa-intro.md) y [protocolos](/previous-versions//aa767743(v=vs.85)) que la aplicación puede controlar. Todas las aplicaciones deben establecer la capacidad del controlador en el comando de reinstalación. Las aplicaciones pueden usar el comando REINSTALL para registrar la funcionalidad y, opcionalmente, establecer el estado predeterminado. Cuando una aplicación elige implementar el estado de la capacidad y del controlador predeterminado en el comando de reinstalación, también debe restablecer los vínculos o accesos directos visibles que desee. Los puntos de entrada visibles que la mayoría de las aplicaciones elija aparecen en [el comando Ocultar iconos](#the-hide-icons-command).

> [!Note]  
> Se recomienda encarecidamente que las aplicaciones implementen la funcionalidad de administración en el comando de reinstalación.

 

Una vez completado el proceso de reinstalación, el programa iniciado por la línea de comandos de reinstalación debe salir. No debe iniciar el programa correspondiente; simplemente debe registrar los valores predeterminados. Por ejemplo, el comando reinstalar de un explorador no debe abrir la Página principal del usuario.

> [!Note]  
> En el caso de los clientes de explorador y de correo electrónico en Windows XP y Windows Vista, las aplicaciones que optan por establecer la capacidad de control y el estado predeterminado en el comando de reinstalación deben registrarse para el icono correspondiente en la parte superior del menú Inicio. Consulte [registro del menú Inicio](#start-menu-registration) para obtener información adicional.

 

### <a name="the-hide-icons-command"></a>Comando Ocultar iconos

La línea de comandos declarada en el valor HideIconsCommand se ejecuta cuando el usuario desactiva el cuadro **Habilitar acceso a este programa** de la página **establecer los valores predeterminados de acceso a programas y del equipo** . Esta línea de comandos debe ocultar todos los puntos de acceso del programa que estén visibles en la interfaz de usuario. Las instrucciones específicas son para quitar accesos directos e iconos de las siguientes ubicaciones:

-   Iconos de escritorio
-   Vínculos del menú Inicio, incluido el grupo **Inicio**
-   Vínculos de la barra de inicio rápido
-   Área de notificaciones
-   Menús contextuales
-   Banda de tareas de carpeta

Esta línea de comandos también debe evitar las invocaciones automáticas del programa, como las especificadas en la clave **Ejecutar** registro. Se recomienda a los proveedores que implementen estas instrucciones en la devolución de llamada de ocultación de acceso de la aplicación.

No es necesario renunciar al registro (capacidad de aplicación) de los tipos de archivo cuando se ocultan los iconos. Tampoco es necesario ceder el estado predeterminado de la aplicación para los tipos de protocolo y archivo. Esto puede dar lugar a una experiencia de usuario incorrecta cuando estos tipos se encuentran en la interfaz de usuario.

Después de ocultar correctamente los iconos, debe actualizar el valor del registro IconsVisible a 0, como se muestra a continuación:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

La entrada IconsVisible es de tipo **reg \_ DWORD**.

### <a name="an-alternate-hide-icons-method-in-spad"></a>Un método de ocultar iconos alternativo en SPAD

En el caso de algunas aplicaciones heredadas, es posible que una implementación completa de ocultar acceso no sea práctica. Un método alternativo que logra el mismo efecto es desinstalar la aplicación. En la sección siguiente se muestra el comportamiento de ejemplo y el código de ejemplo para implementar esta alternativa. En general, los fabricantes de software independientes (ISV) deben evitar esta alternativa, ya que lo hará:

-   Desinstale la aplicación por completo del sistema.
-   Quitar los valores predeterminados previamente seleccionados.
-   No deje la opción de interfaz de usuario para volver a instalar la aplicación.
-   Haga que la característica habilitar acceso deje de estar disponible, ya que una desinstalación quita la aplicación completamente de SPAD.

La experiencia de usuario recomendada es la siguiente:

-   Cuando el usuario desactive la casilla **Habilitar el acceso a este programa** en SPAD, se presenta la siguiente interfaz de usuario.

    ![cuadro de diálogo sobre cómo ocultar el acceso al programa](images/hideaccessvista.png)

-   Cuando el usuario selecciona **Aceptar**, se inicia el elemento **programas y características** del panel de control para permitir que el usuario desinstale la aplicación.
-   Los usuarios de Windows XP deben aparecer con este cuadro de diálogo.

    ![cuadro de diálogo equivalente de Windows XP](images/hideaccessxp.png)

-   Cuando el usuario de Windows XP selecciona **Aceptar**, se inicia el elemento **Agregar o quitar programas** del panel de control para permitir que el usuario desinstale la aplicación.

El código siguiente proporciona una implementación reutilizable para la característica de ocultación de acceso, como se describe anteriormente. Se puede usar en Windows XP, Windows Vista y Windows 7.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a>Comando Mostrar iconos

La línea de comandos declarada en la entrada ShowIconsCommand se ejecuta cuando el usuario activa la casilla **Habilitar el acceso a este programa** en la página **establecer los valores predeterminados de acceso a programas y del equipo** . Esta línea de comandos puede restaurar los puntos de acceso de su programa, incluidos los que están en el menú **Inicio** , en el escritorio y en el grupo **Inicio** , así como las invocaciones automáticas normales, como las especificadas en la clave **Ejecutar** registro. Los puntos de acceso visibles de interés para la mayoría de las aplicaciones se muestran en [el comando Ocultar iconos](#the-hide-icons-command). La aplicación no debe cambiar los valores predeterminados por usuario; el usuario debe realizar ese cambio a través de los **programas predeterminados**.

Después de mostrar correctamente los iconos, debe actualizar el valor del registro IconsVisible en 1, como se muestra a continuación:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Tenga en cuenta que si ha usado la entrada HideIconsCommand para solicitar una desinstalación de la aplicación, la entrada ShowIconsCommand no tiene ningún uso. Se debe quitar del registro con el resto de la información de la aplicación durante el proceso de desinstalación.

### <a name="group-program-configuration"></a>Configuración del programa de grupo

> [!Note]  
> Esta sección no se aplica a Windows 2000.

 

Como parte de la preparación del sistema, un OEM puede establecer una configuración que oculte los puntos de acceso para el explorador de Microsoft, el correo electrónico, la reproducción multimedia, la mensajería instantánea o la máquina virtual para los programas cliente de Java y especifique sus propios programas predeterminados. Los OEM pueden permitir que los usuarios restablezcan sus equipos en cualquier momento a esta configuración predeterminada mediante el establecimiento de los siguientes valores del registro.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

Si estas claves están configuradas, los usuarios pueden restaurar la configuración de OEM seleccionando la opción **fabricante del equipo** en la página establecer los **valores predeterminados de acceso a programas y del equipo** . Si no se establecen estas claves, no se muestra la opción **fabricante del equipo** .

La entrada **OEMShowIcons** , si está presente, establece el icono mostrar el estado del cliente especificado que se aplica si el usuario selecciona **fabricante del equipo**. Un valor de 1 hace que se muestren los iconos y un valor de 0 hace que no se muestren los iconos. Si **OEMShowIcons** no está presente, la selección **del fabricante del equipo** no tiene ningún efecto en el icono Mostrar configuración. **OEMShowIcons** es de tipo **reg \_ DWORD**.

La entrada **OEMDefault** , si está presente y está establecida en 1, establece la preferencia del OEM para el cliente predeterminado del tipo indicado. Solo un cliente de un tipo determinado se puede marcar como el valor predeterminado del OEM. Si más de un registro de un cliente contiene la entrada **OEMDefault** , se omiten todos los valores y el cliente actual se sigue usando como cliente predeterminado. Si la entrada **OEMDefault** no está presente o está presente y está establecida en 0, ese cliente concreto no se utiliza como el cliente predeterminado si el usuario selecciona **fabricante del equipo**. **OEMDefault** es de tipo **reg \_ DWORD**.

Además de la opción de restablecer los equipos a la configuración predeterminada establecida por el OEM, los usuarios tienen otras tres opciones de configuración:

-   Establezca su equipo en una configuración de Microsoft Windows. En este caso, la página **establecer los valores predeterminados de acceso a programas y del equipo** permite el acceso a todo el software de Microsoft y que no sea de Microsoft en el equipo registrado en las categorías de productos correspondientes. Los programas de Microsoft Windows se seleccionan como la opción predeterminada para cada categoría.
-   Establezca su equipo en una configuración que no sea de Microsoft. Esta configuración oculta los puntos de acceso (por ejemplo, el menú **Inicio** ) en Windows Internet Explorer, Windows Media Player, Windows Messenger y Microsoft Outlook Express. Permite el acceso al software que no es de Microsoft en el equipo en estas categorías. Además, si un programa que no es de Microsoft está disponible en una categoría, se establece como el valor predeterminado para esa categoría. Si hay más de un programa que no es de Microsoft disponible en una categoría, se pide al usuario que elija el programa que no es de Microsoft que se debe usar como predeterminado.
-   Establezca una configuración personalizada. Los usuarios realizan sus propias selecciones para habilitar o quitar el acceso, y mezclar programas de Microsoft y que no sean de Microsoft tal y como se ven. Los usuarios establecen las opciones predeterminadas categoría por categoría.

Los usuarios pueden cambiar cualquiera de estas opciones en cualquier momento.

### <a name="browser-registration-example"></a>Ejemplo de registro del explorador

En el ejemplo siguiente se muestra el registro completo de **InstallInfo** para un explorador ficticio de vista de Lit. En este caso, los modificadores de la línea de comandos permiten al archivo Litview.exe realizar las acciones necesarias para cada valor.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

Tenga en cuenta que las comillas se colocan alrededor de las rutas de acceso porque contienen espacios incrustados.

## <a name="registration-elements-for-specific-client-types"></a>Elementos de registro para tipos de cliente específicos

La siguiente información también se puede encontrar en los recursos que aparecen en la sección temas relacionados al final de este tema.

-   [Registro del menú Inicio](#start-menu-registration)
-   [Registro del cliente de correo](#mail-client-registration)

### <a name="start-menu-registration"></a>Registro del menú Inicio

En Windows XP, las aplicaciones suelen registrar los valores predeterminados en una máquina (**HKEY \_ local \_ Machine**) en lugar de un ámbito de usuario (**HKEY \_ Current \_ User**). Con la introducción de Windows Vista del control de cuentas de usuario (UAC), las aplicaciones que reclaman las ranuras de **Internet** y de **correo electrónico** en el menú **Inicio** deben implementar el comando REINSTALL en el contexto de ejecución correcto.

> [!Note]  
> El vínculo de **correo electrónico** del menú Inicio se ha quitado de Windows 7. Sin embargo, el registro descrito en esta sección se debe seguir realizando porque asigna el cliente MAPI predeterminado.

 

Un usuario limitado en Windows XP, Windows Vista o Windows 7 no puede tener acceso a SPAD. Por esta razón, se recomienda que los desarrolladores se registren en el elemento configurar el panel de control de **programas predeterminados** para que cualquier usuario pueda administrar los valores predeterminados de la aplicación por usuario.

Las selecciones realizadas en SPAD solo deben afectar a la configuración de cada máquina.

Establezca el valor del registro como se indica a continuación.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **La siguiente información solo se aplica a Windows XP.**
> 
> Si el registro del valor predeterminado de nivel de equipo en HKEY \_ local \_ Machine como se mostró anteriormente es correcto, la aplicación debe eliminar el valor asignado a la entrada predeterminada en la siguiente subclave:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Si se produce un error en el registro del valor predeterminado de nivel de equipo en HKEY \_ local \_ Machine como se mostró anteriormente, normalmente porque el usuario no tiene permiso de escritura en la subclave, la aplicación debe establecer el siguiente valor:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> Esto registra el nombre canónico solo para el usuario actual, no para todos los usuarios.

 

Después de actualizar las claves del registro, el programa debe difundir el mensaje de [**\_ SETTINGCHANGE de WM**](../winmsg/wm-settingchange.md) con **wParam** = 0 y **lParam** que apunta a la cadena terminada en NULL "software \\ clients \\ **ClientTypeName**" para notificar al sistema operativo que el cliente predeterminado ha cambiado.

### <a name="mail-client-registration"></a>Registro del cliente de correo

Para un cliente de correo, el programa debe tener la configuración registrada en la clave correo electrónico **\_ \_ raíz de las clases HKEY** \\  para poder atender las direcciones URL que utilizan el `mailto` Protocolo. Establezca valores y claves que reflejen la configuración de la siguiente clave.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Esta jerarquía del registro reemplaza `mailto` a la jerarquía del registro existente que se encuentra en **HKEY \_ classes \_ root** \\ **mailto**. La jerarquía sigue siendo la misma, solo la ubicación ha cambiado. El formato de esta jerarquía se documenta en MSDN en [información general y tutoriales del protocolo conectable asincrónico](/previous-versions//aa767913(v=vs.85)). Normalmente, el `mailto` Protocolo se registra en un programa en lugar de un Protocolo asincrónico, en cuyo caso se aplica la documentación sobre el [registro de una aplicación en un esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) .

En el ejemplo siguiente se muestra la `mailto` sección del registro de un `mailto` controlador registrado en un programa.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

El valor del registro marcas se documenta en [tipos de archivo](fa-file-types.md) en la sección titulada "definir los atributos de tipo de archivo".

## <a name="complete-sample-registrations"></a>Completar registros de ejemplo

Los ejemplos siguientes se proporcionan para mostrar los requisitos de registro completos para los distintos tipos de cliente.

-   [Un explorador de ejemplo](#a-sample-browser)
-   [Un explorador de correo de ejemplo](#a-sample-mail-browser)
-   [Media Player de ejemplo](#a-sample-media-player)
-   [Un programa de mensajería instantánea de ejemplo](#a-sample-instant-messenger-program)
-   [Una máquina virtual de ejemplo para Java](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>Un explorador de ejemplo

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a>Un explorador de correo de ejemplo

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a>Media Player de ejemplo

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a>Un programa de mensajería instantánea de ejemplo

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a>Una máquina virtual de ejemplo para Java

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

*Las compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y eventos que se describen aquí son ficticios. No se pretende ni se debe inferir ninguna asociación con compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares o eventos reales.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows](start-menu-reg.md)
</dt> <dt>

[Diseño del registro del cliente de Internet Explorer (consulte la sección "definiciones de clave del registro de cliente")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Información general y tutoriales del protocolo acoplable asincrónico](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Registrar una aplicación en un esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
