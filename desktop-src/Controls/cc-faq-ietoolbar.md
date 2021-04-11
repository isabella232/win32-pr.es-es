---
title: Cómo crear una barra de herramientas de Explorer-Style de Internet
description: Una de las principales características de la interfaz de usuario de Windows Internet Explorer es la barra de herramientas. No solo ofrece a los usuarios acceso a una amplia gama de características, sino que también permite a los usuarios personalizar su diseño según sus preferencias personales.
ms.assetid: d24969ec-4dea-44c6-b045-5611de8f1cce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32228f941a7c7e1253884ab5d72368f66f25c7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149667"
---
# <a name="how-to-create-an-internet-explorer-style-toolbar"></a>Cómo crear una barra de herramientas de Explorer-Style de Internet

Una de las principales características de la interfaz de usuario de Windows Internet Explorer es la barra de herramientas. No solo ofrece a los usuarios acceso a una amplia gama de características, sino que también permite a los usuarios personalizar su diseño según sus preferencias personales.

En la captura de pantalla siguiente se muestra la barra de herramientas de Internet Explorer y se resaltan algunas de las características clave.

![captura de pantalla de la barra de herramientas de Windows Internet Explorer, con etiquetas para ocho características](images/howto1a.jpg)

Esta barra de herramientas consta esencialmente de un control rebar con cuatro bandas: tres barras de herramientas y una barra de menús. Dado que se implementa con la API de controles comunes, los desarrolladores pueden crear barras de herramientas con todas o algunas de sus características. En este tema se describen las características esenciales de la barra de herramientas de Internet Explorer y cómo implementarlas en la aplicación.

