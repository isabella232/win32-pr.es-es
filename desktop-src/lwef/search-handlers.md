---
title: Crear controladores de búsqueda
description: El shell admite varias utilidades de búsqueda que permiten a los usuarios buscar objetos de espacio de nombres, como archivos o impresoras. Puede crear un motor de búsqueda personalizado y hacer que esté disponible para los usuarios implementando y registrando un controlador de búsqueda.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- Controladores de búsqueda
- registro, controladores de búsqueda
- Controladores de búsqueda estáticos
- registro, controladores de búsqueda estáticos
- Controladores de búsqueda dinámica
- registro, controladores de búsqueda dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6476109302a176822137747353b2762b0caea8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358940"
---
# <a name="creating-search-handlers"></a>Crear controladores de búsqueda

\[Esta característica solo se admite en Windows XP o versiones anteriores. En su lugar, use Windows Search.\]

El shell admite varias utilidades de búsqueda que permiten a los usuarios buscar objetos de espacio de nombres, como archivos o impresoras. Puede crear un motor de búsqueda personalizado y hacer que esté disponible para los usuarios implementando y registrando un *controlador de búsqueda*.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](/windows/desktop/shell/handlers). Este documento se centra en los aspectos de la implementación que son específicos de los controladores de búsqueda.

-   [Cómo funcionan los controladores de búsqueda](#how-search-handlers-work)
-   [Registrando controladores de búsqueda](#registering-search-handlers)
    -   [Registrar un controlador de búsqueda estático](#registering-a-static-search-handler)
    -   [Registrar un controlador de búsqueda dinámica](#registering-a-dynamic-search-handler)
-   [Implementar controladores de búsqueda](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Cómo funcionan los controladores de búsqueda

Los usuarios tienen dos maneras de seleccionar un motor de búsqueda. La primera manera es desde el menú Inicio. Con sistemas anteriores a Windows 2000, al seleccionar el comando **Buscar** en el menú **Inicio** se muestra un submenú de los motores de búsqueda disponibles. Con Windows 2000 y versiones posteriores, el nombre del comando **Buscar** del menú de **St** Art se cambia a Search. En la ilustración siguiente se muestra el botón **Buscar** en un sistema Windows XP.

![el submenú buscar del menú Inicio](images/searchhandler1.jpg)

Los usuarios también pueden iniciar una búsqueda desde el explorador de Windows. En sistemas anteriores a Windows 2000, se hace clic en el comando **Buscar** del menú **herramientas** para mostrar esencialmente el mismo menú que el asociado al menú **Inicio** . Sin embargo, el explorador de Windows para Windows 2000 controla los motores de búsqueda de una manera muy diferente. En lugar de controlar los motores de búsqueda como un submenú del menú **herramientas** , ahora hay un botón **Buscar** en la barra de herramientas. Al hacer clic en este botón, se abre el panel de **búsqueda** de la barra del explorador. En la ilustración siguiente se muestra el panel **de búsqueda buscar archivos y carpetas** .

![panel de búsqueda de la barra del explorador de Windows](images/searchhandler2.jpg)

Hay una serie de diferencias en el modo en que Windows 2000 y los sistemas anteriores administran los controladores de búsqueda que afectan tanto a la implementación como al registro.



| Anterior a Windows 2000                                                                                                                                                                                                       | Windows 2000 y versiones posteriores                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Los controladores de búsqueda se implementan como un tipo de [controlador de menú contextual](/windows/desktop/shell/context-menu-handlers).                                                                                                                     | Los controladores de búsqueda se pueden implementar como controladores de menú contextual o como documentos HTML dinámico (DHTML).                                                                                                                                                                                                               |
| Los controladores de búsqueda pueden ser estáticos o dinámicos. Los controladores estáticos solo se cargan cuando los selecciona el usuario. El shell carga los controladores dinámicos en el inicio y no finalizan hasta que se cierra el shell. | Los controladores implementados como controladores de menús contextuales pueden ser estáticos o dinámicos. Los controladores implementados como documentos DHTML deben ser estáticos.                                                                                                                                                                           |
| Los controladores de búsqueda aparecen en el submenú **Buscar** del menú **Inicio** y en el submenú **Buscar** del menú  **herramientas** del explorador de Windows.                                                                                  | Los controladores de búsqueda solo aparecen en el submenú **Buscar** del menú **Inicio** . Para que un panel de búsqueda personalizado esté disponible a través de la barra de menús del explorador de Windows, debe implementarlo como un [objeto de banda](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)). A continuación, se muestra en el submenú de la **barra del explorador** del menú  **vista** del explorador de Windows. |



 

## <a name="registering-search-handlers"></a>Registrando controladores de búsqueda

Los controladores de búsqueda se registran en la subclave **FindExtensions** de los tipos de archivo.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Desde este punto, el procedimiento de registro depende de si el controlador debe ser estático o dinámico. Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](/windows/desktop/shell/handlers).

### <a name="registering-a-static-search-handler"></a>Registrar un controlador de búsqueda estático

Los controladores de búsqueda estáticos solo se cargan cuando los inicia el usuario. Este enfoque funciona mejor para los archivos DLL que son pequeños y se pueden cargar rápidamente. Si utiliza DHTML para implementar el controlador, debe ser estático. Para registrar un controlador de extensión estático, cree una subclave denominada para el controlador bajo la subclave **static** de la subclave **FindExtensions** . El sistema no utiliza el nombre, pero no debe ser idéntico a otros nombres de controlador de búsqueda de la subclave **FindExtensions** .

### <a name="shortcut-menu-based-search-handlers"></a>Controladores de búsqueda basados en menús contextuales

Si el controlador se implementa como [controlador de menú contextual](/windows/desktop/shell/context-menu-handlers), establezca el valor predeterminado de la subclave Name del controlador en el GUID del identificador de clase (CLSID) del objeto. En la subclave nombre del controlador, cree una subclave denominada **0**   (cero) y establezca su valor predeterminado en la cadena que se mostrará en el submenú **Buscar** o **Buscar** . Puede habilitar los métodos abreviados de teclado de la manera habitual, precediendo el carácter de acceso directo con una y comercial (&). Puede hacer que se muestre un icono pequeño opcional a la derecha del texto del menú mediante la creación de una subclave **DefaultIcon** en la subclave **0** . Establezca su valor predeterminado en una cadena que contenga la ruta de acceso del archivo que contiene el icono, seguida de una coma, seguida del índice basado en cero del icono.

En el ejemplo siguiente se registra el controlador de búsqueda de **MySearchEngine** . El texto del menú es "My Search Engine", donde M se especifica como la tecla de método abreviado. El icono está en C: \\ MyDir \\MySearch.dll, con un índice de 2.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {MySearchEngine CLSID GUID}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
```

### <a name="dhtml-based-search-handlers"></a>Controladores de búsqueda basados en DHTML

Con Windows 2000, también puede implementar un controlador de búsqueda como un documento DHTML. Su nombre se muestra en el submenú **Buscar** del menú **Inicio** . Cuando el usuario lo selecciona, inicia el explorador de Windows con la barra del explorador abierta al documento de búsqueda. También puede especificar un documento DHTML para que se muestre a la derecha de la barra del explorador. No hay ninguna manera de iniciar un controlador diferente a partir del panel de búsqueda predeterminado. Los motores de búsqueda se pueden iniciar directamente desde el explorador de Windows, pero solo si se implementan como [objetos de banda](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)).

Para registrar un controlador de búsqueda basado en DHTML, establezca la subclave Name del controlador en la forma de cadena de CLSID \_ ShellSearchExt (actualmente {169A0691-8DF9-11D1-A1C4-00C04FD75D13}) y cree las siguientes subclaves.

1.  Cree una subclave **0**(cero) en la subclave de nombre de controlador y establezca su valor predeterminado en el texto de menú.
2.  Para que se muestre un icono junto al texto del menú, cree una subclave **DefaultIcon** en **0** y establezca su valor predeterminado en la ruta de acceso y el índice del icono.
3.  Cree una subclave **SearchGUID** en **0**. Asigne un GUID al documento DHTML y establezca el valor predeterminado de **SearchGUID** en su forma de cadena. No es necesario registrar este GUID en el **\_ \_ \\ CLSID raíz de las clases HKEY**.
4.  Cree una subclave de **dirección URL** en **SearchGUID**. Establezca su valor predeterminado en la ruta de acceso del documento HTML que aparecerá en la barra del explorador.
5.  Cree una subclave **UrlNavNew** en **SearchGUID**. Establezca su valor predeterminado en la ruta de acceso del documento HTML que aparecerá a la derecha de la barra del explorador.

En el ejemplo siguiente se registra el controlador de búsqueda de **MySearchEngine** implementado como un documento DHTML. El texto del menú es "My Search Engine", donde M se especifica como la tecla de método abreviado. El icono está en C: \\ MyDir \\MySearch.dll, con un índice de 2. El documento DHTML de la barra del explorador es C: \\ MyDir \\MySearch.htm y el documento que se mostrará a la derecha de la barra del explorador es c: \\ MyDir \\MySearchPage.htm.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {169A0691-8DF9-11d1-A1C4-00C04FD75D13}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
                                 SearchGUID
                                    (Default) = {My Search GUID}
                                    Url
                                       (Default) = C:\MyDir\MySearch.htm
                                    UrlNavNew
                                       (Default) = C:\MyDir\MySearchPage.htm
```

### <a name="registering-a-dynamic-search-handler"></a>Registrar un controlador de búsqueda dinámica

Si el controlador se implementa como un [controlador de menú contextual](/windows/desktop/shell/context-menu-handlers), también puede registrarlo como un controlador dinámico. En ese caso, se cargará con el Shell y finalizará solo cuando se cierre el shell. Los controladores de búsqueda dinámica responden mucho más rápidamente que los controladores estáticos cuando los inicia el usuario. Este enfoque funciona mejor si la DLL del controlador puede tardar mucho tiempo en cargarse, o si es probable que se llame con frecuencia.

Los controladores de búsqueda dinámica se registran en la subclave **FindExtensions** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Cree una subclave de **FindExtensions** denominada para el controlador y establezca su valor predeterminado en el GUID de CLSID del controlador. Los iconos de menú no se admiten para los controladores de búsqueda dinámica. En el ejemplo siguiente se registra MySearchEngine como controlador de búsqueda dinámica.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     MySearchEngine
                        (Default) = {MySearchEngine CLSID GUID}
                        0
                           (Default) = &My Search Engine
```

A diferencia de los controladores de búsqueda estáticos, no se especifica el texto del menú en el registro. Cuando se carga el controlador, el shell llamará al método [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del controlador para agregar elementos al submenú **Buscar** o **Buscar** .

## <a name="implementing-search-handlers"></a>Implementar controladores de búsqueda

Los controladores de búsqueda se pueden implementar como controladores de menú contextual para todas las versiones de Windows. En Windows 2000, también se pueden implementar como documentos DHTML.

Para obtener una explicación general sobre cómo implementar controladores de menús contextuales, vea [crear controladores de menús contextuales](/windows/desktop/shell/context-menu-handlers). Los controladores de búsqueda se diferencian de los controladores de menú contextual estándar solo en algunas maneras.

En el caso de los controladores de menú estáticos, el submenú **Buscar** o **Buscar** se crea a partir de la información del registro. No es necesario que el controlador agregue un elemento de menú, como haría un controlador de menú contextual normal. El shell administra los controladores de menú estáticos de la siguiente manera.

-   Cuando el usuario inicia el elemento de menú del controlador, el shell carga el archivo DLL del controlador y llama a [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para notificar al controlador que inicie el motor de búsqueda. No se llama a los métodos [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) y [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .
-   Cuando se llama a [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , el miembro **lpVerb** de la estructura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) que se pasa identifica el comando. La palabra de orden inferior de **lpVerb** se establece en el equivalente numérico del nombre de la subclave del comando. Puesto que esta subclave se denomina normalmente **0**, **lpVerb** normalmente se establece en cero. Después, el controlador debe iniciar el motor de búsqueda.

Los controladores de búsqueda dinámica se implementan de forma muy similar a los controladores de menú contextuales normales. La excepción principal es que cuando se llama a [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) , los argumentos *pidlFolder* y *lpdobj* se establecen en **null**.

Los controladores de búsqueda basados en DHTML se implementan como un documento DHTML normal. Pueden incluir cualquier tecnología HTML, DHTML o de scripting que sea compatible con Windows Internet Explorer.

 

 