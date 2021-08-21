---
description: La menú Inicio de Windows XP y Windows Vista contiene ranuras reservadas para los clientes predeterminados de Internet (explorador) y correo electrónico (correo), conocidos normalmente como aplicaciones de Internet del menú Inicio.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Cómo registrar un explorador de Internet o un cliente de correo electrónico con el Windows inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa40a8775a60fbdd55ba33c2039065d744734a3331727a749b2c3a2e3d564be2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046682"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a>Cómo registrar un explorador de Internet o un cliente de correo electrónico con el Windows inicio

> [!Note]  
> Este tema se aplica a Windows XP, Windows Vista y Windows 7.

 

La menú Inicio de Windows XP y Windows Vista contiene ranuras reservadas para los clientes predeterminados de **Internet** (explorador) y correo electrónico **(correo),** conocidos normalmente como Aplicaciones de *Internet* del menú Inicio. Las aplicaciones que se registran como menú Inicio Aplicaciones de Internet lo hacen en todo el sistema (por equipo). En Windows Vista, el usuario puede usar la **característica Programas** predeterminados para establecer un valor predeterminado por usuario.

Cuando las aplicaciones se registran como Aplicaciones de Internet del menú Inicio, Windows XP y Windows Vista crean iconos **de** **Internet** y correo electrónico en el menú Inicio. Al hacer clic en estos iconos, menú Inicio comprobar el subárbol del Registro por usuario (**HKEY \_ CURRENT \_ USER**). Si no se encuentra ninguna configuración predeterminada por usuario, menú Inicio busca la subclave predeterminada por equipo en el subárbol **HKEY \_ LOCAL \_ MACHINE.**

> [!Note]  
> La instalación predeterminada de Windows no registra un programa predeterminado de Internet o correo electrónico por usuario, solo un valor predeterminado de todo el sistema. Esto proporciona una ruta de actualización sin problemas de las versiones anteriores del sistema operativo, en las que solo se admite el subárbol HKEY LOCAL MACHINE para \_ \_ los registros de cliente.

 

En este tema se de abordan los siguientes elementos:

