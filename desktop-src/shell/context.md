---
description: Al hacer clic con el botón derecho en un objeto, normalmente se muestra un menú contextual. Este menú contiene una lista de comandos que el usuario puede seleccionar para realizar varias acciones en el objeto. Esta sección es una introducción a los menús contextuales para objetos del sistema de archivos.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Extender menús contextuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d046805ebc787f5cad2bfaa40538c51b826c3f0541f3ec1afad508202a4a25fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460652"
---
# <a name="extending-shortcut-menus"></a>Extender menús contextuales

Al hacer clic con el botón derecho en un objeto, normalmente se muestra un *menú contextual.* Este menú contiene una lista de comandos que el usuario puede seleccionar para realizar varias acciones en el objeto. Esta sección es una introducción a los menús contextuales para objetos del sistema de archivos.

-   [Menús contextuales para objetos del sistema de archivos](#shortcut-menus-for-file-system-objects)
-   [Verbos del menú contextual](#shortcut-menu-verbs)
    -   [Verbos canónicos](#canonical-verbs)
    -   [Verbos extendidos](#extended-verbs)
-   [Extender el menú contextual para un tipo de archivo](#extending-the-shortcut-menu-for-a-file-type)
-   [Extender el menú contextual para objetos de shell predefinidos](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Registro de una aplicación para controlar tipos de archivo arbitrarios](#registering-an-application-to-handle-arbitrary-file-types)
-   [Extender el nuevo submenú](#extending-the-new-submenu)

Puede encontrar información adicional aquí:

-   [Definición de verbos extendidos](how-to-define-extended-verbs.md)
-   [Cómo asociar verbos a comandos DDE](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Menús contextuales para objetos del sistema de archivos

Cuando un usuario hace clic con el botón derecho en un objeto, como un archivo, que se muestra en el Explorador de Windows o en el escritorio, aparece un menú contextual con una lista de comandos. A continuación, el usuario puede realizar una acción en el archivo, como abrirlo o eliminarlo, seleccionando el comando adecuado.

Dado que los menús contextuales se usan a menudo para la administración de archivos, el Shell proporciona un conjunto de comandos predeterminados, como Cortar y Copiar, que aparecen en el menú contextual de cualquier archivo. Tenga en cuenta que aunque Abrir con es un comando predeterminado, no se muestra para algunos tipos de archivo estándar, como .wav. En la siguiente ilustración del directorio Mis documentos ejemplo, que también se usó como ejemplo en Personalización de iconos [,](icon.md)se muestra un menú contextual predeterminado que se muestra haciendo clic con el botón derecho MyDocs4.xyz.

![captura de pantalla del menú contextual predeterminado para objetos del sistema de archivos](images/context1.jpg)

La razón MyDocs4.xyz muestra un menú contextual predeterminado es que no es miembro de un tipo de [archivo registrado.](fa-file-types.md) Por otro lado, .txt es un tipo de archivo registrado. Si hace clic con el botón derecho en uno de los .txt, verá en su lugar un menú contextual con dos comandos adicionales en su sección **superior:** Abrir **e imprimir**.

![captura de pantalla del menú contextual personalizado para objetos del sistema de archivos](images/context2.jpg)

Una vez registrado un tipo de archivo, puede ampliar su menú contextual con comandos adicionales. Se muestran encima de los comandos predeterminados cuando se hace clic con el botón derecho en cualquier archivo de ese tipo. Aunque la mayoría de los comandos agregados de esta  manera son comunes, como Imprimir o Abrir **,** puede agregar cualquier comando que un usuario pueda encontrar útil.

Todo lo que se necesita para ampliar el menú contextual de un tipo de archivo es crear una entrada del Registro para cada comando. Un enfoque más sofisticado es implementar un controlador de menús contextuales, que permite ampliar el menú contextual de un tipo de archivo archivo a archivo. Para obtener más información, vea [Crear controladores de menú contextual](context-menu-handlers.md).

## <a name="shortcut-menu-verbs"></a>Verbos del menú contextual

Cada comando del menú contextual se identifica en el Registro por su *verbo*. Estos verbos son los mismos que los que usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) al iniciar aplicaciones mediante programación. Para obtener más información sobre el uso de **ShellExecuteEx**, vea la explicación en [Inicio de aplicaciones](launch.md).

Un verbo es una cadena de texto simple que el Shell usa para identificar el comando asociado. Cada verbo corresponde a la cadena *de comando* utilizada para iniciar el comando en una ventana de consola o un archivo por lotes (.bat). Por ejemplo, el **verbo abierto** normalmente inicia un programa para abrir un archivo. Normalmente, su cadena de comandos tiene un aspecto similar al siguiente:

``` syntax
"My Program.exe" "%1"
```

"%1" es el marcador de posición estándar para un parámetro de línea de comandos proporcionado con el nombre de archivo. Por ejemplo, puede especificar una página determinada para mostrarla en una vista con pestañas.

> [!Note]  
> Si algún elemento de la cadena de comando contiene o puede contener espacios, debe incluirse entre comillas. De lo contrario, si el elemento contiene un espacio, no se analizará correctamente. Por ejemplo, "My Program.exe" iniciará la aplicación correctamente. Si usa My Program.exe, el sistema intentará iniciar "My" con "Program.exe" como primer argumento de línea de comandos. Siempre debe usar comillas con argumentos como "%1" que el Shell expande a cadenas, ya que no puede estar seguro de que la cadena no contendrá un espacio.

 

Los verbos también pueden tener una *cadena de* presentación asociada a ellos, que se muestra en el menú contextual en lugar de en la propia cadena de verbo. Por ejemplo, la cadena para mostrar **de openas** es Open With. Al igual que las cadenas de menú normales, incluida una yerba (&) en la cadena de presentación permite la selección del teclado del comando.

### <a name="canonical-verbs"></a>Verbos canónicos

En general, las aplicaciones son responsables de proporcionar cadenas de presentación localizadas para los verbos que definen. Sin embargo, para proporcionar un grado de independencia del lenguaje, el sistema define un conjunto estándar de verbos de uso común denominados *verbos canónicos*. Un verbo canónico se puede usar con cualquier idioma y el sistema genera automáticamente una cadena de presentación localizada correctamente. Por ejemplo, la **cadena de** presentación del verbo abierto se establecerá en Abrir en un sistema en inglés y en Öffnen en un sistema alemán.

Los verbos canónicos incluyen:



| Valor      | Descripción                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| abierto       | Abre el archivo o la carpeta.                                                                   |
| opennew    | Abre el archivo o la carpeta en una nueva ventana.                                                   |
| imprimir      | Imprime el archivo.                                                                            |
| explore    | Abre Windows Explorer con la carpeta seleccionada.                                            |
| find       | Abre el **cuadro Windows de diálogo Buscar** con la carpeta establecida como ubicación de búsqueda predeterminada. |
| openas     | Abre el **cuadro de diálogo Abrir** con .                                                         |
| properties | Abre la hoja de propiedades del objeto.                                                          |



 

El verbo printto también es canónico, pero nunca se muestra. Permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.

### <a name="extended-verbs"></a>Verbos extendidos

Cuando el usuario hace clic con el botón derecho en un objeto, el menú contextual contiene todos los verbos normales. Sin embargo, podría haber comandos que quiera admitir, pero que no se han mostrado en todos los menús contextuales. Por ejemplo, podría tener comandos que no se usan normalmente o que están pensados para usuarios experimentados. Por esta razón, también puede definir uno o varios *verbos extendidos.* Estos verbos también son cadenas de caracteres y son similares a los verbos normales. Se distinguen de los verbos normales por la forma en que se registran. Para tener acceso a los comandos asociados con verbos extendidos, el usuario debe hacer clic con el botón derecho en un objeto mientras presiona la tecla MAYÚS. Los verbos extendidos se mostrarán junto con los verbos normales.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Extender el menú contextual para un tipo de archivo

La manera más sencilla de ampliar el menú contextual de un tipo de archivo es con el Registro. Para ello, agregue una **subclave shell** debajo de la clave para el ProgID de la aplicación asociada al [tipo de archivo](fa-file-types.md). Opcionalmente, puede definir un *verbo predeterminado* para el tipo de archivo si lo hace el valor predeterminado de la **subclave shell.**

El verbo predeterminado se muestra primero en el menú contextual. Su propósito es proporcionar al Shell un verbo que puede usar cuando se llama a [**ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pero no se especifica ningún verbo. El shell no selecciona necesariamente el verbo predeterminado cuando se usa **ShellExecuteEx** de esta manera. Para las versiones [5.0](versions.md) y posteriores de Shell, que se encuentran en Windows 2000 y sistemas posteriores, shell usa el primer verbo disponible de la lista siguiente. Si no hay ninguna disponible, se produce un error en la operación.

-   Verbo abierto
-   Verbo predeterminado
-   Primer verbo del registro
-   Verbo openwith

Para las versiones de Shell anteriores a [la versión 5.0,](versions.md)omita el tercer elemento.

Debajo **de la** subclave Shell, cree una subclave para cada verbo que quiera agregar. Cada una de estas subclaves tendrá un **valor REG \_ SZ** establecido en la cadena de presentación del verbo. Puede omitir la cadena de presentación para los verbos canónicos porque el sistema mostrará automáticamente una cadena localizada correctamente. Si omite la cadena de presentación para verbos no cíclicos, se mostrará la cadena de verbo. Para cada subclave de verbo, cree **una** subclave de comando con el valor predeterminado establecido en la cadena de comando.

En la ilustración siguiente se muestra un menú contextual para el tipo de archivo .myp usado en Tipos [de archivo](fa-file-types.md) e Iconos [de personalización](icon.md). Ahora tiene verbos open, doit, print e printto en su menú contextual, con doit como verbo predeterminado. El menú contextual tiene este aspecto.

![captura de pantalla del menú contextual personalizado](images/context3.jpg)

Las entradas del Registro usadas para extender el menú contextual que se muestra en la ilustración anterior son:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

Aunque el **comando Abrir con** está encima del primer separador, el sistema lo crea automáticamente y no requiere una entrada del Registro. El sistema crea automáticamente nombres para mostrar para los verbos canónicos abiertos e impresos. Dado que doit no es un verbo canónico, se le asigna un nombre para mostrar, "&Do It", que se puede seleccionar presionando la tecla D. El verbo printto no aparece en el menú contextual, pero su inclusión permite al usuario imprimir archivos al colocarlos en un icono de impresora. En este ejemplo, %1 representa el nombre de archivo y %2 el nombre de impresora.

Los verbos se pueden suprimir mediante la configuración de directiva agregando un valor SuppressionPolicy a la clave del verbo. Establezca el valor de SuppressionPolicy en el identificador de directiva. Si la directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada. Para ver los posibles valores de identificador de directiva, consulte [**la enumeración RESTRICTIONS.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Extender el menú contextual para objetos de shell predefinidos

Muchos objetos de Shell predefinidos tienen menús contextuales que se pueden extender. Registre el comando de la misma manera que registra los tipos de archivo típicos, pero use el nombre del objeto predefinido como nombre del tipo de archivo.

Puede encontrar una lista de objetos predefinidos en la sección Objetos de *shell* [predefinidos](handlers.md)de Crear controladores de extensión de shell . Los objetos predefinidos de Shell cuyos menús contextuales se pueden extender agregando verbos en el Registro se marcan en la tabla con la palabra "Verbo".

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Registro de una aplicación para controlar tipos de archivo arbitrarios

En las secciones anteriores de este documento se ha analizado cómo definir elementos de menú contextual para un tipo de archivo determinado. Entre otras cosas, la definición del menú contextual le permite especificar cómo la aplicación asociada abre un miembro del tipo de archivo. Sin embargo, como se describe en Tipos de archivo [,](fa-file-types.md)las aplicaciones también pueden registrar un procedimiento predeterminado independiente que se usará cuando un usuario intente usar la aplicación para abrir un tipo de archivo que no haya asociado a la aplicación. Este tema se describe aquí porque registra el procedimiento predeterminado de la misma manera que registra los elementos del menú contextual.

El procedimiento predeterminado tiene dos fines básicos. Una es especificar cómo se debe invocar la aplicación para abrir un tipo de archivo arbitrario. Por ejemplo, podría usar una marca de línea de comandos para indicar que se está abierto un tipo de archivo desconocido. El otro propósito es definir las distintas características de un tipo de archivo, como los elementos del menú contextual y el icono. Si un usuario asocia la aplicación a un tipo de archivo adicional, ese tipo tendrá estas características. Si el tipo de archivo adicional se asoció previamente a otra aplicación, estas características reemplazarán a los originales.

Para registrar el procedimiento predeterminado, coloque las mismas claves del Registro que creó para el ProgID de la aplicación en la subclave de la aplicación de **HKEY \_ CLASSES \_ ROOT** \\ **Applications**. También puede incluir un valor FriendlyAppName para proporcionar al sistema un nombre descriptivo para la aplicación. El nombre descriptivo de la aplicación también se puede extraer de su archivo ejecutable, pero solo si el valor FriendlyAppName no está presente. El siguiente fragmento del Registro muestra un procedimiento predeterminado de ejemplo MyProgram.exe que define un nombre descriptivo y varios elementos de menú contextual. Las cadenas de comando incluyen la marca /a para notificar a la aplicación que está abriendo un tipo de archivo arbitrario. Si incluye una subclave **DefaultIcon,** debe usar un icono genérico.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         FriendlyAppName = Friendly Name
         shell
            open
               command
                  (Default) = C:\MyDir\MyProgram.exe /a "%1"
            print
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
            printto
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2" %3 %4
```

## <a name="extending-the-new-submenu"></a>Extender el nuevo submenú

Cuando un usuario abre el **menú** Archivo en Windows Explorer, el primer comando es **Nuevo.** Al seleccionar este comando se muestra un submenú. De forma predeterminada, contiene dos comandos, **Carpeta** y **Acceso** directo, que permiten a los usuarios crear subcarpetas y accesos directos. Este submenú se puede extender para incluir comandos de creación de archivos para cualquier tipo de archivo.

Para agregar un comando de creación de archivos al submenú **Nuevo,** los archivos de la aplicación deben tener un tipo [de archivo](fa-file-types.md) asociado a ellos. Incluya una **subclave ShellNew** en la clave de la extensión de nombre de archivo. Cuando **se selecciona** el comando **Nuevo** del menú Archivo, el Shell lo agregará al **submenú** Nuevo. La cadena de presentación del comando será la cadena descriptiva que se asigna al ProgID del programa.

Asigne uno o varios valores de datos a la subclave **ShellNew** para especificar el método de creación de archivos. A continuación se encuentran los valores disponibles.



| Valor    | Descripción                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando  | Ejecuta una aplicación. Se trata de **un valor \_ REG SZ** que especifica la ruta de acceso de la aplicación que se va a ejecutar. Por ejemplo, podría establecerlo para iniciar un asistente. |
| Datos     | Crea un archivo que contiene los datos especificados. Data es un **valor REG \_ BINARY** con los datos del archivo. Los datos se omiten si se especifica NullFile o FileName.  |
| FileName | Crea un archivo que es una copia de un archivo especificado. FileName es un **valor \_ REG SZ,** establecido en la ruta de acceso completa del archivo que se va a copiar.                 |
| NullFile | Crea un archivo vacío. No se asigna un valor a NullFile. Si se especifica NullFile, se omiten los valores Data y FileName.                                  |



 

En la ilustración siguiente se muestra el submenú **Nuevo** [](fa-file-types.md) para el tipo de archivo .myp usado como ejemplo en Tipos de archivo e [Iconos de personalización](icon.md). Ahora tiene un comando, **MyProgram Application**. Cuando un usuario selecciona **MyProgram Application** en el **submenú** New (Nuevo), shell crea un archivo denominado "New MyProgram Application.myp" (Nueva aplicación MyPrograma.myp) y lo pasa a MyProgram.exe.

![captura de pantalla del nuevo menú personalizado](images/context5.png)

La entrada del Registro ahora es la siguiente:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
            NullFile
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



