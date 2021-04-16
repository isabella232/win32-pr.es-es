---
description: Al hacer clic con el botón secundario en un objeto, normalmente se muestra un menú contextual. Este menú contiene una lista de comandos que el usuario puede seleccionar para realizar diversas acciones en el objeto. Esta sección es una introducción a los menús contextuales para los objetos del sistema de archivos.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Extender menús contextuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895550ff050d559b3523676ddaa2a58099398a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563195"
---
# <a name="extending-shortcut-menus"></a>Extender menús contextuales

Al hacer clic con el botón secundario en un objeto, normalmente se muestra un *menú contextual*. Este menú contiene una lista de comandos que el usuario puede seleccionar para realizar diversas acciones en el objeto. Esta sección es una introducción a los menús contextuales para los objetos del sistema de archivos.

-   [Menús contextuales para objetos del sistema de archivos](#shortcut-menus-for-file-system-objects)
-   [Verbos del menú contextual](#shortcut-menu-verbs)
    -   [Verbos canónicos](#canonical-verbs)
    -   [Verbos extendidos](#extended-verbs)
-   [Extender el menú contextual para un tipo de archivo](#extending-the-shortcut-menu-for-a-file-type)
-   [Extender el menú contextual para objetos de Shell predefinidos](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Registro de una aplicación para controlar tipos de archivo arbitrarios](#registering-an-application-to-handle-arbitrary-file-types)
-   [Extender el nuevo submenú](#extending-the-new-submenu)

Aquí encontrará información adicional:

-   [Cómo definir verbos extendidos](how-to-define-extended-verbs.md)
-   [Cómo asociar verbos con comandos DDE](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Menús contextuales para objetos del sistema de archivos

Cuando un usuario hace clic con el botón secundario en un objeto, como un archivo, que se muestra en el explorador de Windows o en el escritorio, aparece un menú contextual con una lista de comandos. El usuario puede realizar una acción en el archivo, como abrirlo o eliminarlo, seleccionando el comando adecuado.

Dado que los menús contextuales suelen usarse para la administración de archivos, el Shell proporciona un conjunto de comandos predeterminados, como cortar y copiar, que aparecen en el menú contextual de cualquier archivo. Tenga en cuenta que aunque abrir con es un comando predeterminado, no se muestra para algunos tipos de archivo estándar, como. wav. La siguiente ilustración del directorio mis documentos de ejemplo, que también se usó como ejemplo en la [Personalización de iconos](icon.md), muestra un menú contextual predeterminado que se muestra al hacer clic con el botón secundario en MyDocs4.XYZ.

![captura de pantalla del menú contextual predeterminado para los objetos del sistema de archivos](images/context1.jpg)

La razón por la que MyDocs4.xyz muestra un menú contextual predeterminado es que no es miembro de un [tipo de archivo](fa-file-types.md)registrado. Por otro lado,. txt es un tipo de archivo registrado. Si hace clic con el botón secundario en uno de los archivos. txt, verá un menú contextual con dos comandos adicionales en la sección superior: **abrir** e **Imprimir**.

![captura de pantalla del menú contextual personalizado para objetos del sistema de archivos](images/context2.jpg)

Una vez que se registra un tipo de archivo, puede extender su menú contextual con comandos adicionales. Se muestran encima de los comandos predeterminados cuando se hace clic con el botón derecho en cualquier archivo de ese tipo. Aunque la mayoría de los comandos que se agregan de esta manera son comunes, como **Imprimir** o **abrir**, es libre de agregar cualquier comando que un usuario pueda encontrar de utilidad.

Todo lo que se necesita para extender el menú contextual de un tipo de archivo consiste en crear una entrada del registro para cada comando. Un enfoque más sofisticado consiste en implementar un *controlador de menú contextual*, que le permite extender el menú contextual de un tipo de archivo cada archivo. Para obtener más información, vea [crear controladores de menús contextuales](context-menu-handlers.md).

## <a name="shortcut-menu-verbs"></a>Verbos del menú contextual

Cada comando del menú contextual se identifica en el registro mediante su *verbo*. Estos verbos son los mismos que los utilizados por [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) al iniciar aplicaciones mediante programación. Para obtener más información sobre el uso de **ShellExecuteEx**, vea la explicación de [Launching Applications](launch.md).

Un verbo es una cadena de texto simple que el shell usa para identificar el comando asociado. Cada verbo corresponde a la *cadena de comandos* que se usa para iniciar el comando en una ventana de la consola o en un archivo por lotes (. bat). Por ejemplo, el verbo **abrir** normalmente inicia un programa para abrir un archivo. Normalmente, su cadena de comandos tiene un aspecto similar al siguiente:

``` syntax
"My Program.exe" "%1"
```

"%1" es el marcador de posición estándar para un parámetro de línea de comandos proporcionado con el nombre de archivo. Por ejemplo, puede especificar que se muestre una página determinada en una vista con pestañas.

> [!Note]  
> Si algún elemento de la cadena de comandos contiene o puede contener espacios, debe escribirse entre comillas. De lo contrario, si el elemento contiene un espacio, no se analizará correctamente. Por ejemplo, "My Program.exe" iniciará la aplicación correctamente. Si usa mi Program.exe, el sistema intentará iniciar "My" con "Program.exe" como el primer argumento de la línea de comandos. Siempre debe usar comillas con argumentos como "%1" que se expandan a cadenas mediante el Shell, ya que no puede estar seguro de que la cadena no contendrá un espacio.

 

Los verbos también pueden tener una *cadena de presentación* asociada, que se muestra en el menú contextual en lugar de la propia cadena de verbo. Por ejemplo, la cadena de presentación para **openas** está abierta con. Al igual que las cadenas de menú normales, incluso una y comercial (&) en la cadena de presentación permite la selección del teclado del comando.

### <a name="canonical-verbs"></a>Verbos canónicos

En general, las aplicaciones son responsables de proporcionar cadenas de presentación localizadas para los verbos que definen. Sin embargo, para proporcionar un grado de independencia de lenguaje, el sistema define un conjunto estándar de verbos usados comúnmente denominados *verbos canónicos*. Un verbo canónico se puede usar con cualquier lenguaje y el sistema genera automáticamente una cadena de presentación localizada correctamente. Por ejemplo, la cadena de presentación del verbo **abierto** se establecerá en abierto en un sistema en inglés y en öffnen en un sistema alemán.

Los verbos canónicos incluyen:



| Value      | Descripción                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| abrir       | Abre el archivo o la carpeta.                                                                   |
| opennew    | Abre el archivo o la carpeta en una nueva ventana.                                                   |
| imprimir      | Imprime el archivo.                                                                            |
| explore    | Abre el explorador de Windows con la carpeta seleccionada.                                            |
| find       | Abre el cuadro de diálogo de **búsqueda de Windows** con la carpeta establecida como ubicación de búsqueda predeterminada. |
| abriras     | Abre el cuadro **de diálogo Abrir con** .                                                         |
| properties | Abre la hoja de propiedades del objeto.                                                          |



 

El verbo printto también es canónico, pero nunca se muestra. Permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.

### <a name="extended-verbs"></a>Verbos extendidos

Cuando el usuario hace clic con el botón secundario en un objeto, el menú contextual contiene todos los verbos normales. Sin embargo, podría haber comandos que desee admitir pero que no se hayan mostrado en cada menú contextual. Por ejemplo, podría tener comandos que no se usan habitualmente o que están destinados a usuarios con experiencia. Por esta razón, también puede definir uno o más *verbos extendidos*. Estos verbos también son cadenas de caracteres y son similares a los verbos normales. Se distinguen de los verbos normales por la forma en que se registran. Para tener acceso a los comandos asociados a los verbos extendidos, el usuario debe hacer clic con el botón derecho en un objeto mientras presiona la tecla Mayús. Los verbos extendidos se mostrarán junto con los verbos normales.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Extender el menú contextual para un tipo de archivo

La manera más sencilla de extender el menú contextual para un tipo de archivo es con el registro. Para ello, agregue una subclave de **Shell** debajo de la clave para el ProgID de la aplicación asociada con el [tipo de archivo](fa-file-types.md). Opcionalmente, puede definir un *verbo predeterminado* para el tipo de archivo convirtiéndolo en el valor predeterminado de la subclave del **Shell** .

En primer lugar, se muestra el verbo predeterminado en el menú contextual. Su finalidad es proporcionar el shell con un verbo que se puede usar cuando se llama a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pero no se especifica ningún verbo. El shell no selecciona necesariamente el verbo predeterminado cuando se usa **ShellExecuteEx** de este modo. En el caso de [las versiones](versions.md) de Shell 5,0 y posteriores, que se encuentran en los sistemas Windows 2000 y versiones posteriores, el shell usa el primer verbo disponible de la lista siguiente. Si no hay ninguno disponible, se produce un error en la operación.

-   El verbo Open
-   El verbo predeterminado
-   Primer verbo del registro
-   El verbo OpenWith

En el caso de las versiones de Shell anteriores a la [versión 5,0](versions.md), omita el tercer elemento.

Debajo de la subclave del **Shell** , cree una subclave para cada verbo que desee agregar. Cada una de estas subclaves tendrá un valor de **reg \_ SZ** establecido en la cadena de presentación del verbo. Puede omitir la cadena de presentación para verbos canónicos, ya que el sistema mostrará automáticamente una cadena localizada correctamente. Si omite la cadena de presentación para verbos no canónicos, se mostrará la cadena de verbo. Para cada subclave de verbo, cree una subclave de **comando** con el valor predeterminado establecido en la cadena de comando.

En la ilustración siguiente se muestra un menú contextual para el tipo de archivo. MYP que se usa en los [tipos de archivo](fa-file-types.md) y la [Personalización de iconos](icon.md). Ahora tiene los verbos Open, doit, Print e printto en el menú contextual, con doit como el verbo predeterminado. El menú contextual tiene el siguiente aspecto.

![captura de pantalla del menú contextual personalizado](images/context3.jpg)

Las entradas del registro que se usan para extender el menú contextual que se muestra en la ilustración anterior son:

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

Aunque el comando **abrir con** está por encima del primer separador, el sistema lo crea automáticamente y no requiere una entrada del registro. El sistema crea automáticamente nombres para mostrar para los verbos canónicos abrir e imprimir. Dado que doit no es un verbo canónico, se le asigna un nombre para mostrar, "&hacerlo", que se puede seleccionar presionando la tecla D. El verbo printto no aparece en el menú contextual, pero la inclusión permite al usuario imprimir archivos colocándolos en un icono de impresora. En este ejemplo, %1 representa el nombre de archivo y %2 el nombre de la impresora.

Los verbos se pueden suprimir a través de la configuración de la Directiva agregando un valor de SuppressionPolicy a la clave del verbo. Establezca el valor de SuppressionPolicy en el identificador de la Directiva. Si la Directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada. Para ver los posibles valores de ID. de Directiva, consulte la enumeración [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Extender el menú contextual para objetos de Shell predefinidos

Muchos objetos de Shell predefinidos tienen menús contextuales que se pueden extender. Registre el comando de la misma manera que registra los tipos de archivo típicos, pero use el nombre del objeto predefinido como el nombre del tipo de archivo.

Puede encontrar una lista de objetos predefinidos en la sección *objetos de Shell predefinidos* de [crear controladores de extensión de Shell](handlers.md). Los objetos de Shell predefinidos cuyos menús contextuales se pueden extender agregando verbos en el registro se marcan en la tabla con la palabra "verbo".

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Registro de una aplicación para controlar tipos de archivo arbitrarios

En las secciones anteriores de este documento se ha explicado cómo definir los elementos de menú contextual para un tipo de archivo determinado. Entre otras cosas, la definición del menú contextual permite especificar el modo en que la aplicación asociada abre un miembro del tipo de archivo. Sin embargo, como se describe en [tipos de archivo](fa-file-types.md), las aplicaciones también pueden registrar un procedimiento predeterminado independiente que se utilizará cuando un usuario intente usar la aplicación para abrir un tipo de archivo que no se haya asociado a la aplicación. Este tema se describe aquí porque el procedimiento predeterminado se registra de forma muy similar a como se registran los elementos de menú contextual.

El procedimiento predeterminado sirve para dos propósitos básicos. Uno consiste en especificar cómo se debe invocar la aplicación para abrir un tipo de archivo arbitrario. Por ejemplo, podría usar una marca de línea de comandos para indicar que se está abriendo un tipo de archivo desconocido. El otro propósito es definir las distintas características de un tipo de archivo, como los elementos de menú contextual y el icono. Si un usuario asocia su aplicación con un tipo de archivo adicional, ese tipo tendrá estas características. Si el tipo de archivo adicional estaba asociado previamente a otra aplicación, estas características reemplazarán a los originales.

Para registrar el procedimiento predeterminado, coloque las mismas claves del registro que creó para el ID. de programa de la aplicación en la subclave de la aplicación de las aplicaciones **\_ \_ raíz HKEY** \\ . También puede incluir un valor de FriendlyAppName para proporcionar al sistema un nombre descriptivo para la aplicación. También se puede extraer el nombre descriptivo de la aplicación de su archivo ejecutable, pero solo si el valor de FriendlyAppName no está presente. El siguiente fragmento del registro muestra un procedimiento predeterminado de ejemplo para MyProgram.exe que define un nombre descriptivo y varios elementos de menú contextual. Las cadenas de comandos incluyen la marca/a para notificar a la aplicación que está abriendo un tipo de archivo arbitrario. Si incluye una subclave **DefaultIcon** , debe usar un icono genérico.

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

Cuando un usuario abre el menú **archivo** en el explorador de Windows, el primer comando es **nuevo**. Al seleccionar este comando se muestra un submenú. De forma predeterminada, contiene dos comandos, **carpeta** y **acceso directo**, que permiten a los usuarios crear subcarpetas y accesos directos. Este submenú se puede extender para incluir comandos de creación de archivos para cualquier tipo de archivo.

Para agregar un comando de creación de archivos al **nuevo** submenú, los archivos de la aplicación deben tener un [tipo de archivo](fa-file-types.md) asociado. Incluya una subclave **ShellNew** en la clave para la extensión de nombre de archivo. Cuando se selecciona el comando **nuevo** del menú **archivo** , el shell lo agregará al **nuevo** submenú. La cadena de presentación del comando será la cadena descriptiva que se asigna al ProgID del programa.

Asigne uno o más valores de datos a la subclave **ShellNew** para especificar el método de creación de archivos. Los valores disponibles son los siguientes.



| Value    | Descripción                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando  | Ejecuta una aplicación. Se trata de un valor de **reg \_ SZ** que especifica la ruta de acceso de la aplicación que se va a ejecutar. Por ejemplo, puede establecerlo para iniciar un asistente. |
| Datos     | Crea un archivo que contiene los datos especificados. Los datos son un valor **\_ binario de registro** con los datos del archivo. Los datos se omiten si se especifica NullFile o FileName.  |
| FileName | Crea un archivo que es una copia de un archivo especificado. FileName es un valor de **reg \_ SZ** , establecido en la ruta de acceso completa del archivo que se va a copiar.                 |
| NullFile | Crea un archivo vacío. NullFile no tiene asignado un valor. Si se especifica NullFile, se omiten los valores de los datos y del nombre de archivo.                                  |



 

En la ilustración siguiente se muestra el **nuevo** submenú para el tipo de archivo. MYP que se usa como ejemplo en [tipos de archivo](fa-file-types.md) y [personalizar iconos](icon.md). Ahora tiene un comando, una **aplicación de programa**. Cuando un usuario selecciona mi **aplicación** en el submenú **nuevo** , el shell crea un archivo denominado "New MYP Application." y lo pasa a MyProgram.exe.

![captura de pantalla del menú nuevo personalizado](images/context5.png)

La entrada del registro es ahora como sigue:

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

 

 



