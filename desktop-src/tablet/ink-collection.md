---
description: La colección de lápiz comienza con el digitalizador.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Ink Collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45988ea93aac5016391e22c352b9d0123a5e122f4a79c55e41e06834ed040e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452072"
---
# <a name="ink-collection"></a>Ink Collection

La colección de lápiz comienza con el digitalizador. Un usuario coloca un lápiz en el digitalizador y comienza a escribir. Puede usar las características de la colección de lápiz de la API para administrar la colección de datos de entrada de lápiz que "fluyen" desde el lápiz. Tiene acceso a información sobre el hardware disponible en Tablet PC a través de la colección [**Tabletas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) y el [**objeto Tablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) A continuación, use [**el objeto InkCollector**](inkcollector-class.md) para obtener los datos que proceden del digitalizador.

## <a name="tablets-and-the-tablet-object"></a>Tabletas y el objeto de tableta

Una [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) representa un dispositivo digitalizador de Tablet PC. Un tablet PC puede tener más de un digitalizador. Con el **objeto Tableta,** puede consultar los dispositivos digitalizadores disponibles que están conectados a Tablet PC y sus respectivas funcionalidades de hardware. Por ejemplo, puede determinar si la **tableta** con la que está trabajando está integrada con la pantalla o si es un dispositivo externo independiente.

## <a name="inkcollector-object"></a>InkCollector (objeto)

El [**objeto InkCollector**](inkcollector-class.md) captura la entrada de lápiz de los dispositivos [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) disponibles. El **objeto InkCollector** solo recopila la entrada de lápiz y los gestos que se introducen en una ventana específica. Un receptor de eventos muy eficaz representa esta entrada en tiempo real. El **objeto InkCollector** captura la entrada y la dirige a un [**objeto Ink.**](inkdisp-class.md)

> [!Note]  
> La colocación simultánea de la entrada de lápiz con varios lápices puede funcionar o no, en función de las funcionalidades de hardware del dispositivo digitalizador.

 

### <a name="how-the-ink-collector-works"></a>Funcionamiento del recopilador de lápiz

El [**objeto InkCollector**](inkcollector-class.md) se asocia a una ventana de aplicación conocida. A continuación, permite a los usuarios emplear cualquier dispositivo Tablet PC disponible (incluido el mouse) para poner la entrada de lápiz en tiempo real en esa ventana. Los trazos de lápiz que recopila se almacenan en un objeto [**Ink**](inkdisp-class.md) asociado. Estos trazos se pueden manipular o enviar a un reconocedor para su reconocimiento. El **objeto InkCollector** también notifica a la aplicación cuando un cursor entra en el intervalo de cualquiera de los dispositivos Tablet PC que se usan.

Para que [**el objeto InkCollector**](inkcollector-class.md) establezca con precisión el cursor del mouse dentro de una ventana habilitada para lápiz, esa ventana debe poder recibir el mensaje **\_ SETCURSOR** de WM. Esto es correcto para todas las ventanas normales, pero, para un control dentro de un cuadro de diálogo, el elemento primario del diálogo del control filtra este mensaje. Para que el control reciba el mensaje, establezca el **estilo NOTIFY \_ de SS.**

## <a name="inkoverlay-object"></a>InkOverlay (objeto)

El [**objeto InkCollector,**](inkcollector-class.md) que se ha analizado anteriormente, es útil para que las aplicaciones proporcionen su propio modelo para seleccionar, borrar y otra interacción del usuario. El [**objeto InkOverlay**](inkoverlay-class.md) es un superconjunto del objeto **InkCollector** que proporciona compatibilidad con la edición. Esto es útil para que las aplicaciones integren el dibujo y la edición de lápiz en su propio lienzo de documento mediante un conjunto de modelos de selección de entrada de lápiz estándar que proporciona el objeto .

Tanto el objeto [**InkCollector**](inkcollector-class.md) como el objeto [**InkOverlay**](inkoverlay-class.md) (así como el control [InkPicture)](inkpicture-control.md) usan construcciones comunes, como el objeto [**Ink**](inkdisp-class.md) y la colección [**DrawingAttributes,**](inkdrawingattributes-class.md) para que la manera básica de cambiar el color de la entrada de lápiz sea la misma en todas partes. Esto le permite reutilizar el código y tener acceso común mediante programación, lo que puede ser especialmente importante si ofrece compatibilidad con scripting en la aplicación.

[**InkOverlay**](inkoverlay-class.md) es un objeto COM que resulta útil para escenarios de anotación en los que los usuarios no están interesados en realizar el reconocimiento en la entrada de lápiz, sino que, en su lugar, están interesados en el tamaño, la forma, el color y la posición de la entrada de lápiz. Es adecuado para tomar notas y la transcripción básica. La interfaz de usuario predeterminada es un rectángulo transparente con entrada de lápiz opaca.

[**InkOverlay**](inkoverlay-class.md) extiende la [**clase InkCollector**](inkcollector-class.md) de tres maneras:

-   Genera eventos para el trazo de inicio, el trazo final y los cambios en los atributos de entrada de lápiz.
-   Permite a los usuarios seleccionar, borrar y cambiar el tamaño de la entrada de lápiz.
-   Admite los comandos Cortar, Copiar y Pegar.

Un escenario típico en el [**que InkOverlay**](inkoverlay-class.md) es útil es marcar una diapositiva o imagen de presentación. El **objeto InkOverlay** permite una implementación sencilla de las funcionalidades de lápiz y diseño que requiere este escenario.

