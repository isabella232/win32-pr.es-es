---
title: Creación de una barra de menús de Explorer-Style de Internet
description: A primera vista, la barra de menús de Microsoft Internet Explorer 5 y versiones posteriores tiene un aspecto similar al de un menú estándar. Sin embargo, tiene un aspecto bastante diferente cuando empieza a usarlo.
ms.assetid: e0fe25f2-3d49-4c5a-a3f9-2f468f2cfef2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b262bc55407d263c97d4bd7e3938a9794d3a58f5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904844"
---
# <a name="how-to-create-an-internet-explorer-style-menu-bar"></a>Creación de una barra de menús de Explorer-Style de Internet

A primera vista, la barra de menús de Microsoft Internet Explorer 5 y versiones posteriores tiene un aspecto similar al de un menú estándar. Sin embargo, tiene un aspecto bastante diferente cuando empieza a usarlo.

En la captura de pantalla siguiente se muestra la barra de menús de Windows Internet Explorer con el menú herramientas seleccionado.

![captura de pantalla que muestra la barra de menús de Windows Internet Explorer, con el menú herramientas seleccionado](images/howto8.jpg)

La barra de menús es en realidad un control de barra de herramientas que se parece a un menú estándar. En lugar de los elementos de menú de nivel superior, una barra de menús tiene una serie de botones de solo texto que muestran un menú desplegable cuando se hace clic en él. Sin embargo, como un tipo especializado de barra de herramientas, una barra de menús tiene algunas capacidades que carecen de los menús estándar:

-   Se puede personalizar mediante técnicas de barra de herramientas estándar, lo que permite al usuario desplace, elimine o agregue elementos.
-   Puede tener un seguimiento activo, de modo que los usuarios sepan cuándo están sobre un elemento de nivel superior sin tener que hacer clic primero en él.

Una barra de menús se puede incorporar a un control rebar, lo que le ofrece las siguientes características:

-   Puede tener un agarrador, que permite al usuario desplace o cambie el tamaño de la banda.
-   Puede compartir una franja en el control rebar con otras bandas, como la barra de herramientas estándar de la ilustración anterior.
-   Puede mostrar un botón de contenido adicional cuando está incluido en una banda adyacente, lo que permite al usuario acceder a los elementos ocultos.
-   Puede tener un mapa de bits de fondo definido por la aplicación.

En este tema se describe cómo implementar una barra de menús. Puesto que una barra de menús es una implementación especializada de un control de barra de herramientas, el foco se centrará en los temas específicos de las barras de menús. Para obtener una explicación de cómo incorporar una barra de herramientas a un control rebar, vea [Cómo crear una barra de herramientas de Explorer-Style de Internet](cc-faq-ietoolbar.md) y [acerca de los controles rebar](rebar-controls.md).

