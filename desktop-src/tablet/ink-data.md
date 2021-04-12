---
description: Una vez recopilada la tinta, las aplicaciones pueden administrar, manipular y/o transferir los datos a otros medios.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Datos de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de73291269398ae42a47ee26897c8da9bac8abe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541310"
---
# <a name="ink-data"></a>Datos de tinta

Una vez recopilada la tinta, las aplicaciones pueden administrar, manipular y/o transferir los datos a otros medios. Las acciones de seleccionar, copiar, mover, guardar, ver y modificar la entrada de lápiz tienen lugar en el objeto de [**entrada manuscrita**](inkdisp-class.md) y en sus miembros contenidos, como la colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) y los objetos de [**trazo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

> [!Note]  
> Con Real-Time lápiz, las aplicaciones pueden optar por mantener los datos en su propio formato (por ejemplo, guardar trazos).

 

## <a name="ink-strokes-and-packets"></a>Tinta, trazos y paquetes

Un objeto [**Ink**](inkdisp-class.md) es el tipo de datos fundamental que administra, manipula y almacena la entrada recopilada desde el objeto [**InkCollector**](inkcollector-class.md) . Un objeto **Ink** contiene uno o varios objetos [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) y métodos y propiedades comunes para administrar y manipular esos trazos. Un trazo se define como el conjunto de datos que se capturan en un solo lápiz, movimiento de lápiz y secuencia de lápiz. Los datos del trazo contienen una colección de paquetes. Un paquete es el conjunto de datos que el dispositivo de tableta envía en cada punto de ejemplo. Estos datos contienen información como las coordenadas, la presión del lápiz, el ángulo del lápiz y cualquier otro elemento que pueda transmitir el hardware. La propiedad [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) del objeto **Stroke** describe los paquetes que genera una [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

## <a name="strokes"></a>Trazos

Puede obtener una instantánea de los trazos en un objeto de [**entrada manuscrita**](inkdisp-class.md) utilizando la propiedad [**trazos**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) del objeto de **entrada manuscrita** . La propiedad **Strokes** es una colección de referencias a los trazos en el objeto **Ink** en el momento en que se lee la propiedad **Strokes** . Si posteriormente se agregan o eliminan trazos del objeto de **entrada manuscrita** , no se actualiza una colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) obtenida previamente. Además, la propiedad **Strokes** es un valor y, como cualquier valor, queda fuera del ámbito, a menos que se asigne a una variable.

Para mantener una propiedad [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) sincronizada con un objeto [**Ink**](inkdisp-class.md) , debe encapsularla en un controlador de eventos para los eventos [**StrokesAdded**](inkstrokes-strokesadded.md) y [**StrokesRemoved**](inkstrokes-strokesremoved.md) de la colección [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . El controlador debe obtener una nueva copia de la propiedad **Strokes** cuando se desencadena cualquiera de los eventos. Tenga cuidado de no agregar el controlador de eventos a una colección de **trazos** que esté fuera del ámbito antes de que se desencadene el evento.

Observe que en este ejemplo `theAddedStrokesIDs` se actualiza con una nueva copia de la propiedad Strokes en el `StrokesAdded_Event` controlador.


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

La propiedad [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) del objeto de [**entrada de lápiz**](inkdisp-class.md) define el conjunto de información de cada paquete que la aplicación obtiene de un dispositivo de Tablet PC. La información normalmente incluye coordenadas, pero puede incluir información mucho más detallada (en función de las capacidades del digitalizador de Tablet PC), como la presión del lápiz o el ángulo del lápiz. Al establecer descripciones de paquetes en el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) antes de que se recopile cualquier entrada de lápiz (mediante la propiedad DesiredPacketDescription), tendrá control total sobre cuál de las propiedades de dispositivos de Tablet PC desea recibir.

## <a name="extended-properties"></a>Propiedades extendidas

Las propiedades extendidas proporcionan un mecanismo para asociar los datos definidos por la aplicación a la [**entrada de lápiz**](inkdisp-class.md) y otros objetos. Para obtener más información sobre las propiedades extendidas, vea la colección [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) .

## <a name="ink-rendering"></a>Representación de entradas manuscritas

El objeto [**representador**](inkrenderer-class.md) es responsable de la representación de la [**entrada manuscrita**](inkdisp-class.md). Dado un contexto de tableta adecuado, el objeto de **representador** puede asignar coordenadas de espacio de tinta a píxeles, aplicar transformaciones de vista y mostrar la entrada de lápiz en pantallas e impresoras. Los métodos [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) y [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) son los métodos principales para representar la entrada de lápiz. Para obtener más información sobre cómo mostrar la entrada de lápiz en una ventana, vea el objeto **representador** .

## <a name="cusps"></a>Crestas

Normalmente, un trazo comienza cuando se baja el lápiz en la superficie de dibujo y termina cuando se genera el lápiz. Dentro de un trazo, los cambios de picos, ángulos y radicales de dirección se denominan crestas. Los puntos de conexión de un trazo también se consideran de cresta. Por ejemplo, la letra mayúscula "L" tiene tres elevaciones, una en el centro y otra en cada extremo.

A medida que se escribe un trazo, normalmente se suaviza y se representa mediante una curva Bézier (o Polyline). Las curvas de Bézier pueden convertir las cresta en bucles pequeños. Por ejemplo, el pico de la letra cursiva "i" se podría suavizar para que se parezca a la "e" cursiva. Para evitar esto, los representadores de Microsoft tienen una fase "anterior a Bézier" que controla las crestas de forma diferente.

También se pueden usar las cresta para subdividir los objetos de [**trazo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en unidades que se puedan borrar. Por ejemplo, si se selecciona el lado vertical de una "L" mayúscula, se podría indicar que se borrará solo ese lado. La parte del trazo que se va a borrar sería la parte entre dos cresta.

 

 
