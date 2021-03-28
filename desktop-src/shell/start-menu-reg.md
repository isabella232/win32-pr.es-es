---
description: El menú Inicio de Windows XP y Windows vista contiene ranuras reservadas para los clientes Internet (explorador) y correo electrónico (correo electrónico) predeterminados, que suelen denominarse aplicaciones de Internet del menú Inicio.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279856"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a>Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows

> [!Note]  
> Este tema se aplica a Windows XP, Windows Vista y Windows 7.

 

El menú Inicio de Windows XP y Windows vista contiene ranuras reservadas para los clientes **Internet** (explorador) y **correo electrónico** (correo electrónico) predeterminados, que suelen denominarse aplicaciones de Internet del *menú Inicio*. Las aplicaciones que se registran como aplicaciones de Internet del menú Inicio lo hacen en todo el sistema (por equipo). En Windows Vista, el usuario puede usar la característica **programas predeterminados** para establecer un valor predeterminado por usuario.

Cuando las aplicaciones se registran como menú Inicio aplicaciones de Internet, Windows XP y Windows Vista, cree iconos de **Internet** y **correo electrónico** en el menú Inicio. Al hacer clic en estos iconos, el menú Inicio comprueba el subárbol del registro por usuario (**HKEY \_ Current \_ User**). Si no se encuentra ninguna configuración predeterminada por usuario, el menú Inicio busca la subclave predeterminada por equipo en el subárbol de la **\_ \_ máquina local HKEY** .

> [!Note]  
> La instalación predeterminada de Windows no registra un programa de correo electrónico o Internet predeterminado por usuario, solo un valor predeterminado para todo el sistema. Esto proporciona una ruta de acceso de actualización sin problemas de las versiones anteriores del sistema operativo, en la que solo \_ \_ se admite el subárbol de la máquina local HKEY para los registros de cliente.

 

En este tema se describen los siguientes elementos:

