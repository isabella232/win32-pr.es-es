---
description: A partir de la versión 1,0 del kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition, el panel de entrada de Tablet PC de nivel de sistema proporciona un mecanismo universal para realizar la entrada de texto en la plataforma Windows, aunque no proporciona acceso mediante programación. El objeto del SDK de Tablet PC versión 1,5 PenInputPanel integra las herramientas de entrada de texto en las aplicaciones.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: Acerca del panel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db733e49e49d428b5ff8072a1315787d9fafd25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423512"
---
# <a name="about-the-input-panel"></a>Acerca del panel de entrada

\[[**PenInputPanel**](peninputpanel-class.md) ha sido reemplazado por [**TextInput**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel). Para obtener más información, vea [programar el panel de entrada de texto](programming-the-text-input-panel.md).\]

A partir de la versión 1,0 del kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition, el panel de entrada de Tablet PC de nivel de sistema proporciona un mecanismo universal para realizar la entrada de texto en la plataforma Windows, aunque no proporciona acceso mediante programación. El objeto del SDK de Tablet PC versión 1,5 [**PenInputPanel**](peninputpanel-class.md) integra las herramientas de entrada de texto en las aplicaciones.

En el gráfico siguiente se muestra el panel de entrada del lápiz que se muestra sobre el ejemplo de [formulario de notificaciones automáticas](auto-claims-form-sample.md) .

