---
description: A partir de microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) versión 1.0, el Panel de entrada de Tablet PC de nivel del sistema proporciona un mecanismo universal para realizar la entrada de texto en la plataforma Windows, aunque no proporciona acceso mediante programación. El objeto PenInputPanel de la versión 1.5 del SDK de Tablet PC integra las herramientas de entrada de texto en las aplicaciones.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: Acerca del panel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044e8c3a43127bd765fd5004329352956e4be8bb9f214f8dda8896fa318832a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844415"
---
# <a name="about-the-input-panel"></a>Acerca del panel de entrada

\[[**PenInputPanel se**](peninputpanel-class.md) ha reemplazado por [**TextInput.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) Para obtener más información, vea [Programar el panel de entrada de texto](programming-the-text-input-panel.md).\]

A partir de microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) versión 1.0, el Panel de entrada de Tablet PC de nivel del sistema proporciona un mecanismo universal para realizar la entrada de texto en la plataforma Windows, aunque no proporciona acceso mediante programación. El objeto [**PenInputPanel**](peninputpanel-class.md) de la versión 1.5 del SDK de Tablet PC integra las herramientas de entrada de texto en las aplicaciones.

En el gráfico siguiente se muestra el panel de entrada del lápiz que se muestra sobre el ejemplo de [ejemplo de formulario de notificaciones](auto-claims-form-sample.md) automáticas.

