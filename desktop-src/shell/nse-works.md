---
description: El explorador de Windows proporciona una representación gráfica del espacio de nombres del shell combinada con las herramientas que permiten a los usuarios interactuar con los objetos de Shell.
ms.assetid: cc387338-15fa-4350-b039-61a0f1c5030a
title: Descripción de las extensiones de espacio de nombres de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0150092a25708c1f079160a9d106a7b8205e231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985647"
---
# <a name="understanding-shell-namespace-extensions"></a>Descripción de las extensiones de espacio de nombres de Shell

El explorador de Windows proporciona una representación gráfica del espacio de nombres del shell combinada con las herramientas que permiten a los usuarios interactuar con los objetos de Shell. Con una extensión de espacio de nombres, puede tomar cualquier cuerpo de datos y hacer que el explorador de Windows lo presente al usuario como una carpeta virtual. Cuando un usuario examina esta carpeta, los datos se presentan como una jerarquía estructurada en árbol de carpetas y archivos, de forma muy parecida al resto del espacio de nombres del shell. Los usuarios y las aplicaciones pueden interactuar con el contenido de esta carpeta virtual prácticamente de la misma manera que con cualquier otro objeto de espacio de nombres. En este documento se explica cómo crear una extensión de espacio de nombres.

-   [Cómo funciona una extensión de espacio de nombres](#how-a-namespace-extension-works)
-   [Objeto de vista de carpeta del sistema predeterminado (DefView)](#the-default-system-folder-view-object-defview)
-   [Cómo interactúa el explorador de Windows con una extensión de espacio de nombres](#how-windows-explorer-interacts-with-a-namespace-extension)
    -   [Vista de árbol](#tree-view)
    -   [Vista de carpetas](#folder-view)
    -   [Barra de menús y barras de herramientas](#menu-bar-and-toolbars)
    -   [Barra de estado](#status-bar)

## <a name="how-a-namespace-extension-works"></a>Cómo funciona una extensión de espacio de nombres

En segundo plano, cada carpeta que se muestra en el explorador de Windows se representa mediante un objeto de modelo de objetos componentes (COM) denominado *objeto de carpeta*. Cada vez que el usuario interactúa con una carpeta o su contenido, el Shell se comunica con el objeto de carpeta asociado a través de una serie de interfaces estándar. A continuación, el objeto de carpeta hace todo lo necesario para responder a la acción del usuario y el shell actualiza la pantalla del explorador de Windows.

La mayoría de los archivos y carpetas con los que interactúan los usuarios forman parte del sistema de archivos o de una carpeta virtual del sistema, como la papelera de reciclaje. En otra documentación se ha explicado cómo personalizar el comportamiento de estas carpetas estándar para cumplir los requisitos de la aplicación modificando el registro o implementando [controladores de extensión de Shell](handlers.md). Sin embargo, la extensión del shell de estas maneras resulta muy útil cuando la información se puede empaquetar fácilmente en forma de archivos o carpetas normales del sistema de archivos.

Hay una serie de situaciones en las que el almacenamiento de datos como una colección de archivos y carpetas del sistema de archivos podría no ser deseable o incluso imposible. Algunos ejemplos de este tipo de datos son:

-   Colección de elementos que se empaquetan de forma más eficaz en un solo archivo, como una base de datos.
-   Colección de elementos almacenados en un equipo remoto que no tiene un sistema de archivos de Windows estándar. Un ejemplo de estos datos es la información almacenada en un asistente digital personal (PDA) o una cámara digital.
-   Colección de elementos que no representan datos almacenados. Un ejemplo de estos datos son los vínculos de impresora contenidos en la carpeta Impresoras estándar.

Una manera de presentar este tipo de datos a un usuario es escribir una aplicación para permitir a los usuarios ver e interactuar con los distintos elementos. Sin embargo, si los datos se pueden presentar como una jerarquía de archivos o carpetas, gran parte de la funcionalidad que necesitará implementar puede ser servicios de interfaz de usuario que ya se proporcionan en el explorador de Windows. Un enfoque mucho más eficaz podría ser escribir una extensión de espacio de nombres y dejar que el explorador de Windows se convierta en la GUI.

Para implementar una extensión de espacio de nombres, su información debe estar organizada como un espacio de nombres estructurado en árbol. La *raíz del espacio de nombres* se presenta como una carpeta virtual en el espacio de nombres del shell. La carpeta raíz y todas sus subcarpetas y elementos de datos se convierten en parte del espacio de nombres del shell y el explorador de Windows se convierte en la interfaz de usuario. Por lo tanto, puede presentar su información al usuario de una manera conocida y accesible fácilmente con mucha menos programación de la interfaz de usuario de la que sería necesaria para una aplicación personalizada.

Una extensión de espacio de nombres consta de dos componentes básicos:

-   Un administrador de datos
-   Una interfaz entre el administrador de datos y el explorador de Windows

El primer componente de la lista es totalmente suya. Puede almacenar y administrar los datos de la manera más eficaz. El segundo componente es el código necesario para empaquetar los datos como objetos de carpeta y controlar la interacción con el explorador de Windows. Después, el explorador de Windows puede llamar a estos objetos para que los usuarios puedan ver los datos e interactuar con ellos como si se tratara de una colección de carpetas y archivos. Los objetos de carpeta de la extensión de espacio de nombres deben interactuar con el explorador de Windows como si fueran carpetas normales. Antes de intentar implementar una extensión de espacio de nombres, primero debe comprender cómo controla el explorador de Windows un objeto de carpeta.

## <a name="the-default-system-folder-view-object-defview"></a>Objeto de vista de carpeta del sistema predeterminado (DefView)

El Shell proporciona una implementación predeterminada de la vista de carpetas, suele conocida como DefView, para que pueda evitar gran parte del trabajo de implementar su propia extensión de espacio de nombres. Dado que algunas características de vista no se pueden lograr mediante vistas personalizadas, a menudo se recomienda usar el objeto de vista de carpeta del sistema predeterminado en lugar de una vista personalizada. Para obtener más información, vea [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview).

## <a name="how-windows-explorer-interacts-with-a-namespace-extension"></a>Cómo interactúa el explorador de Windows con una extensión de espacio de nombres

El explorador de Windows proporciona a los usuarios una GUI que les permite realizar diversas tareas, entre las que se incluyen:

-   [Navegar](navigate.md) por la jerarquía de espacios de nombres y ver el contenido de las carpetas.
-   [Administrar](manage.md) el contenido del espacio de nombres moviendo, eliminando y copiando objetos.
-   [Recuperar](folder-info.md) una gran variedad de información acerca de los objetos.
-   [Iniciar](launch.md) aplicaciones.

La GUI del explorador de Windows tiene cinco componentes básicos. La siguiente ilustración nombra los componentes de y muestra dónde se muestran normalmente en el explorador de Windows.

![Ilustración que muestra los componentes de la interfaz de usuario del explorador de Windows ](images/nse1.png)

Cuando un usuario muestra una carpeta que pertenece a una extensión de espacio de nombres en el explorador de Windows, el objeto de carpeta tiene al menos el control parcial sobre el contenido de las cinco áreas.

### <a name="tree-view"></a>Vista de árbol

La vista de árbol proporciona una vista de alto nivel del espacio de nombres. Esta área hospeda un [control de vista de árbol](../controls/tree-view-controls.md) que puede mostrar cada carpeta de espacio de nombres y la posición de la carpeta en la jerarquía de espacios de nombres. Un usuario puede realizar varias operaciones con el área de vista de árbol, entre las que se incluyen:

-   Mostrar u ocultar el siguiente nivel en el espacio de nombres.
-   Copiar, mover o eliminar carpetas.
-   Haga clic con el botón secundario en una carpeta para mostrar un menú contextual.
-   Seleccionar una carpeta y ver su contenido en la vista de carpetas.

La vista de árbol se comunica con objetos de carpeta principalmente a través de su interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Por ejemplo, cuando un usuario hace clic en el signo más (+) situado junto al icono de la carpeta, el explorador de Windows expande la pantalla para mostrar las subcarpetas de la carpeta. Para obtener la información necesaria para actualizar la vista de árbol, el shell realiza varias llamadas a la interfaz **IShellFolder** del objeto de carpeta para:

-   Solicite los atributos de la carpeta.
-   Enumerar el contenido de la carpeta.
-   Solicitar nombres para mostrar para cada subcarpeta.
-   Solicite que se muestre un icono junto a cada carpeta.

Después, el explorador de Windows actualiza la vista de árbol para mostrar las subcarpetas de la carpeta seleccionada. Si las subcarpetas tienen subcarpetas, se muestra un carácter "+" junto a su icono de carpeta. Hay una serie de tareas más sofisticadas que un usuario puede realizar también con la vista de árbol, entre las que se incluyen:

-   Usar el portapapeles para cortar o copiar una carpeta y pegarla en otra carpeta.
-   Usar arrastrar y colocar para cortar o copiar una carpeta y colocarla en otra carpeta.
-   Uso de un motor de búsqueda para buscar elementos en una carpeta o en sus subcarpetas.
-   Modificar las propiedades de la carpeta.

Para obtener una explicación más detallada de cómo una extensión de espacio de nombres controla estas acciones de usuario, vea [implementar las interfaces de objeto de carpeta básicas](nse-implement.md).

### <a name="folder-view"></a>Vista de carpetas

Cuando un usuario selecciona una carpeta, el contenido de la carpeta se muestra en la vista de carpetas. En cierta medida, la funcionalidad normal de la vista de carpeta se superpone con la vista de árbol. Los usuarios pueden moverse o copiar carpetas, cambiar las propiedades de la carpeta, ver el contenido de una subcarpeta, mostrar un menú contextual para una carpeta, etc. Sin embargo, hay algunas diferencias diferenciales entre la vista de árbol y la vista de carpetas:

-   La vista de carpetas muestra solo el contenido de una sola carpeta, no de una parte o de toda la jerarquía de espacios de nombres.
-   La vista de carpetas muestra objetos de archivo y objetos de carpeta.
-   La vista de carpetas puede mostrar mucha más información sobre los objetos que la vista de árbol.
-   La vista de carpetas permite que las extensiones de espacio de nombres tengan un control casi completo sobre la información que se muestra y cómo. Solo se pueden modificar los aspectos secundarios de la vista de árbol, como los iconos de carpeta.

A diferencia de la vista de árbol, el explorador de Windows no controla directamente el contenido de la vista de carpetas. La vista de carpetas es un área que el explorador de Windows proporciona a los objetos de carpeta. Mostrar y administrar el contenido de una carpeta en la vista de carpeta es responsabilidad del objeto de carpeta. Aunque la mayoría de las vistas de carpeta siguen un formato bastante estándar, existen algunas limitaciones en lo que se puede mostrar o cómo. Un caso extremo es la carpeta de Internet, que es un explorador con todas las características.

Cuando un usuario selecciona una carpeta que pertenece a la extensión de espacio de nombres, crea una ventana y pasa su identificador al explorador de Windows. Esta ventana se convierte en un elemento secundario de la ventana vista de carpetas. El explorador de Windows proporciona las dimensiones de la ventana de vista de carpetas pero no impone restricciones en el contenido de la ventana secundaria. Después, puede usar la ventana secundaria para mostrar la vista de carpetas de la carpeta.

Las extensiones de espacio de nombres usan uno de los dos métodos para crear una vista de carpetas:

-   Use la ventana secundaria para hospedar un control de [vista de lista](../controls/list-view-control-reference.md) . Este control permite mostrar el contenido de una carpeta de forma muy similar a la [vista clásica](../lwef/web-view.md)del explorador de Windows.
-   Use la ventana secundaria para hospedar un [control WebBrowser](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752044(v=vs.85)) y use un documento HTML dinámico (DHTML) para mostrar el contenido de la carpeta.

Ambos enfoques muestran una vista de carpeta que se parece mucho a la que se muestra para las carpetas del sistema. Sin embargo, si desea usar un esquema de presentación diferente, puede hacerlo de forma gratuita.

### <a name="menu-bar-and-toolbars"></a>Barra de menús y barras de herramientas

Como la mayoría de las aplicaciones de Windows, el explorador de Windows proporciona al usuario una colección de herramientas. En la barra de menús está disponible una selección completa de herramientas. Las herramientas de uso más frecuente también se representan mediante botones o cuadros de edición en una barra de herramientas. A diferencia de muchas aplicaciones de Windows, la barra de menús del explorador de Windows es en realidad un [control de barra de herramientas](../controls/toolbar-control-reference.md) que se ha personalizado para que se comporte como un menú convencional. La barra de menús y la barra de herramientas se incorporan en un [control rebar](../controls/rebar-control-reference.md) para que los usuarios puedan organizar los controles individuales para que se adapten a sus necesidades.

De forma predeterminada, el explorador de Windows admite un conjunto estándar de botones y elementos de menú, como copiar y propiedades. La extensión de espacio de nombres puede personalizar la barra de menús y las barras de herramientas eliminando herramientas estándar y agregando herramientas personalizadas. Cuando se inicializa el objeto de vista de carpeta, el explorador de Windows pasa un puntero a su interfaz [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) . Esta interfaz admite varios métodos a los que se puede llamar para personalizar la barra de menús y la barra de herramientas. Cuando el usuario selecciona uno de los elementos de menú o botones de la barra de herramientas personalizados, el explorador de Windows reenvía \_ los mensajes de comandos de WM para los elementos de menú y de barra de herramientas personalizados al procedimiento de ventana de la ventana secundaria.

### <a name="status-bar"></a>Barra de estado

La barra de estado del explorador de Windows muestra información sobre el objeto seleccionado actualmente. La extensión de espacio de nombres puede usar la barra de estado para mostrar información de estado, como una cadena de texto. Puede personalizar la barra de estado mediante una llamada a [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser).

 

 