Para trabajar con [**InkOverlay,**](inkoverlay-class.md)haga lo siguiente:

1.  Cree una instancia de [**un objeto InkOverlay.**](inkoverlay-class.md)
2.  Adjunte el hWnd (identificador, en código administrado) de una ventana a la propiedad [**hWnd**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) del objeto [**InkOverlay**](inkoverlay-class.md) (propiedad [Handle,](/previous-versions/ms582171(v=vs.100)) en código administrado).
3.  Establezca la propiedad Enabled [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) del objeto [**InkOverlay**](inkoverlay-class.md) en **TRUE.**

El [**objeto InkOverlay**](inkoverlay-class.md) incluye compatibilidad básica con la impresión, pero debe implementar la vista previa de impresión u otras funcionalidades avanzadas de impresión.

[**InkOverlay conserva**](inkoverlay-class.md) la entrada de lápiz en formato serializado de entrada de lápiz (ISF).

> [!Note]  
> Si [**editingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) del objeto [**InkOverlay**](inkoverlay-class.md) está establecido en **Eliminar** o Seleccionar **,** se desencadenan otros eventos (como [**InkAdded,**](inkdisp-inkadded.md) [**InkDeleted**](inkdisp-inkdeleted.md)y [**Stroke).**](inkoverlay-stroke.md) Estos eventos son útiles si desea implementar sus propios modos de eliminación o selección.

 

### <a name="selecting-ink"></a>Selección de Ink

El [**objeto InkOverlay**](inkoverlay-class.md) permite a los usuarios usar una herramienta de pestañas para seleccionar objetos de entrada de lápiz contenidos en una región de seguimiento. Los usuarios también pueden seleccionar la entrada de lápiz pulsando cualquier [**objeto Ink.**](inkdisp-class.md)

Use la [**propiedad Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) para devolver una [**colección Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que puede usar para manipular la selección de un usuario.

Cuando se [**selecciona un**](inkdisp-class.md) objeto Ink o un conjunto de objetos **Ink,** los identificadores de ajuste de tamaño aparecen en las cuatro esquinas del cuadro de límite de la entrada de lápiz y en todos los puntos intermedios entre las esquinas adyacentes. Si el usuario arrastra cualquier lugar dentro de la región seleccionada, la entrada de lápiz se puede mover dentro del control.

### <a name="default-behavior"></a>Comportamiento predeterminado

El [**objeto InkOverlay**](inkoverlay-class.md) se establece para recopilar entrada de lápiz de forma predeterminada. La entrada de lápiz tiene 53 unidades de espacio de entrada de lápiz de ancho (donde 1 unidad de espacio de entrada de lápiz = 1 HIMETRIC). La entrada de lápiz es negra si el usuario no se ejecuta en modo de contraste alto. De lo contrario, la entrada de lápiz se establece en el **valor \_ DE COLOR WINDOWTEXT** (**WindowText** en código administrado). [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) es **FALSE.**

### <a name="cursor-and-button-objects"></a>Objetos de cursor y botón

Un cursor corresponde a la punta del lápiz que se usa en tablet PC. Por ejemplo, un lápiz tiene dos extremos. Normalmente, se usa un extremo para escribir y el otro para borrar. Estos dos extremos corresponden a dos cursores. La [**clase Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) no se debe confundir con [**System.Windows. Forms.Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

En Tablet PC, normalmente se define un cursor para usarse para escribir o borrar. Un cursor puede cambiar los roles si la aplicación habilita esta funcionalidad. Algunos dispositivos tablet PC permiten varios lápices. Cada cursor tiene un identificador de cursor asociado que es único en el sistema. Un cursor puede tener cero o más botones asociados. Estos botones se proporcionan a la aplicación como objetos CursorButton. La aplicación puede proporcionar un objeto [**DrawingAttributes**](inkdrawingattributes-class.md) específico para cualquier cursor determinado.

### <a name="drawing-attributes-object"></a>Objeto Atributos de dibujo

Un [**objeto DrawingAttributes**](inkdrawingattributes-class.md) describe cómo se va a dibujar cualquier conjunto conocido de lápiz. Un **objeto DrawingAttributes** incluye propiedades básicas como [**Color,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color) [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)y [**PenTip.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip) También puede abarcar parámetros avanzados, como la transparencia variable y el suavizado Bezier, que pueden proporcionar efectos interesantes o mejorar la legibilidad de la entrada de lápiz.

### <a name="peninputpanel-object"></a>PenInputPanel (objeto)

> [!Note]  
> La [**clase PenInputPanel**](peninputpanel-class.md) está en desuso. La **clase PenInputPanel** se ha reemplazado por la [**clase TextInputPanel.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)

 

El [**objeto PenInputPanel**](peninputpanel-class.md) permite agregar fácilmente entradas de lápiz en su lugar a las aplicaciones. **PenInputPanel está** disponible como un objeto adjuntable que le permite agregar la funcionalidad panel de entrada de Tablet PC a los controles existentes. La interfaz de usuario se exige en gran medida por el idioma de entrada actual. Tiene la opción de elegir el método de entrada predeterminado para **PenInputPanel,** ya sea la escritura a mano o el teclado. El usuario final puede cambiar entre métodos de entrada mediante botones en la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InkCollector (Clase, C++)**](inkcollector-class.md)
</dt> <dt>

[**InkOverlay (Clase, C++)**](inkoverlay-class.md)
</dt> <dt>

[**Espacio de nombres Microsoft.Ink**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