![Panel de entrada de lápiz que se muestra en el ejemplo de ejemplo de formulario de notificaciones automáticas](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

El [**objeto PenInputPanel es**](peninputpanel-class.md) práctico para los desarrolladores de aplicaciones. No es necesario reemplazar controles en formularios existentes. Simplemente puede adjuntar objetos **PenInputPanel a** controles existentes que reciben entrada de texto y pueden empezar a recibir entradas del **objeto PenInputPanel.**

El [**objeto PenInputPanel**](peninputpanel-class.md) adopta la configuración del Panel de entrada para las siguientes propiedades:

-   Layout
-   Grosor de la tinta
-   Tiempo de espera de reconocimiento
-   Tamaño del cuadro, modo de envío y otros valores específicos de la entrada con caja de Asia Oriental

El [**objeto PenInputPanel**](peninputpanel-class.md) no proporciona acceso a la entrada de lápiz subyacente. Para obtener la entrada de lápiz, use el control [InkPicture.](inkpicture-control-reference.md)

El [**objeto PenInputPanel proporciona**](peninputpanel-class.md) una interfaz de usuario (UI) local que los usuarios finales de las aplicaciones pueden detectar fácilmente. Se activa automáticamente cuando el usuario pulsa en una ventana con un **objeto PenInputPanel** mediante el lápiz de tableta. El panel de entrada del lápiz aparece automáticamente cuando el sistema detecta un evento CursorButtonUp para la ventana a la que está asociado **el objeto PenInputPanel.** La activación automática se puede deshabilitar estableciendo la [**propiedad AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) en **FALSE.**

El panel de entrada del lápiz no aparece automáticamente en los eventos del mouse. Los eventos de lápiz se convierten en eventos del mouse cuando se usa Terminal Services. El [**objeto PenInputPanel**](peninputpanel-class.md) no funciona a través de una conexión de Terminal Services.

## <a name="pen-input-panel-input-modes"></a>Modos de entrada del panel de entrada del lápiz

El [**objeto PenInputPanel permite**](peninputpanel-class.md) la funcionalidad del teclado o la entrada de escritura a mano, con teclados adicionales para ayudar a la entrada. La interfaz de usuario del panel de entrada del lápiz incluye:

-   Panel de escritura
-   Panel de escritura para idiomas de Este de Asia
-   Teclados de QuickKeys
-   Teclado local

La disponibilidad del panel de escritura frente al panel de escritura para idiomas de Asia Oriental depende de la configuración regional predeterminada del usuario en el sistema operativo.

### <a name="writing-pad"></a>Panel de escritura

El panel de escritura se parece a la conocida interfaz de usuario del panel de entrada.

El panel de escritura recopila escritura a mano del usuario final. La interfaz de usuario básica incluye una sola línea de escritura en la que el usuario puede escribir texto con un lápiz digital. Cuando el usuario termina de escribir y pulsa el botón Enviar o espera a que se agote el tiempo de espera, la escritura a mano se envía al reconocedor.

La entrada de lápiz se reconoce una vez transcurrido un período de tiempo especificado desde el momento en que se recopiló el último trazo de lápiz. Cuando se agota el tiempo de espera, se quita la entrada de lápiz de la superficie de la colección y se produce el reconocimiento. A continuación, el texto reconocido se inserta en el control al que está asociado [**el objeto PenInputPanel.**](peninputpanel-class.md)

### <a name="east-asian-multibox-pad"></a>Panel multibox de Asia Oriental

La versión este de Asia del panel de entrada del lápiz muestra una interfaz multibox para escribir caracteres asiáticos. Proporciona alternativas y es similar a la interfaz de usuario del panel de entrada. Los usuarios pueden corregir caracteres desconocidos pulsando en un cuadro de escritura y seleccionando el carácter correcto de una lista de alternativas en la barra de la parte superior del panel de entrada del lápiz. Los botones de filtro están disponibles para restringir la lista de alternativas de reconocimiento a los tipos de caracteres especificados, como los símbolos.

Las versiones en coreano y japonés del panel de escritura tienen una clave de conversión además de las mini teclas rápidas que son comunes a todas las máscaras de idioma.

Para obtener caracteres latinos en el panel de escritura para idiomas de Asia Oriental, establezca la [**propiedad Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) para aumentar la precisión del reconocimiento de caracteres latinos. Establezca el **miembro Digit** del objeto [**Factoid**](factoid-constants.md) para caracteres numéricos o el **miembro OneChar** del objeto **Factoid** para caracteres alfabéticos y numéricos.

### <a name="quickkeys-keypads"></a>Teclados quickkeys

El panel de entrada del lápiz proporciona dos teclados pequeños para escribir símbolos y números.

### <a name="in-place-keyboard"></a>Teclado local

El panel de entrada del lápiz proporciona un modo de teclado para situaciones en las que el reconocimiento de escritura a mano no es suficiente. Por ejemplo, al escribir una contraseña o un número de parte, es probable que los usuarios tengan más éxito con el teclado del panel de entrada del lápiz que con el panel de escritura. Esto se debe a que es poco probable que las contraseñas o números de partes estén en el diccionario de reconocedor del panel de escritura.

## <a name="recognizer-support"></a>Compatibilidad con reconocedor

El [**objeto PenInputPanel admite**](peninputpanel-class.md) reconocedores de envío para Windows XP Tablet PC Edition versión 1.0 y el SDK de Tablet PC versión 1.5.

## <a name="automatic-positioning"></a>Posicionamiento automático

De forma predeterminada, el panel de entrada del lápiz se coloca automáticamente en relación con el control al que está asociado. No se superpone al control a menos que no haya suficiente espacio de pantalla para el panel de entrada del lápiz y el control, o a menos que el desarrollador establezca explícitamente la posición del panel de entrada del lápiz.

Funciones de posicionamiento automático solo cuando el desarrollador no ha establecido explícitamente la posición mediante el [**método MoveTo.**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) Para invalidar el posicionamiento automático, cambie los valores de las propiedades [**Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) en un controlador de eventos [**PanelMoving.**](peninputpanel-panelmoving.md)

La posición del panel de entrada del lápiz está restringida por los bordes de la pantalla. Ningún borde del panel de entrada del lápiz puede estar más cerca de 0,25 pulgadas desde cualquier borde de la pantalla.

De forma predeterminada, la parte superior del panel de entrada del lápiz aparece en la parte inferior del control al que está asociado y se separa del control por el valor de la [**propiedad VerticalOffset.**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) Si no hay suficiente espacio debajo del control, la parte inferior del panel de entrada del lápiz aparece en la parte superior del control al que está asociado y se separa del control por el valor de la **propiedad VerticalOffset.** Si todavía no hay suficiente espacio, como en el caso de un control de edición a pantalla completa, el panel de entrada del lápiz se superpone al control.

El panel de entrada del lápiz del borde izquierdo aparece en el borde izquierdo del control al que está asociado y está separado del control por el valor de la propiedad [**HorizontalOffset,**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) excepto cuando está delimitado por la pantalla. Si la posición deseada coloca el panel de entrada del lápiz más allá de los límites de pantalla disponibles, el panel de entrada del lápiz asume la posición horizontal más cercana posible.

### <a name="forced-overlap"></a>Superposición forzada

A veces es necesario que el panel de entrada del lápiz superponga el control adjunto, como en el caso de un control de edición de pantalla completa. En tales casos, el posicionamiento automático del panel de entrada del lápiz se determina mediante las reglas siguientes:

-   Cuando el punto de inserción se encuentra en la mitad superior del control adjunto, la posición vertical del panel de entrada del lápiz se encuentra en la parte inferior de la pantalla, lo que posiblemente lo coloca sobre la parte inferior del control.
-   Cuando el punto de inserción se encuentra en la mitad inferior del control adjunto, la posición vertical del panel de entrada del lápiz se encuentra en la parte superior de la pantalla, lo que posiblemente lo coloca sobre la mitad superior del control.

### <a name="windowless-controls"></a>Controles sin ventana

En el caso de que un [**objeto PenInputPanel**](peninputpanel-class.md) esté asociado a un control sin ventanas, el panel de entrada del lápiz se coloca en relación con el elemento primario del control sin ventanas. Establezca las [**propiedades Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) en un controlador de eventos [**PanelMoving**](peninputpanel-panelmoving.md) o use el [**método MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) para colocar manualmente el panel de entrada del lápiz.

 

 
