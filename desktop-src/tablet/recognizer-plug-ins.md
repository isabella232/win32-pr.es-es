---
description: Un complemento de reconocedor es un objeto que supervisa el movimiento del lápiz de tableta en busca de gestos, escritura a mano u otros objetos.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Complementos de Recognizer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3ac866a211a78e2d8f347e89ca20a1906f436
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467160"
---
# <a name="recognizer-plug-ins"></a>Complementos de Recognizer

Un complemento de reconocedor es un objeto que supervisa el movimiento del lápiz de tableta en busca de gestos, escritura a mano u otros objetos.

## <a name="system-gestures"></a>Gestos del sistema

El [**objeto RealTimeStylus**](realtimestylus-class.md) reconoce los gestos del sistema. El objeto **RealTimeStylus** agrega un objeto [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) a la cola [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en respuesta a los datos que finalizan el gesto, como un objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) para [SystemGesture](/previous-versions/bb345349(v=vs.100)). Para obtener más información, vea [Datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-gesturerecognizer-object"></a>El objeto GestureRecognizer

El [**objeto GestureRecognizer**](gesturerecognizer-class.md) implementa las interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) El **objeto GestureRecognizer** reconoce los gestos de la aplicación. Internamente, **el objeto GestureRecognizer usa** el reconocedor de gestos de Microsoft para realizar el reconocimiento de gestos.

Cuando el [**objeto GestureRecognizer**](gesturerecognizer-class.md) reconoce un gesto, agrega datos de lápiz personalizados a la cola [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en respuesta al objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) del trazo. La propiedad [CustomDataId](/previous-versions/ms824748(v=msdn.10)) del objeto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) se establece en el valor [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) y la propiedad [Data](/previous-versions/ms824749(v=msdn.10)) del objeto CustomStylusData contiene un objeto [GestureRecognitionData.](/previous-versions/ms824594(v=msdn.10))

En el diagrama siguiente se muestra cómo el objeto [**GestureRecognizer**](gesturerecognizer-class.md) agrega datos a los datos del lápiz de tableta.

![ilustración del flujo de datos gesturerecognizer](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

En este diagrama, el círculo con la letra "SD" representa un objeto [StylusDownData](/previous-versions/ms824107(v=msdn.10)) y los círculos con la letra "P" representan objetos [PacketsData](/previous-versions/ms824590(v=msdn.10)) que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con letra "SU" representa un [objeto StylusUpData](/previous-versions/ms824057(v=msdn.10)) que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónica y, a continuación, se coloca en la cola de salida. Los círculos con letra "GR" representan datos de lápiz óptico personalizados que el complemento [**GestureRecognizer**](gesturerecognizer-class.md) agrega a la cola de entrada en respuesta a la notificación de lápiz óptico asociada a "SU". A continuación, los datos del lápiz óptico personalizados con letra "GR" se pasan a los complementos sincrónicos y, a continuación, a la cola de salida antes de que se procese el siguiente lápiz de tableta. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

De forma predeterminada, [**el objeto GestureRecognizer**](gesturerecognizer-class.md) solo reconoce gestos de un solo trazo; sin embargo, **el objeto GestureRecognizer** se puede establecer para reconocer gestos de varias pulsaciones. Para los gestos de pulsación múltiple, el objeto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) se agrega a la cola [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en respuesta al objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) para el trazo final del gesto. Al reconocer gestos de pulsación múltiple, puede recibir notificaciones de conjuntos superpuestos de trazos. Por ejemplo, el primer y segundo trazos juntos se pueden reconocer como un gesto y el segundo trazo por sí mismo se puede reconocer como un gesto. Para obtener más información sobre el reconocimiento de gestos multistroke, vea la clase **GestureRecognizer** y la [propiedad MaxStrokeCount.](/previous-versions/ms826053(v=msdn.10))

Si usa el objeto [**GestureRecognizer**](gesturerecognizer-class.md) para el reconocimiento de gestos de múltiples pulsaciones, puede lograr un rendimiento óptimo mediante un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada y adjuntar el objeto **GestureRecognizer** al objeto **Secundario RealTimeStylus.** Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Consideraciones especiales

En la lista siguiente se describen otros puntos que se deben tener en cuenta al usar el objeto [**GestureRecognizer.**](gesturerecognizer-class.md)

-   No debe adjuntar un [**objeto GestureRecognizer**](gesturerecognizer-class.md) a más de un [**objeto RealTimeStylus.**](realtimestylus-class.md) Una vez que se habilitan dos objetos **RealTimeStylus** a los que está asociado el objeto **GestureRecognizer,** se produce lo siguiente.
    -   El [**objeto GestureRecognizer**](gesturerecognizer-class.md) produce una excepción en respuesta a la segunda llamada a su método RealTimeStylusEnabled.
    -   El segundo [**objeto RealTimeStylus**](realtimestylus-class.md) habilitado genera un objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) y notifica el error a los complementos restantes en sus colecciones de complementos.
    -   El [**objeto GestureRecognizer**](gesturerecognizer-class.md) deja de reconocer gestos.
-   El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción cuando se llama a su método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) con el parámetro *GUID* establecido en el identificador único global (GUID) [Microsoft.StylusInput.GestureRecognizer.GestureRecognitionDataGuid.](/previous-versions/ms826344(v=msdn.10))
-   El objeto [**GestureRecognizer**](gesturerecognizer-class.md) se implementa como un contenedor del Modelo de objetos componentes (COM) y no se puede llamar directamente a sus métodos de interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Para obtener más información sobre la implementación com y el [**objeto RealTimeStylus,**](realtimestylus-class.md) vea Notas de implementación de [las API StylusInput.](implementation-notes-for-the-stylusinput-apis.md)

## <a name="custom-gesture-recognition"></a>Reconocimiento de gestos personalizados

Puede crear un complemento de reconocedor personalizado que reconozca escritura a mano, gestos u otros objetos mediante:

-   Pasar la información del trazo a un objeto [Recognizer](/previous-versions/ms829434(v=msdn.10)) existente y usar el método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) para agregar los resultados al flujo de datos del lápiz de tableta.
-   Realizar el reconocimiento en el complemento y usar el [método AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) para agregar los resultados al flujo de datos del lápiz de tableta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gestos de aplicación](application-gestures.md)
</dt> <dt>

[Gestos del sistema](system-gestures.md)
</dt> <dt>

[Escala de tiempo de mensajes del mouse y eventos del sistema](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