-   [Registro para el vínculo a Internet del menú Inicio](#registering-for-the-start-menu-internet-link)
    -   [Cómo registrarse como el cliente de Internet predeterminado](#how-to-register-as-the-default-internet-client)
-   [Registro para el vínculo de correo electrónico del menú Inicio](#registering-for-the-start-menu-email-link)
    -   [Cómo el menú Inicio muestra el cliente de correo electrónico predeterminado](#how-the-start-menu-displays-the-default-email-client)
    -   [Cómo registrarse como cliente de correo electrónico predeterminado](#how-to-register-as-the-default-email-client)
-   [Personalización del menú contextual](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a>Registro para el vínculo a Internet del menú Inicio

> [!Note]  
> Este registro está en desuso a partir de Windows 7, que ya no proporciona un vínculo a Internet del menú Inicio. Los registros existentes se omiten en Windows 7 y versiones posteriores. Si se registra como la aplicación de Internet predeterminada del menú Inicio, no se registrará como el explorador Web predeterminado. El explorador Web predeterminado se utiliza para iniciar direcciones URL arbitrarias desde cualquier parte del sistema. La aplicación de Internet del menú Inicio simplemente controla el programa que se inicia cuando el usuario hace clic en el icono de Internet del menú Inicio.

 

Cualquier aplicación de explorador Web puede registrarse para aparecer como un cliente de Internet en el menú Inicio. Esta visibilidad, junto con el registro adecuado para los tipos de [protocolos](/previous-versions//aa767743(v=vs.85)) y [archivos](fa-intro.md) de una aplicación, proporciona un estado de explorador predeterminado de la aplicación.

Los registros realizados en el subárbol de **\_ \_ usuario de HKEY Current** tienen mayor prioridad para el usuario de la consola que los registros correspondientes realizados en el **\_ \_ equipo local HKEY**. En el caso de los nuevos usuarios del sistema, se usan las opciones almacenadas en **HKEY \_ local \_ Machine** . A partir de Windows XP, la configuración de Internet del menú Inicio se mantiene en las entradas predeterminadas de dos ubicaciones del registro:

-   **HKEY \_ \_** Clientes de \\ **software** de usuario actual \\  \\ **StartMenuInternet**
-   **HKEY \_ \_** Clientes de \\ **software** de equipo local \\  \\ **StartMenuInternet**

La subclave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **StartMenuInternet** describe el explorador de Internet que se inicia cuando el usuario hace clic en el icono de **Internet** del menú Inicio. Si esa subclave está en blanco o falta, el icono de **Internet** del menú Inicio se establece en el valor predeterminado del sistema almacenado en la segunda ubicación en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** , que describe todas las aplicaciones de explorador de Internet instaladas en el sistema.

Cuando un usuario nuevo inicia sesión en el sistema, el menú Inicio usa el valor predeterminado de la subclave en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** para mostrar el cliente de Internet predeterminado e inicia la aplicación registrada cuando se hace clic en ese icono.

### <a name="how-to-register-as-the-default-internet-client"></a>Cómo registrarse como el cliente de Internet predeterminado

Debajo de la subclave **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** puede haber cero o más subclaves, una para cada aplicación de explorador de Internet registrada. Por ejemplo, un sistema hipotético podría tener esta disposición:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

Se mostrarán las entradas del registro con un explorador hipotético denominado "Lit View" desde una empresa ficticia denominada Litware Inc. Supongamos que el nombre del archivo ejecutable para la vista Lit es Litview.exe. El registro de la vista Lit se produce como se muestra aquí:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Los datos de LocalizedString son del tipo REG \_ SZ o REG \_ Expand \_ SZ si se usan variables de ruta de acceso como `%programfiles%` . LocalizedString proporciona la ruta de acceso a un archivo ejecutable (. exe) o de biblioteca (. dll). Tenga en cuenta que la cadena de ruta de acceso comienza con un signo "arroba" (@) y que no se requieren comillas alrededor de la ruta de acceso, independientemente de los espacios que contiene. El entero decimal es el identificador de un recurso de cadena, incluido en el archivo DLL especificado, cuyo valor se va a mostrar al usuario. Esto permite usar el mismo registro para varios idiomas. Cada lenguaje proporciona una ResourceDLL.dll diferente. Esto permite que el sistema muestre la cadena correcta según el idioma seleccionado actualmente.

Los siguientes valores de REG \_ SZ o REG \_ Expand, indican al \_ menú Inicio del icono predeterminado que se muestre cuando el usuario selecciona Lit View como el explorador de Internet del menú Inicio.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

La siguiente subclave del registro especifica una línea de comandos que se ejecuta cuando el usuario hace clic en el comando de menú de Internet en el menú Inicio, suponiendo que Lit View es el explorador de Internet seleccionado del menú Inicio. Por ejemplo, el comando podría abrir el explorador con la Página principal del usuario o el comando podría iniciar una interfaz de usuario introductoria que el fabricante de software independiente (ISV) cree que es adecuado. Los datos son de tipo REG \_ SZ o REG \_ Expand \_ , pero Observe que, dado que hay un espacio en la ruta de acceso de la línea de comandos, la ruta de acceso del archivo ejecutable está entre comillas.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

Cuando el usuario especifica [establecer el acceso y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md) que Lit View debe usar como explorador Web predeterminado de nivel de equipo, la aplicación debe establecer la siguiente \_ entrada reg SZ. Tenga en cuenta que, dado que SPAD se ejecuta con privilegios de administrador, se permite el acceso a esta subclave.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> En Windows Vista, el explorador Web predeterminado de nivel de usuario debe establecerse con la herramienta **programas predeterminados** , no con [SPAD](cpl-setprogramaccess.md).
> 
> **La siguiente información solo se aplica a Windows XP.**
> 
> Si el registro del explorador Web predeterminado de nivel de equipo en HKEY \_ local \_ Machine, tal como se mostró anteriormente, es correcto, la aplicación debe eliminar la entrada predeterminada en la siguiente subclave:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> Si se produce un error en el registro del explorador Web predeterminado de nivel de equipo en HKEY \_ local \_ Machine, la aplicación debe establecer los datos de reg \_ SZ tal como se muestra en este ejemplo para la aplicación Lit View:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

Después de actualizar las subclaves adecuadas, la aplicación difunde el mensaje de [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con el parámetro *wParam* establecido en 0 y su parámetro *lParam* que apunta a la cadena terminada en NULL `"Software\Clients\StartMenuInternet"` . Esto notifica al sistema operativo que el cliente predeterminado ha cambiado.

La configuración de estas subclaves para el explorador de Internet predeterminado es necesaria para mantener la compatibilidad con versiones anteriores de los exploradores Web que no admiten registros por usuario.

## <a name="registering-for-the-start-menu-email-link"></a>Registro para el vínculo de correo electrónico del menú Inicio

> [!Note]  
> El vínculo de correo electrónico del menú Inicio se ha quitado de Windows 7. Sin embargo, este registro que se trata en esta sección todavía debe realizarse para su efecto en la asignación del cliente MAPI predeterminado.

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a>Cómo el menú Inicio muestra el cliente de correo electrónico predeterminado

Cualquier aplicación de correo electrónico puede registrarse para aparecer como un cliente de correo electrónico en el menú Inicio. Esta visibilidad, junto con el registro adecuado para los tipos de [protocolos](/previous-versions//aa767743(v=vs.85)) y [archivos](fa-intro.md) de una aplicación, proporciona un estado de correo predeterminado de la aplicación.

Los registros realizados en el subárbol de **\_ \_ usuario de HKEY Current** tienen mayor prioridad para el usuario de la consola que los registros correspondientes realizados en el **\_ \_ equipo local HKEY**. En el caso de los nuevos usuarios del sistema, se usan las opciones almacenadas en **HKEY \_ local \_ Machine** . A partir de Windows XP, la configuración de correo electrónico del menú Inicio se mantiene en las entradas predeterminadas de dos ubicaciones del registro:

-   **HKEY \_ \_** \\  \\  \\ **Correo electrónico** de clientes de software del usuario actual
-   **HKEY \_ \_** \\  \\  \\ **Correo electrónico** de clientes de software de máquina local

La subclave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **mail** describe el cliente de correo electrónico que se inicia cuando el usuario hace clic en el icono de **correo electrónico** del menú Inicio.

La subclave **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** describe las aplicaciones de correo electrónico instaladas en el sistema, así como la aplicación de correo electrónico predeterminada.

Si el correo de los clientes de software del **\_ \_ usuario actual de HKEY** \\  \\  \\  está en blanco o falta, se utiliza el valor predeterminado definido en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** para seleccionar la aplicación de correo electrónico que aparece en el menú Inicio.

Cuando un usuario nuevo inicia sesión en el sistema, el menú Inicio usa el valor predeterminado de la subclave en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** para mostrar el cliente de correo electrónico predeterminado e inicia la aplicación registrada cuando se hace clic en ese icono.

### <a name="how-to-register-as-the-default-email-client"></a>Cómo registrarse como cliente de correo electrónico predeterminado

**HKEY \_ El \_** \\  \\ correo electrónico de **los clientes** \\  de software de máquina local puede contener cero o más subclaves, una para cada aplicación de correo electrónico registrada. Por ejemplo, un sistema hipotético podría definir las subclaves siguientes:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

Se mostrarán las entradas del registro con un cliente de correo electrónico hipotético llamado "Lit mail" de la empresa ficticia denominada Litware Inc. Litware Inc. decide registrar este cliente de correo electrónico con el nombre interno "LitMail". Al igual que con un explorador, el nombre interno es una cadena única que se usa como nombre de la subclave, pero nunca se muestra al usuario.

Para instalar el cliente de correo electrónico de lit mail como predeterminado, usan la siguiente subclave y sus entradas:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

Los datos de LocalizedString son del tipo REG \_ SZ o REG \_ Expand \_ SZ si se usan variables de ruta de acceso como `%programfiles%` . LocalizedString proporciona la ruta de acceso a un archivo ejecutable (. exe) o de biblioteca (. dll). Tenga en cuenta que la cadena de ruta de acceso comienza con un signo "arroba" (@) y que no se requieren comillas alrededor de la ruta de acceso, independientemente de los espacios que contiene. El entero decimal es el identificador de un recurso de cadena, incluido en el archivo DLL especificado, cuyo valor se va a mostrar al usuario. Esto permite usar el mismo registro para varios idiomas. Cada lenguaje proporciona una ResourceDLL.dll diferente. Esto permite que el sistema muestre la cadena correcta según el idioma seleccionado actualmente.

Después de actualizar las subclaves adecuadas, la aplicación difunde el mensaje de [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con el parámetro *wParam* establecido en 0 y su parámetro *lParam* que apunta a la cadena terminada en NULL `"Software\Clients\Mail"` . Esto notifica al sistema operativo que el cliente predeterminado ha cambiado.

Para mantener la compatibilidad con las aplicaciones que no admiten cadenas localizadas, el nombre de la aplicación en el idioma instalado también debe establecerse como el valor predeterminado de la subclave.

Los siguientes valores de **reg \_ SZ** o **reg \_ Expand \_** se muestran en el menú Inicio del icono predeterminado para que se muestren cuando el usuario selecciona Lit mail como programa de correo del menú Inicio:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

La entrada siguiente especifica una línea de comandos que se ejecutará cuando el usuario haga clic en el elemento de menú **correo electrónico** en el menú Inicio, suponiendo que Lit mail es el programa de correo electrónico seleccionado del menú Inicio. Esta línea de comandos también se ejecuta si el usuario selecciona **leer correo electrónico** en el menú **herramientas** de Windows Internet Explorer. Los datos son de tipo **reg \_ SZ** o **reg \_ Expand \_**, pero Observe que, dado que hay un espacio en la ruta de acceso de la línea de comandos, la ruta de acceso del archivo ejecutable está entre comillas.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

Si (y solo si) *el usuario* especifica que Lit mail sea la aplicación de correo electrónico predeterminada del menú Inicio, la aplicación Lit mail puede escribir su nombre interno en el siguiente valor **reg \_ SZ** :

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

Si (y solo si) *el usuario* especifica que Lit mail sea la aplicación de correo electrónico predeterminada para todo el sistema, la aplicación Lit mail puede escribir su nombre interno en el valor **reg \_ SZ** que se especifica a continuación. Tenga en cuenta que el acceso a esta subclave podría estar restringido. Las aplicaciones no deben suponer que todos los usuarios tienen permiso para cambiar la aplicación de correo electrónico predeterminada para todo el sistema.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

El registro como la aplicación de correo electrónico predeterminada del menú Inicio no es equivalente al registro como el cliente de correo electrónico predeterminado del sistema o el controlador *mailto* registrado.

-   El cliente de correo electrónico predeterminado del sistema se inicia cuando el usuario hace clic en **leer correo electrónico** en el menú **herramientas** de Internet Explorer.
-   El controlador *mailto* registrado se inicia cuando el usuario hace clic en una dirección URL del formulario `mailto:someone@example.com` .
-   La aplicación de correo electrónico del menú Inicio se inicia cuando el usuario hace clic en el icono de **correo electrónico** del menú Inicio.

Si no se especifica ninguna aplicación de correo electrónico predeterminada del menú Inicio, el icono de correo electrónico del menú Inicio inicia el cliente de correo electrónico predeterminado del sistema.

En este tema no se trata el registro de la aplicación como el controlador de protocolo *mailto* predeterminado. Las aplicaciones que desean registrarse de este modo deben seguir las especificaciones existentes sobre este asunto.

## <a name="customizing-the-context-menu"></a>Personalización del menú contextual

Una aplicación puede personalizar las páginas de propiedades que se muestran cuando el usuario selecciona **propiedades** en el menú contextual del icono de **correo electrónico** (o **Internet**). Por ejemplo, la aplicación de correo electrónico Litware agrega los siguientes datos de **reg \_ SZ** o **reg \_ Expand \_ SZ** para mostrar una hoja de propiedades personalizada para el icono de **correo electrónico** en lugar de su hoja de propiedades predeterminada.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

El elemento de datos MUIVerb se construye a partir de un signo "arroba" (@), seguido de la ruta de acceso completa al archivo DLL de recursos, una coma, un signo menos (-) y, a continuación, el identificador de recursos de cadena decimal que se va a mostrar. Tenga en cuenta que la ruta de acceso al LitMail.exe programa contiene espacios, por lo que la cadena de ruta de acceso se coloca entre comillas.

Una aplicación también puede Agregar comandos adicionales al menú contextual. Por ejemplo, la aplicación de correo electrónico de Litware agrega un comando de **búsqueda** con los siguientes datos de **reg \_ SZ** :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

El nombre de la subclave que se encuentra debajo del **Shell** (en este caso, "Find") es un nombre arbitrario no traducido. Una vez más, los datos de MUIVerb contienen un signo de arroba (@) como primer elemento, seguido de la ruta de acceso a un archivo DLL de recursos, un separador de coma y, a continuación, un signo menos que precede al identificador de recursos de cadena decimal. Por ejemplo, ese recurso de cadena podría ser "Abrir libreta de direcciones". Por último, tenga en cuenta que la cadena de la línea de comandos contiene espacios, por lo que está entre comillas.

 

 
