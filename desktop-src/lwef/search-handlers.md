---
title: Crear controladores de búsqueda
description: Shell admite varias utilidades de búsqueda que permiten a los usuarios buscar objetos de espacio de nombres, como archivos o impresoras. Puede crear un motor de búsqueda personalizado y ponerlo a disposición de los usuarios implementando y registrando un controlador de búsqueda.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- controladores de búsqueda
- register,search handlers
- controladores de búsqueda estática
- register,static search handlers
- controladores de búsqueda dinámica
- register,dynamic search handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be891247c36687b0305e7e9c60711a233fb9b1d4f7f8554d0103be4cc0dc5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975788"
---
# <a name="creating-search-handlers"></a>Crear controladores de búsqueda

\[Esta característica solo se admite en Windows XP o versiones anteriores. Use Windows Search en su lugar.\]

Shell admite varias utilidades de búsqueda que permiten a los usuarios buscar objetos de espacio de nombres, como archivos o impresoras. Puede crear un motor de búsqueda personalizado y ponerlo a disposición de los usuarios implementando y registrando un controlador *de búsqueda.*

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se de abordan en [Crear controladores de extensión de shell](/windows/desktop/shell/handlers). Este documento se centra en los aspectos de implementación específicos de los controladores de búsqueda.

-   [Cómo funcionan los controladores de búsqueda](#how-search-handlers-work)
-   [Registro de controladores de búsqueda](#registering-search-handlers)
    -   [Registrar un controlador de búsqueda estática](#registering-a-static-search-handler)
    -   [Registro de un controlador de búsqueda dinámica](#registering-a-dynamic-search-handler)
-   [Implementar controladores de búsqueda](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Cómo funcionan los controladores de búsqueda

Los usuarios tienen dos maneras de seleccionar un motor de búsqueda. La primera forma es desde el menú Inicio. Con sistemas anteriores a Windows 2000,  al seleccionar  el comando Buscar en el menú Inicio se muestra un submenú de los motores de búsqueda disponibles. Con Windows 2000 y versiones posteriores, el  comando Buscar del menú St **art** se denomina Buscar. En la ilustración siguiente se muestra **el botón** Buscar en un Windows XP.

![submenú de búsqueda del menú Inicio](images/searchhandler1.jpg)

Los usuarios también pueden iniciar una búsqueda desde Windows Explorer. En sistemas anteriores a Windows 2000,  hacen clic  en el comando Buscar del menú Herramientas para mostrar básicamente el mismo menú que el asociado al **menú** Inicio. Sin embargo, Windows explorer para Windows 2000 controla los motores de búsqueda de una manera muy diferente. En lugar de controlar los motores de búsqueda como un submenú del **menú Herramientas,** ahora hay un **botón Buscar** en la barra de herramientas. Al hacer clic en este botón, se abre el panel **Búsqueda de la barra del** explorador. En la ilustración siguiente se muestra **el panel de búsqueda Buscar archivos y** carpetas.

![panel de búsqueda de la barra del explorador de Windows](images/searchhandler2.jpg)

Hay varias diferencias en la forma en que Windows 2000 y sistemas anteriores administran controladores de búsqueda que afectan tanto a la implementación como al registro.



| Anterior a Windows 2000                                                                                                                                                                                                       | Windows 2000 y versiones posteriores                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Los controladores de búsqueda se implementan como un tipo de controlador [de menú contextual.](/windows/desktop/shell/context-menu-handlers)                                                                                                                     | Los controladores de búsqueda se pueden implementar como controladores de menús contextuales o como documentos HTML dinámicos (DHTML).                                                                                                                                                                                                               |
| Los controladores de búsqueda pueden ser estáticos o dinámicos. Los controladores estáticos solo se cargan cuando el usuario los selecciona. Los controladores dinámicos los carga el Shell en el inicio y no finalizan hasta que se cierra el shell. | Los controladores implementados como controladores de menú contextual pueden ser estáticos o dinámicos. Los controladores implementados como documentos DHTML deben ser estáticos.                                                                                                                                                                           |
| Los controladores de búsqueda aparecen en  el **submenú** Buscar del menú Inicio y en el **submenú** Buscar del Windows herramientas del Explorador **de** aplicaciones.                                                                                  | Los controladores de búsqueda solo aparecen en el **submenú Buscar** del **menú** Inicio. Para que un panel de búsqueda personalizado esté disponible a través de la barra de menús Windows Explorer, debe implementarlo como un objeto [de banda](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)). A continuación, aparece en el **submenú Barra** del explorador del menú Windows **Explorador.** |



 

## <a name="registering-search-handlers"></a>Registro de controladores de búsqueda

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

Desde este punto, el procedimiento de registro depende de si el controlador va a ser estático o dinámico. Para obtener una explicación general de cómo registrar controladores de extensión de Shell, vea [Creating Shell Extension Handlers](/windows/desktop/shell/handlers).

### <a name="registering-a-static-search-handler"></a>Registrar un controlador de búsqueda estática

Los controladores de búsqueda estática solo se cargan cuando el usuario los inicia. Este enfoque funciona mejor para los archivos DLL que son pequeños y se pueden cargar rápidamente. Si usa DHTML para implementar el controlador, debe ser estático. Para registrar un controlador de extensión estático, cree una subclave denominada para el controlador en la subclave **Static** de la subclave **FindExtensions.** El sistema no usa el nombre, pero no debe ser idéntico a otros nombres de controlador de búsqueda en la subclave **FindExtensions.**

### <a name="shortcut-menu-based-search-handlers"></a>Controladores de búsqueda basados en menús contextuales

Si el controlador se implementa como un controlador de menú [contextual,](/windows/desktop/shell/context-menu-handlers)establezca el valor predeterminado de la subclave name del controlador en el GUID del identificador de clase (CLSID) del objeto. En la subclave name del controlador, cree una subclave denominada **0** (cero) y establezca su valor predeterminado en la cadena que se mostrará en el **submenú** **Buscar** o Buscar. Puede habilitar los métodos abreviados de teclado de la manera habitual, precediendo el carácter de método abreviado con una yand (&). Puede mostrar un icono pequeño opcional a la derecha del texto del menú mediante la creación de una subclave **DefaultIcon** bajo la subclave **0.** Establezca su valor predeterminado en una cadena que contenga la ruta de acceso del archivo que contiene el icono, seguida de una coma, seguida del índice de base cero del icono.

En el ejemplo siguiente se registra el controlador **de búsqueda MySearchEngine.** El texto del menú es "Mi motor de búsqueda", con M especificado como tecla de método abreviado. El icono está en C: \\ MyDir \\MySearch.dll, con un índice de 2.

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

Con Windows 2000, también puede implementar un controlador de búsqueda como un documento DHTML. Su nombre aparece en el **submenú Buscar** del **menú** Inicio. Cuando el usuario lo selecciona, se inicia Windows Explorer con la barra Explorador abierta en el documento de búsqueda. También puede especificar un documento DHTML que se mostrará a la derecha de la barra del explorador. No hay ninguna manera de iniciar un controlador diferente del panel de búsqueda predeterminado. Los motores de búsqueda se pueden iniciar directamente desde Windows Explorer, pero solo si se implementan como objetos [de banda](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)).

Para registrar un controlador de búsqueda basado en DHTML, establezca la subclave name del controlador en el formato de cadena de CLSID \_ ShellSearchExt (actualmente {169A0691-8DF9-11d1-A1C4-00C04FD75D13}) y cree las subclaves siguientes.

1.  Cree una **subclave 0**(cero) en la subclave de nombre de controlador y establezca su valor predeterminado en el texto del menú.
2.  Para que se muestre un icono junto al texto del menú, cree una subclave **DefaultIcon** en **0** y establezca su valor predeterminado en la ruta de acceso e índice del icono.
3.  Cree una **subclave SearchGUID** en **0**. Asigne un GUID al documento DHTML y establezca el valor predeterminado de **SearchGUID** en su forma de cadena. No es necesario registrar este GUID en **HKEY \_ CLASSES ROOT \_ \\ CLSID**.
4.  Cree una **subclave Url** en **SearchGUID.** Establezca su valor predeterminado en la ruta de acceso del documento HTML que aparecerá en la barra del explorador.
5.  Cree una **subclave UrlNavNew** en **SearchGUID.** Establezca su valor predeterminado en la ruta de acceso del documento HTML que aparecerá a la derecha de la barra del explorador.

En el ejemplo siguiente se registra el **controlador de búsqueda MySearchEngine** implementado como un documento DHTML. El texto del menú es "Mi motor de búsqueda", con M especificado como tecla de método abreviado. El icono está en C: \\ MyDir \\MySearch.dll, con un índice de 2. El documento DHTML de la barra del explorador es C: MyDirMySearch.htm y el documento que se mostrará a la derecha de la barra del explorador es \\ \\ C: \\ MyDir \\MySearchPage.htm.

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

### <a name="registering-a-dynamic-search-handler"></a>Registro de un controlador de búsqueda dinámica

Si el controlador se implementa como un controlador [de menú](/windows/desktop/shell/context-menu-handlers)contextual, también puede registrarlo como un controlador dinámico. En ese caso, se cargará con el shell y finalizará solo cuando se cierre el shell. Los controladores de búsqueda dinámica responden mucho más rápidamente que los controladores estáticos cuando los inicia el usuario. Este enfoque funciona mejor si el archivo DLL del controlador puede tardar mucho tiempo en cargarse o si es probable que se llame con frecuencia.

Los controladores de búsqueda dinámica se registran en la **subclave FindExtensions.**

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

A diferencia de los controladores de búsqueda estática, no se especifica el texto del menú en el Registro. Cuando se carga el controlador, el Shell llamará al método [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del controlador para agregar elementos al submenú **Buscar** **o** Buscar.

## <a name="implementing-search-handlers"></a>Implementar controladores de búsqueda

Los controladores de búsqueda se pueden implementar como controladores de menú contextual para todas las versiones de Windows. Para Windows 2000, también se pueden implementar como documentos DHTML.

Para obtener una explicación general de cómo implementar controladores de menús contextuales, vea [Crear controladores de menú contextual.](/windows/desktop/shell/context-menu-handlers) Los controladores de búsqueda difieren de los controladores de menús contextuales estándar de solo algunas maneras.

Para los controladores de menú estáticos, **el** submenú **Buscar o Buscar** se crea a partir de la información del Registro. No es necesario que el controlador agregue un elemento de menú, como lo haría un controlador de menús contextuales normal. Shell administra los controladores de menú estáticos de la siguiente manera.

-   Cuando el usuario inicia el elemento de menú del controlador, el Shell carga el archivo DLL del controlador y llama a [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para notificar al controlador que inicie el motor de búsqueda. No se llama a los métodos [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) [**e IContextMenu::QueryContextMenu.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)
-   Cuando se llama a [**IContextMenu::InvokeCommand,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) el miembro **lpVerb** de la estructura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) que se pasa identifica el comando. La palabra de orden inferior **lpVerb** se establece en el equivalente numérico del nombre de subclave del comando. Puesto que esta subclave normalmente se denomina **0,** **lpVerb** normalmente se establece en cero. A continuación, el controlador debe iniciar el motor de búsqueda.

Los controladores de búsqueda dinámica se implementan de la misma manera que los controladores de menús contextuales normales. La excepción principal es que cuando se llama a [**IShellExtInit::Initialize,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) los *argumentos pidlFolder* y *lpdobj* se establecen en **NULL.**

Los controladores de búsqueda basados en DHTML se implementan como un documento DHTML normal. Pueden incluir cualquier tecnología html, DHTML o scripting que sea compatible con Windows Internet Explorer.

 

 