![panel de entrada del lápiz mostrado en el ejemplo de formulario de notificaciones automáticas](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

El objeto [**PenInputPanel**](peninputpanel-class.md) es práctico para los desarrolladores de aplicaciones. No es necesario reemplazar los controles de los formularios existentes. Simplemente puede adjuntar objetos **PenInputPanel** a los controles existentes que reciben la entrada de texto y pueden empezar a recibir la entrada del objeto **PenInputPanel** .

El objeto [**PenInputPanel**](peninputpanel-class.md) adopta la configuración del panel de entrada para las siguientes propiedades:

-   Diseño
-   Grosor de la tinta
-   Tiempo de espera de reconocimiento
-   Tamaño de cuadro, modo de envío y otras opciones de configuración específicas de la entrada con conversión boxing asiática oriental

El objeto [**PenInputPanel**](peninputpanel-class.md) no proporciona acceso a la tinta subyacente. Para obtener la entrada de lápiz, use el control [InkPicture](inkpicture-control-reference.md) .

El objeto [**PenInputPanel**](peninputpanel-class.md) proporciona una interfaz de usuario (UI) en contexto que los usuarios finales de las aplicaciones pueden detectar fácilmente. Se activa automáticamente cuando el usuario puntea en una ventana con un objeto **PenInputPanel** mediante el lápiz de Tablet PC. El panel de entrada del lápiz aparece automáticamente cuando el sistema detecta un evento CursorButtonUp para la ventana a la que se adjunta el objeto **PenInputPanel** . La activación automática puede deshabilitarse si se establece la propiedad [**Autoshow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) en **false**.

El panel de entrada del lápiz no aparece automáticamente en los eventos del mouse. Los eventos de lápiz se convierten en eventos del mouse cuando se usa Terminal Services. El objeto [**PenInputPanel**](peninputpanel-class.md) no funciona en una conexión Terminal Services.

## <a name="pen-input-panel-input-modes"></a>Modos de entrada del panel de entrada de lápiz

El objeto [**PenInputPanel**](peninputpanel-class.md) permite la funcionalidad de teclado o la entrada de escritura a mano, con teclados adicionales para ayudar a la entrada. La interfaz de usuario del panel de entrada del lápiz incluye:

-   Panel de escritura
-   Panel de escritura para idiomas de Asia oriental
-   Teclados de QuickKeys
-   Teclado en contexto

La disponibilidad del panel de escritura en lugar del panel de escritura de los idiomas de Asia Oriental depende de la configuración regional predeterminada del usuario en el sistema operativo.

### <a name="writing-pad"></a>Panel de escritura

El panel de escritura es similar a la conocida interfaz de usuario del panel de entrada.

El panel de escritura recopila escritura a mano del usuario final. La interfaz de usuario básica incluye una sola línea de escritura en la que el usuario puede escribir texto con un lápiz digital. Cuando el usuario termina de escribir y pulsa el botón Enviar o espera a que se produzca un tiempo de espera, se envía al reconocedor de escritura a mano.

La entrada de lápiz se reconoce después de que haya transcurrido un período de tiempo especificado desde el momento en que se recopiló el último trazo de tinta. Cuando se agota el tiempo de espera, se quita la tinta de la superficie de la colección y se produce el reconocimiento. A continuación, se inserta el texto reconocido en el control al que está asociado el objeto [**PenInputPanel**](peninputpanel-class.md) .

### <a name="east-asian-multibox-pad"></a>Panel de MULTIBOX de Asia oriental

La versión asiática oriental del panel de entrada del lápiz muestra una interfaz MULTIBOX para escribir caracteres asiáticos. Proporciona alternativas y es similar a la interfaz de usuario del panel de entrada. Los usuarios pueden corregir los caracteres mal reconocidos punteando en un cuadro de escritura y seleccionando el carácter correcto en una lista de alternativas de la barra situada en la parte superior del panel de entrada del lápiz. Los botones de filtro están disponibles para restringir la lista de alternativas de reconocimiento a los tipos de caracteres especificados, como los símbolos.

Las versiones de Coreano y japonés del panel de escritura tienen una clave de conversión además de las teclas rápidas que son comunes a todas las máscaras de lenguaje.

Para obtener caracteres latinos en el panel de escritura para idiomas de Asia oriental, establezca la propiedad [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) para aumentar la precisión del reconocimiento de caracteres latinos. Establezca el miembro **digit** del objeto [**Factoid**](factoid-constants.md) para los caracteres numéricos o el miembro **OneChar** del objeto **Factoid** para los caracteres alfabéticos y numéricos.

### <a name="quickkeys-keypads"></a>Teclados de QuickKeys

El panel de entrada del lápiz proporciona dos teclados pequeños para escribir símbolos y números.

### <a name="in-place-keyboard"></a>Teclado en contexto

El panel entrada manuscrita proporciona un modo de teclado en situaciones en las que el reconocimiento de escritura a mano no es suficiente. Por ejemplo, al escribir una contraseña o un número de pieza, es probable que los usuarios tengan más éxito con el teclado del panel de entrada del lápiz que el panel de escritura. Esto se debe a que es improbable que las contraseñas o los números de pieza estén en el Diccionario de reconocedor del panel de escritura.

## <a name="recognizer-support"></a>Compatibilidad con el reconocedor

El objeto [**PenInputPanel**](peninputpanel-class.md) admite reconocedores de envío para Windows XP Tablet PC Edition versión 1,0 y la versión 1,5 del SDK de Tablet PC.

## <a name="automatic-positioning"></a>Posicionamiento automático

De forma predeterminada, el panel de entrada del lápiz se coloca automáticamente en relación con el control al que está asociado. No se superpone al control a menos que no haya suficiente espacio real de pantalla para el panel de entrada del lápiz y el control, o a menos que el desarrollador establezca la posición del panel de entrada del lápiz explícitamente.

La colocación automática solo funciona cuando el desarrollador no ha establecido explícitamente la posición mediante el método [**moveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) . Para invalidar la posición automática, cambie los valores de las propiedades [**superior**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**izquierda**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) en un controlador de eventos [**PanelMoving**](peninputpanel-panelmoving.md) .

La posición del panel de entrada del lápiz está restringida por los bordes de la pantalla. Ningún borde del panel de entrada del lápiz puede tener más de 0,25 pulgadas desde cualquier borde de la pantalla.

De forma predeterminada, la parte superior del panel de entrada del lápiz aparece en la parte inferior del control al que está adjunto y se separa del control por el valor de la propiedad [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) . Si no hay suficiente espacio debajo del control, la parte inferior del panel de entrada del lápiz aparece en la parte superior del control al que está adjunto y se separa del control por el valor de la propiedad **VerticalOffset** . Si todavía no hay suficiente espacio, como sucede en el caso de un control de edición de pantalla completa, el panel de entrada del lápiz se superpone al control.

El panel de entrada del lápiz de borde izquierdo aparece en el borde izquierdo del control al que está adjunto y se separa del control por el valor de la propiedad [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) , excepto según lo límite de la pantalla. Si la posición deseada coloca el panel de entrada del lápiz más allá de los límites de pantalla disponibles, el panel de entrada del lápiz supone la posición horizontal más cercana posible.

### <a name="forced-overlap"></a>Superposición forzada

A veces es necesario que el panel de entrada del lápiz se superponga al control adjunto, como en el caso de un control de edición de pantalla completa. En tales casos, el posicionamiento automático del panel de entrada del lápiz se determina mediante las siguientes reglas:

-   Cuando el punto de inserción está en la mitad superior del control adjunto, la posición vertical del panel de entrada del lápiz se encuentra en la parte inferior de la pantalla, lo que posiblemente lo coloca sobre la parte inferior del control.
-   Cuando el punto de inserción está en la mitad inferior del control adjunto, la posición vertical del panel de entrada del lápiz se encuentra en la parte superior de la pantalla, lo que posiblemente lo coloca sobre la mitad superior del control.

### <a name="windowless-controls"></a>Controles sin ventana

En el caso de que un objeto [**PenInputPanel**](peninputpanel-class.md) se adjunte a un control sin ventana, el panel de entrada del lápiz se coloca en relación con el elemento primario del control sin ventana. Establezca las propiedades [**superior**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**izquierda**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) en un controlador de eventos [**PanelMoving**](peninputpanel-panelmoving.md) o use el método [**moveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) para colocar manualmente el panel de entrada del lápiz.

 

 
