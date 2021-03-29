---
title: Acerca de las barras de desplazamiento
description: Una ventana puede mostrar un objeto de datos, como un documento o un mapa de bits, que es mayor que el área cliente de la ventana.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d410e98ea1fe722d6dc1c4869010df30f99bddb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078396"
---
# <a name="about-scroll-bars"></a>Acerca de las barras de desplazamiento

Una ventana puede mostrar un objeto de datos, como un documento o un mapa de bits, que es mayor que el área cliente de la ventana. Cuando se proporciona con una barra de desplazamiento, el usuario puede desplazarse por un objeto de datos en el área cliente para mostrar las partes del objeto que se extienden más allá de los bordes de la ventana.

Las barras de desplazamiento deben estar incluidas en cualquier ventana para la que el contenido del área cliente se extienda más allá de los bordes de la ventana. La orientación de una barra de desplazamiento determina la dirección en la que se produce el desplazamiento cuando el usuario trabaja con la barra de desplazamiento. Una barra de desplazamiento horizontal permite al usuario desplazarse por el contenido de una ventana hacia la izquierda o la derecha. Una barra de desplazamiento vertical permite al usuario desplazar el contenido hacia arriba o hacia abajo.

Los temas siguientes se describen en esta sección.

-   [Partes de una barra de desplazamiento](#parts-of-a-scroll-bar)
-   [Barras de desplazamiento estándar y controles de barra de desplazamiento](#standard-scroll-bars-and-scroll-bar-controls)
-   [Posición y intervalo de desplazamiento del cuadro de desplazamiento](#scroll-box-position-and-scrolling-range)
-   [Visibilidad de la barra de desplazamiento](#scroll-bar-visibility)
-   [Solicitudes de barra de desplazamiento](#scroll-bar-requests)
-   [Interfaz de teclado de una barra de desplazamiento](#keyboard-interface-for-a-scroll-bar)
-   [Desplazarse por el área cliente](#scrolling-the-client-area)
-   [Colores y métricas de la barra de desplazamiento](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Partes de una barra de desplazamiento

Una barra de desplazamiento consta de un eje sombreado con un botón de flecha en cada extremo y un *cuadro de desplazamiento* (a veces denominado control de posición) entre los botones de flecha. Una barra de desplazamiento representa la longitud total o el ancho de un objeto de datos en el área de cliente de una ventana; el cuadro de desplazamiento representa la parte del objeto que está visible en el área cliente. La posición del cuadro de desplazamiento cambia siempre que el usuario desplaza un objeto de datos para mostrar una parte diferente. El sistema también ajusta el tamaño del cuadro de desplazamiento de una barra de desplazamiento para indicar qué parte del objeto de datos completo está visible actualmente en la ventana. Si la mayor parte del objeto es visible, el cuadro de desplazamiento ocupa la mayor parte del eje de la barra de desplazamiento. Del mismo modo, si solo una pequeña parte del objeto es visible, el cuadro de desplazamiento ocupa una pequeña parte del eje de la barra de desplazamiento.

El usuario desplaza el contenido de una ventana haciendo clic en uno de los botones de flecha, haciendo clic en el área del eje de la barra de desplazamiento sombreada o arrastrando el cuadro de desplazamiento. Cuando el usuario hace clic en un botón de flecha, la aplicación desplaza el contenido en una unidad (normalmente una sola línea o columna). Cuando el usuario hace clic en las áreas sombreadas, la aplicación desplaza el contenido en una ventana. La cantidad de desplazamiento que se produce cuando el usuario arrastra el cuadro de desplazamiento depende de la distancia con la que el usuario arrastra el cuadro de desplazamiento y en el intervalo de desplazamiento de la barra de desplazamiento. Para obtener más información sobre el intervalo de desplazamiento, vea [posición del cuadro de desplazamiento e intervalo de desplazamiento](#scroll-box-position-and-scrolling-range).

En la captura de pantalla siguiente se muestra un control Rich Edit con barras de desplazamiento horizontal y vertical, tal como pueden aparecer en Windows Vista. La barra de desplazamiento vertical está actualmente "activa" porque el puntero del mouse se mantiene sobre él cuando se tomó la captura de pantalla.

![captura de pantalla de un control Rich Edit con barras de desplazamiento](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Barras de desplazamiento estándar y controles de barra de desplazamiento

Una barra de desplazamiento se incluye en una ventana, ya sea como una barra de desplazamiento estándar o como un control de barra de desplazamiento. Una barra de desplazamiento estándar se encuentra en el área no cliente de una ventana. Se crea con la ventana y se muestra cuando se muestra la ventana. El único propósito de una barra de desplazamiento estándar es permitir al usuario generar solicitudes de desplazamiento para ver todo el contenido del área de cliente. Puede incluir una barra de desplazamiento estándar en una ventana especificando [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)o ambos estilos al crear la ventana. El estilo **WS \_ HSCROLL** crea una barra de desplazamiento horizontal situada en la parte inferior del área cliente. El estilo **WS \_ VSCROLL** crea una barra de desplazamiento vertical situada a la derecha del área cliente. Los \_ \_ valores de métrica del sistema SM CXHSCROLL y SM CYHSCROLL definen el ancho y el alto de una barra de desplazamiento horizontal estándar. Los \_ valores SM CXVSCROLL y SM \_ CYVSCROLL definen el ancho y el alto de una barra de desplazamiento vertical estándar. Una barra de desplazamiento estándar forma parte de su ventana asociada y, por lo tanto, no tiene un identificador de ventana propio.

Un control de barra de desplazamiento es una ventana de control que pertenece a la clase de ventana de la barra de desplazamiento. Aparece un control de barra de desplazamiento y funciona como una barra de desplazamiento estándar, pero es una ventana independiente. Como ventana independiente, un control de barra de desplazamiento toma el foco de entrada directa. A diferencia de una barra de desplazamiento estándar, un control de barra de desplazamiento también tiene una interfaz de teclado integrada.

Puede usar tantos controles de barra de desplazamiento como sea necesario en una sola ventana. Al crear un control de barra de desplazamiento, debe especificar el tamaño y la posición de la barra de desplazamiento. Sin embargo, si se puede cambiar el tamaño de la ventana de un control de barra de desplazamiento, se deben realizar ajustes en el tamaño de la barra de desplazamiento cada vez que cambie el tamaño de la ventana.

La ventaja de usar una barra de desplazamiento estándar es que el sistema crea la barra de desplazamiento y establece automáticamente su tamaño y posición. Sin embargo, las barras de desplazamiento estándar a veces son demasiado restrictivas. Por ejemplo, suponga que desea dividir un área de cliente en cuadrantes y utilizar un conjunto independiente de barras de desplazamiento para controlar el contenido de cada cuadrante. No puede utilizar las barras de desplazamiento estándar porque solo puede crear un conjunto de barras de desplazamiento para una ventana determinada. En su lugar, use los controles de barra de desplazamiento, ya que puede agregar tantos como desee a una ventana.

Las aplicaciones pueden proporcionar controles de barra de desplazamiento para fines distintos de desplazarse por el contenido de una ventana. Por ejemplo, una aplicación de protector de pantalla podría proporcionar una barra de desplazamiento para establecer la velocidad a la que se mueven los gráficos en la pantalla.

Un control de barra de desplazamiento puede tener varios estilos que sirven para controlar la orientación y la posición de la barra de desplazamiento. Especifique los estilos que desea al llamar a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de barra de desplazamiento. Algunos de los estilos crean un control de barra de desplazamiento que usa un ancho o un alto predeterminados. Sin embargo, siempre debe especificar las coordenadas x e y y las demás dimensiones de la barra de desplazamiento.

Para obtener una tabla de estilos de control de barra de desplazamiento, vea [estilos de control de barra de desplazamiento](scroll-bar-control-styles.md).

> [!Note]  
> Para usar estilos visuales con barras de desplazamiento, una aplicación debe incluir un manifiesto y debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa. Para obtener información sobre los estilos visuales, vea [estilos visuales](themes-overview.md). Para obtener información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="scroll-box-position-and-scrolling-range"></a>Posición y intervalo de desplazamiento del cuadro de desplazamiento

La posición del cuadro de desplazamiento se representa como un entero; es relativo al extremo izquierdo o superior de la barra de desplazamiento, dependiendo de si la barra de desplazamiento es horizontal o vertical. La posición debe estar dentro de los valores mínimo y máximo del intervalo de desplazamiento. Por ejemplo, en una barra de desplazamiento con un intervalo de 0 a 100, la posición 50 está en el medio, y las posiciones restantes se distribuyen uniformemente a lo largo de la barra de desplazamiento. El intervalo inicial depende de la barra de desplazamiento. Las barras de desplazamiento estándar tienen un intervalo inicial de 0 a 100; los controles de barra de desplazamiento tienen un intervalo vacío (los valores mínimo y máximo son cero), a menos que proporcione un intervalo explícito cuando se cree el control. Puede cambiar el intervalo en cualquier momento. Puede usar la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para establecer los valores del intervalo y la función [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para recuperar los valores del intervalo actual.

Normalmente, una aplicación ajusta el intervalo de desplazamiento a los enteros cómodos, lo que facilita la conversión de la posición del cuadro de desplazamiento en un valor correspondiente al objeto de datos que se va a desplazar. Por ejemplo, si una aplicación debe mostrar 260 líneas de un archivo de texto en una ventana que solo puede mostrar 16 líneas a la vez, el intervalo de la barra de desplazamiento vertical se puede establecer en 1 a 244. Si el cuadro de desplazamiento está en la posición 1, la primera línea estará en la parte superior de la ventana. Si el cuadro de desplazamiento está en la posición 244, la última línea (línea 260) estará en la parte inferior de la ventana. Si una aplicación intenta especificar un valor de posición menor que el mínimo o mayor que el máximo, se utiliza en su lugar el valor de intervalo de desplazamiento mínimo o máximo.

Puede establecer un tamaño de página para una barra de desplazamiento. El *tamaño de página* representa el número de unidades de datos que pueden caber en el área cliente de la ventana propietaria a partir de su tamaño actual. Por ejemplo, si el área cliente puede contener 16 líneas de texto, una aplicación establecería el tamaño de la página en 16. El sistema utiliza el tamaño de página, junto con el intervalo de desplazamiento y la longitud del eje de la barra de desplazamiento, para establecer el tamaño del cuadro de desplazamiento. Cada vez que se cambia el tamaño de una ventana que contiene una barra de desplazamiento, una aplicación debe llamar a la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para establecer el tamaño de página. Una aplicación puede recuperar el tamaño de página actual llamando a la función de envío de [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) .

Para establecer una relación útil entre el intervalo de la barra de desplazamiento y el objeto de datos, una aplicación debe ajustar el intervalo cada vez que cambie el tamaño del objeto de datos.

Cuando el usuario mueve el cuadro de desplazamiento en una barra de desplazamiento, la barra de desplazamiento notifica la posición del cuadro de desplazamiento como un entero en el intervalo de desplazamiento. Si la posición es el valor mínimo, el cuadro de desplazamiento está en la parte superior de una barra de desplazamiento vertical o en el extremo izquierdo de una barra de desplazamiento horizontal. Si la posición es el valor máximo, el cuadro de desplazamiento está en la parte inferior de una barra de desplazamiento vertical o en el extremo derecho de una barra de desplazamiento horizontal.

El valor máximo que puede notificar una barra de desplazamiento (es decir, la posición de desplazamiento máxima) depende del tamaño de página. Si la barra de desplazamiento tiene un tamaño de página mayor que uno, la posición de desplazamiento máxima es menor que el valor de intervalo máximo. Puede usar la fórmula siguiente para calcular la posición de desplazamiento máximo:


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Una aplicación debe desplazar el cuadro de desplazamiento en una barra de desplazamiento. Aunque el usuario realiza una solicitud de desplazamiento en una barra de desplazamiento, la barra de desplazamiento no actualiza automáticamente la posición del cuadro de desplazamiento. En su lugar, pasa la solicitud a la ventana primaria, que debe desplazarse por los datos y actualizar la posición del cuadro de desplazamiento. Una aplicación utiliza la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para actualizar la posición del cuadro de desplazamiento. de lo contrario, utiliza la función [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Dado que controla el movimiento del cuadro de desplazamiento, la aplicación puede mover el cuadro de desplazamiento en incrementos que funcionan mejor para los datos que se desplazan.

## <a name="scroll-bar-visibility"></a>Visibilidad de la barra de desplazamiento

El sistema oculta y deshabilita una barra de desplazamiento estándar cuando se especifican los valores mínimo y máximo. El sistema también oculta y deshabilita una barra de desplazamiento estándar si se especifica un tamaño de página que incluye todo el intervalo de desplazamiento de la barra de desplazamiento. Esta es la manera de ocultar temporalmente una barra de desplazamiento cuando no es necesaria para el contenido del área de cliente. No es necesario hacer solicitudes de desplazamiento a través de la barra de desplazamiento cuando está oculta. El sistema habilita la barra de desplazamiento y la muestra de nuevo cuando establece los valores mínimo y máximo en valores distintos o cuando el tamaño de página no incluye el intervalo de desplazamiento completo. La función [**ShowScrollBar**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) también se puede usar para ocultar o mostrar una barra de desplazamiento. No afecta a la posición del intervalo de la barra de desplazamiento, el tamaño de página o el cuadro de desplazamiento.

La función [**EnableScrollBar**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) se puede usar para deshabilitar una o ambas flechas de una barra de desplazamiento. Una aplicación muestra las flechas deshabilitadas en gris y no responde a los datos proporcionados por el usuario.

## <a name="scroll-bar-requests"></a>Solicitudes de barra de desplazamiento

El usuario realiza las solicitudes de desplazamiento haciendo clic en varias partes de una barra de desplazamiento. El sistema envía la solicitud a la ventana especificada en forma de un mensaje [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) . Una barra de desplazamiento horizontal envía el mensaje de **\_ HSCROLL de WM** ; una barra de desplazamiento vertical envía el mensaje de **\_ VSCROLL de WM** . Cada mensaje incluye un código de solicitud que corresponde a la acción del usuario, al identificador de la barra de desplazamiento (solo controles de barra de desplazamiento) y, en algunos casos, a la posición del cuadro de desplazamiento.

En el diagrama siguiente se muestra el código de solicitud que el usuario genera al hacer clic en varias partes de una barra de desplazamiento.

![diagrama que muestra los códigos de solicitud asociados a cada región en dos barras de desplazamiento](images/csscr-02.png)

Los valores de SB \_ especifican la acción que realiza el usuario. Una aplicación examina los códigos que acompañan a los mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) y, a continuación, realiza la operación de desplazamiento adecuada. En la tabla siguiente, se especifica la acción del usuario para cada valor, seguido de la respuesta de la aplicación. En cada caso, la aplicación define una unidad según corresponda para los datos. Por ejemplo, la unidad típica para desplazar el texto verticalmente es una línea de texto.



| Request           | Acción                                                                               | Response                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_línea SB        | El usuario hace clic en la flecha de desplazamiento superior.                                                | Disminuye la posición del cuadro de desplazamiento; se desplaza hacia la parte superior de los datos en una unidad.                                                                                                                                                                                                                                              |
| SB \_ LINEDOWN      | El usuario hace clic en la flecha de desplazamiento inferior.                                             | Incrementa la posición del cuadro de desplazamiento; se desplaza hacia la parte inferior de los datos en una unidad.                                                                                                                                                                                                                                           |
| SB \_ LINELEFT      | El usuario hace clic en la flecha de desplazamiento de la izquierda.                                               | Disminuye la posición del cuadro de desplazamiento; se desplaza hacia el extremo izquierdo de los datos en una unidad.                                                                                                                                                                                                                                         |
| SB \_ LINERIGHT     | El usuario hace clic en la flecha de desplazamiento de la derecha.                                              | Incrementa la posición del cuadro de desplazamiento; se desplaza hacia el extremo derecho de los datos en una unidad.                                                                                                                                                                                                                                        |
| \_Re Pág de SB        | El usuario hace clic en el eje de la barra de desplazamiento sobre el cuadro de desplazamiento.                           | Disminuye la posición del cuadro de desplazamiento por el número de unidades de datos de la ventana; se desplaza hacia la parte superior de los datos en el mismo número de unidades.                                                                                                                                                                                    |
| reavpág SB \_      | El usuario hace clic en el eje de la barra de desplazamiento debajo del cuadro de desplazamiento.                           | Incrementa la posición del cuadro de desplazamiento por el número de unidades de datos de la ventana; se desplaza hacia la parte inferior de los datos en el mismo número de unidades.                                                                                                                                                                                 |
| SB \_ PAGELEFT      | El usuario hace clic en el eje de la barra de desplazamiento a la izquierda del cuadro de desplazamiento.                  | Disminuye la posición del cuadro de desplazamiento por el número de unidades de datos de la ventana; se desplaza hacia el extremo izquierdo de los datos en el mismo número de unidades.                                                                                                                                                                               |
| SB \_ anclada     | El usuario hace clic en el eje de la barra de desplazamiento a la derecha del cuadro de desplazamiento.                 | Incrementa la posición del cuadro de desplazamiento por el número de unidades de datos de la ventana; se desplaza hacia el extremo derecho de los datos en el mismo número de unidades.                                                                                                                                                                              |
| SB \_ THUMBPOSITION | El usuario suelta el cuadro de desplazamiento después de arrastrarlo.                                  | Establece el cuadro de desplazamiento en la posición especificada en el mensaje; desplaza los datos por el mismo número de unidades que ha desplazado el cuadro de desplazamiento.                                                                                                                                                                                             |
| SB \_ THUMBTRACK    | El usuario arrastra el cuadro de desplazamiento.                                                       | Establece el cuadro de desplazamiento en la posición especificada en el mensaje y desplaza los datos por el mismo número de unidades que ha desplazado el cuadro de desplazamiento para las aplicaciones que dibujan los datos rápidamente. Las aplicaciones que no pueden dibujar datos rápidamente deben esperar el \_ código de solicitud de SB THUMBPOSITION antes de mover el cuadro de desplazamiento y desplazarse por los datos. |
| SB \_ ENDSCROLL     | El usuario suelta el mouse después de mantenerlo en una flecha o en el eje de la barra de desplazamiento. | No se necesita ninguna respuesta.                                                                                                                                                                                                                                                                                                           |



 

Una barra de desplazamiento genera \_ código de solicitud SB THUMBPOSITION y SB \_ THUMBTRACK cuando el usuario hace clic y arrastra el cuadro de desplazamiento. Una aplicación debe programarse para procesar el código de \_ solicitud SB THUMBTRACK o SB \_ THUMBPOSITION.

El \_ código de solicitud THUMBPOSITION de SB se produce cuando el usuario suelta el botón del mouse después de hacer clic en el cuadro de desplazamiento. Una aplicación que procesa este mensaje realiza la operación de desplazamiento una vez que el usuario ha arrastrado el cuadro de desplazamiento a la posición deseada y ha soltado el botón del mouse.

El \_ código de solicitud THUMBTRACK de SB se produce cuando el usuario arrastra el cuadro de desplazamiento. Si una aplicación procesa \_ códigos de solicitud THUMBTRACK de SB, puede desplazarse por el contenido de una ventana cuando el usuario arrastra el cuadro de desplazamiento. Sin embargo, una barra de desplazamiento puede generar muchos \_ código de solicitud THUMBTRACK de SB en un breve período, por lo que una aplicación debe procesar estos códigos de solicitud solo si puede volver a pintar rápidamente el contenido de la ventana.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Interfaz de teclado de una barra de desplazamiento

Un control de barra de desplazamiento proporciona una interfaz de teclado integrada que permite al usuario emitir solicitudes de desplazamiento mediante el teclado; no se trata de una barra de desplazamiento estándar. Cuando un control de barra de desplazamiento tiene el foco de teclado, envía mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) a su ventana primaria cuando el usuario presiona las teclas de dirección. El código de solicitud se envía con cada mensaje correspondiente a la tecla de dirección que el usuario ha presionado. A continuación se muestran las teclas de dirección y sus códigos de solicitud correspondientes.



| Tecla de dirección | Código de solicitud                  |
|-----------|-------------------------------|
| ABAJO      | SB \_ LINEDOWN o SB \_ LINERIGHT |
| FIN       | SB \_ inferior                    |
| INICIO      | SB \_ superior                       |
| LEFT      | \_Línea SB o SB \_ LINELEFT    |
| PÁG      | SB \_ AvPág o SB \_ anclada |
| RE      | SB \_ RePág o SB \_ PAGELEFT    |
| RIGHT     | SB \_ LINEDOWN o SB \_ LINERIGHT |
| UP        | \_Línea SB o SB \_ LINELEFT    |



 

 

> [!Note]  
> La interfaz de teclado de un control de barra de desplazamiento envía los \_ códigos de solicitud SB Top y SB \_ Bottom. El \_ código de solicitud principal de SB indica que el usuario ha alcanzado el valor superior del intervalo de desplazamiento. Una aplicación desplaza el contenido de la ventana hacia abajo para que la parte superior del objeto de datos sea visible. El \_ código de solicitud de SB inferior indica que el usuario ha alcanzado el valor inferior del intervalo de desplazamiento. Si una aplicación procesa el código de solicitud de SB \_ inferior, desplaza el contenido de la ventana hacia arriba para que la parte inferior del objeto de datos sea visible.

 

Si desea una interfaz de teclado para una barra de desplazamiento estándar, puede crear una mediante el procesamiento del mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) en el procedimiento de ventana y, a continuación, realizar la acción de desplazamiento adecuada en función del código de clave virtual que acompaña al mensaje. Para obtener información sobre cómo crear una interfaz de teclado para una barra de desplazamiento, vea [crear una interfaz de teclado para una barra de desplazamiento estándar](using-scroll-bars.md).

## <a name="scrolling-the-client-area"></a>Desplazarse por el área cliente

La manera más sencilla de desplazarse por el contenido de un área cliente es borrarlo y volver a dibujarlo. Este es el método que es probable que use una aplicación con los \_ códigos de solicitud de reinicio de SB, SB \_ Av Pág y SB \_ principales, que normalmente requieren contenido completamente nuevo.

En algunos códigos de solicitud, como la \_ línea SB y SB \_ LINEDOWN, no es necesario borrar todo el contenido, ya que algunos permanecen visibles una vez que se produce el desplazamiento. La función [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) conserva una parte del contenido del área del cliente, mueve la parte conservada una cantidad especificada y, a continuación, prepara el resto del área cliente para pintar la nueva información. **ScrollWindowEx** usa la función [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para trasladar una parte específica del objeto de datos a una nueva ubicación dentro del área cliente. Cualquier parte no cubierta del área de cliente (cualquier cosa no conservada) se invalida, borra y pinta cuando se produce el siguiente mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) .

La función [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) se puede utilizar para excluir una parte del área de cliente de la operación de desplazamiento. Esto hace que los elementos con posiciones fijas, como las ventanas secundarias, se muevan dentro del área cliente. Invalida automáticamente la parte del área de cliente que va a recibir la nueva información, por lo que la aplicación no tiene que calcular sus propias regiones de recorte. Para obtener más información sobre el recorte, vea [recorte](/windows/desktop/gdi/clipping).

Normalmente, una aplicación desplaza el contenido de una ventana en la dirección opuesta a la indicada por la barra de desplazamiento. Por ejemplo, cuando el usuario hace clic en el eje de la barra de desplazamiento en el área situada debajo del cuadro de desplazamiento, una aplicación desplaza el objeto en la ventana hacia arriba para mostrar una parte del objeto que está por debajo de la parte visible.

También puede desplazarse por una región rectangular mediante la función [**ScrollDC**](/windows/desktop/api/Winuser/nf-winuser-scrolldc) .

## <a name="scroll-bar-colors-and-metrics"></a>Colores y métricas de la barra de desplazamiento

El valor de color definido por el sistema, ScrollBar de COLOR \_ , controla el color del eje de una barra de desplazamiento. Utilice la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) para determinar el color del eje de la barra de desplazamiento y la función [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) para establecer el color del eje de la barra de desplazamiento. Sin embargo, tenga en cuenta que este cambio de color afecta a todas las barras de desplazamiento del sistema.

Puede obtener las dimensiones de los mapas de bits que el sistema utiliza en las barras de desplazamiento estándar mediante una llamada a la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . A continuación se muestran los valores de métrica del sistema asociados a las barras de desplazamiento.



| Métrica del sistema | Descripción                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| SM \_ CXHSCROLL | Ancho del mapa de bits de las flechas en la barra de desplazamiento horizontal                                                                             |
| SM \_ CXHTHUMB  | Ancho del cuadro de desplazamiento en la barra de desplazamiento horizontal. Este valor recupera el ancho de una barra de desplazamiento que tiene un tamaño de página de cero.    |
| SM \_ CXVSCROLL | Ancho del mapa de bits de las flechas en la barra de desplazamiento vertical                                                                               |
| SM \_ CYHSCROLL | Alto del mapa de bits de las flechas en la barra de desplazamiento horizontal                                                                            |
| SM \_ CYVSCROLL | Alto del mapa de bits de las flechas en la barra de desplazamiento vertical                                                                              |
| SM \_ CYVTHUMB  | Alto del cuadro de desplazamiento en la barra de desplazamiento vertical. Este valor recupera el alto de una barra de desplazamiento que tiene un tamaño de página cero. |



 

 

 