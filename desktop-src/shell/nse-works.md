---
description: Windows El Explorador proporciona una representación gráfica del espacio de nombres de Shell combinada con herramientas que permiten a los usuarios interactuar con objetos de Shell.
ms.assetid: cc387338-15fa-4350-b039-61a0f1c5030a
title: Descripción de las extensiones de espacio de nombres de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d972239320c633a12d4d162ec1593b82b9b02fb9d15a1a0bc9ee908abc8ac64d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820955"
---
# <a name="understanding-shell-namespace-extensions"></a>Descripción de las extensiones de espacio de nombres de Shell

Windows El Explorador proporciona una representación gráfica del espacio de nombres de Shell combinada con herramientas que permiten a los usuarios interactuar con objetos de Shell. Con una extensión de espacio de nombres, puede tomar cualquier cuerpo de datos y hacer que Windows Explorer los presente al usuario como una carpeta virtual. Cuando un usuario examina esta carpeta, los datos se presentan como una jerarquía estructurada en árbol de carpetas y archivos, de forma muy parecido al resto del espacio de nombres de Shell. Los usuarios y las aplicaciones pueden interactuar con el contenido de esta carpeta virtual de la misma manera que con cualquier otro objeto de espacio de nombres. En este documento se describe cómo crear una extensión de espacio de nombres.

