---
description: La colección de entradas manuscritas comienza con el digitalizador.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Colección de entradas manuscritas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fcd5bf0d73f48e63366843c85c9d6dd7cd388f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540435"
---
# <a name="ink-collection"></a>Colección de entradas manuscritas

La colección de entradas manuscritas comienza con el digitalizador. Un usuario coloca un lápiz en el digitalizador y comienza a escribir. Puede usar las características de recopilación de entradas manuscritas de la API para administrar la colección de datos de tinta que "fluye" desde el lápiz. Tiene acceso a información sobre el hardware disponible en Tablet PC a través de la colección [**tabletas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) y el objeto de [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . A continuación, use el objeto [**InkCollector**](inkcollector-class.md) para obtener los datos que provienen del digitalizador.

## <a name="tablets-and-the-tablet-object"></a>Tabletas y el objeto de Tablet PC

Una [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) representa un dispositivo digitalizador de Tablet PC. Un Tablet PC puede tener más de un digitalizador. Con el objeto de **tableta** , puede consultar los dispositivos de digitalización disponibles que están conectados a Tablet PC y sus capacidades de hardware respectivas. Por ejemplo, puede determinar si la **tableta** con la que trabaja está integrada con la pantalla o es un dispositivo externo independiente.

## <a name="inkcollector-object"></a>InkCollector (objeto)

El objeto [**InkCollector**](inkcollector-class.md) captura la entrada manuscrita de los dispositivos de [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) disponibles. El objeto **InkCollector** solo recopila entradas de lápiz y movimientos que se introducen en una ventana específica. Un receptor de eventos muy eficaz representa esta entrada en tiempo real. El objeto **InkCollector** captura la entrada y la dirige a un objeto de [**entrada de lápiz**](inkdisp-class.md) .

> [!Note]  
> La disposición simultánea de tinta con varios lápices puede funcionar o no, en función de las capacidades de hardware del dispositivo del digitalizador.

 

### <a name="how-the-ink-collector-works"></a>Cómo funciona el recopilador de tinta

El objeto [**InkCollector**](inkcollector-class.md) se adjunta a una ventana de la aplicación conocida. Después, permite a los usuarios emplear cualquier dispositivo de Tablet PC disponible (incluido el mouse) para diseñar la tinta en tiempo real en esa ventana. Los trazos de tinta que recopila se almacenan en un objeto de [**entrada manuscrita**](inkdisp-class.md) asociado. Estos trazos se pueden manipular o enviar a un reconocedor para su reconocimiento. El objeto **InkCollector** también notifica a la aplicación cuando un cursor entra en el intervalo de cualquiera de los dispositivos de Tablet PC que se están utilizando.

Para que el objeto [**InkCollector**](inkcollector-class.md) establezca con precisión el cursor del mouse en una ventana con tinta habilitada, esa ventana debe ser capaz de recibir el mensaje de **\_ SETCURSOR de WM** . Esto es correcto para todas las ventanas normales, pero para un control dentro de un cuadro de diálogo, el elemento primario del cuadro de diálogo del control filtra este mensaje. Para que el control reciba el mensaje, establezca el estilo de **\_ notificación SS** .

## <a name="inkoverlay-object"></a>Objeto InkOverlay

El objeto [**InkCollector**](inkcollector-class.md) , descrito anteriormente, resulta útil para que las aplicaciones proporcionen su propio modelo para seleccionar, borrar y otra interacción del usuario. El objeto [**InkOverlay**](inkoverlay-class.md) es un supraconjunto del objeto **InkCollector** que proporciona compatibilidad con la edición. Esto resulta útil para que las aplicaciones integren el dibujo y la edición de tinta en su propio lienzo del documento mediante un conjunto de modelos de selección de tinta estándar que proporciona el objeto.

Tanto el objeto [**InkCollector**](inkcollector-class.md) como el objeto [**InkOverlay**](inkoverlay-class.md) (así como el control [InkPicture](inkpicture-control.md) ) usan construcciones comunes, como el objeto [**Ink**](inkdisp-class.md) y la colección [**DrawingAttributes**](inkdrawingattributes-class.md) , de modo que la forma básica de cambiar el color de la tinta es la misma en todas partes. Esto le permite volver a usar el código y tener acceso mediante programación común, lo que puede ser especialmente importante si ofrece compatibilidad con scripting en la aplicación.

[**InkOverlay**](inkoverlay-class.md) es un objeto com que es útil para escenarios de anotación en los que los usuarios no están preocupados por realizar el reconocimiento de la entrada manuscrita, sino que, en su lugar, están interesados en el tamaño, la forma, el color y la posición de la tinta. Es adecuado para tomar notas y scribbling básicas. La interfaz de usuario predeterminada es un rectángulo transparente con tinta opaca.

[**InkOverlay**](inkoverlay-class.md) amplía la clase [**InkCollector**](inkcollector-class.md) de tres maneras:

-   Genera eventos para los cambios de los atributos de lápiz de inicio, de fin y de trazo.
-   Permite a los usuarios seleccionar, borrar y cambiar el tamaño de la tinta.
-   Admite comandos de cortar, copiar y pegar.

Un escenario típico en el que [**InkOverlay**](inkoverlay-class.md) es útil es marcar una imagen o una diapositiva de presentación. El objeto **InkOverlay** facilita la implementación de las capacidades de tinta y diseño que requiere este escenario.

Para trabajar con [**InkOverlay**](inkoverlay-class.md), puede:

1.  Cree una instancia de un objeto [**InkOverlay**](inkoverlay-class.md) .
2.  Adjunte el hWnd (identificador, en código administrado) de una ventana a la propiedad [**hWnd**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) del objeto [**InkOverlay**](inkoverlay-class.md) (propiedad [Handle](/previous-versions/ms582171(v=vs.100)) , en código administrado).
3.  Establezca la propiedad [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) del objeto [**InkOverlay**](inkoverlay-class.md) en **true**.

El objeto [**InkOverlay**](inkoverlay-class.md) incluye compatibilidad con la impresión básica, pero debe implementar la vista previa de impresión o cualquier otra funcionalidad de impresión avanzada.

[**InkOverlay**](inkoverlay-class.md) conserva la tinta en el formato serializado de entrada de lápiz (ISF).

> [!Note]  
> Si el valor de [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) del objeto [**InkOverlay**](inkoverlay-class.md) está establecido en **Delete** o **Select**, se desencadenan otros eventos (como [**InkAdded**](inkdisp-inkadded.md), [**InkDeleted**](inkdisp-inkdeleted.md)y [**Stroke**](inkoverlay-stroke.md)). Estos eventos son útiles si desea implementar sus propios modos de eliminación o selección.

 

### <a name="selecting-ink"></a>Seleccionar tinta

El objeto [**InkOverlay**](inkoverlay-class.md) permite a los usuarios usar una herramienta de lazo para seleccionar los objetos de entrada de lápiz contenidos en una región de la que se ha realizado un seguimiento. Los usuarios también pueden seleccionar la entrada manuscrita punteando en cualquier objeto de [**entrada de lápiz**](inkdisp-class.md) .

Use la propiedad [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) para devolver una colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que puede usar para manipular la selección de un usuario.

Cuando se selecciona un objeto de [**entrada manuscrita**](inkdisp-class.md) o un conjunto de objetos de **entrada de lápiz** , los controladores de tamaño aparecen en las cuatro esquinas del rectángulo de selección de la tinta y en todos los puntos intermedios entre las esquinas adyacentes. Si el usuario arrastra cualquier parte dentro de la región seleccionada, la tinta se convierte en movible dentro del control.

### <a name="default-behavior"></a>Comportamiento predeterminado

El objeto [**InkOverlay**](inkoverlay-class.md) está configurado para recopilar la entrada de lápiz de forma predeterminada. La tinta es 53 unidades de espacio de tinta de ancho (donde 1 unidad de espacio de tinta = 1 HIMETRIC). La tinta es negra si el usuario no se está ejecutando en modo de alto contraste. De lo contrario, Ink se establece en el valor de **color \_ WINDOWTEXT** (**WINDOWTEXT** en código administrado). [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) es **false**.

### <a name="cursor-and-button-objects"></a>Objetos de botón y cursor

Un cursor corresponde a la punta del lápiz que se usa en Tablet PC. Por ejemplo, un lápiz tiene dos extremos. Normalmente, un extremo se utiliza para la escritura y el otro se usa para el borrado. Estos dos extremos se corresponden con dos cursores. La clase [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) no se confundirá con [**System. Windows. Forms. cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

En Tablet PC, normalmente se define un cursor que se utilizará para escribir o borrar. Un cursor podría cambiar los roles si la aplicación habilita esta funcionalidad. Algunos dispositivos de Tablet PC permiten varios lápices. Cada cursor tiene un ID. de cursor asociado que es único en el sistema. Un cursor puede tener cero o más botones asociados. Estos botones se proporcionan a la aplicación como objetos CursorButton. La aplicación puede proporcionar un objeto [**DrawingAttributes**](inkdrawingattributes-class.md) específico para cualquier cursor determinado.

### <a name="drawing-attributes-object"></a>Drawing Attributes (objeto)

Un objeto [**DrawingAttributes**](inkdrawingattributes-class.md) describe cómo se dibuja cualquier conjunto conocido de entradas de lápiz. Un objeto **DrawingAttributes** incluye propiedades básicas como [**color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color), [**width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)y [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip). También puede incluir parámetros avanzados, como la transparencia de variables y el suavizado de Bézier, que pueden proporcionar efectos interesantes o mejorar la legibilidad de la tinta.

### <a name="peninputpanel-object"></a>Objeto PenInputPanel

> [!Note]  
> La clase [**PenInputPanel**](peninputpanel-class.md) está en desuso. La clase **PenInputPanel** se ha reemplazado por la clase [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .

 

El objeto [**PenInputPanel**](peninputpanel-class.md) permite agregar fácilmente entradas manuscritas en contexto a las aplicaciones. **PenInputPanel** está disponible como un objeto que se puede adjuntar y que permite agregar la funcionalidad del panel de entrada de Tablet PC a los controles existentes. La interfaz de usuario está asignada en gran medida por el idioma de entrada actual. Tiene la opción de elegir el método de entrada predeterminado para **PenInputPanel**, ya sea escritura a mano o teclado. El usuario final puede cambiar entre los métodos de entrada mediante los botones de la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InkCollector (clase) (C++)**](inkcollector-class.md)
</dt> <dt>

[**InkOverlay (clase) (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Espacio de nombres Microsoft. Ink**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
