---
description: Un complemento de reconocedor es un objeto que supervisa el movimiento del lápiz de Tablet PC en busca de gestos, escritura a mano u otros objetos.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Complementos de reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3ac866a211a78e2d8f347e89ca20a1906f436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568731"
---
# <a name="recognizer-plug-ins"></a>Complementos de reconocedor

Un complemento de reconocedor es un objeto que supervisa el movimiento del lápiz de Tablet PC en busca de gestos, escritura a mano u otros objetos.

## <a name="system-gestures"></a>Gestos del sistema

El objeto [**RealTimeStylus**](realtimestylus-class.md) reconoce los gestos del sistema. El objeto **RealTimeStylus** agrega un objeto [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) a la cola [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en respuesta a los datos que finalizan el gesto, como un objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) para [SystemGesture](/previous-versions/bb345349(v=vs.100)). Para obtener más información, vea [datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-gesturerecognizer-object"></a>El objeto GestureRecognizer

El objeto [**GestureRecognizer**](gesturerecognizer-class.md) implementa las interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) y [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . El objeto **GestureRecognizer** reconoce los gestos de la aplicación. Internamente, el objeto **GestureRecognizer** usa el reconocedor de gestos de Microsoft para realizar el reconocimiento de gestos.

Cuando el objeto [**GestureRecognizer**](gesturerecognizer-class.md) reconoce un gesto, agrega datos de lápiz personalizados a la cola de [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en respuesta al objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) del trazo. La propiedad [CustomDataId](/previous-versions/ms824748(v=msdn.10)) del objeto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) se establece en el valor [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) y la propiedad [Data](/previous-versions/ms824749(v=msdn.10)) del objeto CustomStylusData contiene un objeto [GestureRecognitionData](/previous-versions/ms824594(v=msdn.10)) .

En el diagrama siguiente se ilustra cómo el objeto [**GestureRecognizer**](gesturerecognizer-class.md) agrega datos a los datos del lápiz de Tablet PC.

![Ilustración del flujo de datos de GestureRecognizer](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

En este diagrama, el círculo "SD" representa un objeto [StylusDownData](/previous-versions/ms824107(v=msdn.10)) y los círculos "P" representan objetos [PacketsData](/previous-versions/ms824590(v=msdn.10)) que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. El círculo "SU" representa un objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónicos y, a continuación, se coloca en la cola de salida. Los círculos con letras "GR" representan los datos del lápiz óptico que se agregan a la cola de entrada mediante el complemento [**GestureRecognizer**](gesturerecognizer-class.md) en respuesta a la notificación del lápiz óptico asociada a "su". A continuación, se pasa a los complementos sincrónicos y, a continuación, a la cola de salida, los datos del lápiz óptico personalizados que se pasan a la carta de salida antes de procesar los siguientes datos del lápiz de Tablet PC. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

De forma predeterminada, el objeto [**GestureRecognizer**](gesturerecognizer-class.md) solo reconoce los gestos de un solo trazo; sin embargo, el objeto **GestureRecognizer** se puede establecer para que reconozca los gestos de multitrazo. En el caso de los gestos de multitrazo, el objeto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) se agrega a la cola [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en respuesta al objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) para el trazo final del gesto. Al reconocer los gestos de multitrazo, puede recibir notificaciones para conjuntos de trazos superpuestos. Por ejemplo, el primer y el segundo trazo juntos se pueden reconocer como un gesto y el segundo trazo solo se puede reconocer como un gesto. Para obtener más información sobre el reconocimiento de gestos de multitrazo, vea la clase **GestureRecognizer** y la propiedad [MaxStrokeCount](/previous-versions/ms826053(v=msdn.10)) .

Si usa el objeto [**GestureRecognizer**](gesturerecognizer-class.md) para el reconocimiento de gestos de multitrazo, puede lograr un rendimiento óptimo mediante el uso de un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada y asociar el objeto **GestureRecognizer** al objeto **RealTimeStylus** secundario. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Consideraciones especiales

En la lista siguiente se describen otros puntos que se deben tener en cuenta al usar el objeto [**GestureRecognizer**](gesturerecognizer-class.md) .

-   No debe adjuntar un objeto [**GestureRecognizer**](gesturerecognizer-class.md) a más de un objeto [**RealTimeStylus**](realtimestylus-class.md) . Una vez que se habilitan dos objetos **RealTimeStylus** a los que está asociado el objeto **GestureRecognizer** , ocurre lo siguiente.
    -   El objeto [**GestureRecognizer**](gesturerecognizer-class.md) produce una excepción en respuesta a la segunda llamada a su método RealTimeStylusEnabled.
    -   El segundo objeto [**RealTimeStylus**](realtimestylus-class.md) que se ha habilitado genera un objeto [datoserror](/previous-versions/ms824740(v=msdn.10)) y notifica los complementos restantes en sus colecciones de complementos del error.
    -   El objeto [**GestureRecognizer**](gesturerecognizer-class.md) deja de reconocer gestos.
-   El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción cuando se llama a su método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) con el parámetro *GUID* establecido en el identificador único global (GUID) de [Microsoft. StylusInput. GestureRecognizer. GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) .
-   El objeto [**GestureRecognizer**](gesturerecognizer-class.md) se implementa como un contenedor com (modelo de objetos componentes) y no se puede llamar directamente a sus métodos de interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Para obtener más información sobre la implementación de COM y el objeto [**RealTimeStylus**](realtimestylus-class.md) , consulte [las notas de implementación de las API de StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-gesture-recognition"></a>Reconocimiento de gestos personalizados

Puede crear un complemento de reconocedor personalizado que reconozca la escritura a mano, los gestos u otros objetos de la siguiente manera:

-   Pasar la información del trazo a un objeto de [reconocedor](/previous-versions/ms829434(v=msdn.10)) existente y usar el método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) para agregar los resultados al flujo de datos del lápiz de Tablet PC.
-   Realizar el reconocimiento en el complemento y usar el método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) para agregar los resultados al flujo de datos del lápiz de Tablet PC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gestos de aplicación](application-gestures.md)
</dt> <dt>

[Gestos del sistema](system-gestures.md)
</dt> <dt>

[Escala de tiempo de los mensajes del mouse y eventos del sistema](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
