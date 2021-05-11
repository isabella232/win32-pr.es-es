---
description: Los controladores de menús contextuales, también conocidos como controladores de menú contextual o controladores de verbos, son un tipo de controlador de tipo de archivo. Al igual que todos estos controladores, son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Crear controladores de menús contextuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e102833453566f42d058ff82061f34ebc65691
ms.sourcegitcommit: 9655f82be96b11258276fdefff14423c30552fbb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/11/2021
ms.locfileid: "109740576"
---
# <a name="creating-shortcut-menu-handlers"></a>Crear controladores de menús contextuales

Los controladores de menús contextuales, también conocidos como controladores de menú contextual o controladores de verbos, son un tipo de controlador de tipo de archivo. Estos controladores se pueden impelenciar de forma que se carguen en su propio proceso, en el explorador o en otros procesos de terceros. Al crear controladores en proceso, debe tener cuidado, ya que pueden causar daños en el proceso que los carga.

> [!Note]  
> Hay consideraciones especiales para las versiones de Windows basadas en 64 bits al registrar controladores que funcionan en el contexto de aplicaciones de 32 bits: cuando se invoca en el contexto de una aplicación de bits diferente, el subsistema WOW64 redirige el acceso del sistema de archivos a algunas rutas de acceso. Si el controlador .exe se almacena en una de esas rutas de acceso, no es accesible en este contexto. Por lo tanto, para evitarlo, almacene el archivo .exe en una ruta de acceso que no se redirija o almacene una versión de código auxiliar de .exe que inicie la versión real.

Este tema se organiza de la siguiente manera:

