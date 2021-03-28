---
description: Los controladores de menú contextual, también denominados controladores de menú contextual o de verbo, son un tipo de controlador de tipo de archivo. Como todos estos controladores, se trata de objetos de modelo de objetos componentes (COM) implementados como dll.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Crear controladores de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "103913926"
---
# <a name="creating-shortcut-menu-handlers"></a>Crear controladores de menú contextual

Los controladores de menú contextual, también denominados controladores de menú contextual o de verbo, son un tipo de controlador de tipo de archivo. Como todos estos controladores, se trata de objetos de modelo de objetos componentes (COM) implementados como dll.

> [!Note]  
> Existen consideraciones especiales para Windows de 64 bits al registrar controladores que funcionan en el contexto de las aplicaciones de 32 bits: cuando los verbos de Shell se invocan en el contexto de una aplicación de 32 bits, el subsistema WOW64 redirige el acceso del sistema de archivos a algunas rutas de acceso. Si el controlador. exe se almacena en una de esas rutas de acceso, no es accesible en este contexto. Por lo tanto, como solución alternativa, almacene el archivo. exe en una ruta de acceso que no se redirija, o bien almacene una versión de código auxiliar del archivo. exe que inicia la versión real.

 

Este tema se organiza de la siguiente manera:

-   [Verbos canónicos](#canonical-verbs)
-   [Verbos extendidos](#extended-verbs)
-   [Personalizar un menú contextual mediante verbos estáticos](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Activar el controlador mediante la interfaz IDropTarget](#activating-your-handler-using-the-idroptarget-interface)
    -   [Especificar la posición y el orden de los verbos estáticos](#specifying-the-position-and-order-of-static-verbs)
    -   [Colocar verbos en la parte superior o inferior del menú](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Crear menús en cascada estáticos](#creating-static-cascading-menus)
    -   [Obtener el comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [En desuso: asociar verbos con comandos de Intercambio dinámico de datos](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Completar tareas de implementación de verbo](#completing-verb-implementation-tasks)
    -   [Personalización del menú contextual para objetos de Shell predefinidos](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Extender un nuevo submenú](#extending-a-new-submenu)
    -   [Suprimir verbos y controlar la visibilidad](#suppressing-verbs-and-controlling-visibility)
    -   [Usar el modelo de selección de verbos](#employing-the-verb-selection-model)
    -   [Usar atributos de elemento](#using-item-attributes)
    -   [Implementar verbos personalizados para carpetas a través de Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Temas relacionados](#related-topics)

## <a name="canonical-verbs"></a>Verbos canónicos

Las aplicaciones suelen ser responsables de proporcionar cadenas de presentación localizadas para los verbos que definen. Sin embargo, para proporcionar un grado de independencia de lenguaje, el sistema define un conjunto estándar de verbos usados comúnmente denominados verbos canónicos. Un verbo canónico nunca se muestra al usuario y se puede usar con cualquier idioma de la interfaz de usuario. El sistema utiliza el nombre canónico para generar automáticamente una cadena de presentación localizada correctamente. Por ejemplo, la cadena de presentación del verbo abierto está establecida en **abierto** en un sistema en inglés y en el equivalente en alemán en un sistema alemán.



| Verbo canónico | Descripción                                                          |
|----------------|----------------------------------------------------------------------|
| Abrir           | Abre el archivo o la carpeta.                                            |
| Opennew        | Abre el archivo o la carpeta en una nueva ventana.                            |
| Impresión          | Imprime el archivo.                                                     |
| Imprimir en        | Permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora. |
| Explorar        | Abre el explorador de Windows con la carpeta seleccionada.                     |
| Propiedades     | Abre la hoja de propiedades del objeto.                                   |



 

> [!Note]  
> El verbo **printto** también es canónico, pero nunca se muestra. Su inclusión permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.

 

Los controladores de menú contextual pueden proporcionar sus propios verbos canónicos a través de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **GC \_ VERBW** o de los **catálogos globales \_**. El sistema usará los verbos canónicos como el segundo parámetro (*lpOperation*) pasado a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)y es [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). miembro **lpVerb** pasado al método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .

## <a name="extended-verbs"></a>Verbos extendidos

Cuando el usuario hace clic con el botón secundario en un objeto, el menú contextual muestra los verbos predeterminados. Es posible que desee agregar y admitir comandos en algunos menús contextuales que no se muestran en todos los menús contextuales. Por ejemplo, podría tener comandos que no se usan habitualmente o que están destinados a usuarios con experiencia. Por esta razón, también puede definir uno o más verbos extendidos. Estos verbos son similares a los verbos normales, pero se distinguen de los verbos normales por la forma en que se registran. Para tener acceso a los verbos extendidos, el usuario debe hacer clic con el botón derecho en un objeto mientras presiona la tecla Mayús. Cuando el usuario lo hace, se muestran los verbos extendidos además de los verbos predeterminados.

Puede utilizar el registro para definir uno o más verbos extendidos. Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto y presione la tecla Mayús. Para definir un verbo como extendido, agregue un valor de **reg \_ SZ** "extendido" a la subclave del verbo. El valor no debe tener ningún dato asociado.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Personalizar un menú contextual mediante verbos estáticos

Después de [elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md) , puede extender el menú contextual de un tipo de archivo registrando un verbo estático para el tipo de archivo. Para ello, agregue una subclave de **Shell** debajo de la subclave para el identificador de programa de la aplicación asociada al tipo de archivo. Opcionalmente, puede definir un verbo predeterminado para el tipo de archivo convirtiéndolo en el valor predeterminado de la subclave del **Shell** .

En primer lugar, se muestra el verbo predeterminado en el menú contextual. Su finalidad es proporcionar el shell con un verbo que se puede usar cuando se llama a la función [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) , pero no se especifica ningún verbo. El shell no selecciona necesariamente el verbo predeterminado cuando se usa **ShellExecuteEx** de este modo.

El shell usa el primer verbo disponible en el orden siguiente:

1.  El verbo predeterminado
2.  Primer verbo del registro, si se especifica el orden del verbo
3.  El verbo **Open**
4.  El verbo **Open with**

Si ninguno de los verbos enumerados está disponible, se produce un error en la operación.

Cree una subclave para cada verbo que desee agregar bajo la subclave del shell. Cada una de estas subclaves debe tener un valor de **reg \_ SZ** establecido en la cadena de presentación del verbo (cadena localizada). Para cada subclave de verbo, cree una subclave de comando con el valor predeterminado establecido en la línea de comandos para activar los elementos. En el caso de los verbos canónicos, como **abrir** e **Imprimir**, puede omitir la cadena de presentación, ya que el sistema muestra automáticamente una cadena localizada correctamente. En el caso de verbos no canónicos, si se omite la cadena de presentación, se muestra la cadena de verbo.

En el siguiente ejemplo del registro, tenga en cuenta que:

-   Dado que **doit** no es un verbo canónico, se le asigna un nombre para mostrar, que se puede seleccionar presionando la tecla D.
-   El verbo **printto** no aparece en el menú contextual. Sin embargo, su inclusión en el registro permite al usuario imprimir archivos colocándolos en un icono de impresora.
-   Se muestra una subclave para cada verbo. **%1** representa el nombre de archivo y **%2** el nombre de la impresora.

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

En el diagrama siguiente se muestra la extensión del menú contextual de acuerdo con las entradas del registro anteriores. Este menú contextual tiene los verbos **abrir**, **hacer** e **Imprimir** en su menú, con lo que lo **hace** como el verbo predeterminado.

![captura de pantalla del menú contextual del verbo predeterminado](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Activar el controlador mediante la interfaz IDropTarget

Intercambio dinámico de datos (DDE) está en desuso; en su lugar, use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . **IDropTarget** es más robusto y tiene una mejor compatibilidad con la activación porque utiliza la activación com del controlador. En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y en [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la función [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) . Hacerlo es más sencillo y no pierde información de espacio de nombres como ocurre cuando el elemento se convierte en una ruta de acceso para los protocolos de línea de comandos o DDE.

Para obtener más información sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y las consultas de Shell para los atributos de Asociación de archivos, consulte [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Especificar la posición y el orden de los verbos estáticos

Normalmente, los verbos se ordenan en un menú contextual en función de cómo se enumeran; la enumeración se basa primero en el orden de la matriz de asociación y, a continuación, en el orden de los elementos de la matriz de asociación, tal y como se define en el criterio de ordenación del registro.

Los verbos se pueden ordenar especificando el valor predeterminado de la subclave de Shell para la entrada de asociación. Este valor predeterminado puede incluir un solo elemento, que se mostrará en la parte superior del menú contextual, o una lista de elementos separados por espacios o comas. En el último caso, el primer elemento de la lista es el elemento predeterminado y los demás verbos se muestran inmediatamente debajo de él en el orden especificado.

Por ejemplo, la siguiente entrada del registro genera verbos de menú contextual en el orden siguiente:

1.  Pantalla
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

Del mismo modo, la siguiente entrada del registro genera verbos de menú contextual en el orden siguiente:

1.  Personalización
2.  Gadgets
3.  Pantalla

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Colocar verbos en la parte superior o inferior del menú

El siguiente atributo del registro se puede usar para colocar un verbo en la parte superior o inferior del menú. Si hay varios verbos que especifican este atributo, el último de ellos obtiene la prioridad:

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Crear menús en cascada estáticos

En Windows 7 y versiones posteriores, la implementación de menús en cascada se admite a través de la configuración del registro. Antes de Windows 7, la creación de menús en cascada solo era posible a través de la implementación de la interfaz [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . En Windows 7 y versiones posteriores, debe recurrir a las soluciones basadas en código COM solo cuando los métodos estáticos no sean suficientes.

La siguiente captura de pantalla proporciona un ejemplo de un menú en cascada.

![captura de pantalla que muestra un ejemplo de un menú en cascada](images/file-assoc/filecascademenu2ndex.png)

En Windows 7 y versiones posteriores, hay tres maneras de crear menús en cascada:

-   [Crear menús en cascada con la entrada del registro subcomandos](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Crear menús en cascada con la entrada del registro ExtendedSubCommandsKey](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Crear menús en cascada con la interfaz IExplorerCommand](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Crear menús en cascada con la entrada del registro subcomandos

En Windows 7 y versiones posteriores, puede usar la entrada subcomandos para crear menús en cascada mediante el procedimiento siguiente.

**Para crear un menú en cascada mediante la entrada subcomandos**

1.  Cree una subclave en **HKEY \_ classes \_ raíz** \\ *ProgID* \\ **Shell** para representar el menú en cascada. En este ejemplo, se asigna a esta subclave el nombre *CascadeTest*. Asegúrese de que el valor predeterminado de la subclave *CascadeTest* esté vacío y se muestre como **(valor no establecido)**.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  En la subclave *CascadeTest* , agregue una entrada MUIVerb de tipo **reg \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual. En este ejemplo, lo asignaremos "menú en cascada de prueba".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  En la subclave *CascadeTest* , agregue una entrada subcomandos de tipo **reg \_ SZ** que tenga asignada la lista, demlimited mediante punto y coma, de los verbos que deben aparecer en el menú, en el orden de aparición. Por ejemplo, aquí se asigna un número de verbos proporcionados por el sistema:

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  En el caso de los verbos personalizados, se implementan mediante cualquiera de los métodos de implementación de verbos estáticos y se enumeran en la subclave **CommandStore** , tal como se muestra en este ejemplo para un verbo ficticio *VerbName*:

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
> Este método tiene la ventaja de que los verbos personalizados se pueden registrar una vez y reutilizarlos enumerando el nombre del verbo en la entrada subcomandos. Sin embargo, requiere que la aplicación tenga permiso para modificar el registro en **el \_ \_ equipo local HKEY**.

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Crear menús en cascada con la entrada del registro ExtendedSubCommandsKey

En Windows 7 y versiones posteriores, puede usar la entrada ExtendedSubCommandKey para crear menús en cascada extendida: menús en cascada en menús en cascada.

La siguiente captura de pantalla es un ejemplo de un menú en cascada extendido.

![captura de pantalla que muestra el menú en cascada ampliado para dispositivos](images/file-assoc/extendedsubcommandskey.png)

Dado que la **\_ \_ raíz de las clases HKEY** es una combinación de **HKEY \_ Current \_ User** y **HKEY \_ local \_ Machine**, puede registrar verbos personalizados en la subclave de clases de software de **\_ \_ usuario actual de HKEY** \\  \\  . La principal ventaja de hacerlo es que el permiso elevado no es necesario. Además, otras asociaciones de archivo pueden volver a usar todo el conjunto de verbos especificando la misma subclave ExtendedSubCommandsKey. Si no necesita volver a usar este conjunto de verbos, puede enumerar los verbos en el elemento primario, pero asegúrese de que el valor predeterminado del elemento primario está vacío.

**Para crear un menú en cascada mediante una entrada ExtendedSubCommandsKey**

1.  Cree una subclave en **HKEY \_ classes \_ raíz** \\ *ProgID* \\ **Shell** para representar el menú en cascada. En este ejemplo, se asigna a esta subclave el nombre *CascadeTest2*. Asegúrese de que el valor predeterminado de la subclave *CascadeTest* esté vacío y se muestre como **(valor no establecido)**.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  En la subclave *CascadeTest* , agregue una entrada MUIVerb de tipo **reg \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual. En este ejemplo, lo asignaremos "menú en cascada de prueba".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  En la subclave *CascadeTest* que ha creado, agregue una subclave **ExtendedSubCommandsKey** y, a continuación, agregue los subcomandos de documento (of **reg \_ SZ** Type); por ejemplo:

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

    Asegúrese de que el valor predeterminado de la subclave *Test Cascade Menu 2* esté vacío y se muestre como **(valor no establecido)**.

4.  Rellene los subverbos utilizando cualquiera de las siguientes implementaciones de verbo estático. Tenga en cuenta que la subclave CommandFlags representa los valores de EXPCMDFLAGS. Si desea agregar un separador antes o después del elemento de menú en cascada, use ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40). Para obtener una descripción de estas marcas de Windows 7 y versiones posteriores, vea [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE solo funciona para los elementos de menú de nivel superior. MUIVerb es de tipo **reg \_ SZ** y CommandFlags es de tipo **reg \_ DWORD**.

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

La siguiente captura de pantalla es una ilustración de los ejemplos anteriores de entradas de la clave del registro.

![captura de pantalla que muestra un ejemplo de un menú en cascada con opciones de Bloc de notas y WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Crear menús en cascada con la interfaz IExplorerCommand

Otra opción para agregar verbos a un menú en cascada es a través de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Este método habilita los orígenes de datos que proporcionan los comandos del módulo de comandos a través de [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esos comandos como verbos en un menú contextual. En Windows 7 y versiones posteriores, puede proporcionar la misma implementación de verbo mediante [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como se puede hacer con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).

En las dos capturas de pantalla siguientes se muestra el uso de menús en cascada en la carpeta **dispositivos** .

![Captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos.](images/file-assoc/filecascademenu.png)

En la captura de pantalla siguiente se muestra otra implementación de un menú en cascada en la carpeta **dispositivos** .

![captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Dado que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) solo admite la activación en proceso, se recomienda para su uso por parte de los orígenes de datos de Shell que necesitan compartir la implementación entre los comandos y los menús contextuales.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Obtener el comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada

La sintaxis de consulta avanzada (AQS) puede expresar una condición que se evaluará mediante las propiedades del elemento para el que se crea una instancia del verbo. Este sistema solo funciona con propiedades rápidas. Estas son las propiedades que el origen de datos de Shell informa de forma rápida al no devolver [* * * * SHCOLSTATE \_ Slow * * *](/windows/win32/api/shtypes/ne-shtypes-shcolstate) * de [**IShellFolder2:: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).

Windows 7 y versiones posteriores admiten valores canónicos que evitan problemas en las compilaciones localizadas. La siguiente sintaxis canónica es necesaria en las compilaciones localizadas para aprovechar esta mejora de Windows 7.

``` syntax
System.StructuredQueryType.Boolean#True
```

En la siguiente entrada del registro de ejemplo:

-   El valor **appliesTo** controla si el verbo se muestra u oculta.
-   El valor DefaultAppliesTo controla qué verbo es el valor predeterminado.
-   El valor HasLUAShield controla si se muestra un escudo de control de cuentas de usuario (UAC).

En este ejemplo, el valor **DefaultAppliesTo** hace que este verbo sea el predeterminado para cualquier archivo con la palabra "exampleText1" en el nombre de archivo. El valor **appliesTo** habilita el verbo para cualquier archivo con "exampleText1" en el nombre. El valor **HasLUAShield** muestra el escudo para los archivos con "exampleText2" en el nombre.

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Agregue la subclave **Command** y un valor:

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

En el registro de Windows 7, consulte **HKEY \_ classes \_ root** \\ **Drive** como ejemplo de verbos de BitLocker que emplean el siguiente enfoque:

-   AppliesTo = System. VOLUME. BitlockerProtection: = 2
-   System. VOLUME. BitlockerRequiresAdmin: = System. StructuredQueryType. Boolean \# true

Para obtener más información sobre AQS, consulte [Sintaxis de consulta avanzada](../search/-search-3x-advancedquerysyntax.md).

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>En desuso: asociar verbos con comandos de Intercambio dinámico de datos

DDE está en desuso; en su lugar, use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . DDE está en desuso porque se basa en un mensaje de ventana de difusión para detectar el servidor DDE. Un bloqueo de servidor DDE detiene el mensaje de la ventana de difusión y, por tanto, cuelga las conversaciones DDE para otras aplicaciones. Es habitual que una sola aplicación atascada cause bloqueos posteriores en todo el proceso del usuario.

El método [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) es más sólido y tiene una mejor compatibilidad con la activación porque utiliza la activación com del controlador. En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y en [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la función [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) . Hacerlo es más sencillo y no pierde información de espacio de nombres como ocurre cuando el elemento se convierte en una ruta de acceso para los protocolos de línea de comandos o DDE.

Para obtener más información sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y las consultas de Shell para los atributos de Asociación de archivos, consulte [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).

## <a name="completing-verb-implementation-tasks"></a>Completar tareas de implementación de verbo

Las siguientes tareas para implementar verbos son relevantes para las implementaciones de verbos estáticos y dinámicos. Para obtener más información sobre los verbos dinámicos, vea [personalizar un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md).

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Personalización del menú contextual para objetos de Shell predefinidos

Muchos objetos de Shell predefinidos tienen menús contextuales que se pueden personalizar. Registre el comando de la misma manera que registra los tipos de archivo típicos, pero use el nombre del objeto predefinido como el nombre del tipo de archivo.

Una lista de objetos predefinidos está en la sección *objetos de Shell predefinidos* de [crear controladores de extensión de Shell](handlers.md). Los objetos de Shell predefinidos cuyos menús contextuales se pueden personalizar agregando verbos en el registro se marcan en la tabla con el verbo palabra.

### <a name="extending-a-new-submenu"></a>Extender un nuevo submenú

Cuando un usuario abre el menú **archivo** en el explorador de Windows, uno de los comandos que se muestran es **nuevo**. Al seleccionar este comando se muestra un submenú. De forma predeterminada, el submenú contiene dos comandos, **carpeta** y **acceso directo**, que permiten a los usuarios crear subcarpetas y accesos directos. Este submenú se puede extender para incluir comandos de creación de archivos para cualquier tipo de archivo.

Para agregar un comando de creación de archivos al **nuevo** submenú, los archivos de la aplicación deben tener un tipo de archivo asociado. Incluya una subclave **ShellNew** en el nombre de archivo. Cuando se selecciona el comando **nuevo** del menú **archivo** , el shell agrega el tipo de archivo al **nuevo** submenú. La cadena de presentación del comando es la cadena descriptiva que se asigna al ProgID del programa.

Para especificar el método de creación de archivos, asigne uno o varios valores de datos a la subclave **ShellNew** . Los valores disponibles se muestran en la tabla siguiente.



| Valor de la subclave ShellNew | Descripción                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando               | Ejecuta una aplicación. Este valor **reg \_ SZ** especifica la ruta de acceso de la aplicación que se va a ejecutar. Por ejemplo, puede establecerlo para iniciar un asistente.                  |
| Datos                  | Crea un archivo que contiene los datos especificados. Este **valor \_ binario de reg** especifica los datos del archivo. Los **datos** se omiten si se especifica **NullFile** o **filename** . |
| FileName              | Crea un archivo que es una copia de un archivo especificado. Este valor **reg \_ SZ** especifica la ruta de acceso completa del archivo que se va a copiar.                                   |
| NullFile              | Crea un archivo vacío. **NullFile** no tiene asignado un valor. Si se especifica **NullFile** , se omiten los valores de registro de los **datos** y del **nombre de archivo** .                    |



 

El siguiente ejemplo de clave del registro y captura de pantalla ilustran el **nuevo** submenú para el tipo de archivo. MYP-ms. Tiene un comando, **aplicación de programa**.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

En la captura de pantalla se muestra el **nuevo** submenú. Cuando un usuario selecciona mi **aplicación** en el submenú **nuevo** , el shell crea un archivo denominado **nueva aplicación de MYP-ms** y lo pasa a **MyProgram.exe**.

![captura de pantalla del explorador de Windows que muestra un nuevo comando "mi aplicación" en el submenú "nuevo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Crear controladores de arrastrar y colocar

El procedimiento básico para implementar un controlador de arrastrar y colocar es el mismo que el de los controladores de menú contextuales convencionales. Sin embargo, los controladores de menús contextuales normalmente usan solo el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que se pasa al método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del controlador para extraer el nombre del objeto. Un controlador de arrastrar y colocar podría implementar un controlador de datos más sofisticado para modificar el comportamiento del objeto arrastrado.

Cuando un usuario hace clic con el botón secundario en un objeto de Shell para arrastrar un objeto, se muestra un menú contextual cuando el usuario intenta quitar el objeto. En la captura de pantalla siguiente se muestra un menú contextual típico de arrastrar y colocar.

![captura de pantalla del menú contextual de arrastrar y colocar](images/context-menu/context-dragdrop.png)

Un controlador de arrastrar y colocar es un controlador de menú contextual que puede agregar elementos a este menú contextual. Los controladores de arrastrar y colocar se registran normalmente en la subclave siguiente.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Agregue una subclave en la subclave **DragDropHandlers** denominada para el controlador de arrastrar y colocar, y establezca el valor predeterminado de la subclave en el formato de cadena del GUID del identificador de clase (CLSID) del controlador. En el ejemplo siguiente se habilita el controlador de arrastrar y colocar de **MyDD** .

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Suprimir verbos y controlar la visibilidad

Puede usar la configuración de directiva de Windows para controlar la visibilidad de los verbos. Los verbos se pueden suprimir a través de la configuración de la Directiva agregando un valor de **SuppressionPolicy** o un valor de GUID de **SuppressionPolicyEx** a la subclave del registro del verbo. Establezca el valor de la subclave **SuppressionPolicy** en el identificador de la Directiva. Si la Directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada. Para ver los posibles valores de ID. de Directiva, consulte la enumeración [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

### <a name="employing-the-verb-selection-model"></a>Usar el modelo de selección de verbos

Los valores del registro se deben establecer para que los verbos controlen las situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento. Un verbo requiere valores de registro independientes para cada una de estas tres situaciones que admite el verbo. Los valores posibles para el modelo de selección de verbos son los siguientes:

-   Especifique el valor de MultiSelectModel para todos los verbos. Si no se especifica el valor MultiSelectModel, se deduce del tipo de implementación de verbo que ha elegido. En el caso de los métodos basados en COM (como DropTarget y ExecuteCommand), se supone que el **jugador** y para el resto **de métodos se** supone.
-   Especifique **Single** para los verbos que solo admiten una sola selección.
-   Especifique **Player** para los verbos que admiten cualquier número de elementos.
-   Especifique el **documento** para los verbos que crean una ventana de nivel superior para cada elemento. Esto limita el número de elementos activados y ayuda a evitar quedarse sin recursos del sistema si el usuario abre demasiadas ventanas.

Cuando el número de elementos seleccionados no coincide con el modelo de selección de verbos o es mayor que los límites predeterminados que se describen en la tabla siguiente, el verbo no aparece.



| Tipo de implementación de verbo | Documento | Reproductor    |
|-----------------------------|----------|-----------|
| Heredado                      | 15 elementos | 100 elementos |
| COM                         | 15 elementos | Sin límite  |



 

A continuación se muestran las entradas del registro de ejemplo con el valor MultiSelectModel.

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

Los valores de marca [**SFGAO**](sfgao.md) de los atributos de Shell para un elemento pueden probarse para determinar si el verbo debe estar habilitado o deshabilitado.

Para usar esta característica de atributo, agregue los siguientes valores de **reg \_ DWORD** en el verbo:

-   El valor AttributeMask especifica el valor de [**SFGAO**](sfgao.md) de los valores de bit de la máscara que se va a probar con.
-   El valor AttributeValue especifica el valor de [**SFGAO**](sfgao.md) de los bits que se prueban.
-   ImpliedSelectionModel especifica cero para los verbos de elemento o un valor distinto de cero para los verbos en el menú contextual del fondo.

En la siguiente entrada del registro de ejemplo, AttributeMask se establece en [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>Implementar verbos personalizados para carpetas a través de Desktop.ini

En Windows 7 y versiones posteriores, puede Agregar verbos a una carpeta a través de Desktop.ini. Para obtener más información acerca de los archivos de Desktop.ini, consulte [Cómo personalizar carpetas con Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini archivos siempre deben estar marcados como **sistema**  +  **oculto** para que no se muestren a los usuarios.

 

**Para agregar verbos personalizados para carpetas a través de un archivo de Desktop.ini, realice los pasos siguientes:**

1.  Cree una carpeta marcada como **de solo lectura** o **sistema**.
2.  Cree un archivo de Desktop.ini que incluya un \[ . ShellClassInfo \] DirectoryClass = ProgID.
3.  En el registro, cree **HKEY \_ classes \_ raíz** \\ **ProgID** con un valor de CanUseForDirectory. El valor CanUseForDirectory evita el uso incorrecto de los ProgID que se establecen para no participar en la implementación de verbos personalizados para carpetas a través de Desktop.ini.
4.  Agregue verbos en la subclave ProgID de la **carpeta**, por ejemplo:

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Estos verbos pueden ser el verbo predeterminado, en cuyo caso al hacer doble clic en la carpeta se activa el verbo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas para los controladores de menú contextual y varios verbos de selección](verbs-best-practices.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menú contextual](context-menu.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 