-   [El control rebar](#the-rebar-control)
    -   [Implementar el control rebar](#implementing-the-rebar-control)
-   [Las barras de herramientas](#how-to-create-an-internet-explorer-style-toolbar)
    -   [Botones desplegables](#drop-down-buttons)
    -   [Botones de estilo de lista](#list-style-buttons)
    -   [Comillas angulares](#handling-chevrons)
    -   [Seguimiento activo](#hot-tracking)
-   [Temas relacionados](#related-topics)

## <a name="the-rebar-control"></a>El control rebar

La estructura subyacente de la barra de herramientas de Internet Explorer se proporciona mediante un [control rebar](rebar-controls.md). Este control proporciona a los usuarios una manera de personalizar la organización de una colección de herramientas. Cada rebar contiene una o más *bandas*, que suelen ser largas, rectángulos estrechos que contienen una ventana secundaria, normalmente un control de barra de herramientas.

El control rebar muestra sus bandas en un área rectangular, normalmente en la parte superior de la ventana. Este rectángulo se divide en una o más bandas que son el alto de una banda. Cada banda puede estar en una franja independiente o se pueden colocar varias bandas en la misma banda.

Un control rebar proporciona a los usuarios dos maneras de organizar sus herramientas:

-   Cada banda tiene normalmente un *agarrador* en su borde izquierdo. Se usan barras de redimensionamiento cuando dos o más bandas en una sola franja superan el ancho de la ventana. Al arrastrar el agarrador hacia la izquierda o la derecha, los usuarios pueden controlar la cantidad de espacio que se asigna a cada banda.
-   Los usuarios pueden mover las bandas dentro del rectángulo de visualización del rebar arrastrando y colocando. Después, el control rebar cambia la presentación para acomodar la nueva organización de bandas. Si todas las bandas se quitan de una franja, se reducirá el alto del rebar, ampliando el área de visualización.

Una aplicación puede Agregar o quitar bandas según sea necesario. Normalmente, las aplicaciones permiten a los usuarios seleccionar qué bandas desean mostrar en el menú Ver o en un menú contextual.

Si el ancho combinado de las bandas de una franja supera el ancho de la ventana, el control rebar ajustará sus anchos según sea necesario. Es posible que algunas de las herramientas estén tratadas por la banda adyacente.

La [versión 5,80](common-control-versions.md) de los controles comunes proporciona una manera de hacer que las herramientas que se han incluido en otra banda estén accesibles para el usuario. Si establece la marca RBBS \_ USECHEVRON en el miembro **fStyle** de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) de la banda, se mostrará un *botón de contenido adicional* para las barras de herramientas que se han tratado. Cuando un usuario hace clic en el botón de contenido adicional, se muestra un menú que le permite usar las herramientas ocultas. La siguiente captura de pantalla de Microsoft Internet Explorer 6 muestra el menú que se muestra cuando se trata parte de la barra de herramientas estándar.

![captura de pantalla que muestra el menú que se muestra al hacer clic en el botón de contenido adicional](images/howto2.jpg)

Puesto que cada banda contiene un control, puede proporcionar flexibilidad adicional a través de la API del control. Por ejemplo, puede implementar la personalización de la barra de herramientas para permitir que el usuario agregue, mueva o elimine botones en una barra de herramientas.

### <a name="implementing-the-rebar-control"></a>Implementar el control rebar

La mayoría de las características de la barra de herramientas de Internet Explorer se implementan realmente en las bandas individuales. La implementación del propio control rebar es sencilla y se muestra a continuación.

1.  Cree el control rebar con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Establezca *dwExStyle* en la ventana de configuración de [**WS \_ ex \_**](/windows/desktop/winmsg/extended-window-styles) y *lpClassName* en [**REBARCLASSNAME**](common-control-window-classes.md). Internet Explorer usa los siguientes estilos de ventana:

    -   [**BANDBORDERS de RBS \_**](rebar-control-styles.md)
    -   [**DBLCLKTOGGLE de RBS \_**](rebar-control-styles.md)
    -   [**REGISTERDROP de RBS \_**](rebar-control-styles.md)
    -   [**VARHEIGHT de RBS \_**](rebar-control-styles.md)
    -   [**CCS \_ divisor**](common-control-styles.md)
    -   [**CCS \_ NOPARENTALIGN**](common-control-styles.md)
    -   [**\_borde WS**](/windows/desktop/winmsg/window-styles)
    -   [**\_elemento secundario WS**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPCHILDREN**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ visible**](/windows/desktop/winmsg/window-styles)

    Establezca los otros parámetros según sea necesario para la aplicación.

2.  Cree un control con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o una función de creación de controles especializada como [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex).
3.  Inicialice una banda para el control rellenando los miembros de [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa). Incluya el \_ estilo RBBS USECHEVRON con el miembro **fStyle** para habilitar las comillas angulares.
4.  Agregue la banda al control rebar con un mensaje [**de \_ INSERTBAND de RB**](rb-insertband.md) .
5.  Repita los pasos 2-4 para las bandas restantes.
6.  Implementar Controladores para las notificaciones rebar. En concreto, tendrá que controlar [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) para mostrar un menú desplegable cuando se haga clic en un botón de contenido adicional. Para obtener más información, vea [controlar las comillas angulares](#handling-chevrons).

De forma predeterminada, se incluyen los agarradores. Para omitir el agarrador de una banda, establezca la \_ marca RBBS NOagarrator en el miembro **fStyle** de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) de la banda. Para obtener más información sobre la implementación de controles Rebar, vea [acerca de los controles rebar](rebar-controls.md).

### <a name="handling-chevrons"></a>Controlar cheurones

Cuando un usuario hace clic en un botón de contenido adicional, el control rebar envía una notificación [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) a la aplicación. La estructura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que se pasa con la notificación contiene el identificador de la banda y una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) con el rectángulo ocupado por el botón de contenido adicional. El controlador debe determinar qué botones están ocultos y mostrar los comandos asociados en un menú emergente.

En el procedimiento siguiente se describe cómo controlar una notificación de [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) :

1.  Recupera el rectángulo delimitador actual para la banda seleccionada enviando el control rebar a un mensaje [**\_ GETRECT de RB**](rb-getrect.md) .
2.  Recupere el número total de botones mediante el envío del control de barra de herramientas de la banda a un mensaje de [**TB \_ BUTTONCOUNT**](tb-buttoncount.md) .
3.  Empezando por el botón situado más a la izquierda, recupere el rectángulo delimitador del botón enviando el control de barra de herramientas a un mensaje de [**TB \_ GETITEMRECT**](tb-getitemrect.md) .
4.  Pase los rectángulos de banda y de botón a la función [**IntersectRect**](/windows/desktop/api/winuser/nf-winuser-intersectrect) . Esta función devolverá una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que corresponde a la parte visible del botón.
5.  Pase el rectángulo del botón y el rectángulo de la parte visible del botón a la función [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) .
6.  Si [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) devuelve **true**, todo el botón es visible. Repita los pasos 3-5 para el botón siguiente en la barra de herramientas. Si **EqualRect** devuelve **false**, el botón está al menos parcialmente oculto y todos los botones restantes se ocultan por completo. Continúe con el paso siguiente.
7.  Cree un menú emergente con elementos para cada uno de los botones ocultos.
8.  Mostrar el menú emergente mediante la función [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) . Use el rectángulo de cheurones que se pasó con la notificación [ \_ CHEVRONPUSHED de RBN](rbn-chevronpushed.md) para colocar el menú. El menú debe estar justo debajo del botón de contenido adicional, con los bordes alineados a la izquierda.
9.  Controle los comandos de menú.

## <a name="the-toolbars"></a>Las barras de herramientas

La mayor parte de la complejidad de la barra de herramientas de Internet Explorer se basa en la implementación de controles que componen las bandas rebar. Internet Explorer suele mostrar cuatro bandas:

-   Barra de menús
-   Barra de herramientas estándar
-   Barra de herramientas de vínculos
-   Barra de herramientas dirección

Todas estas bandas, incluida la barra de menús, contienen controles de barra de herramientas. En esta sección se describe la implementación de las barras de herramientas estándar y vínculos. La barra de menús es algo más complicada y se describe por separado en [creación de una barra de menús de Explorer-Style de Internet](cc-faq-iemenubar.md).

Los procedimientos básicos para implementar controles de barra de herramientas se describen en [acerca de los controles de barra de herramientas](toolbar-controls-overview.md). Esta sección se centra en algunas de las nuevas características de la barra de herramientas que usa Internet Explorer para aumentar la facilidad de uso del control.

-   [Botones desplegables](#drop-down-buttons)
-   [Botones de estilo de lista](#list-style-buttons)
-   [Comillas angulares](#handling-chevrons)
-   [Seguimiento activo](#hot-tracking)

### <a name="drop-down-buttons"></a>Botones desplegables

Los botones desplegables admiten varios comandos. Cuando el usuario hace clic en un botón desplegable, el botón muestra un menú emergente en lugar de iniciar un comando. El usuario inicia un comando seleccionándolo en el menú. En la captura de pantalla siguiente se muestra un botón desplegable y un menú de la barra de herramientas estándar de Internet Explorer.

![captura de pantalla que muestra el menú desplegable de correo](images/howto3.jpg)

La funcionalidad desplegable se puede Agregar a cualquier estilo de botón agregando una marca de estilo al miembro **fStyle** de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del botón. Hay tres estilos de botón desplegable, todos ellos usados por Internet Explorer:

-   Los botones desplegables sin formato tienen el estilo [**\_ desplegable BTNS**](toolbar-control-and-button-styles.md) . Aparecen como botones normales, pero muestran un menú cuando se hace clic en él, en lugar de iniciar un comando.
-   Los botones de flecha desplegable simple tienen el estilo [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) . Aparecen una flecha junto a la imagen o el texto del botón. Aparte de la diferencia en la apariencia, son idénticas a los botones desplegables sin formato. El botón correo que se usa como ejemplo en la ilustración anterior es un botón de flecha desplegable.
-   Los botones de flecha desplegable que agregan el estilo extendido [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) a la [**\_ lista**](toolbar-control-and-button-styles.md) desplegable BTNS tienen una flecha que se separa del texto o de la imagen. Este estilo de botón combina la funcionalidad de los botones desplegable y estándar. Si el usuario hace clic en la flecha, se muestra un menú y el usuario puede elegir entre varios comandos. Si el usuario hace clic en el botón adyacente, inicia un comando predeterminado. En la captura de pantalla siguiente se muestra el botón **atrás** de Internet Explorer, que utiliza una flecha separada.

    ![captura de pantalla que muestra el menú del botón de división posterior](images/howto4.jpg)

Cuando el usuario hace clic en un botón desplegable con los estilos de flecha sencillo o simple, el control de barra de herramientas envía a la aplicación una notificación de [ \_ desplegable de TBN](tbn-dropdown.md) . Cuando la aplicación recibe este mensaje, es responsable de crear y mostrar el menú y de controlar el comando seleccionado.

Cuando el usuario hace clic en una flecha separada, el control de barra de herramientas envía a la aplicación una notificación de [ \_ desplegable de TBN](tbn-dropdown.md) . La aplicación debe controlarla de la misma manera que controla los otros dos tipos de botones desplegables. Si el usuario hace clic en el botón principal, la aplicación recibe un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) con el identificador de comando del botón, como si fuera un botón estándar. Normalmente, las aplicaciones responden iniciando el comando superior en el menú desplegable, pero puede responder de forma adecuada.

### <a name="list-style-buttons"></a>Botones de List-Style

Con los botones estándar, si agrega texto, se muestra debajo del mapa de bits. En la captura de pantalla siguiente se muestran los botones de **búsqueda** y **Favoritos** de Internet Explorer con el texto de botón estándar.

![captura de pantalla que muestra la barra de herramientas buscar y favoritos con botones estándar](images/howto6.jpg)

Microsoft Internet Explorer 5 y versiones posteriores usan el estilo de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) . El texto está a la derecha del mapa de bits, lo que reduce el alto del botón y amplía el área de visualización. En la ilustración siguiente se muestran los botones **Buscar** y **Favoritos** de Internet Explorer 6 con el estilo de **\_ lista TBSTYLE** .

![captura de pantalla que muestra la barra de herramientas buscar y favoritos con botones de estilo de lista](images/howto5.jpg)

### <a name="chevrons"></a>Comillas angulares

Cuando el usuario reorganiza las bandas en el control rebar, es posible que parte de una barra de herramientas esté incluida. Si la banda se creó con el \_ estilo RBBS USECHEVRON, el control rebar mostrará un botón de contenido adicional en el borde derecho de la barra de herramientas. El usuario hace clic en el botón de contenido adicional para mostrar un menú con las herramientas ocultas.

### <a name="hot-tracking"></a>Hot-Tracking

Cuando está habilitado el seguimiento activo, se *activa* un botón cuando el cursor se sitúa sobre él. El botón de acceso frecuente se distingue normalmente de los otros botones de la barra de herramientas por una imagen distintiva. De forma predeterminada, aparece un botón activo encima del resto de la barra de herramientas. Cuando se activa un botón nuevo, la aplicación recibe una notificación de [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) . En la ilustración siguiente se muestran los botones **Buscar** y **Favoritos** de Internet Explorer 5 con un botón de **búsqueda** activa. Además de tener una apariencia en relieve, el mapa de bits gris del botón se ha reemplazado por uno coloreado.

![captura de pantalla que muestra los botones buscar y favoritos con un botón de búsqueda activa](images/howto7.jpg)

Para habilitar el seguimiento activo, cree un control de barra de herramientas con el estilo [**de \_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plano**](toolbar-control-and-button-styles.md) o TBSTYLE. Estos se conocen como barras de herramientas *sin formato* , ya que los botones individuales no se resaltan normalmente de ningún modo. Los mapas de bits se muestran simplemente unos junto a otros. Solo toman una apariencia similar a un botón cuando están activas. Estos dos estilos también son transparentes, lo que significa que el fondo de los iconos será el color de la ventana de cliente subyacente.

Para que se muestre un mapa de bits diferente cuando el botón esté activo, cree una segunda [lista de imágenes](image-lists.md) que contenga imágenes activas para todos los botones de la barra de herramientas. El tamaño y el orden de estas imágenes deben ser los mismos que los de la lista de imágenes predeterminada. Envíe el control de barra de herramientas a un mensaje de [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) para establecer la lista de imágenes activas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de una barra de menús de Explorer-Style de Internet](cc-faq-iemenubar.md)
</dt> </dl>

 

 