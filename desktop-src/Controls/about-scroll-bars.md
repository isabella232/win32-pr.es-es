---
title: Acerca de las barras de desplazamiento
description: Una ventana puede mostrar un objeto de datos, como un documento o un mapa de bits, que es mayor que el área de cliente de la ventana.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea93e3228a11f702865c7fd2b9da353d3791f87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061411"
---
# <a name="about-scroll-bars"></a>Acerca de las barras de desplazamiento

Una ventana puede mostrar un objeto de datos, como un documento o un mapa de bits, que es mayor que el área de cliente de la ventana. Cuando se proporciona con una barra de desplazamiento, el usuario puede desplazar un objeto de datos en el área de cliente para ver las partes del objeto que se extienden más allá de los bordes de la ventana.

Las barras de desplazamiento deben incluirse en cualquier ventana para la que el contenido del área de cliente se extienda más allá de los bordes de la ventana. La orientación de una barra de desplazamiento determina la dirección en la que se produce el desplazamiento cuando el usuario opera la barra de desplazamiento. Una barra de desplazamiento horizontal permite al usuario desplazar el contenido de una ventana a la izquierda o derecha. Una barra de desplazamiento vertical permite al usuario desplazar el contenido hacia arriba o hacia abajo.

En esta sección se tratan los temas siguientes.