-   [Registro en el vínculo internet del menú Inicio](#registering-for-the-start-menu-internet-link)
    -   [Registro como cliente de Internet predeterminado](#how-to-register-as-the-default-internet-client)
-   [Registro en el vínculo de correo electrónico del menú Inicio](#registering-for-the-start-menu-email-link)
    -   [Cómo muestra el menú Inicio el cliente de correo electrónico predeterminado](#how-the-start-menu-displays-the-default-email-client)
    -   [Cómo registrarse como el cliente de correo electrónico predeterminado](#how-to-register-as-the-default-email-client)
-   [Personalizar el menú contextual](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a>Registro en el vínculo internet del menú Inicio

> [!Note]  
> Este registro está en desuso a partir de Windows 7, que ya no proporciona un vínculo menú Inicio Internet. Los registros existentes se omiten en Windows 7 y versiones posteriores. El registro como el valor menú Inicio aplicación de Internet no es lo mismo que registrarse como explorador web predeterminado. El explorador web predeterminado se usa para iniciar direcciones URL arbitrarias desde cualquier lugar del sistema. La menú Inicio de Internet simplemente controla el programa que se inicia cuando el usuario hace clic en el icono de Internet en el menú Inicio.

 

Cualquier aplicación de explorador web puede registrarse para aparecer como un cliente de Internet en el menú Inicio. Esta visibilidad, junto con el [](fa-intro.md) registro adecuado para los tipos de archivo y protocolo [de](/previous-versions//aa767743(v=vs.85)) una aplicación, proporciona un estado de explorador predeterminado de la aplicación.

Los registros realizados en el subárbol **HKEY \_ CURRENT \_ USER** tienen mayor prioridad para el usuario de consola que los registros correspondientes realizados en **HKEY \_ LOCAL \_ MACHINE**. Para los nuevos usuarios del sistema, se usa la configuración almacenada en **HKEY \_ LOCAL \_ MACHINE.** A Windows XP, menú Inicio configuración de Internet se mantiene en las entradas predeterminadas de dos ubicaciones del Registro:

-   **HKEY \_ CLIENTES \_ DE** \\ **SOFTWARE DE USUARIO** \\  \\ **ACTUAL StartMenuInternet**
-   **HKEY \_ Clientes \_ de** \\ **SOFTWARE DE MÁQUINA LOCAL** \\  \\ **StartMenuInternet**

La subclave **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet**  describe el explorador de Internet que se inicia cuando el usuario hace clic en el icono de Internet en el menú Inicio. Si esa subclave está en blanco o falta, el icono de **Internet** del menú Inicio se establece en el valor predeterminado del sistema almacenado en la segunda ubicación en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet** , que describe todas las aplicaciones de explorador de Internet instaladas en el sistema.

Cuando un nuevo usuario inicia sesión en el sistema, menú Inicio usa el valor predeterminado de la subclave en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet** para mostrar el cliente de Internet predeterminado e inicia la aplicación registrada cuando se hace clic en ese icono.

### <a name="how-to-register-as-the-default-internet-client"></a>Registro como cliente de Internet predeterminado

Debajo de la subclave **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet** puede haber cero o más subclaves, una para cada aplicación de explorador de Internet registrada. Por ejemplo, un sistema hipotético podría tener esta disposición:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

Se mostrarán las entradas del Registro con un explorador hipotético llamado "Lit View" de una empresa ficticia llamada Litware Inc. Supongamos que el nombre ejecutable de Lit View es Litview.exe. El registro de la vista lit se produce como se muestra aquí:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Los datos LocalizedString son de tipo REG SZ o REG EXPAND SZ si se usan variables de ruta \_ \_ de acceso como \_ `%programfiles%` . LocalizedString proporciona la ruta de acceso a un archivo ejecutable (.exe) o biblioteca (.dll). Tenga en cuenta que la cadena de ruta de acceso comienza con un signo "at" (@) y que no se requieren comillas alrededor de la ruta de acceso independientemente de los espacios que contiene. El entero decimal es el identificador de un recurso de cadena, incluido en el archivo DLL especificado, cuyo valor se va a mostrar al usuario. Esto permite usar el mismo registro para varios idiomas. Cada lenguaje proporciona un ResourceDLL.dll. Esto permite que el sistema muestre la cadena correcta en función del idioma seleccionado actualmente.

El siguiente valor REG SZ o REG EXPAND SZ informa al menú Inicio del icono predeterminado que se mostrará cuando el usuario seleccione Lit View (Vista lit) menú Inicio \_ \_ Explorador de \_ Internet.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

La siguiente subclave del Registro especifica una línea de comandos que se ejecutará cuando el usuario haga clic en el comando de menú Internet en el menú Inicio, suponiendo que La vista lit es el explorador de Internet menú Inicio seleccionado. Por ejemplo, el comando podría abrir el explorador con la página principal del usuario o el comando podría iniciar una interfaz de usuario introductoria que el proveedor de software independiente (ISV) considera adecuado. Los datos son de tipo REG SZ o REG EXPAND SZ, pero observe que, dado que hay un espacio en la ruta de acceso de la línea de comandos, la ruta de acceso ejecutable se incluye \_ \_ entre \_ comillas.

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

Cuando el usuario especifica a través de Establecer el acceso al programa y los valores predeterminados del equipo [(SPAD)](cpl-setprogramaccess.md) que la vista lit debe usarse como explorador web predeterminado de nivel de equipo, la aplicación debe establecer la siguiente entrada REG \_ SZ. Tenga en cuenta que, dado que SPAD se ejecuta con privilegios de administrador, se permite el acceso a esta subclave.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> En Windows Vista, el explorador web predeterminado de nivel de usuario debe establecerse mediante la **herramienta Programas** predeterminados, no [SPAD](cpl-setprogramaccess.md).
> 
> **La siguiente información solo se aplica Windows XP.**
> 
> Si el registro del explorador web predeterminado de nivel de equipo en HKEY LOCAL MACHINE como se muestra anteriormente es correcto, la aplicación debe eliminar la entrada Predeterminada en \_ \_ la subclave siguiente:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> Si se produce un error en el registro del explorador web predeterminado de nivel de equipo en HKEY LOCAL MACHINE, la aplicación debe establecer los datos DE REG SZ como se muestra en este ejemplo para la aplicación \_ \_ Lit \_ View:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

Después de actualizar las subclaves adecuadas, la aplicación difunde el mensaje [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con su parámetro *wParam* establecido en 0 y su parámetro *lParam* que apunta a la cadena terminada en `"Software\Clients\StartMenuInternet"` NULL. Esto notifica al sistema operativo que el cliente predeterminado ha cambiado.

El establecimiento de estas subclaves para el explorador menú Inicio Internet es necesario para conservar la compatibilidad con los exploradores web antiguos que no admiten registros por usuario.

## <a name="registering-for-the-start-menu-email-link"></a>Registro en el vínculo de correo electrónico del menú Inicio

> [!Note]  
> El menú Inicio correo electrónico se ha quitado a partir Windows 7. Sin embargo, este registro que se describe en esta sección todavía debe realizarse para su efecto en la asignación del cliente de MAPI predeterminado.

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a>Cómo muestra el menú Inicio el cliente de correo electrónico predeterminado

Cualquier aplicación de correo electrónico puede registrarse para aparecer como un cliente de correo electrónico en el menú Inicio. Esta visibilidad, junto con el [](fa-intro.md) registro adecuado para los tipos de archivo y protocolo [de](/previous-versions//aa767743(v=vs.85)) una aplicación, proporciona un estado de correo predeterminado de la aplicación.

Los registros realizados en el subárbol **HKEY \_ CURRENT \_ USER** tienen mayor prioridad para el usuario de consola que los registros correspondientes realizados en **HKEY \_ LOCAL \_ MACHINE**. Para los nuevos usuarios del sistema, se usa la configuración almacenada en **HKEY \_ LOCAL \_ MACHINE.** A Windows XP, menú Inicio configuración de correo electrónico se mantiene en las entradas predeterminadas de dos ubicaciones del Registro:

-   **HKEY \_ CORREO \_ ELECTRÓNICO DE CLIENTES** DE \\ **SOFTWARE** \\ **DE USUARIO** \\ **ACTUAL**
-   **HKEY \_ CORREO \_ DE CLIENTES** DE SOFTWARE \\  \\ **DE** MÁQUINA \\ **LOCAL**

La subclave **HKEY \_ CURRENT \_ USER** SOFTWARE Clients Mail describe el cliente de correo electrónico que se inicia cuando el usuario hace clic en el icono Correo electrónico en el \\  \\  \\  menú Inicio. 

La subclave **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Clients Mail describe las aplicaciones de correo electrónico instaladas en el sistema, así como la \\  \\  \\  aplicación de correo electrónico predeterminada.

Si el correo de clientes de SOFTWARE DE USUARIO ACTUAL de **HKEY \_ \_** está en blanco o falta, el valor predeterminado definido en \\  \\  \\  **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **Mail** se usa para seleccionar la aplicación de correo electrónico que aparece en el menú Inicio.

Cuando un nuevo usuario inicia sesión en el sistema, menú Inicio usa el valor predeterminado de la subclave en **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Clients Mail para mostrar el cliente de correo electrónico predeterminado e inicia la aplicación registrada cuando se hace clic en ese \\  \\  \\  icono.

### <a name="how-to-register-as-the-default-email-client"></a>Cómo registrarse como el cliente de correo electrónico predeterminado

**HKEY \_ Local \_ MACHINE** SOFTWARE Clients Mail puede contener cero o \\  \\  \\  más subclaves, una para cada aplicación de correo electrónico registrada. Por ejemplo, un sistema hipotético podría definir las subclaves siguientes:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

Mostraremos las entradas del Registro con un cliente de correo electrónico hipotético llamado "Lit Mail" de la empresa ficticia litware Inc. Litware Inc. decide registrar este cliente de correo electrónico con el nombre interno "LitMail". Al igual que con un explorador, el nombre interno es una cadena única que se usa como nombre de subclave, pero nunca se muestra al usuario.

Para instalar el cliente de correo electrónico de Lit Mail como valor predeterminado, usan la siguiente subclave y sus entradas:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

Los datos LocalizedString son de tipo REG SZ o REG EXPAND SZ si se usan variables de ruta \_ \_ de acceso como \_ `%programfiles%` . LocalizedString proporciona la ruta de acceso a un archivo ejecutable (.exe) o biblioteca (.dll). Tenga en cuenta que la cadena de ruta de acceso comienza con un signo "at" (@) y que no se requieren comillas alrededor de la ruta de acceso independientemente de los espacios que contiene. El entero decimal es el identificador de un recurso de cadena, incluido en el archivo DLL especificado, cuyo valor se va a mostrar al usuario. Esto permite usar el mismo registro para varios idiomas. Cada lenguaje proporciona un ResourceDLL.dll. Esto permite que el sistema muestre la cadena correcta en función del idioma seleccionado actualmente.

Después de actualizar las subclaves adecuadas, la aplicación difunde el mensaje [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con su parámetro *wParam* establecido en 0 y su parámetro *lParam* que apunta a la cadena terminada en `"Software\Clients\Mail"` NULL. Esto notifica al sistema operativo que el cliente predeterminado ha cambiado.

Para la compatibilidad con versiones anteriores con aplicaciones que no admiten cadenas localizadas, el nombre de la aplicación en el idioma instalado también debe establecerse como el valor predeterminado de la subclave.

El siguiente **valor REG \_ SZ** o **REG EXPAND \_ \_ SZ** informa al menú Inicio del icono predeterminado que se mostrará cuando el usuario seleccione Lit Mail como el programa de correo electrónico menú Inicio predeterminado:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

La entrada siguiente especifica una línea de comandos  que se ejecutará cuando el usuario haga clic en el elemento de menú Correo electrónico en el menú Inicio, suponiendo que Lit Mail es el programa de correo electrónico menú Inicio seleccionado. Esta línea de comandos también se ejecuta si el usuario selecciona Leer correo **electrónico** en el Windows Internet Explorer **herramientas.** Los datos son de tipo **REG \_ SZ** o **REG EXPAND \_ \_ SZ,** pero observe que, dado que hay un espacio en la ruta de acceso de la línea de comandos, la ruta de acceso ejecutable se incluye entre comillas.

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

Si (y solo *si)* el usuario especifica Lit Mail como la aplicación de correo electrónico menú Inicio predeterminada, la aplicación Lit Mail puede escribir su nombre interno en el siguiente valor **REG \_ SZ:**

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

Si (y solo *si)* el usuario especifica que Lit Mail es la aplicación de correo electrónico predeterminada para todo el sistema, la aplicación Lit Mail puede escribir su nombre interno en el valor **REG \_ SZ** especificado a continuación. Tenga en cuenta que el acceso a esta subclave puede estar restringido. Las aplicaciones no deben asumir que todos los usuarios tienen permiso para cambiar la aplicación de correo electrónico predeterminada de todo el sistema.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

El registro como valor predeterminado menú Inicio aplicación de correo electrónico no equivale al registro como el cliente de correo electrónico predeterminado del sistema o el controlador *mailto* registrado.

-   El cliente de correo electrónico predeterminado del sistema se inicia cuando el usuario hace clic en Leer **correo electrónico** desde Internet Explorer **Herramientas.**
-   El controlador *mailto registrado* se inicia cuando el usuario hace clic en una dirección URL con el formato `mailto:someone@example.com` .
-   La menú Inicio de correo electrónico se inicia cuando el usuario hace clic en el icono **correo electrónico** de la menú Inicio.

Si no se menú Inicio aplicación de correo electrónico predeterminada, el icono Correo electrónico del menú Inicio inicia el cliente de correo electrónico predeterminado del sistema.

En este tema no se trata el registro de la aplicación como controlador de *protocolo mailto* predeterminado. Las aplicaciones que desean registrarse de este modo deben seguir siguiendo las especificaciones existentes sobre este tema.

## <a name="customizing-the-context-menu"></a>Personalizar el menú contextual

Una aplicación puede personalizar las páginas de propiedades  que se muestran cuando el usuario selecciona Propiedades en el menú contextual del icono de correo electrónico **(o** **Internet).** Por ejemplo, la aplicación de correo electrónico Litware agrega los siguientes datos  **REG \_ SZ** o **REG \_ EXPAND \_ SZ** para mostrar una hoja de propiedades personalizada para el icono correo electrónico en lugar de su hoja de propiedades predeterminada.

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

El elemento de datos CSVVerb se construye a partir de un signo "at" (@), seguido de la ruta de acceso completa al archivo DLL de recursos, una coma, un signo menos (-) y, a continuación, el identificador de recurso de cadena decimal que se va a mostrar. Tenga en cuenta que la ruta de acceso LitMail.exe programa contiene espacios, por lo que la cadena de ruta de acceso se coloca entre comillas.

Una aplicación también puede agregar comandos adicionales al menú contextual. Por ejemplo, la aplicación de correo electrónico Litware agrega un **comando find** con los siguientes datos **REG \_ SZ:**

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

El nombre de la **subclave debajo** del shell (en este caso, "find") es un nombre arbitrario y no localizado. Una vez más, los datos DE LAVERB contienen un signo "at" (@) como primer elemento, seguido de la ruta de acceso a un archivo DLL de recursos, un separador de comas y, a continuación, un signo menos que precede al identificador de recurso de cadena decimal. Por ejemplo, ese recurso de cadena podría ser "Abrir libreta de direcciones". Por último, tenga en cuenta que la cadena de línea de comandos contiene espacios, por lo que se incluye entre comillas.

 

 
