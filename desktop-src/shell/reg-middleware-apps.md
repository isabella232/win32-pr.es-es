---
description: 'En este tema se explica cómo registrar un programa en el registro de Windows como uno de los siguientes tipos de cliente: explorador, correo electrónico, reproducción multimedia, mensajería instantánea o máquina virtual para Java.'
title: Registro de programas con tipos de cliente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9c2d9a4589b684580250c487a6f83c3c9e79dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470423"
---
# <a name="registering-programs-with-client-types"></a>Registro de programas con tipos de cliente

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

-   [Elementos de registro comunes para todos los tipos de cliente](#common-registration-elements-for-all-client-types)
    -   [Selección de un nombre canónico](#selecting-a-canonical-name)
    -   [Registrar el nombre para mostrar de un programa](#registering-a-programs-display-name)
    -   [Registrar el icono de un programa](#registering-a-programs-icon)
    -   [Registro de un verbo abierto](#registering-an-open-verb)
    -   [Registrar información de instalación](#registering-installation-information)
-   [Elementos de registro para tipos de cliente específicos](#registration-elements-for-specific-client-types)
    -   [Registro del menú Inicio](#start-menu-registration)
    -   [Registro de cliente de correo](#mail-client-registration)
-   [Registros de ejemplo completos](#complete-sample-registrations)
    -   [Un explorador de ejemplo](#a-sample-browser)
    -   [Un explorador de correo de ejemplo](#a-sample-mail-browser)
    -   [Un ejemplo Media Player](#a-sample-media-player)
    -   [Un programa instant messenger de ejemplo](#a-sample-instant-messenger-program)
    -   [Una máquina virtual de ejemplo para Java](#a-sample-virtual-machine-for-java)
-   [Temas relacionados](#related-topics)

En este tema se amplía la documentación existente sobre el registro de un programa como un tipo de cliente determinado. Para obtener vínculos a esa documentación, consulte la sección Temas relacionados.

## <a name="common-registration-elements-for-all-client-types"></a>Elementos de registro comunes para todos los tipos de cliente

Al registrar un programa como un tipo de cliente, la mayoría de las entradas del Registro son las mismas independientemente del tipo de cliente. Sin embargo, algunas entradas del Registro son específicas del tipo de cliente y se anotan en la sección Elementos de registro [para tipos de cliente específicos.](#registration-elements-for-specific-client-types)

En esta sección se de tratan los temas siguientes:

-   [Selección de un nombre canónico](#selecting-a-canonical-name)
-   [Registrar el nombre para mostrar de un programa](#registering-a-programs-display-name)
-   [Registrar el icono de un programa](#registering-a-programs-icon)
-   [Registro de un verbo abierto](#registering-an-open-verb)
-   [Registrar información de instalación](#registering-installation-information)

> [!Note]  
> Los nombres de subclave que se dan en cursiva a lo largo de este tema son marcadores de posición para los nombres de subclave definidos por el usuario o un conjunto de valores posibles. En la sección Complete [Sample Registrations](#complete-sample-registrations) (Completar registros de ejemplo) se proporcionan ejemplos completos con nombres de ejemplo.

 

Toda la información de registro de tipos de cliente se almacena en la subclave siguiente:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* es uno de los siguientes nombres de subclave:

-   StartMenuInternet (para exploradores)
-   Correo electrónico (por correo electrónico)
-   Medios (para la reproducción multimedia)
-   MENSAJERÍA INSTANTÁNEA (para mensajería instantánea)
-   JavaVM (para máquina virtual para Java)

A lo largo de este tema, verá referencias a un programa informático ficticio denominado "Lit View" de Litware Inc., con un archivo ejecutable denominado Litview.exe. Este programa hipotético se usa indistintamente como mensajería instantánea, un explorador u otro tipo de programa cliente según sea necesario para fines ilustrativos.

### <a name="selecting-a-canonical-name"></a>Selección de un nombre canónico

El proveedor debe elegir un *nombre canónico* para el programa. El nombre canónico nunca se muestra al usuario, por lo que no es necesario localizarlo. Su único propósito es proporcionar una cadena única que se pueda usar para identificar el programa. Normalmente es el mismo que el nombre en inglés del programa, pero se trata simplemente de una convención.

Para los tipos de cliente distintos de los exploradores, el nombre canónico puede ser cualquier cadena. Elija un nombre único, uno que no sea probable que lo utilice otro proveedor.

En el caso de los clientes del explorador, el nombre canónico debe ser el nombre (incluida la extensión) del ejecutable asociado. por ejemplo, "Litview.exe".

Estos son algunos ejemplos de nombres canónicos.

-   Iexplore.exe (explorador)
-   Windows Correo electrónico (correo electrónico)
-   Reproductor de Windows Media (medios)
-   Windows Messenger (mensajería instantánea)

Registre el nombre canónico mediante la creación de una subclave como se muestra aquí. El nombre de la subclave es el nombre canónico. Toda la información relacionada con el registro de ese programa existirá en esta subclave.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Registrar el nombre para mostrar de un programa

El siguiente paso del registro es especificar el nombre para mostrar del programa. Se da como un valor bajo la clave de nombre canónica, como se muestra aquí. Tenga en cuenta de nuevo que *CanonicalName* y *ClientTypeName* no son los nombres reales de las claves, sino solo los marcadores de posición de los nombres verdaderos, como *la vista Lit*.

> [!Note]  
> A Windows 8, el nombre usado para registrarse en Establecer acceso a programas [](default-programs.md) y valores predeterminados del equipo [(SPAD)](cpl-setprogramaccess.md) y para Programas predeterminados debe coincidir para que los cambios de SPAD desencadene registros de programas predeterminados.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

El valor **LocalizedString** es una cadena REG SZ y consta de un signo "at" (@), la ruta de acceso completa a un archivo .dll o .exe, una coma, un signo menos y un \_ entero decimal. El entero decimal es el identificador de un recurso de cadena, incluido en el archivo .dll o .exe, cuyo valor se mostrará al usuario como nombre de este cliente. Tenga en cuenta que la ruta de acceso del archivo no requiere comillas, aunque contenga espacios.

El registro de la cadena de nombre para mostrar de esta manera permite usar el mismo registro para varios idiomas. Cada instalación de idioma proporciona un archivo de recursos diferente con el nombre para mostrar almacenado en el mismo identificador de recurso.

En el ejemplo siguiente se muestra el registro de un programa ficticio de mensajería instantánea Lit View. Dado que se trata de un programa de mensajería instantánea, la subclave *CanonicalName* (en este caso *Lit View)* se almacena en la subclave **IM.**

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Observe el uso de la entrada (valor predeterminado) como declaración secundaria del nombre para mostrar del cliente. Si **LocalizedString no** está presente, se usa el valor (predeterminado) en su lugar. Esto funciona con todos los tipos de cliente (exploradores de Internet, exploradores de correo electrónico, mensajería instantánea y reproductores multimedia). Para la compatibilidad con versiones anteriores con el diseño del Registro de cliente de [Internet Explorer,](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))los programas de correo electrónico deben establecer el valor (predeterminado) de la subclave *CanonicalName* en el nombre para mostrar del cliente en el idioma instalado actualmente.

### <a name="registering-a-programs-icon"></a>Registrar el icono de un programa

> [!Note]  
> Esta sección no se aplica a Windows 2000.

 

De forma predeterminada, la sección superior de Windows XP y Windows **menú** Inicio de Vista contiene iconos de **Internet** **y correo** electrónico. Estos iconos no están presentes en Windows 7 y versiones posteriores. Para los clientes de explorador y correo electrónico, cuando se asigna un programa como valor predeterminado para su tipo de cliente, se muestra el icono registrado de ese programa para esas entradas del **menú** Inicio.

El registro del icono de un programa es obligatorio para los clientes de explorador y correo electrónico. El registro de un icono para la reproducción multimedia, la mensajería instantánea o la máquina virtual para tipos de cliente java es opcional, y los iconos registrados para esos tipos de cliente no se usan actualmente en Windows y no se muestran en la sección superior de los menús inicio de Windows XP o Windows **Vista.**

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

El **valor FilePath** es la ruta de acceso completa al archivo que contiene el icono. Esta ruta de acceso no requiere comillas, aunque contenga espacios.

El **valor IconIndex** se interpreta como sigue:

-   Si **IconIndex** es un número positivo, el número  se usa como índice de la matriz de base cero de iconos almacenados en el archivo. Por ejemplo, si **IconIndex** es 1, el segundo icono se carga desde el archivo .
-   Si **IconIndex** es un número negativo, se usa el valor absoluto de **IconIndex** como identificador de recurso (en lugar del índice) para el icono. Por ejemplo, si **IconIndex** es -3, el icono cuyo identificador de recurso es 3 se carga desde el archivo.

En el ejemplo siguiente se muestra el registro de un explorador lit view hipotético. El segundo icono almacenado en el Litview.exe se usa como valor predeterminado.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Registro de un verbo abierto

> [!Note]  
> Esta sección no se aplica a Windows 2000. El siguiente paso solo es necesario para los clientes de explorador y correo electrónico.

 

Suponga que un usuario ha seleccionado el programa como el programa predeterminado de Internet o correo electrónico. Ese usuario hace clic  en **el icono internet** o correo electrónico del Windows XP o Windows **menú** Inicio de Vista para abrir el programa. En ese momento, se ejecuta la línea de comandos registrada como se muestra aquí.

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

La línea de comandos debe especificar una ruta de acceso absoluta completa al archivo, seguida de opciones de línea de comandos opcionales. Si el tipo de entrada es REG EXPAND SZ, se pueden usar \_ variables de entorno en la ruta de \_ acceso. Use las comillas correctamente para asegurarse de que los espacios de la línea de comandos no se interpretan mal. La línea de comandos debe ejecutar el programa con los valores predeterminados adecuados. Los exploradores suelen tener como valor predeterminado la página principal del usuario. Por lo general, los programas de correo electrónico abren la **bandeja de entrada del usuario.**

En el ejemplo siguiente se muestra el registro de un `open` verbo para un explorador hipotético lit View. No especifica ninguna opción de línea de comandos.

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

Tenga en cuenta que, en este valor, las comillas se colocan alrededor de la ruta de acceso porque contiene espacios incrustados. Si se omiten estas comillas, la línea de comandos podría malinterpretarse.

### <a name="registering-installation-information"></a>Registrar información de instalación

> [!Note]  
> Esta sección no se aplica a Windows Server 2003.

 

-   [El comando Reinstalar](#the-reinstall-command)
-   [El comando Ocultar iconos](#the-hide-icons-command)
-   [El comando Mostrar iconos](#the-show-icons-command)
-   [Configuración del programa de grupo](#group-program-configuration)
-   [Ejemplo de registro de explorador](#browser-registration-example)

La característica por la que el usuario selecciona programas predeterminados por equipo se denomina y se accede a ellos, como se muestra en la tabla siguiente. (Windows Vista introdujo una nueva característica, **Establecer** los programas predeterminados, mediante la cual un usuario puede establecer valores predeterminados por usuario).




| Sistema operativo | Título | Ubicación de acceso | 
|------------------|-------|-----------------|
| Windows 7 | Establecer el acceso al programa y los valores predeterminados del equipo | <ul><li><strong>Opción Programas</strong> predeterminados <strong>del menú</strong> Inicio</li><li><strong>Programas predeterminados</strong> Panel de control elemento</li></ul> | 
| Windows Vista | Establecer el acceso al programa y los valores predeterminados del equipo | <ul><li><strong>Opción Programas</strong> predeterminados <strong>del menú</strong> Inicio</li><li><strong>Programas predeterminados</strong> Panel de control elemento</li></ul> | 
| Windows XP SP2 | Establecer el acceso al programa y los valores predeterminados | <ul><li><strong>Menú</strong> Inicio</li><li><strong>Agregar o quitar programas</strong> Panel de control elemento</li></ul> | 
| Windows XP SP1 | Configurar programas | <ul><li><strong>Agregar o quitar programas</strong> Panel de control elemento</li></ul> | 




 

Para simplificar, en este tema se usa el Windows 7 de la característica. Todas las versiones de la característica se conocen popularmente como SPAD.

> [!Note]  
> Si ejecuta Windows 2000 o Windows XP, debe tener al menos Windows 2000 SP3 o Windows XP SP1 instalados para ver la página Establecer el acceso al programa y los valores predeterminados.  En Windows Vista y versiones posteriores, el acceso a la página Establecer el acceso al programa y los valores predeterminados del equipo requiere **privilegios** de administrador. Por este motivo, se recomienda a los desarrolladores que se registren en el elemento Set [your default programs](default-programs.md) Panel de control (Establecer los programas predeterminados) para que cualquier usuario pueda administrar los valores predeterminados de la aplicación.

 

En el siguiente árbol del Registro se muestra la variedad de información que se debe  registrar en la clave **InstallInfo** del programa para que el programa aparezca en la página Establecer acceso al programa y Valores predeterminados del equipo como opción para su tipo de cliente. Cada uno de estos valores se describe con detalle en las secciones siguientes.

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

La línea de comandos debe especificar una ruta de acceso absoluta completa al archivo, seguida de opciones de línea de comandos opcionales. Use las comillas correctamente para asegurarse de que los espacios de la línea de comandos no se interpretan mal.

### <a name="the-reinstall-command"></a>El comando Reinstalar

La línea de comandos reinstall declarada en el valor ReinstallCommand se ejecuta cuando el usuario usa la página Establecer acceso al programa y Valores predeterminados del equipo para seleccionar el programa como el valor predeterminado para su tipo de cliente.  En Windows Vista y versiones posteriores, el acceso a esta página requiere un nivel de privilegios de administrador. En Windows 8, si ha registrado la aplicación con  el mismo nombre para Establecer acceso al programa y  Valores predeterminados del equipo y Programas predeterminados **,** los valores predeterminados especificados en Programas predeterminados para esa aplicación se aplicarán al usuario actual, así como la ejecución del comando de reinstalación.

El programa iniciado por la línea de comandos de [](fa-intro.md) reinstalación debe asociar la aplicación con el conjunto completo de tipos de archivo y [protocolo](/previous-versions//aa767743(v=vs.85)) que la aplicación puede controlar. Todas las aplicaciones deben establecer la funcionalidad de controlador en el comando reinstall. Las aplicaciones pueden usar el comando reinstall para registrar la funcionalidad, así como establecer opcionalmente el estado predeterminado. Cuando una aplicación decide implementar la funcionalidad y el estado de controlador predeterminado en el comando reinstall, también debe restablecer los vínculos visibles o los accesos directos deseados. Los puntos de entrada visibles que la mayoría de las aplicaciones eligen se muestran [en el comando Ocultar iconos](#the-hide-icons-command).

> [!Note]  
> Se recomienda encarecidamente que las aplicaciones implementen la funcionalidad de control en el comando reinstall.

 

Una vez completado el proceso de reinstalación, el programa iniciado por la línea de comandos de reinstalación debe salir. No debe iniciar el programa correspondiente; simplemente debe registrar los valores predeterminados. Por ejemplo, el comando reinstall de un explorador no debe abrir la página principal del usuario.

> [!Note]  
> En el caso de los clientes de explorador y correo electrónico en Windows XP y Windows Vista, las aplicaciones que deciden establecer la funcionalidad de control y el estado predeterminado en el comando de reinstalación deben registrarse para el icono correspondiente en la parte superior de la menú Inicio. Consulte [Inicio del registro del menú](#start-menu-registration) para obtener información adicional.

 

### <a name="the-hide-icons-command"></a>El comando Ocultar iconos

La línea de comandos declarada en el valor HideIconsCommand  se ejecuta cuando el usuario borra el cuadro Habilitar acceso a este programa en la página Establecer acceso al programa y Valores predeterminados **del** equipo. Esta línea de comandos debe ocultar todos los puntos de acceso del programa que están visibles en la interfaz de usuario. Las directrices específicas son quitar accesos directos e iconos de las siguientes ubicaciones:

-   Iconos de escritorio
-   menú Inicio vínculos, incluido el grupo **Inicio**
-   inicio rápido vínculos de barra de texto
-   Área de notificaciones
-   Menús contextuales
-   Banda de tareas de carpeta

Esta línea de comandos también debe evitar las invocaciones automáticas del programa, como las especificadas en La **clave del** Registro de ejecución. Se recomienda a los proveedores que implementen estas directrices en la devolución de llamada Ocultar acceso de la aplicación.

No es necesario volver a inscribir el registro (funcionalidad de la aplicación) de los tipos de archivo cuando los iconos están ocultos. Tampoco es necesario volver a crear el estado predeterminado de la aplicación para los tipos de archivo y protocolo. Esto puede provocar una mala experiencia del usuario cuando estos tipos se encuentran en la interfaz de usuario.

Después de ocultar correctamente los iconos, debe actualizar el valor del Registro IconsVisible a 0 como se muestra:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

La entrada IconsVisible es de tipo **REG \_ DWORD.**

### <a name="an-alternate-hide-icons-method-in-spad"></a>Un método alternativo ocultar iconos en SPAD

Para algunas aplicaciones heredadas, una implementación completa de Ocultar acceso puede no ser práctica. Un método alternativo que logra el mismo efecto es desinstalar la aplicación. En la sección siguiente se muestra el comportamiento de ejemplo y el código de ejemplo para implementar esta alternativa. En general, los proveedores de software independientes (ISV) deben evitar esta alternativa, ya que:

-   Desinstale completamente la aplicación del sistema.
-   Quite los valores predeterminados seleccionados previamente.
-   No deje ninguna opción de interfaz de usuario para volver a instalar la aplicación.
-   Haga que la característica habilitar acceso ya no esté disponible, ya que una desinstalación quita completamente la aplicación de SPAD.

La experiencia de usuario recomendada es la siguiente:

-   Cuando el usuario desactiva la casilla Habilitar acceso a **este programa** en SPAD, se presenta la siguiente interfaz de usuario.

    ![cuadro de diálogo sobre cómo ocultar el acceso al programa](images/hideaccessvista.png)

-   Cuando el usuario selecciona  **Aceptar,** se inicia el elemento Panel de control programas para permitir que el usuario desinstale la aplicación.
-   Windows Los usuarios de XP deben presentarse con este cuadro de diálogo.

    ![cuadro de diálogo de Windows XP equivalente](images/hideaccessxp.png)

-   Cuando el Windows XP selecciona **Aceptar,** se inicia el elemento Agregar o quitar programas **Panel de control** para permitir que el usuario desinstale la aplicación.

El código siguiente proporciona una implementación reutilizable para la característica Ocultar acceso, como se ha descrito anteriormente. Se puede usar en Windows XP, Windows Vista y Windows 7.


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



### <a name="the-show-icons-command"></a>El comando Mostrar iconos

La línea de comandos declarada en la entrada ShowIconsCommand  se ejecuta cuando el usuario comprueba el cuadro Habilitar acceso a este programa en la página Establecer acceso al programa y Valores predeterminados **del** equipo. Esta línea de comandos puede restaurar los puntos  de acceso del programa, incluidos los del menú Inicio, en el escritorio y en el grupo Inicio, así como las invocaciones automáticas normales, como las especificadas en la clave ejecutar **del** Registro.  Los puntos de acceso visibles de interés para la mayoría de las aplicaciones se muestran [en el comando Ocultar iconos](#the-hide-icons-command). La aplicación no debe cambiar los valores predeterminados por usuario; el usuario debe realizar ese cambio a través de **programas predeterminados.**

Después de mostrar correctamente los iconos, debe actualizar el valor del Registro IconsVisible a 1 como se muestra:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Tenga en cuenta que si ha usado la entrada HideIconsCommand para solicitar una desinstalación de la aplicación, la entrada ShowIconsCommand no es de uso. Debe quitarse del Registro con el resto de la información de la aplicación durante el proceso de desinstalación.

### <a name="group-program-configuration"></a>Configuración del programa de grupo

> [!Note]  
> Esta sección no se aplica a Windows 2000.

 

Como parte de la preparación del sistema, un OEM puede establecer una configuración que oculta los puntos de acceso para el explorador de Microsoft, el correo electrónico, la reproducción multimedia, la mensajería instantánea o la máquina virtual para los programas cliente de Java y especifica sus propios programas predeterminados. Los OEM pueden permitir que los usuarios restablezcan sus equipos en cualquier momento a esta configuración predeterminada estableciendo los siguientes valores del Registro.

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

Si se establecen estas claves, los usuarios pueden  restaurar la configuración de OEM seleccionando la opción Fabricante del equipo en la página Establecer el acceso al programa y los valores **predeterminados del** equipo. Si no se establecen estas claves, **no** se muestra la opción Fabricante del equipo.

La **entrada OEMShowIcons,** si está presente, establece el estado de presentación del icono para el cliente especificado que se aplica si el usuario selecciona **Fabricante del equipo.** Un valor de 1 hace que se muestran iconos y un valor de 0 hace que los iconos no se muestran. Si **OEMShowIcons no** está presente, seleccionar **Fabricante del equipo** no tiene ningún efecto en la configuración de presentación del icono. **OEMShowIcons** es de tipo **REG \_ DWORD.**

La **entrada OEMDefault,** si está presente y se establece en 1, establece la preferencia de OEM para el cliente predeterminado del tipo indicado. Solo un cliente de un tipo determinado se puede marcar como el valor predeterminado de OEM. Si más de un registro de cliente contiene la entrada **OEMDefault,** se omiten todos y el cliente actual continúa usándose como cliente predeterminado. Si la **entrada OEMDefault** no está presente o está presente y se establece en 0, ese cliente concreto no se usa como cliente predeterminado si el usuario selecciona **Fabricante del equipo**. **OEMDefault** es de tipo **REG \_ DWORD.**

Además de la opción de restablecer sus equipos a la configuración predeterminada establecida por el OEM, los usuarios tienen otras tres opciones de configuración:

-   Establezca su equipo en una configuración de Windows Microsoft. En este caso, la página Establecer el acceso al programa y los valores predeterminados del equipo permite el acceso a todo el software de Microsoft y que no es de Microsoft en el equipo registrado en las categorías de productos pertinentes.  Los Windows de microsoft se seleccionan como opción predeterminada para cada categoría.
-   Establezca su equipo en una configuración que no es de Microsoft. Esta configuración oculta los puntos  de acceso (como el menú Inicio) para Windows Internet Explorer, Reproductor de Windows Media, Windows Messenger y Microsoft Outlook Express. Permite el acceso al software que no es de Microsoft en el equipo en estas categorías. Además, si un programa que no es de Microsoft está disponible en una categoría, se establece como valor predeterminado para esa categoría. Si hay más de un programa que no es de Microsoft disponible en una categoría, se pide al usuario que elija qué programa que no es de Microsoft debe usarse como valor predeterminado.
-   Establezca una configuración personalizada. Los usuarios hacen sus propias selecciones para habilitar o quitar el acceso, y mezclan programas de Microsoft y que no son de Microsoft según les conste. Los usuarios establecen opciones predeterminadas por categoría.

Los usuarios pueden cambiar cualquiera de estas opciones en cualquier momento.

### <a name="browser-registration-example"></a>Ejemplo de registro de explorador

En el ejemplo siguiente se muestra el **registro InstallInfo** completo para un explorador ficticio lit view. En este caso, los modificadores de línea de comandos permiten que Litview.exe archivo realice las acciones necesarias para cada valor.

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

La siguiente información también se puede encontrar en los recursos enumerados en la sección Temas relacionados al final de este tema.

-   [Inicio del registro del menú](#start-menu-registration)
-   [Registro de cliente de correo](#mail-client-registration)

### <a name="start-menu-registration"></a>Inicio del registro del menú

En Windows XP, las aplicaciones suelen registrar valores predeterminados en todo el equipo **(HKEY \_ LOCAL \_ MACHINE**) en lugar de en un ámbito de usuario **(HKEY \_ CURRENT \_ USER).** Con la introducción de Windows Vista del Control de cuentas de usuario  (UAC),  las aplicaciones que reclaman las ranuras de **Internet** y correo electrónico en el menú Inicio deben implementar el comando reinstall en el contexto de ejecución correcto.

> [!Note]  
> El menú Inicio **de correo electrónico** se ha quitado a partir Windows 7. Sin embargo, el registro que se describe en esta sección todavía debe realizarse porque asigna el cliente PREDETERMINADO DE LA MARCA.

 

Un usuario limitado en Windows XP, Windows Vista o Windows 7 no puede acceder a SPAD. Por esta razón, se recomienda a los desarrolladores que se registren en el elemento Set **your default programs** Panel de control (Establecer los programas predeterminados) para que cualquier usuario pueda administrar los valores predeterminados de la aplicación por usuario.

Las selecciones realizadas en SPAD solo deben afectar a la configuración por equipo.

Establezca el valor del Registro como se muestra a continuación.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **La siguiente información solo se aplica Windows XP.**
> 
> Si el registro del valor predeterminado de nivel de equipo en HKEY LOCAL MACHINE como se muestra anteriormente es correcto, la aplicación debe eliminar el valor asignado a la entrada Predeterminada en la \_ \_ subclave siguiente:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Si se produce un error en el registro del valor predeterminado de nivel de equipo en HKEY LOCAL MACHINE como se muestra anteriormente, normalmente porque el usuario no tiene permiso de escritura para la \_ subclave, la aplicación debe establecer el \_ siguiente valor:
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

 

Después de actualizar las claves del Registro, el programa debe difundir el mensaje [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con **wParam** = 0 y **lParam** que apunte a la cadena terminada en NULL "Software \\ Clients \\ **ClientTypeName"** para notificar al sistema operativo que el cliente predeterminado ha cambiado.

### <a name="mail-client-registration"></a>Registro de cliente de correo

Para un cliente de correo, el programa debe tener la configuración registrada en la clave **HKEY \_ CLASSES \_ ROOT** mailto para poder dar servicio a las direcciones URL que \\  usan el `mailto` protocolo. Establezca valores y claves que reflejan esa configuración en la clave siguiente.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Esta jerarquía del Registro reemplaza la jerarquía del `mailto` Registro existente que se encuentra en **HKEY CLASSES \_ \_ ROOT** \\ **mailto**. La jerarquía sigue siendo la misma, solo ha cambiado la ubicación. El formato de esta jerarquía se documenta en MSDN en Información general y tutoriales del protocolo asincrónico [conectable.](/previous-versions//aa767913(v=vs.85)) Normalmente, el protocolo se registra en un programa en lugar de en un protocolo asincrónico, en cuyo caso se aplica la documentación sobre el registro de una aplicación `mailto` en un esquema de [URI.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

En el ejemplo siguiente se `mailto` muestra la sección del registro de un controlador registrado en un `mailto` programa.

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

El valor del Registro EditFlags se documenta en Tipos de [archivo](fa-file-types.md) en la sección titulada "Definición de atributos de tipo de archivo".

## <a name="complete-sample-registrations"></a>Completar registros de ejemplo

Se proporcionan los ejemplos siguientes para mostrar los requisitos de registro completos para los distintos tipos de cliente.

-   [Un explorador de ejemplo](#a-sample-browser)
-   [Un explorador de correo de ejemplo](#a-sample-mail-browser)
-   [Un ejemplo Media Player](#a-sample-media-player)
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

### <a name="a-sample-media-player"></a>Un ejemplo Media Player

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

*Las empresas, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y eventos de ejemplo que se muestran en este documento son ficticios. No se pretende ni se debe inferir ninguna asociación con ninguna empresa, organización, producto, nombre de dominio, dirección de correo electrónico, logotipo, persona, lugar o evento real.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Cómo registrar un explorador de Internet o un cliente de correo electrónico con el Windows inicio](start-menu-reg.md)
</dt> <dt>

[Internet Explorer diseño del registro de cliente (consulte la sección "Definiciones de clave del Registro de cliente")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Tutoriales y información general sobre el protocolo conectable asincrónico](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Registro de una aplicación en un esquema uri](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