-   [Crear una barra de herramientas en una barra de menús](#making-a-toolbar-into-a-menu-bar)
-   [Controlar la navegación con el menú Hot-Tracking deshabilitado](#handling-navigation-with-menu-hot-tracking-disabled)
    -   [Navegación con el mouse](#mouse-navigation)
    -   [Navegación con el teclado](#keyboard-navigation)
    -   [Navegación mixta](#mixed-navigation)
-   [Controlar la navegación con el Hot-Tracking de menús habilitado](#handling-navigation-with-menu-hot-tracking-enabled)
    -   [Procesamiento de mensajes para el seguimiento activo de menús](#message-processing-for-menu-hot-tracking)
    -   [Navegación con el mouse](#mouse-navigation)
    -   [Navegación con el teclado](#keyboard-navigation)

## <a name="making-a-toolbar-into-a-menu-bar"></a>Crear una barra de herramientas en una barra de menús

Para crear una barra de herramientas en una barra de menús:

-   Cree una barra de herramientas plana incluyendo [**TBSTYLE \_ plano**](toolbar-control-and-button-styles.md) con las demás marcas de estilo de ventana. El **estilo \_ plano TBSTYLE** también habilita el seguimiento activo. Con este estilo, la barra de menús tiene un aspecto muy similar al de un menú estándar hasta que el usuario activa un botón. A continuación, el botón parece salir de la barra de herramientas y dejar de presionar cuando se hace clic en él, al igual que un botón estándar. Dado que está habilitado el seguimiento activo, todo lo que se necesita para activar un botón es que el cursor mantenga el mouse sobre él. Si el cursor se mueve a otro botón, se activará y se desactivará el botón anterior.
-   Cree botones de estilo de lista incluyendo [**la \_ lista TBSTYLE**](toolbar-control-and-button-styles.md) con las demás marcas de estilo de ventana. Este estilo crea un botón más delgado que es más parecido a un elemento de menú de nivel superior estándar.
-   Para que los botones sean de solo texto, establezca el miembro **iBitmap** de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del botón en I \_ IMAGENONE y el miembro **iString** en el texto del botón.
-   Asigne a cada botón el estilo de [**\_ lista desplegable BTNS**](toolbar-control-and-button-styles.md) . Al hacer clic en el botón, el control de barra de herramientas envía a la aplicación una notificación [ \_ desplegable de TBN](tbn-dropdown.md) para pedirle que muestre el menú del botón.
-   Incorpore la barra de menús en una banda rebar. Habilite los agarradores y las comillas angulares, como [se describe en cómo crear una barra de herramientas de Explorer-Style de Internet](cc-faq-ietoolbar.md).
-   Implemente un controlador [ \_ desplegable de TBN](tbn-dropdown.md) para mostrar el *menú* desplegable del botón cuando se haga clic en él. El menú desplegable es un tipo de menú emergente. Se crea mediante la función [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) , con la esquina superior izquierda alineada con la esquina inferior izquierda del botón.
-   Implemente la navegación con el teclado, de modo que la barra de menús sea totalmente accesible sin un mouse.
-   Implemente el seguimiento activo del menú. Con los menús estándar, una vez que se muestra el menú de un elemento de menú de nivel superior, al mover el cursor sobre otro elemento de nivel superior, se muestra automáticamente el menú y se contrae el menú del elemento anterior. El control de barra de herramientas realizará un seguimiento del cursor y cambiará la imagen del botón, pero mostrará automáticamente el nuevo menú. La aplicación debe hacerlo explícitamente.

La mayoría de estos elementos son sencillos de implementar y se tratan en otro lugar. Vea [Cómo crear una barra de herramientas de Explorer-Style de Internet](cc-faq-ietoolbar.md), [acerca de los controles de barra de herramientas](toolbar-controls-overview.md)o acerca de [los controles rebar](rebar-controls.md) para obtener una explicación general sobre cómo utilizar las barras de herramientas y los controles rebar. Vea [menús](/windows/desktop/menurc/menus) para obtener una explicación de cómo controlar los menús emergentes. En el resto de este tema se explican los dos últimos elementos, la navegación con el teclado y el seguimiento de los menús.

## <a name="handling-navigation-with-menu-hot-tracking-disabled"></a>Controlar la navegación con el menú Hot-Tracking deshabilitado

Los usuarios pueden elegir entre desplazarse por la barra de menús con el mouse, el teclado o una combinación de ambos. Para implementar la navegación por la barra de menús, la aplicación debe controlar las notificaciones de la barra de herramientas y supervisar el mouse y el teclado. Esta tarea se puede dividir en dos partes distintas: con y sin seguimiento activo de menús. En esta sección se describe cómo controlar la navegación cuando no se muestra ningún menú y el seguimiento activo del menú no está habilitado.

### <a name="mouse-navigation"></a>Navegación con el mouse

Si el seguimiento activo de menú está deshabilitado, puede tratar una barra de menús como una barra de herramientas normal. Si el usuario navega por un mouse, todo lo que tiene que hacer la aplicación es controlar la notificación de [ \_ desplegable TBN](tbn-dropdown.md) . Cuando se reciba esta notificación, mostrar el menú desplegable correspondiente y habilitar el seguimiento activo del menú. A partir de ese entonces, se encontrará en el régimen de seguimiento de cambios activos descrito en [controlar la navegación con el menú Hot-Tracking habilitado](#handling-navigation-with-menu-hot-tracking-enabled).

Como se describe en [navegación mixta](#mixed-navigation), también debe controlar la notificación [de \_ HOTITEMCHANGE de TBN](tbn-hotitemchange.md) para realizar un seguimiento del botón activo. Esta notificación es irrelevante si el usuario solo está navegando con el mouse, pero es necesario cuando se mezcla la navegación con el mouse y el teclado.

### <a name="keyboard-navigation"></a>Navegación mediante teclado

Como se indicó en la sección anterior, el usuario puede realizar una serie de operaciones de navegación con el teclado cuando el seguimiento activo del menú está deshabilitado. Los controles de barra de herramientas solo admiten la navegación con el teclado si tienen el foco. Tampoco controlan todas las pulsaciones de teclas necesarias para las barras de menús. La solución más sencilla para controlar la navegación mediante el teclado es procesar explícitamente los eventos de presión de teclas relevantes.

Si el seguimiento activo de menú está deshabilitado, la aplicación debe controlar estos eventos de pulsación de teclas de la siguiente manera:

-   Tecla F10. Active el primer botón con [**TB \_ SETHOTITEM**](tb-sethotitem.md).
-   Las teclas de flecha izquierda y derecha. Active el botón adyacente con [**TB \_ SETHOTITEM**](tb-sethotitem.md). Si el usuario intenta navegar fuera de cualquier extremo de la barra de menús, active el primer botón en el extremo opuesto.
-   Tecla ESCAPE. Desactivar el botón activo con [**TB \_ SETHOTITEM**](tb-sethotitem.md). La barra de menús debe devolverse al estado que tenía antes de activar el primer botón.
-   Tecla de aceleración de *tecla* Alt. Use el mensaje [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) para determinar a qué botón corresponde el carácter de *tecla* . Mostrar el menú desplegable del botón y habilitar el seguimiento activo del menú.
-   Tecla FLECHA ABAJO. Si un botón está activo pero no se ha mostrado ningún menú, muestre el menú del botón y habilite el seguimiento activo del menú.
-   Tecla ENTRAR. Desactivar el botón activo con [**TB \_ SETHOTITEM**](tb-sethotitem.md). La barra de menús debe devolverse al estado que tenía antes de activar el primer botón.

### <a name="mixed-navigation"></a>Navegación mixta

Los controladores de navegación de teclado descritos en la sección anterior básicamente realizan dos tareas: realizar un seguimiento del botón activo y mostrar el menú adecuado cuando se selecciona un botón. Estos controladores son suficientes siempre que el usuario navegue solo con el teclado. Sin embargo, los usuarios suelen mezclar la navegación con el teclado y el mouse. Por ejemplo, pueden activar el primer botón con la tecla F10, usar el mouse para activar otro botón y, a continuación, abrir su menú con la tecla flecha abajo. Si solo está supervisando las pulsaciones de teclas para realizar un seguimiento de la clave activa, se mostrará el menú equivocado. También debe controlar la notificación [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) para realizar un seguimiento preciso del botón activo.

## <a name="handling-navigation-with-menu-hot-tracking-enabled"></a>Controlar la navegación con el Hot-Tracking de menús habilitado

Cuando el seguimiento activo del menú está habilitado, la aplicación debe cambiar la manera en que responde a la navegación del usuario. Para replicar el comportamiento de los menús estándar, debe implementar las siguientes características explícitamente.

Con la navegación del mouse:

-   Si el usuario mueve el cursor sobre otro botón, ese menú aparece inmediatamente y desaparece el menú anterior.
-   El seguimiento activo del menú permanece activo hasta que el usuario selecciona un comando o hace clic en un punto que no forma parte de la región del menú. Cualquier acción desactiva el seguimiento activo del menú hasta que se hace clic en otro botón.
-   Si el cursor se desplaza fuera del menú, el menú desplegable actual permanece hasta que el cursor se desplaza de nuevo a, o cuando el usuario hace clic en un punto externo, el área que se incluye en el menú. Si el cursor vuelve a un botón diferente del que se muestra actualmente, se contrae el menú anterior y se muestra el menú nuevo.

Con la navegación mediante el teclado:

-   La tecla de flecha derecha mueve el foco a la derecha. Si el elemento tiene un submenú, muestre el submenú. Si el elemento no tiene un submenú, contraiga el menú y los submenús, active el botón siguiente con [**TB \_ SETHOTITEM**](tb-sethotitem.md)y muestre el menú del botón adyacente. Si el último botón está activo cuando se recibe este mensaje, muestra el menú del primer botón.
-   La tecla de flecha izquierda mueve el foco a la izquierda. Si el elemento es un submenú, debe contraerlo y cambiar el foco a su menú primario. Si el elemento no es un submenú, contraiga el menú, active el botón siguiente con [**TB \_ SETHOTITEM**](tb-sethotitem.md)y muestre el menú de ese botón.

<!-- -->

-   La tecla ESCAPE hace una copia de seguridad de la pantalla en un solo paso.
    -   Si se muestra un submenú, se contrae y el foco se desplaza hasta el menú primario.
    -   Si se muestra el menú de un botón, se contrae y el seguimiento activo del menú está deshabilitado. El botón del elemento permanece activo.
    -   Si no se muestra ningún menú pero hay un botón activo, el botón está desactivado y el seguimiento activo del menú está deshabilitado.
-   Las teclas flecha arriba y flecha abajo solo se usan para navegar dentro de un menú determinado.
-   La tecla entrar inicia el comando asociado a un elemento de menú. Si el elemento de menú tiene un submenú, la tecla entrar lo muestra.

Al igual que en el caso de los menús deshabilitados de seguimiento activo, la aplicación debe ser capaz de controlar el mouse, el teclado y la navegación mixta. Sin embargo, el hecho de que se muestre un menú significa que la mensajería tendrá que administrarse de un modo diferente.

### <a name="message-processing-for-menu-hot-tracking"></a>Procesamiento de mensajes para Hot-Tracking de menú

El seguimiento activo del menú requiere que se muestre un menú en todo momento, además del breve intervalo necesario para cambiar a un nuevo menú. Sin embargo, el menú desplegable que muestra [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) es modal. La aplicación seguirá recibiendo algunos mensajes directamente, incluido el [**\_ comando de WM**](/windows/desktop/menurc/wm-command), [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)y mensajes de menú normales, como [**WM \_ MENUSELECT**](/windows/desktop/menurc/wm-menuselect). Sin embargo, no recibirá directamente mensajes de teclado o de mouse de bajo nivel. Para controlar mensajes como [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove), debe establecer un enlace de mensaje para interceptar los mensajes que se dirigen al menú.

Cuando se muestra un menú desplegable, establezca el enlace del mensaje mediante una llamada a la función [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) con el parámetro *IDHOOK* establecido en qu \_ MSGFILTER. Todos los mensajes destinados al menú se pasarán al [procedimiento de enlace](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)). Por ejemplo, el fragmento de código siguiente establece un enlace de mensaje que interceptará los mensajes que vayan a un menú desplegable. `MsgHook` es el nombre del procedimiento de enlace y `hhookMsg` es el identificador del procedimiento.


```
hhookMsg = SetWindowsHookEx(WH_MSGFILTER, MsgHook, HINST_THISDLL, 0);
```



Los mensajes de menú se identifican estableciendo el parámetro *nCode* del procedimiento de enlace en el \_ menú MSGF. El parámetro *lParam* apuntará a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) con el mensaje. En el resto de este tema se explican los detalles de los mensajes que se deben controlar y cómo hacerlo.

La aplicación debe pasar todos los mensajes al siguiente enlace de mensaje mediante una llamada a la función [**CallNextHookEx**](/windows/desktop/api/winuser/nf-winuser-callnexthookex) . También debe enviar los mensajes del mouse directamente al control de barra de herramientas, asegurándose de convertir las coordenadas del punto en el espacio de coordenadas del cliente de la barra de herramientas. El envío de los mensajes directamente garantiza que el control de barra de herramientas reciba los mensajes de mouse correspondientes. Por ejemplo, la barra de herramientas debe recibir mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) para realizar un seguimiento activo de sus botones.

Cuando se activa un botón nuevo, la aplicación debe contraer el menú desplegable anterior con un mensaje de [**\_ CANCELMODE de WM**](/windows/desktop/winmsg/wm-cancelmode) y mostrar un menú nuevo. También debe contraer el menú desplegable cuando el foco se realiza desde la barra de menús con la navegación mediante el teclado o haciendo clic fuera del área de menús. Siempre que se contrae un menú, debe liberar su enlace de mensaje mediante la función [**UnhookWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-unhookwindowshookex) . Si necesita mostrar otro menú desplegable, cree un nuevo enlace de mensaje. Cuando se inicia un comando, el menú se contrae automáticamente, pero debe liberar explícitamente el enlace del mensaje.

En el ejemplo de código siguiente se libera el enlace del mensaje que se estableció en el ejemplo anterior.


```
UnhookWindowsHookEx(hhookMsg);
```



### <a name="mouse-navigation"></a>Navegación con el mouse

Cuando un control de barra de herramientas normal realiza un seguimiento activo de los botones, resalta el botón activo y envía a la aplicación una notificación de [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) cada vez que se activa un botón nuevo. La aplicación es responsable de mostrar el menú desplegable adecuado. Así, debe:

-   Controle la notificación de [ \_ HOTITEMCHANGE de TBN](tbn-hotitemchange.md) para realizar un seguimiento del botón activo. Cuando el botón activo cambie, contraiga el menú anterior y cree uno nuevo.
-   Controle la notificación de [ \_ desplegable TBN](tbn-dropdown.md) que se envía cuando se hace clic en un botón. A continuación, debe contraer el menú y deshabilitar el seguimiento activo del menú. El botón permanece activo.
-   Controle los mensajes [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)y [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) en el procedimiento de enlace de mensajes, para realizar un seguimiento de la posición del mouse. Si se hace clic en el mouse fuera del área de menú, contraiga el menú desplegable actual, desactive el seguimiento activo del menú y devuelva la barra de menús a su estado de preactivación.
-   Cuando se inicia un comando de menú, deshabilite el seguimiento activo del menú. El menú se contraerá automáticamente, pero debe liberar explícitamente el enlace del mensaje.

También debe controlar la mensajería relacionada con menús, como el mensaje de [**\_ INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) que se envía cuando un elemento de menú necesita mostrar un submenú. Para obtener una explicación de cómo controlar estos mensajes, vea [menús](/windows/desktop/menurc/menus).

### <a name="keyboard-navigation"></a>Navegación mediante teclado

La aplicación debe procesar los mensajes del teclado en el procedimiento de enlace de mensajes y actuar sobre los que afectan al seguimiento activo del menú. Se deben administrar las siguientes presiones de tecla:

-   Tecla ESCAPE. La tecla ESCAPE hace una copia de seguridad de la presentación un nivel. Si se muestra un submenú, debe contraerse. Si se muestra el menú principal de un botón, contraigalo y deshabilite el seguimiento activo del menú. El botón permanece activo.
-   Tecla FLECHA DERECHA. Si el elemento tiene un submenú, lo muestra. Si el elemento no tiene un submenú, contraiga el menú y los submenús, active el botón siguiente con [**TB \_ SETHOTITEM**](tb-sethotitem.md)y muestre el menú. Si el último botón estaba activo cuando se recibió esta notificación, muestre el menú del primer botón.
-   Tecla FLECHA IZQUIERDA. Si el elemento está en un submenú, debe contraerlo y cambiar el foco a su menú primario. Si el elemento no es un submenú, contraiga el menú, active el botón adyacente con [**TB \_ SETHOTITEM**](tb-sethotitem.md)y muestre el menú. Si el primer botón estaba activo cuando se recibió esta notificación, muestre el menú del último botón.
-   Las teclas flecha arriba y flecha abajo. Estas teclas se utilizan para navegar dentro de un menú, pero no afectan directamente al seguimiento activo del menú.
-   Tecla de aceleración de *tecla* Alt. Use el mensaje [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) para determinar a qué botón corresponde el carácter de *tecla* . Si corresponde a un botón diferente del que está activo actualmente, contraiga el menú desplegable actual, active el botón nuevo con [**TB \_ SETHOTITEM**](tb-sethotitem.md)y muestre el menú del botón adyacente. Si el *carácter de tecla* corresponde al botón que se muestra actualmente, contraiga el menú desplegable y deshabilite el seguimiento activo del menú. El botón debe permanecer activo.

 

 