-   [Partes de una barra de desplazamiento](#parts-of-a-scroll-bar)
-   [Barras de desplazamiento estándar y controles de barra de desplazamiento](#standard-scroll-bars-and-scroll-bar-controls)
-   [Posición del cuadro de desplazamiento e intervalo de desplazamiento](#scroll-box-position-and-scrolling-range)
-   [Visibilidad de la barra de desplazamiento](#scroll-bar-visibility)
-   [Solicitudes de barra de desplazamiento](#scroll-bar-requests)
-   [Interfaz de teclado para una barra de desplazamiento](#keyboard-interface-for-a-scroll-bar)
-   [Desplazamiento del área de cliente](#scrolling-the-client-area)
-   [Colores y métricas de la barra de desplazamiento](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Partes de una barra de desplazamiento

Una barra de desplazamiento consta de una zona sombreada con un botón de flecha en cada extremo y un cuadro de desplazamiento *(a* veces denominado thumb) entre los botones de flecha. Una barra de desplazamiento representa la longitud total o el ancho de un objeto de datos en el área de cliente de una ventana; el cuadro de desplazamiento representa la parte del objeto que está visible en el área de cliente. La posición del cuadro de desplazamiento cambia cada vez que el usuario desplaza un objeto de datos para mostrar una parte diferente de él. El sistema también ajusta el tamaño del cuadro de desplazamiento de una barra de desplazamiento para que indique qué parte de todo el objeto de datos está visible actualmente en la ventana. Si la mayor parte del objeto está visible, el cuadro de desplazamiento ocupa la mayor parte del desplazamiento de la barra de desplazamiento. De forma similar, si solo una pequeña parte del objeto está visible, el cuadro de desplazamiento ocupa una pequeña parte del desplazamiento de la barra de desplazamiento.

El usuario desplaza el contenido de una ventana haciendo clic en uno de los botones de flecha, haciendo clic en el área de la barra de desplazamiento sombreada o arrastrando el cuadro de desplazamiento. Cuando el usuario hace clic en un botón de flecha, la aplicación desplaza el contenido por una unidad (normalmente una sola línea o columna). Cuando el usuario hace clic en las áreas sombreadas, la aplicación desplaza el contenido por una ventana. La cantidad de desplazamiento que se produce cuando el usuario arrastra el cuadro de desplazamiento depende de la distancia que el usuario arrastre el cuadro de desplazamiento y del intervalo de desplazamiento de la barra de desplazamiento. Para obtener más información sobre el intervalo de desplazamiento, vea Posición del cuadro de desplazamiento [e Intervalo de desplazamiento](#scroll-box-position-and-scrolling-range).

En la siguiente captura de pantalla se muestra un control de edición enriquecido con barras de desplazamiento verticales y horizontales, como pueden aparecer en Windows Vista. La barra de desplazamiento vertical está actualmente "activa" porque el puntero del mouse estaba sobre ella cuando se tomó la captura de pantalla.

![captura de pantalla de un control de edición enriquecido con barras de desplazamiento](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Barras de desplazamiento estándar y controles de barra de desplazamiento

Una barra de desplazamiento se incluye en una ventana como una barra de desplazamiento estándar o como un control de barra de desplazamiento. Una barra de desplazamiento estándar se encuentra en el área no cliente de una ventana. Se crea con la ventana y se muestra cuando se muestra la ventana. El único propósito de una barra de desplazamiento estándar es permitir que el usuario genere solicitudes de desplazamiento para ver todo el contenido del área de cliente. Puede incluir una barra de desplazamiento estándar en una ventana especificando [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)o ambos estilos al crear la ventana. El **estilo WS \_ HSCROLL** crea una barra de desplazamiento horizontal que se encuentra en la parte inferior del área de cliente. El **estilo \_ VSCROLL** de WS crea una barra de desplazamiento vertical situado a la derecha del área de cliente. Los valores de métricas del sistema SM \_ CXHSCROLL y SM CYHSCROLL definen el ancho y el alto de una \_ barra de desplazamiento horizontal estándar. Los valores \_ DE SM CXVSCROLL y SM CYVSCROLL definen el ancho y el alto de una \_ barra de desplazamiento vertical estándar. Una barra de desplazamiento estándar forma parte de su ventana asociada y, por tanto, no tiene un identificador de ventana propio.

Un control de barra de desplazamiento es una ventana de control que pertenece a la clase de ventana SCROLLBAR. Aparece un control de barra de desplazamiento y funciona como una barra de desplazamiento estándar, pero es una ventana independiente. Como ventana independiente, un control de barra de desplazamiento toma el foco de entrada directo. A diferencia de una barra de desplazamiento estándar, un control de barra de desplazamiento también tiene una interfaz de teclado integrada.

Puede usar tantos controles de barra de desplazamiento como sea necesario en una sola ventana. Al crear un control de barra de desplazamiento, debe especificar el tamaño y la posición de la barra de desplazamiento. Sin embargo, si se puede cambiar el tamaño de la ventana de un control de barra de desplazamiento, se deben realizar ajustes en el tamaño de la barra de desplazamiento siempre que cambie el tamaño de la ventana.

La ventaja de usar una barra de desplazamiento estándar es que el sistema crea la barra de desplazamiento y establece automáticamente su tamaño y posición. Sin embargo, las barras de desplazamiento estándar a veces son demasiado restrictivas. Por ejemplo, suponga que quiere dividir un área de cliente en cuadrantes y usar un conjunto independiente de barras de desplazamiento para controlar el contenido de cada cuadrante. No puede usar barras de desplazamiento estándar porque solo puede crear un conjunto de barras de desplazamiento para una ventana determinada. En su lugar, use controles de barra de desplazamiento, ya que puede agregar tantos de ellos a una ventana como desee.

Las aplicaciones pueden proporcionar controles de barra de desplazamiento con fines distintos de desplazar el contenido de una ventana. Por ejemplo, una aplicación de protector de pantalla podría proporcionar una barra de desplazamiento para establecer la velocidad a la que se mueven los gráficos en la pantalla.

Un control de barra de desplazamiento puede tener varios estilos que sirven para controlar la orientación y la posición de la barra de desplazamiento. Especifique los estilos que desee al llamar a la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de barra de desplazamiento. Algunos de los estilos crean un control de barra de desplazamiento que usa un ancho o alto predeterminados. Sin embargo, siempre debe especificar las coordenadas x e y y y las demás dimensiones de la barra de desplazamiento.

Para obtener una tabla de estilos de control de barra de desplazamiento, vea [Estilos de control de barra de desplazamiento](scroll-bar-control-styles.md).

> [!Note]  
> Para usar estilos visuales con barras de desplazamiento, una aplicación debe incluir un manifiesto y debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa. Para obtener información sobre los estilos visuales, vea [Estilos visuales](themes-overview.md). Para obtener información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="scroll-box-position-and-scrolling-range"></a>Posición del cuadro de desplazamiento e intervalo de desplazamiento

La posición del cuadro de desplazamiento se representa como un entero; es relativa al extremo izquierdo o superior de la barra de desplazamiento, en función de si la barra de desplazamiento es horizontal o vertical. La posición debe estar dentro de los valores mínimo y máximo del intervalo de desplazamiento. Por ejemplo, en una barra de desplazamiento con un intervalo de 0 a 100, la posición 50 está en el centro, con las posiciones restantes distribuidas equitativamente a lo largo de la barra de desplazamiento. El intervalo inicial depende de la barra de desplazamiento. Las barras de desplazamiento estándar tienen un intervalo inicial de 0 a 100; Los controles de barra de desplazamiento tienen un intervalo vacío (los valores mínimo y máximo son cero), a menos que proporcione un intervalo explícito cuando se crea el control. Puede cambiar el intervalo en cualquier momento. Puede usar la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para establecer los valores de intervalo y la función [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para recuperar los valores de intervalo actuales.

Normalmente, una aplicación ajusta el intervalo de desplazamiento a enteros prácticos, lo que facilita la traducción de la posición del cuadro de desplazamiento en un valor correspondiente al objeto de datos que se va a desplazar. Por ejemplo, si una aplicación debe mostrar 260 líneas de un archivo de texto en una ventana que solo puede mostrar 16 líneas a la vez, el intervalo de barra de desplazamiento vertical se puede establecer en 1 a 244. Si el cuadro de desplazamiento está en la posición 1, la primera línea estará en la parte superior de la ventana. Si el cuadro de desplazamiento está en la posición 244, la última línea (línea 260) estará en la parte inferior de la ventana. Si una aplicación intenta especificar un valor de posición menor que el mínimo o mayor que el máximo, se usa en su lugar el valor de intervalo de desplazamiento mínimo o máximo.

Puede establecer un tamaño de página para una barra de desplazamiento. El *tamaño de página* representa el número de unidades de datos que pueden caber en el área de cliente de la ventana de propietario según su tamaño actual. Por ejemplo, si el área de cliente puede contener 16 líneas de texto, una aplicación establecería el tamaño de página en 16. El sistema usa el tamaño de página, junto con el intervalo de desplazamiento y la longitud de la barra de desplazamiento, para establecer el tamaño del cuadro de desplazamiento. Cada vez que se cambia el tamaño de una ventana que contiene una barra de desplazamiento, una aplicación debe llamar a la [**función SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para establecer el tamaño de página. Una aplicación puede recuperar el tamaño de página actual llamando a la [**función GetScrollInfo de**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) envío.

Para establecer una relación útil entre el intervalo de la barra de desplazamiento y el objeto de datos, una aplicación debe ajustar el intervalo siempre que cambie el tamaño del objeto de datos.

A medida que el usuario mueve el cuadro de desplazamiento en una barra de desplazamiento, la barra de desplazamiento informa de la posición del cuadro de desplazamiento como un entero en el intervalo de desplazamiento. Si la posición es el valor mínimo, el cuadro de desplazamiento se encuentra en la parte superior de una barra de desplazamiento vertical o en el extremo izquierdo de una barra de desplazamiento horizontal. Si la posición es el valor máximo, el cuadro de desplazamiento se encuentra en la parte inferior de una barra de desplazamiento vertical o en el extremo derecho de una barra de desplazamiento horizontal.

El valor máximo que puede notificar una barra de desplazamiento (es decir, la posición de desplazamiento máxima) depende del tamaño de página. Si la barra de desplazamiento tiene un tamaño de página mayor que uno, la posición de desplazamiento máxima es menor que el valor de intervalo máximo. Puede usar la fórmula siguiente para calcular la posición de desplazamiento máxima:


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Una aplicación debe mover el cuadro de desplazamiento en una barra de desplazamiento. Aunque el usuario realiza una solicitud de desplazamiento en una barra de desplazamiento, la barra de desplazamiento no actualiza automáticamente la posición del cuadro de desplazamiento. En su lugar, pasa la solicitud a la ventana primaria, que debe desplazar los datos y actualizar la posición del cuadro de desplazamiento. Una aplicación usa la [**función SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para actualizar la posición del cuadro de desplazamiento; de lo contrario, usa la [**función SetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) Dado que controla el movimiento del cuadro de desplazamiento, la aplicación puede mover el cuadro de desplazamiento en incrementos que funcionen mejor para los datos que se desplazan.

## <a name="scroll-bar-visibility"></a>Visibilidad de la barra de desplazamiento

El sistema oculta y deshabilita una barra de desplazamiento estándar cuando se especifican valores mínimos y máximos iguales. El sistema también oculta y deshabilita una barra de desplazamiento estándar si especifica un tamaño de página que incluye todo el intervalo de desplazamiento de la barra de desplazamiento. Esta es la manera de ocultar temporalmente una barra de desplazamiento cuando no es necesaria para el contenido del área cliente. No es necesario realizar solicitudes de desplazamiento a través de la barra de desplazamiento cuando está oculta. El sistema habilita la barra de desplazamiento y la muestra de nuevo cuando se establecen los valores mínimo y máximo en valores desiguales y cuando el tamaño de página no incluye todo el intervalo de desplazamiento. La [**función ShowScrollBar**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) también se puede usar para ocultar o mostrar una barra de desplazamiento. No afecta al intervalo, el tamaño de página o la posición del cuadro de desplazamiento de la barra de desplazamiento.

La [**función EnableScrollBar**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) se puede usar para deshabilitar una o ambas flechas de una barra de desplazamiento. Una aplicación muestra flechas deshabilitadas en gris y no responde a la entrada del usuario.

## <a name="scroll-bar-requests"></a>Solicitudes de barra de desplazamiento

El usuario realiza solicitudes de desplazamiento haciendo clic en varias partes de una barra de desplazamiento. El sistema envía la solicitud a la ventana especificada en forma de mensaje [**\_ WM HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md) Una barra de desplazamiento horizontal envía el **mensaje \_ WM HSCROLL;** una barra de desplazamiento vertical envía el **mensaje \_ VSCROLL de WM.** Cada mensaje incluye un código de solicitud que corresponde a la acción del usuario, al identificador de la barra de desplazamiento (solo controles de barra de desplazamiento) y, en algunos casos, a la posición del cuadro de desplazamiento.

En el diagrama siguiente se muestra el código de solicitud que el usuario genera al hacer clic en varias partes de una barra de desplazamiento.

![diagrama que muestra los códigos de solicitud asociados a cada región en dos barras de desplazamiento](images/csscr-02.png)

Los valores de SB \_ especifican la acción que realiza el usuario. Una aplicación examina los códigos que acompañan a los mensajes [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) y, a continuación, realiza la operación de desplazamiento adecuada. En la tabla siguiente, se especifica la acción del usuario para cada valor, seguida de la respuesta de la aplicación. En cada caso, la aplicación define una unidad según corresponda para los datos. Por ejemplo, la unidad típica para desplazar el texto verticalmente es una línea de texto.



| Solicitud           | Acción                                                                               | Response                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SB \_ LINEUP        | El usuario hace clic en la flecha de desplazamiento superior.                                                | Disminuye la posición del cuadro de desplazamiento; se desplaza hacia la parte superior de los datos en una unidad.                                                                                                                                                                                                                                              |
| SB \_ LINEDOWN      | El usuario hace clic en la flecha de desplazamiento inferior.                                             | Incrementa la posición del cuadro de desplazamiento; se desplaza hacia la parte inferior de los datos en una unidad.                                                                                                                                                                                                                                           |
| SB \_ LINELEFT      | El usuario hace clic en la flecha de desplazamiento izquierda.                                               | Disminuye la posición del cuadro de desplazamiento; se desplaza hacia el extremo izquierdo de los datos por una unidad.                                                                                                                                                                                                                                         |
| SB \_ LINERIGHT     | El usuario hace clic en la flecha de desplazamiento derecha.                                              | Incrementa la posición del cuadro de desplazamiento; se desplaza hacia el extremo derecho de los datos en una unidad.                                                                                                                                                                                                                                        |
| PÁGINA \_ DE SB        | El usuario hace clic en la barra de desplazamiento encima del cuadro de desplazamiento.                           | Disminuye la posición del cuadro de desplazamiento por el número de unidades de datos de la ventana. se desplaza hacia la parte superior de los datos por el mismo número de unidades.                                                                                                                                                                                    |
| SB \_ PAGEDOWN      | El usuario hace clic en la barra de desplazamiento debajo del cuadro de desplazamiento.                           | Incrementa la posición del cuadro de desplazamiento en función del número de unidades de datos de la ventana. se desplaza hacia la parte inferior de los datos por el mismo número de unidades.                                                                                                                                                                                 |
| SB \_ PAGELEFT      | El usuario hace clic en el desplazamiento de la barra de desplazamiento a la izquierda del cuadro de desplazamiento.                  | Disminuye la posición del cuadro de desplazamiento por el número de unidades de datos de la ventana. se desplaza hacia el extremo izquierdo de los datos por el mismo número de unidades.                                                                                                                                                                               |
| SB \_ PAGERIGHT     | El usuario hace clic en el desplazamiento de la barra de desplazamiento a la derecha del cuadro de desplazamiento.                 | Incrementa la posición del cuadro de desplazamiento en función del número de unidades de datos de la ventana. se desplaza hacia el extremo derecho de los datos por el mismo número de unidades.                                                                                                                                                                              |
| SB \_ THUMBPOSITION | El usuario libera el cuadro de desplazamiento después de arrastrarlo.                                  | Establece el cuadro de desplazamiento en la posición especificada en el mensaje; desplaza los datos por el mismo número de unidades que ha movido el cuadro de desplazamiento.                                                                                                                                                                                             |
| SB \_ THUMBTRACK    | El usuario arrastra el cuadro de desplazamiento.                                                       | Establece el cuadro de desplazamiento en la posición especificada en el mensaje y desplaza los datos por el mismo número de unidades que el cuadro de desplazamiento ha movido para las aplicaciones que dibujan datos rápidamente. Las aplicaciones que no pueden dibujar datos rápidamente deben esperar el código de solicitud SB THUMBPOSITION antes de mover el cuadro de desplazamiento y \_ desplazar los datos. |
| SB \_ ENDSCROLL     | El usuario suelta el mouse después de guardarlo en una flecha o en la barra de desplazamiento. | No se necesita ninguna respuesta.                                                                                                                                                                                                                                                                                                           |



 

Una barra de desplazamiento genera el código de solicitud SB THUMBPOSITION y SB THUMBTRACK cuando el usuario hace clic y \_ arrastra el cuadro de \_ desplazamiento. Se debe programar una aplicación para procesar el código de solicitud SB \_ THUMBTRACK o SB \_ THUMBPOSITION.

El código de solicitud SB THUMBPOSITION se produce cuando el usuario suelta \_ el botón del mouse después de hacer clic en el cuadro de desplazamiento. Una aplicación que procesa este mensaje realiza la operación de desplazamiento después de que el usuario haya arrastrado el cuadro de desplazamiento a la posición deseada y liberado el botón del mouse.

El código de solicitud DE SB \_ THUMBTRACK se produce cuando el usuario arrastra el cuadro de desplazamiento. Si una aplicación procesa códigos de solicitud SB THUMBTRACK, puede desplazarse por el contenido de una ventana a medida que el usuario \_ arrastra el cuadro de desplazamiento. Sin embargo, una barra de desplazamiento puede generar muchos códigos de solicitud SB THUMBTRACK en un breve período, por lo que una aplicación debe procesar estos códigos de solicitud solo si puede volver a dibujar rápidamente el contenido de la \_ ventana.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Interfaz de teclado para una barra de desplazamiento

Un control de barra de desplazamiento proporciona una interfaz de teclado integrada que permite al usuario emitir solicitudes de desplazamiento mediante el teclado. Una barra de desplazamiento estándar no lo hace. Cuando un control de barra de desplazamiento tiene el foco del teclado, envía mensajes [**\_ WM HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) a su ventana primaria cuando el usuario presiona las teclas de dirección. El código de solicitud se envía con cada mensaje correspondiente a la tecla de flecha que el usuario ha presionado. A continuación se encuentran las teclas de dirección y sus códigos de solicitud correspondientes.



| Tecla de flecha | Código de solicitud                  |
|-----------|-------------------------------|
| ABAJO      | SB \_ LINEDOWN o SB \_ LINERIGHT |
| FIN       | SB \_ BOTTOM                    |
| INICIO      | SB \_ TOP                       |
| LEFT      | SB \_ LINEUP o SB \_ LINELEFT    |
| PGDN      | SB \_ PAGEDOWN o SB \_ PAGERIGHT |
| PGUP      | SB \_ PAGEUP o SB \_ PAGELEFT    |
| RIGHT     | SB \_ LINEDOWN o SB \_ LINERIGHT |
| UP        | SB \_ LINEUP o SB \_ LINELEFT    |



 

 

> [!Note]  
> La interfaz de teclado de un control de barra de desplazamiento envía los códigos de solicitud SB \_ TOP y SB \_ BOTTOM. El código \_ de solicitud SB TOP indica que el usuario ha alcanzado el valor superior del intervalo de desplazamiento. Una aplicación desplaza el contenido de la ventana hacia abajo para que la parte superior del objeto de datos esté visible. El código \_ de solicitud SB BOTTOM indica que el usuario ha alcanzado el valor inferior del intervalo de desplazamiento. Si una aplicación procesa el código de solicitud SB BOTTOM, desplaza el contenido de la ventana hacia arriba para que se pueda ver la parte inferior \_ del objeto de datos.

 

Si desea una interfaz de teclado para una barra de desplazamiento estándar, puede crear una usted mismo procesando el mensaje [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) en el procedimiento de la ventana y, a continuación, realizando la acción de desplazamiento adecuada en función del código de clave virtual que acompaña al mensaje. Para obtener información sobre cómo crear una interfaz de teclado para una barra de desplazamiento, vea Crear una interfaz [de teclado para una barra de desplazamiento estándar.](using-scroll-bars.md)

## <a name="scrolling-the-client-area"></a>Desplazarse por el área cliente

La manera más sencilla de desplazarse por el contenido de un área de cliente es borrarlo y volver a dibujarlo. Este es el método que es probable que una aplicación use con los códigos de solicitud SB PAGEUP, SB PAGEDOWN y SB TOP, que normalmente requieren \_ \_ contenido completamente \_ nuevo.

Para algunos códigos de solicitud, como SB LINEUP y SB LINEDOWN, no es necesario borrar todo el contenido, ya que algunos permanecen visibles después de que se produzca \_ \_ el desplazamiento. La [**función ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) conserva una parte del contenido del área cliente, mueve la parte conservada una cantidad especificada y, a continuación, prepara el resto del área de cliente para pintar información nueva. **ScrollWindowEx** usa la [**función BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para mover una parte específica del objeto de datos a una nueva ubicación dentro del área de cliente. Cualquier parte que se descubra del área de cliente (todo lo que no se conserve) se invalida, borra y pinta cuando se produce el siguiente mensaje [**\_ WM PAINT.**](/windows/desktop/gdi/wm-paint)

La [**función ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) se puede usar para excluir una parte del área de cliente de la operación de desplazamiento. Esto evita que los elementos con posiciones fijas, como las ventanas secundarias, se muevan dentro del área de cliente. Invalida automáticamente la parte del área cliente que va a recibir la nueva información, por lo que la aplicación no tiene que calcular sus propias regiones de recorte. Para obtener más información sobre el recorte, vea [Recorte de](/windows/desktop/gdi/clipping).

Normalmente, una aplicación desplaza el contenido de una ventana en la dirección opuesta a la indicada por la barra de desplazamiento. Por ejemplo, cuando el usuario hace clic en el desplazamiento de la barra de desplazamiento en el área debajo del cuadro de desplazamiento, una aplicación desplaza el objeto en la ventana hacia arriba para mostrar una parte del objeto que está debajo de la parte visible.

También puede desplazarse por una región rectangular mediante la [**función ScrollDC.**](/windows/desktop/api/Winuser/nf-winuser-scrolldc)

## <a name="scroll-bar-colors-and-metrics"></a>Colores y métricas de la barra de desplazamiento

El valor de color definido por el sistema, COLOR \_ SCROLLBAR, controla el color dentro de una barra de desplazamiento. Use la [**función GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) para determinar el color de la barra de desplazamiento y la función [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) para establecer el color de la barra de desplazamiento. Sin embargo, tenga en cuenta que este cambio de color afecta a todas las barras de desplazamiento del sistema.

Puede obtener las dimensiones de los mapas de bits que el sistema usa en las barras de desplazamiento estándar llamando a la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) A continuación se encuentran los valores de métricas del sistema asociados a las barras de desplazamiento.



| Métrica del sistema | Descripción                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| SM \_ CXHSCROLL | Ancho del mapa de bits de flecha en la barra de desplazamiento horizontal                                                                             |
| SM \_ CXHTHUMB  | Ancho del cuadro de desplazamiento en la barra de desplazamiento horizontal. Este valor recupera el ancho de una barra de desplazamiento que tiene un tamaño de página de cero.    |
| SM \_ CXVSCROLL | Ancho del mapa de bits de flecha en la barra de desplazamiento vertical                                                                               |
| SM \_ CYHSCROLL | Alto del mapa de bits de flecha en la barra de desplazamiento horizontal                                                                            |
| SM \_ CYVSCROLL | Alto del mapa de bits de flecha en la barra de desplazamiento vertical                                                                              |
| SM \_ CYVTHUMB  | Alto del cuadro de desplazamiento en la barra de desplazamiento vertical. Este valor recupera el alto de una barra de desplazamiento que tiene un tamaño de página de cero. |



 

 

 