-   [Funcionamiento de una extensión de espacio de nombres](#how-a-namespace-extension-works)
-   [El objeto de vista de carpeta del sistema predeterminado (DefView)](#the-default-system-folder-view-object-defview)
-   [Cómo Windows explorer interactúa con una extensión de espacio de nombres](#how-windows-explorer-interacts-with-a-namespace-extension)
    -   [Vista de árbol](#tree-view)
    -   [Vista de carpeta](#folder-view)
    -   [Barra de menús y barras de herramientas](#menu-bar-and-toolbars)
    -   [Barra de estado](#status-bar)

## <a name="how-a-namespace-extension-works"></a>Funcionamiento de una extensión de espacio de nombres

En segundo plano, todas las carpetas Windows Explorer se representan mediante un objeto del Modelo de objetos componentes (COM) denominado objeto *de carpeta*. Cada vez que el usuario interactúa con una carpeta o su contenido, el Shell se comunica con el objeto de carpeta asociado a través de una de varias interfaces estándar. A continuación, el objeto de carpeta hace lo necesario para responder a la acción del usuario y el Shell actualiza la Windows Explorer.

La mayoría de los archivos y carpetas con los que interactúan los usuarios forman parte del sistema de archivos o de una carpeta virtual del sistema, como papelera de reciclaje. Otra documentación ha analizado cómo puede personalizar el comportamiento de estas carpetas estándar para satisfacer los [requisitos](handlers.md)de la aplicación modificando el Registro o implementando controladores de extensión de Shell . Sin embargo, la extensión del Shell de estas maneras es muy útil cuando la información se puede empaquetar fácilmente en forma de carpetas o archivos normales del sistema de archivos.

Hay una serie de situaciones en las que el almacenamiento de datos como una colección de archivos y carpetas del sistema de archivos podría ser indeseable o incluso imposible. Algunos ejemplos de este tipo de datos son:

-   Colección de elementos que se empaqueta de forma más eficaz en un único archivo, como una base de datos.
-   Colección de elementos almacenados en un equipo remoto que no tiene un sistema de archivos Windows estándar. Un ejemplo de estos datos es la información almacenada en un asistente digital personal (PDA) o una cámara digital.
-   Colección de elementos que no representan datos almacenados. Un ejemplo de estos datos son los vínculos de impresora incluidos en la carpeta Impresoras estándar.

Una manera de presentar este tipo de datos a un usuario es escribir una aplicación que permita a los usuarios ver los distintos elementos e interactuar con ellos. Sin embargo, si los datos se pueden presentar como una jerarquía de carpetas o archivos, gran parte de la funcionalidad que deberá implementar podría ser servicios de interfaz de usuario que ya se proporcionan mediante Windows Explorer. Un enfoque mucho más eficaz podría ser escribir una extensión de espacio de nombres y permitir que Windows Explorer se convierta en la GUI.

Para implementar una extensión de espacio de nombres, la información debe organizarse como un espacio de nombres estructurado en árbol. La *raíz del espacio de* nombres se presenta como una carpeta virtual en el espacio de nombres de Shell. La carpeta raíz, y todas sus subcarpetas y elementos de datos, se convierten en parte del espacio de nombres shell y Windows Explorer se convierte en la interfaz de usuario. Por lo tanto, puede presentar la información al usuario de una manera familiar y fácilmente accesible con mucha menos programación de la interfaz de usuario de la que sería necesaria para una aplicación personalizada.

Una extensión de espacio de nombres consta de dos componentes básicos:

-   Un administrador de datos
-   Interfaz entre el administrador de datos y Windows Explorer

El primer componente de la lista depende por completo de usted. Puede almacenar y administrar los datos de la manera que sea más eficaz. El segundo componente es el código necesario para empaquetar los datos como objetos de carpeta y controlar la interacción con Windows Explorer. Windows A continuación, el Explorador puede llamar a estos objetos para permitir a los usuarios ver los datos e interactuar con ellos como si se tratase de una colección de carpetas y archivos. Los objetos de carpeta de la extensión de espacio de nombres deben interactuar con Windows Explorer como si fueran carpetas normales. Antes de intentar implementar una extensión de espacio de nombres, primero debe comprender cómo Windows Explorer controla un objeto de carpeta.

## <a name="the-default-system-folder-view-object-defview"></a>El objeto de vista de carpeta del sistema predeterminado (DefView)

Shell proporciona una implementación predeterminada de la vista de carpeta, conocida coloquialmente como DefView, para que pueda evitar gran parte del trabajo de implementar su propia extensión de espacio de nombres. Dado que algunas características de vista no se pueden lograr a través de vistas personalizadas, a menudo se recomienda usar el objeto de vista de carpeta del sistema predeterminado en lugar de una vista personalizada. Para obtener más información, [**vea SHCreateShellFolderView.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview)

## <a name="how-windows-explorer-interacts-with-a-namespace-extension"></a>Cómo Windows explorer interactúa con una extensión de espacio de nombres

Windows El Explorador proporciona a los usuarios una GUI que les permite realizar una variedad de tareas, entre las que se incluyen:

-   [Navegar por la](navigate.md) jerarquía de espacios de nombres y ver el contenido de las carpetas.
-   [Administrar](manage.md) el contenido del espacio de nombres moviendo, eliminando y copiando objetos.
-   [Recuperación](folder-info.md) de una variedad de información sobre los objetos .
-   [Iniciar](launch.md) aplicaciones.

La GUI Windows Explorer tiene cinco componentes básicos. En la ilustración siguiente se denominan los componentes y se muestra dónde se muestran normalmente en Windows Explorer.

![ilustración que muestra los componentes de la interfaz de usuario del Explorador de Windows ](images/nse1.png)

Cuando un usuario muestra una carpeta que pertenece a una extensión de espacio de nombres en Windows Explorer, el objeto de carpeta tiene al menos un control parcial sobre el contenido de las cinco áreas.

### <a name="tree-view"></a>Vista de árbol

La vista de árbol proporciona una vista de alto nivel del espacio de nombres . Esta área hospeda un [control de vista de árbol](../controls/tree-view-controls.md) que puede mostrar cada carpeta de espacio de nombres y la posición de la carpeta en la jerarquía de espacios de nombres. Un usuario puede realizar varias operaciones con el área de vista de árbol, entre las que se incluyen:

-   Mostrar u ocultar el siguiente nivel en el espacio de nombres .
-   Copiar, mover o eliminar carpetas.
-   Haga clic con el botón derecho en una carpeta para mostrar un menú contextual.
-   Seleccionar una carpeta y ver su contenido en la vista de carpetas.

La vista de árbol se comunica con objetos de carpeta principalmente a través de su [**interfaz IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Por ejemplo, cuando un usuario hace clic en el signo más (+) junto al icono de la carpeta, Windows Explorer expande la pantalla para mostrar las subcarpetas de la carpeta. Para obtener la información necesaria para actualizar la vista de árbol, el Shell realiza varias llamadas a la interfaz **IShellFolder** del objeto de carpeta para:

-   Solicite los atributos de la carpeta.
-   Enumerar el contenido de la carpeta.
-   Solicite nombres para mostrar para cada subcarpeta.
-   Solicite un icono para mostrar junto a cada carpeta.

Windows A continuación, el Explorador actualiza la vista de árbol para mostrar las subcarpetas de la carpeta seleccionada. Si las subcarpetas tienen subcarpetas, se muestra un carácter "+" junto a su icono de carpeta. Hay una serie de tareas más sofisticadas que un usuario también puede realizar con la vista de árbol, entre las que se incluyen:

-   Usar el Portapapeles para cortar o copiar una carpeta y pegarla en otra carpeta.
-   Usar arrastrar y colocar para cortar o copiar una carpeta y colocarla en otra carpeta.
-   Usar un motor de búsqueda para buscar elementos en una carpeta o en sus subcarpetas.
-   Modificar las propiedades de la carpeta.

Para obtener una explicación más detallada de cómo una extensión de espacio de nombres controla estas acciones del usuario, vea [Implementing the Basic Folder Object Interfaces](nse-implement.md).

### <a name="folder-view"></a>Vista de carpeta

Cuando un usuario selecciona una carpeta, el contenido de la carpeta se muestra en la vista de carpeta. Hasta cierto punto, la funcionalidad normal de la vista de carpeta se superpone con la vista de árbol. Los usuarios pueden mover o copiar carpetas, cambiar las propiedades de la carpeta, ver el contenido de una subcarpeta, mostrar un menú contextual para una carpeta, y así sucesivamente. Sin embargo, hay algunas diferencias distintas entre la vista de árbol y la vista de carpeta:

-   La vista carpeta muestra solo el contenido de una sola carpeta, no parte ni toda la jerarquía de espacios de nombres.
-   La vista carpeta muestra objetos de archivo, así como objetos de carpeta.
-   La vista carpeta puede mostrar mucha más información sobre los objetos que la vista de árbol.
-   La vista carpeta permite que las extensiones de espacio de nombres tengan un control casi completo sobre qué información se muestra y cómo. Solo se pueden modificar aspectos menores de la vista de árbol, como los iconos de carpeta.

A diferencia de la vista de árbol, Windows explorador no controla directamente el contenido de la vista de carpeta. La vista de carpeta es un área que Windows Explorer proporciona a los objetos de carpeta. Mostrar y administrar el contenido de una carpeta en la vista de carpetas es responsabilidad del objeto de carpeta. Aunque la mayoría de las vistas de carpetas siguen un formato bastante estándar, en realidad hay algunas limitaciones sobre lo que se puede mostrar o cómo. Un caso extremo es la carpeta internet, que es un explorador completo.

Cuando un usuario selecciona una carpeta que pertenece a la extensión de espacio de nombres, se crea una ventana y se pasa su identificador a Windows Explorer. Esta ventana se convierte en un elemento secundario de la ventana de vista de carpetas. Windows El Explorador proporciona las dimensiones de la ventana de vista de carpetas, pero no establece restricciones en el contenido de la ventana secundaria. A continuación, puede usar la ventana secundaria para mostrar la vista de carpeta de la carpeta.

Las extensiones de espacio de nombres usan uno de estos dos enfoques para crear una vista de carpeta:

-   Use la ventana secundaria para hospedar un control [de vista de](../controls/list-view-control-reference.md) lista. Este control permite mostrar el contenido de una carpeta de la misma manera que la vista clásica Windows [Explorer.](../lwef/web-view.md)
-   Use la ventana secundaria para hospedar un [control WebBrowser y](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752044(v=vs.85)) use un documento HTML dinámico (DHTML) para mostrar el contenido de la carpeta.

Ambos enfoques muestran una vista de carpeta muy similar a la que se muestra para las carpetas del sistema. Sin embargo, si desea usar un esquema de presentación diferente, puede hacerlo libremente.

### <a name="menu-bar-and-toolbars"></a>Barra de menús y barras de herramientas

Al igual que Windows aplicaciones, Windows Explorer proporciona al usuario una colección de herramientas. Hay disponible una selección completa de herramientas a través de la barra de menús. Las herramientas más usadas también se representan mediante botones o cuadros de edición en una barra de herramientas. A diferencia de Windows, la barra de menús Windows Explorer es realmente un [control](../controls/toolbar-control-reference.md) de barra de herramientas que se ha personalizado para que se comporte como un menú convencional. Tanto la barra de menús como la barra de herramientas se incorporan en un [control rebar](../controls/rebar-control-reference.md) para permitir a los usuarios organizar los controles individuales para satisfacer sus necesidades.

De forma predeterminada, Windows Explorer admite un conjunto estándar de botones y elementos de menú, como Copiar y Propiedades. La extensión de espacio de nombres puede personalizar la barra de menús y las barras de herramientas mediante la eliminación de herramientas estándar y la adición de herramientas personalizadas. Cuando se inicializa el objeto de vista de carpeta, Windows Explorer pasa un puntero a su [**interfaz IShellBrowser.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) Esta interfaz admite varios métodos a los que puede llamar para personalizar la barra de menús y la barra de herramientas. Cuando el usuario selecciona uno de los elementos de menú personalizados o los botones de la barra de herramientas, Windows Explorer reenvía los mensajes WM COMMAND para los elementos de menú y barra de herramientas personalizados al procedimiento de ventana de \_ la ventana secundaria.

### <a name="status-bar"></a>Barra de estado

La Windows de estado del Explorador de archivos muestra información sobre el objeto seleccionado actualmente. La extensión de espacio de nombres puede usar la barra de estado para mostrar información de estado, como una cadena de texto. Puede personalizar la barra de estado llamando a [**IShellBrowser.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser)

 

 