-   [Verbos canónicos](#canonical-verbs)
-   [Verbos extendidos](#extended-verbs)
-   [Verbos de solo acceso mediante programación](#programmaticaccessonly-verbs)
-   [Personalizar un menú contextual mediante verbos estáticos](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Activación del controlador mediante la interfaz IDropTarget](#activating-your-handler-using-the-idroptarget-interface)
    -   [Especificar la posición y el orden de los verbos estáticos](#specifying-the-position-and-order-of-static-verbs)
    -   [Colocar verbos en la parte superior o inferior del menú](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Crear menús estáticos en cascada](#creating-static-cascading-menus)
    -   [Obtención del comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [En desuso: asociación de verbos Intercambio dinámico de datos comandos](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Completar tareas de implementación de verbos](#completing-verb-implementation-tasks)
    -   [Personalización del menú contextual para objetos de shell predefinidos](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Extender un nuevo submenú](#extending-a-new-submenu)
    -   [Suprimir verbos y controlar la visibilidad](#suppressing-verbs-and-controlling-visibility)
    -   [Empleo del modelo de selección de verbos](#employing-the-verb-selection-model)
    -   [Usar atributos de elemento](#using-item-attributes)
    -   [Implementar verbos personalizados para carpetas mediante Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Temas relacionados](#related-topics)

## <a name="canonical-verbs"></a>Verbos canónicos

Las aplicaciones suelen ser responsables de proporcionar cadenas de presentación localizadas para los verbos que definen. Sin embargo, para proporcionar un grado de independencia del lenguaje, el sistema define un conjunto estándar de verbos de uso común denominados verbos canónicos. Un verbo canónico nunca se muestra al usuario y se puede usar con cualquier lenguaje de interfaz de usuario. El sistema usa el nombre canónico para generar automáticamente una cadena de presentación localizada correctamente. Por ejemplo, la cadena de presentación del verbo abierto se establece en **Abrir** en un sistema en inglés y en el equivalente en alemán en un sistema alemán.


| Verbo canónico | Descripción                                                          |
|----------------|----------------------------------------------------------------------|
| Abrir           | Abre el archivo o la carpeta.                                            |
| Abrirnuevo        | Abre el archivo o la carpeta en una nueva ventana.                            |
| Impresión          | Imprime el archivo.                                                     |
| Printto        | Permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora. |
| Explorar        | Abre Explorador de Windows con la carpeta seleccionada.                     |
| Propiedades     | Abre la hoja de propiedades del objeto.                                   |

> [!Note]  
> El **verbo Printto** también es canónico, pero nunca se muestra. Su inclusión permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.

Los controladores de menús contextuales pueden proporcionar sus propios verbos canónicos a través de [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **\_ GCS VERBW** o **\_ GCS VERBA**. El sistema usará los verbos canónicos como segundo parámetro (*lpOperation*) pasado a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)y [**es CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **Miembro lpVerb** pasado al [**método IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)

## <a name="extended-verbs"></a>Verbos extendidos

Cuando el usuario hace clic con el botón derecho en un objeto, el menú contextual muestra los verbos predeterminados. Es posible que quiera agregar y admitir comandos en algunos menús contextuales que no se muestran en todos los menús contextuales. Por ejemplo, podría tener comandos que no se usan normalmente o que están destinados a usuarios experimentados. Por esta razón, también puede definir uno o varios verbos extendidos. Estos verbos son similares a los verbos normales, pero se distinguen de los verbos normales por la forma en que se registran. Para tener acceso a verbos extendidos, el usuario debe hacer clic con el botón derecho en un objeto mientras presiona la tecla MAYÚS. Cuando el usuario lo hace, se muestran los verbos extendidos además de los verbos predeterminados.

Puede usar el Registro para definir uno o varios verbos extendidos. Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras también presiona la tecla MAYÚS. Para definir un verbo como extendido, agregue un valor **REG \_ SZ** "extendido" a la subclave del verbo. El valor no debe tener ningún dato asociado.

## <a name="programmatic-access-only"></a>Solo acceso mediante programación

Estos verbos nunca se muestran en un menú contextual. Se puede acceder a ellos mediante [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) y especificando el **campo lpVerb** del *parámetro pExecInfo* (un [objeto SHELLEXECUTEINFO).](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) Para definir un verbo solo como acceso mediante programación, agregue un valor **REG \_ SZ** "ProgrammaticAccessOnly" a la subclave del verbo. El valor no debe tener ningún dato asociado.

Puede usar el Registro para definir uno o varios verbos extendidos. Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras también presiona la tecla MAYÚS. Para definir un verbo como extendido, agregue un valor **REG \_ SZ** "extendido" a la subclave del verbo. El valor no debe tener ningún dato asociado.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Personalizar un menú contextual mediante verbos estáticos

Después [de elegir un verbo](shortcut-choose-method.md) estático o dinámico para el menú contextual, puede ampliar el menú contextual de un tipo de archivo registrando un verbo estático para el tipo de archivo. Para ello, agregue una **subclave shell** debajo de la subclave para el ProgID de la aplicación asociada al tipo de archivo. Opcionalmente, puede definir un verbo predeterminado para el tipo de archivo si lo hace el valor predeterminado de la **subclave shell.**

El verbo predeterminado se muestra primero en el menú contextual. Su propósito es proporcionar al Shell un verbo que puede usar cuando se llama a la función [**ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pero no se especifica ningún verbo. El shell no selecciona necesariamente el verbo predeterminado cuando se usa **ShellExecuteEx** de esta manera.

El Shell usa el primer verbo disponible en el orden siguiente:

1.  Verbo predeterminado
2.  Primer verbo del Registro, si se especifica el orden verbal
3.  Verbo  abierto
4.  Verbo **Abrir con**

Si ninguno de los verbos enumerados está disponible, se produce un error en la operación.

Cree una subclave para cada verbo que quiera agregar en la subclave Shell. Cada una de estas subclaves debe tener un **valor REG \_ SZ** establecido en la cadena de presentación del verbo (cadena localizada). Para cada subclave de verbo, cree una subclave de comando con el valor predeterminado establecido en la línea de comandos para activar los elementos. Para verbos canónicos, como **Abrir** e Imprimir **,** puede omitir la cadena de presentación porque el sistema muestra automáticamente una cadena localizada correctamente. En el caso de los verbos no éticos, si omite la cadena para mostrar, se muestra la cadena de verbo.

En el siguiente ejemplo del Registro, tenga en cuenta que:

-   Dado **que Doit** no es un verbo canónico, se le asigna un nombre para mostrar, que se puede seleccionar presionando la tecla D.
-   El **verbo Printto** no aparece en el menú contextual. Sin embargo, su inclusión en el Registro permite al usuario imprimir archivos al colocarlos en un icono de impresora.
-   Se muestra una subclave para cada verbo. **%1 representa** el nombre de archivo y **%2 el** nombre de impresora.

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

En el diagrama siguiente se muestra la extensión del menú contextual de acuerdo con las entradas del Registro anteriores. Este menú contextual tiene los  **verbos** **Abrir,** Hacerlo e Imprimir en su menú, con Do **It (Hacerlo)** como verbo predeterminado.

![captura de pantalla del menú contextual del verbo predeterminado](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Activación del controlador mediante la interfaz IDropTarget

Intercambio dinámico de datos (DDE) está en desuso; use [**IDropTarget en**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) su lugar. **IDropTarget** es más sólido y tiene una mejor compatibilidad con la activación porque usa la activación COM del controlador. En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y [**CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la función [**SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) Esto es más sencillo y no pierde la información del espacio de nombres, como ocurre cuando el elemento se convierte en una ruta de acceso para los protocolos DDE o de línea de comandos.

Para obtener más información sobre [**las consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y Shell para los atributos de asociación de archivos, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Especificar la posición y el orden de los verbos estáticos

Normalmente, los verbos se ordenan en un menú contextual en función de cómo se enumeran; La enumeración se basa primero en el orden de la matriz de asociación y, a continuación, en el orden de los elementos de la matriz de asociación, tal y como se define en el criterio de ordenación del registro.

Los verbos se pueden ordenar especificando el valor predeterminado de la subclave Shell para la entrada de asociación. Este valor predeterminado puede incluir un solo elemento, que se mostrará en la posición superior del menú contextual, o una lista de elementos separados por espacios o comas. En el último caso, el primer elemento de la lista es el elemento predeterminado y los demás verbos se muestran inmediatamente debajo de él en el orden especificado.

Por ejemplo, la siguiente entrada del Registro genera verbos de menú contextual en el orden siguiente:

1.  Mostrar
2.  Gadgets
3.  Personalización

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

De forma similar, la siguiente entrada del Registro genera verbos de menú contextual en el orden siguiente:

1.  Personalización
2.  Gadgets
3.  Mostrar

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Colocar verbos en la parte superior o inferior del menú

El siguiente atributo del Registro se puede usar para colocar un verbo en la parte superior o inferior del menú. Si hay varios verbos que especifican este atributo, el último en hacerlo obtiene prioridad:

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Crear menús estáticos en cascada

En Windows 7 y versiones posteriores, la implementación del menú en cascada se admite a través de la configuración del Registro. Antes de Windows 7, la creación de menús en cascada solo era posible mediante la implementación de la [**interfaz IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) En Windows 7 y versiones posteriores, debe recurrir a soluciones basadas en código COM solo cuando los métodos estáticos no son suficientes.

La siguiente captura de pantalla proporciona un ejemplo de un menú en cascada.

![captura de pantalla que muestra un ejemplo de un menú en cascada](images/file-assoc/filecascademenu2ndex.png)

En Windows 7 y versiones posteriores, hay tres maneras de crear menús en cascada:

-   [Crear menús en cascada con la entrada del Registro SubCommands](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Crear menús en cascada con la entrada del Registro ExtendedSubCommandsKey](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Crear menús en cascada con la interfaz IExplorerCommand](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Crear menús en cascada con la entrada del Registro SubCommands

En Windows 7 y versiones posteriores, puede usar la entrada SubCommands para crear menús en cascada mediante el procedimiento siguiente.

**Para crear un menú en cascada mediante la entrada SubCommands**

1.  Cree una subclave en el shell **de ProgID \_ \_ raíz de HKEY CLASSES** para representar el menú en \\  \\  cascada. En este ejemplo, se le da a esta subclave el nombre *CascadeTest.* Asegúrese de que el valor predeterminado de la subclave *CascadeTest* está vacío y se muestra como **(valor no establecido).**

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  A la subclave *CascadeTest,* agregue una entrada DE TIPO MUIVerb de tipo **REG \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual. En este ejemplo, le asignamos "Test Cascade Menu".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  A la subclave *CascadeTest,* agregue una entrada SubCommands de tipo **REG \_ SZ** que esté asignada a la lista, delimitada por puntos y coma, de los verbos que deben aparecer en el menú, en el orden de apariencia. Por ejemplo, aquí asignamos una serie de verbos proporcionados por el sistema:

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  En el caso de verbos personalizados, implemente con cualquiera de los métodos de implementación de verbo estático y enumérrelos en la subclave **CommandStore** como se muestra en este ejemplo para un *verbo ficticio VerbName*:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> Este método tiene la ventaja de que los verbos personalizados se pueden registrar una vez y reutilizarse enumerando el nombre del verbo en la entrada SubCommands. Sin embargo, requiere que la aplicación tenga permiso para modificar el Registro en **HKEY \_ LOCAL \_ MACHINE**.

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Crear menús en cascada con la entrada del Registro ExtendedSubCommandsKey

En Windows 7 y versiones posteriores, puede usar la entrada ExtendedSubCommandKey para crear menús en cascada extendidos: menús en cascada dentro de menús en cascada.

La siguiente captura de pantalla es un ejemplo de un menú en cascada extendido.

![captura de pantalla que muestra el menú en cascada extendido para dispositivos](images/file-assoc/extendedsubcommandskey.png)

Dado **que HKEY \_ CLASSES ROOT \_ es** una combinación de **HKEY CURRENT \_ \_ USER** y **HKEY LOCAL \_ \_ MACHINE,** puede registrar los verbos personalizados en la subclave clases de software **HKEY CURRENT \_ \_ USER.** \\  \\  La principal ventaja de hacerlo es que no se requiere el permiso con privilegios elevados. Además, otras asociaciones de archivo pueden reutilizar todo este conjunto de verbos especificando la misma subclave ExtendedSubCommandsKey. Si no necesita volver a usar este conjunto de verbos, puede enumerar los verbos bajo el elemento primario, pero asegúrese de que el valor Predeterminado del elemento primario está vacío.

**Para crear un menú en cascada mediante una entrada ExtendedSubCommandsKey**

1.  Cree una subclave en el shell **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\  para representar el menú en cascada. En este ejemplo, se le da a esta subclave el nombre *CascadeTest2.* Asegúrese de que el valor predeterminado de la subclave *CascadeTest* está vacío y se muestra **como (valor no establecido).**

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  A la subclave *CascadeTest,* agregue una entrada DE TIPO INVERB de tipo **REG \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual. En este ejemplo, le asignamos "Test Cascade Menu".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  En la subclave *CascadeTest* que ha creado, agregue una subclave **ExtendedSubCommandsKey** y, a continuación, agregue los subcomandos del documento (del tipo **REG \_ SZ);** por ejemplo:

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    Asegúrese de que el valor predeterminado de la subclave *Test Cascade Menu 2* está vacío y se muestra **como (valor no establecido).**

4.  Rellene las subverberas mediante cualquiera de las siguientes implementaciones de verbo estático. Tenga en cuenta que la subclave CommandFlags representa valores EXPCMDFLAGS. Si desea agregar un separador antes o después del elemento de menú en cascada, use ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40). Para obtener una descripción de estas marcas de Windows 7 y versiones posteriores, vea [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE solo funciona para los elementos de menú de nivel superior. MUIVerb es de tipo **REG \_ SZ** y CommandFlags es de tipo **REG \_ DWORD.**

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

La siguiente captura de pantalla es una ilustración de los ejemplos de entrada de clave del Registro anteriores.

![captura de pantalla que muestra un ejemplo de un menú en cascada que muestra las opciones del Bloc de notas y el Bloc de palabras](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Crear menús en cascada con la interfaz IExplorerCommand

Otra opción para agregar verbos a un menú en cascada es a través de [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Este método permite que los orígenes de datos que proporcionan sus comandos del módulo de comandos a través de [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) usen esos comandos como verbos en un menú contextual. En Windows 7 y versiones posteriores, puede proporcionar la misma implementación de verbo mediante [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) que con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).

Las dos capturas de pantalla siguientes muestran el uso de menús en cascada en la **carpeta Dispositivos.**

![Captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta devices.](images/file-assoc/filecascademenu.png)

En la siguiente captura de pantalla se muestra otra implementación de un menú en cascada en la **carpeta Dispositivos.**

![captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta devices](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Dado [**que IExplorerCommand solo**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) admite la activación en proceso, se recomienda su uso por parte de orígenes de datos de Shell que necesitan compartir la implementación entre comandos y menús contextuales.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Obtención del comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada

La sintaxis de consulta avanzada (AQS) puede expresar una condición que se evaluará mediante las propiedades del elemento para el que se crea una instancia del verbo. Este sistema solo funciona con propiedades rápidas. Estas son propiedades que el origen de datos del shell notifica como rápidas al no devolver [*:SHCOLSTATE \_ SLOW*"](/windows/win32/api/shtypes/ne-shtypes-shcolstate) desde [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).

Windows 7 y versiones posteriores admiten valores canónicos que evitan problemas en las compilaciones localizadas. La siguiente sintaxis canónica es necesaria en las compilaciones localizadas para aprovechar esta mejora de Windows 7.

``` syntax
System.StructuredQueryType.Boolean#True
```

En la siguiente entrada del Registro de ejemplo:

-   El **valor AppliesTo** controla si el verbo se muestra u oculta.
-   El valor DefaultAppliesTo controla qué verbo es el predeterminado.
-   El valor HasLUAShield controla si se muestra un escudo de control de cuentas de usuario (UAC).

En este ejemplo, **el valor DefaultAppliesTo** convierte este verbo en el valor predeterminado para cualquier archivo con la palabra "exampleText1" en su nombre de archivo. El **valor AppliesTo** habilita el verbo para cualquier archivo con "exampleText1" en el nombre. El **valor HasLUAShield** muestra el escudo de los archivos con "exampleText2" en el nombre.

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Agregue **la** subclave Command y un valor:

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

En el Registro de Windows 7, vea HKEY CLASSES ROOT drive (Unidad RAÍZ **HKEY \_ CLASSES) \_** como ejemplo de \\  verbos de BitLocker que emplean el enfoque siguiente:

-   AppliesTo = System.Volume.BitlockerProtection:=2
-   System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True

Para obtener más información sobre AQS, vea [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>En desuso: asociación de verbos Intercambio dinámico de datos comandos

DDE está en desuso; use [**IDropTarget en su**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) lugar. DDE está en desuso porque se basa en un mensaje de ventana de difusión para detectar el servidor DDE. Un servidor DDE detiene el mensaje de la ventana de difusión y, por tanto, se detienen las conversaciones de DDE para otras aplicaciones. Es habitual que una sola aplicación bloqueada cause errores posteriores en toda la experiencia del usuario.

El [**método IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) es más sólido y tiene una mejor compatibilidad con la activación porque usa la activación COM del controlador. En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y [**CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la función [**SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) Esto es más sencillo y no pierde la información del espacio de nombres como ocurre cuando el elemento se convierte en una ruta de acceso para los protocolos DDE o de línea de comandos.

Para obtener más información sobre [**las consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y Shell para los atributos de asociación de archivos, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).

## <a name="completing-verb-implementation-tasks"></a>Completar tareas de implementación de verbos

Las siguientes tareas para implementar verbos son relevantes para las implementaciones de verbos estáticos y dinámicos. Para obtener más información sobre verbos dinámicos, vea [Personalizar un menú contextual mediante verbos dinámicos.](shortcut-menu-using-dynamic-verbs.md)

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Personalizar el menú contextual para objetos de shell predefinidos

Muchos objetos predefinidos de Shell tienen menús contextuales que se pueden personalizar. Registre el comando de la misma manera que registra los tipos de archivo típicos, pero use el nombre del objeto predefinido como nombre del tipo de archivo.

Una lista de objetos predefinidos se encuentra en la *sección Objetos de shell* [predefinidos](handlers.md)de Crear controladores de extensión de shell . Los objetos de Shell predefinidos cuyos menús contextuales se pueden personalizar agregando verbos en el Registro se marcan en la tabla con la palabra Verbo.

### <a name="extending-a-new-submenu"></a>Extensión de un submenú nuevo

Cuando un usuario abre el **menú** Archivo Explorador de Windows, uno de los comandos que se muestran es **Nuevo.** Al seleccionar este comando se muestra un submenú. De forma predeterminada, el submenú contiene dos comandos, **Carpeta** y **Acceso** directo, que permiten a los usuarios crear subcarpetas y accesos directos. Este submenú se puede extender para incluir comandos de creación de archivos para cualquier tipo de archivo.

Para agregar un comando de creación de archivos al submenú **Nuevo,** los archivos de la aplicación deben tener un tipo de archivo asociado. Incluya una **subclave ShellNew** en el nombre de archivo. Cuando se **selecciona** el comando **Nuevo** del menú Archivo, shell agrega el tipo de archivo al submenú **Nuevo.** La cadena para mostrar del comando es la cadena descriptiva que se asigna al ProgID del programa.

Para especificar el método de creación de archivos, asigne uno o varios valores de datos a la **subclave ShellNew.** Los valores disponibles se muestran en la tabla siguiente.



| ShellNuevo valor de subclave | Descripción                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando               | Ejecuta una aplicación. Este **valor DE REG \_ SZ** especifica la ruta de acceso de la aplicación que se va a ejecutar. Por ejemplo, podría establecerlo para iniciar un asistente.                  |
| data                  | Crea un archivo que contiene los datos especificados. Este **valor \_ REG BINARY** especifica los datos del archivo. **Los** datos se omiten **si se especifica NullFile** o **FileName.** |
| FileName              | Crea un archivo que es una copia de un archivo especificado. Este **valor DE REG \_ SZ** especifica la ruta de acceso completa del archivo que se va a copiar.                                   |
| NullFile              | Crea un archivo vacío. **NullFile** no tiene ningún valor asignado. Si **se especifica NullFile,** se omiten los valores del Registro **Data** y **FileName.**                    |



 

El siguiente ejemplo de clave del Registro y captura de pantalla **ilustran** el submenú Nuevo para el tipo de archivo .myp-ms. Tiene un comando, **MyProgram Application**.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

La captura de pantalla muestra el **submenú Nuevo.** Cuando un usuario selecciona **MyProgram Application** en el **submenú** New (Nuevo), el shell crea un archivo denominado New **MyProgram Application.myp-ms** y lo pasa a **MyProgram.exe**.

![captura de pantalla del Explorador de Windows que muestra un nuevo comando "myprogram application" en el submenú "new"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Crear controladores de arrastrar y colocar

El procedimiento básico para implementar un controlador de arrastrar y colocar es el mismo que para los controladores de menús contextuales convencionales. Sin embargo, los controladores de menús contextuales normalmente solo usan el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pasado al método [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del controlador para extraer el nombre del objeto. Un controlador de arrastrar y colocar podría implementar un controlador de datos más sofisticado para modificar el comportamiento del objeto arrastrado.

Cuando un usuario hace clic con el botón derecho en un objeto shell para arrastrar un objeto, se muestra un menú contextual cuando el usuario intenta colocar el objeto. En la siguiente captura de pantalla se muestra un menú contextual típico de arrastrar y colocar.

![captura de pantalla del menú contextual de arrastrar y colocar](images/context-menu/context-dragdrop.png)

Un controlador de arrastrar y colocar es un controlador de menú contextual que puede agregar elementos a este menú contextual. Los controladores de arrastrar y colocar normalmente se registran en la subclave siguiente.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Agregue una subclave bajo la subclave **DragDropHandlers** denominada para el controlador de arrastrar y colocar y establezca el valor predeterminado de la subclave en el formato de cadena del GUID del identificador de clase (CLSID) del controlador. En el ejemplo siguiente se habilita el controlador de arrastrar y colocar **De MyDD.**

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Suprimir verbos y controlar la visibilidad

Puede usar la configuración de directivas de Windows para controlar la visibilidad de verbos. Los verbos se pueden suprimir mediante la configuración de directiva agregando un valor **SuppressionPolicy** o un valor **GUID SuppressionPolicyEx** a la subclave del Registro del verbo. Establezca el valor de la **subclave SuppressionPolicy** en el identificador de directiva. Si la directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada. Para ver los posibles valores de identificador de directiva, consulte la [**enumeración RESTRICTIONS.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)

### <a name="employing-the-verb-selection-model"></a>Empleo del modelo de selección de verbos

Los valores del Registro deben establecerse para que los verbos controle situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento. Un verbo requiere valores del Registro independientes para cada una de estas tres situaciones que admite el verbo. Los valores posibles para el modelo de selección de verbos son los siguientes:

-   Especifique el valor MultiSelectModel para todos los verbos. Si no se especifica el valor MultiSelectModel, se deduce del tipo de implementación de verbo que ha elegido. En el caso de los métodos basados en COM (como DropTarget y **ExecuteCommand),** se da por supuesto el reproductor y, para los demás métodos, se supone que **Document.**
-   Especifique **Single** para los verbos que solo admiten una selección única.
-   Especifique **Player** para los verbos que admiten cualquier número de elementos.
-   Especifique **Documento** para los verbos que crean una ventana de nivel superior para cada elemento. Esto limita el número de elementos activados y ayuda a evitar que se quedándose sin recursos del sistema si el usuario abre demasiadas ventanas.

Cuando el número de elementos seleccionados no coincide con el modelo de selección de verbos o es mayor que los límites predeterminados descritos en la tabla siguiente, el verbo no aparece.



| Tipo de implementación de verbo | Documento | Reproductor    |
|-----------------------------|----------|-----------|
| Heredado                      | 15 elementos | 100 elementos |
| COM                         | 15 elementos | Sin límite  |



 

A continuación se incluyen entradas del Registro de ejemplo que usan el valor MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a>Usar atributos de elemento

Los [**valores de marca SFGAO**](sfgao.md) de los atributos de Shell de un elemento se pueden probar para determinar si el verbo debe habilitarse o deshabilitarse.

Para usar esta característica de atributo, agregue los siguientes valores **REG \_ DWORD** en el verbo :

-   El valor attributeMask especifica el valor [**SFGAO**](sfgao.md) de los valores de bits de la máscara con la que se probará.
-   El valor AttributeValue especifica el valor [**SFGAO**](sfgao.md) de los bits que se prueban.
-   ImpliedSelectionModel especifica cero para verbos de elemento o distinto de cero para verbos en el menú contextual de fondo.

En la siguiente entrada del Registro de ejemplo, AttributeMask se establece en [**SFGAO \_ READONLY**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>Implementar verbos personalizados para carpetas mediante Desktop.ini

En Windows 7 y versiones posteriores, puede agregar verbos a una carpeta mediante Desktop.ini. Para obtener más información sobre Desktop.ini, [vea How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini archivos deben marcarse siempre como **Sistema** oculto para que no se  +   muestren a los usuarios.

 

**Para agregar verbos personalizados para carpetas a través de Desktop.ini archivo, realice los pasos siguientes:**

1.  Cree una carpeta que esté marcada como **De solo lectura** o **Sistema.**
2.  Cree un Desktop.ini que incluya un \[ . ShellClassInfo \] DirectoryClass=Folder ProgID.
3.  En el Registro, **cree HKEY \_ CLASSES \_ ROOT** \\ **Folder ProgID** con un valor de CanUseForDirectory. El valor CanUseForDirectory evita el uso indebido de ProgID que se establecen para no participar en la implementación de verbos personalizados para carpetas a través de Desktop.ini.
4.  Agregue verbos en la subclave **Folder** ProgID ( ProgID de carpeta), por ejemplo:

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Estos verbos pueden ser el verbo predeterminado, en cuyo caso hacer doble clic en la carpeta activa el verbo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados para controladores de menús contextuales y verbos de selección múltiple](verbs-best-practices.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Personalizar un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menús contextuales](context-menu.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 
