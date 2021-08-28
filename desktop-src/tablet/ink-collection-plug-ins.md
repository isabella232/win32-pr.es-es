---
description: El objeto RealTimeStylus no recopila de forma inherente la entrada de lápiz. Para usar RealTimeStylus para recopilar entrada de lápiz, cree un complemento de recopilador de lápiz.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Ink-Collection complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64966e2d088e9145fa4a0c0b29a7f7cc787b8435a3e4a609e75eae27b4e25524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967214"
---
# <a name="ink-collection-plug-ins"></a>Ink-Collection complementos

El [**objeto RealTimeStylus**](realtimestylus-class.md) no recopila de forma inherente la entrada de lápiz. Para usar **RealTimeStylus para** recopilar entrada de lápiz, cree un complemento de recopilador de lápiz.

A continuación se muestra un escenario mínimo para usar el [**objeto RealTimeStylus**](realtimestylus-class.md) en un formulario que recopila lápiz.

1.  Cree un formulario que implemente la [**interfaz IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
2.  Cree un [**objeto RealTimeStylus**](realtimestylus-class.md) y adjójelo a un control en el formulario.
3.  Establezca el interés en las notificaciones StylusDown, Packets y StylusUp en la [propiedad DataInterest del](/previous-versions/ms574886(v=vs.100)) formulario.
4.  En los métodos [**StylusDown,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)y [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) del formulario, agregue código para controlar el lápiz óptico hacia abajo, los paquetes y las notificaciones de lápiz óptico que se envían desde el objeto [**RealTimeStylus**](realtimestylus-class.md) del formulario. Este código debe almacenar los datos del lápiz y crear y almacenar los trazos.

Para obtener un ejemplo de este tipo de aplicación, consulte el ejemplo de colección de lápiz [RealTimeStylus.](realtimestylus-ink-collection-sample.md)

> [!Note]  
> Cuando se produce un evento [DisplaySettingsChanged,](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) llame al método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) de los trazos recopilados en un controlador de eventos DisplaySettingsChanged para volver a calcular las propiedades [Width](/previous-versions/ms582112(v=vs.100)) [y Height.](/previous-versions/ms582106(v=vs.100)) Esto es necesario para tener en cuenta los posibles cambios de puntos por pulgada (ppp) resultantes del evento DisplaySettingsChanged.

 

## <a name="ink-collection-and-recognizers"></a>Ink Collection y Recognizers

Ni el análisis de lápiz ni el reconocimiento de escritura a mano son una función del [**objeto RealTimeStylus.**](realtimestylus-class.md) A medida que el complemento de recopilador de lápiz recopila la entrada de lápiz o cuando desea reconocerla, puede copiar la entrada de lápiz en un objeto [RecognizerContext](/previous-versions/ms552546(v=vs.100)) o [Divider.](/previous-versions/ms583616(v=vs.100)) Para obtener más información sobre el reconocimiento y el análisis de lápiz, vea [Acerca del reconocimiento de escritura a mano](about-handwriting-recognition.md) o El objeto [divisor](the-divider-object.md).

## <a name="static-rendering"></a>Representación estática

Para representar la entrada de lápiz mientras se recopila, adjunte un [objeto DynamicRenderer](/previous-versions/ms575176(v=vs.100)) al [**objeto RealTimeStylus.**](realtimestylus-class.md) Para representar la entrada de lápiz una vez recopilada, use un objeto [Representador](/previous-versions/ms552630(v=vs.100)) para dibujar los trazos en el objeto [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) adecuado. Para obtener más información sobre el objeto DynamicRenderer, vea [Complementos de representador dinámico.](dynamic-renderer-plug-ins.md) Para obtener un ejemplo de representación estática y dinámica, vea [RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md).

 

 
