---
description: Una vez recopilada la entrada de lápiz, las aplicaciones pueden administrar, manipular o transferir los datos a otros medios.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Datos de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f62f566e48859ba2aea7013783b3ccc8c825b8559fdec34e24438d68b6ee65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939415"
---
# <a name="ink-data"></a>Datos de entrada de lápiz

Una vez recopilada la entrada de lápiz, las aplicaciones pueden administrar, manipular o transferir los datos a otros medios. Las acciones de seleccionar, copiar, mover, guardar, ver y modificar la entrada de lápiz tienen lugar en el objeto [**Ink**](inkdisp-class.md) y sus miembros [**contenidos,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) como la colección Strokes y los objetos [**Stroke.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

> [!Note]  
> Con Real-Time Stylus, las aplicaciones pueden optar por mantener los datos en su propio formato (por ejemplo, guardar trazos).

 

## <a name="ink-strokes-and-packets"></a>Entrada de lápiz, trazos y paquetes

Un [**objeto Ink**](inkdisp-class.md) es el tipo de datos fundamental que administra, manipula y almacena la entrada recopilada del objeto [**InkCollector.**](inkcollector-class.md) Un **objeto Ink** contiene uno o varios objetos [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) y métodos y propiedades comunes para administrar y manipular esos trazos. Un trazo se define como el conjunto de datos que se captura en una sola secuencia de ala abajo, de movimiento de lápiz y de pen-up. Los datos del trazo contienen una colección de paquetes. Un paquete es el conjunto de datos que el dispositivo de tableta envía en cada punto de ejemplo. Estos datos contienen información como coordenadas, presión de lápiz, ángulo de lápiz y cualquier otra cosa que el hardware pueda transmitir. La [**propiedad PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) del **objeto Stroke** describe los paquetes que genera [**una**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) tableta.

## <a name="strokes"></a>Trazos

Puede obtener una instantánea de los trazos de un objeto [**Ink**](inkdisp-class.md) mediante la propiedad [**Strokes del objeto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) **Ink.** La **propiedad Strokes** es una colección de referencias a los trazos del objeto **Ink** en el momento en que se lee la propiedad **Strokes.** Si posteriormente se agregan o eliminan trazos del objeto **Ink,** no se actualiza una colección [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) obtenida previamente. Además, la **propiedad Strokes** es un valor y, como cualquier valor, sale del ámbito a menos que se asigne a una variable.

Para mantener [**sincronizada**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) una propiedad Strokes con un objeto [**Ink,**](inkdisp-class.md) envolverla en un controlador de eventos para los eventos [**StrokesAdded**](inkstrokes-strokesadded.md) y [**StrokesRemoved**](inkstrokes-strokesremoved.md) de la [**colección Strokes.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) El controlador debe obtener una nueva copia de la **propiedad Strokes** cuando se desencadena cualquier evento. Tenga cuidado de no agregar el controlador de eventos a una **colección Strokes** que esté fuera del ámbito antes de que se despeda el evento.

Observe que en este ejemplo `theAddedStrokesIDs` se actualiza con una nueva copia de la propiedad strokes en el `StrokesAdded_Event` controlador.


```C++
public void StrokesAdded_Event(object sender, StrokesEventArgs e)
{
    int [] theAddedStrokesIDs = e.StrokeIds;
    theListBox.Items.Clear();
    foreach (int i in theAddedStrokesIDs)
    {
        theListBox.Items.Add("Added Stroke ID: " + i.ToString());
    }
}
```



## <a name="packetdescription-property"></a>Propiedad PacketDescription

La [**propiedad PacketDescription**](inkdisp-class.md) del objeto [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) define el conjunto de información de cada paquete que la aplicación obtiene de un dispositivo Tablet PC. Normalmente, la información incluye coordenadas, pero puede incluir información mucho más detallada (en función de las funcionalidades del digitalizador de Tablet PC), como la presión de lápiz o el ángulo del lápiz. Al establecer descripciones de paquetes en el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) antes de recopilar cualquier entrada de lápiz (mediante la propiedad DesiredPacketDescription), tiene control total sobre cuáles de las propiedades de los dispositivos tablet PC desea recibir.

## <a name="extended-properties"></a>Propiedades extendidas

Las propiedades extendidas proporcionan un mecanismo para adjuntar datos definidos por la aplicación a [**Ink**](inkdisp-class.md) y otros objetos. Para obtener más información sobre las propiedades extendidas, vea [**la colección ExtendedProperties.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties)

## <a name="ink-rendering"></a>Representación de entrada de lápiz

El [**objeto Renderer**](inkrenderer-class.md) es responsable de representar [**Ink.**](inkdisp-class.md) Dado un contexto de tableta adecuado, el objeto **Representador** puede asignar coordenadas de espacio de entrada manuscrita a píxeles, aplicar transformaciones de vista y mostrar la entrada de lápiz en pantallas e impresoras. Los [**métodos Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) [**y DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) son los métodos principales para representar la entrada de lápiz. Para obtener más información sobre cómo mostrar la entrada de lápiz en una ventana, vea el **objeto Representador.**

## <a name="cusps"></a>Cúspides

Normalmente, un trazo comienza cuando el lápiz se baja a la superficie de dibujo y termina cuando se eleva el lápiz. Dentro de un trazo, los picos, ángulos y cambios radicales de dirección se denominan cúsps. Los puntos de conexión de un trazo también se consideran cúsps. Por ejemplo, la letra mayúscula "L" tiene tres cúsps, una en el centro y otra en cada extremo.

A medida que se introduce un trazo, normalmente se suaviza y se representa mediante una curva Bézier (o polilínea). Las curvas Bézier pueden convertir cúsps en bucles pequeños. Por ejemplo, el pico de la letra cursiva "i" podría suavizarse para que se parezca a la "e" cursiva. Para evitar esto, los representadores de Microsoft tienen una fase "anterior a Bézier" que controla los cúsps de forma diferente.

Las cusps también se pueden usar para subdividir objetos [**stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en unidades borrables. Por ejemplo, seleccionar el lado vertical de una "L" mayúscula podría indicar que se borra solo ese lado. La parte del trazo que se va a borrar sería la parte entre dos cúsps.

 

 
