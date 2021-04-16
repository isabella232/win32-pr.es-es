---
description: Información general sobre las consideraciones generales de subprocesos.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Consideraciones generales de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f825ec7a1397dae7d60aa14b31603ee76a2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542139"
---
# <a name="general-threading-considerations"></a>Consideraciones generales de subprocesos

A continuación se enumeran consideraciones generales de subprocesos al desarrollar para Tablet PC.

-   [Subprocesos de aplicación y que no son de aplicación](#application-and-non-application-threads)
-   [Consideraciones de rendimiento](#performance-considerations)
    -   [Controladores de eventos](#event-handlers)
    -   [AutoRedraw (propiedad)](#autoredraw-property)
    -   [Propiedad DynamicRendering](#dynamicrendering-property)
-   [Consideraciones sobre los subprocesos de eventos](#event-threading-considerations)
    -   [Eventos de objetos InkCollector y InkOverlay](#inkcollector-and-inkoverlay-objects-events)
    -   [Eventos de colección de trazos y objetos de entrada manuscrita](#ink-object-and-strokes-collection-events)
    -   [Eventos de reconocimiento](#recognition-events)
    -   [Eventos del panel de entrada de lápiz](#pen-input-panel-events)
-   [Temas relacionados](#related-topics)

## <a name="application-and-non-application-threads"></a>Subprocesos de aplicación y que no son de aplicación

Todos los eventos de entrada de lápiz se generan en un subproceso de entrada de lápiz independiente de alta prioridad. Esto permite que la tinta fluya sin problemas, incluso cuando una aplicación se ejecuta lentamente. Sin embargo, los controladores de eventos pueden ralentizar o bloquear la representación de la entrada de lápiz.

Todos los eventos de reconocimiento generados por llamadas al método de reconocimiento en segundo plano se administran en un subproceso de reconocimiento en segundo plano de prioridad normal.

Todos los eventos del mouse se generan en el subproceso de la interfaz de usuario principal de la aplicación.

## <a name="performance-considerations"></a>Consideraciones de rendimiento

### <a name="event-handlers"></a>Controladores de eventos

La interfaz de programación de aplicaciones (API) de la plataforma de Tablet PC tiene un modelo interactivo para eventos en lugar de un modelo de notificación. Mantenga el código en los controladores de eventos cortos para reducir el tiempo que se bloquea la representación de tinta. La colección de tinta de Tablet PC no está bloqueada, pero la aplicación no recibe la tinta mientras se bloquea la aplicación.

### <a name="autoredraw-property"></a>AutoRedraw (propiedad)

Cuando la aplicación está realizando una representación personalizada o cuando la aplicación es sensible a los problemas de dibujo, puede controlar el repintado y establecer la propiedad [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) en **false** para el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control.md) . Utilice los eventos de la tabla siguiente para controlar el repintado.



| Objeto o control                                            | Evento                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Objeto<br/> | Control del control subyacente [. eventos invalidados](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) y [control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Objeto<br/>     | Control del control subyacente [. eventos invalidados](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) y [control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/>                                 |
| [InkPicture](inkpicture-control.md) Control<br/>      | Control heredado del control [InkPicture](inkpicture-control.md) [. eventos invalidados](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) y [control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/> |



 

### <a name="dynamicrendering-property"></a>Propiedad DynamicRendering

Cuando la aplicación está realizando una representación personalizada o cuando desea la información, pero no la tinta, puede controlar la colocación de la tinta usted mismo y desactivar la representación en tiempo real de la entrada de lápiz estableciendo la propiedad [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) en **false** para el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control.md) .

## <a name="event-threading-considerations"></a>Consideraciones sobre los subprocesos de eventos

Los eventos de la API de la plataforma de Tablet PC se generan en varios subprocesos.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>Eventos de objetos InkCollector y InkOverlay

La mayoría de los eventos de objeto [**InkCollector**](inkcollector-class.md) y [**InkOverlay**](inkoverlay-class.md) se generan en el subproceso de entrada manuscrita. En el subproceso de la interfaz de usuario solo se producen los eventos del mouse para estos objetos. Por ejemplo, para el objeto **InkCollector** , se genera el evento [**MouseDown**](inkcollector-mousedown.md) en el subproceso de la interfaz de usuario y el evento [**CursorDown**](inkcollector-cursordown.md) se genera en el subproceso de entrada manuscrita.

### <a name="ink-object-and-strokes-collection-events"></a>Eventos de colección de trazos y objetos de entrada manuscrita

Los eventos de la colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) y objetos de [**tinta**](inkdisp-class.md) pueden provienen del subproceso de entrada manuscrita o del subproceso de interfaz de usuario. Cuando la aplicación manipula el objeto de **entrada de lápiz** o la colección de **trazos** , el evento se genera en el subproceso de la interfaz de usuario. Cuando el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) actualiza el objeto de **entrada de lápiz** o la colección de **trazos** , el evento se genera en el subproceso de entrada manuscrita.

Los controles [InkPicture](inkpicture-control-reference.md) y [InkEdit](inkedit-control-reference.md) operan en un contenedor uniproceso (STA). Cuando el control InkPicture o InkEdit actualiza el objeto de [**entrada de lápiz**](inkdisp-class.md) o la colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , el evento se genera en el subproceso de la interfaz de usuario.

### <a name="recognition-events"></a>Eventos de reconocimiento

Los eventos de reconocimiento se producen en el subproceso de interfaz de usuario o en el subproceso de reconocimiento en segundo plano.

-   El método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) del control [InkEdit](inkedit-control-reference.md) genera el evento [reconocimiento](/previous-versions/ms836436(v=msdn.10)) (solo biblioteca administrada) o [**RecognitionResult**](inkedit-recognitionresult.md) (solo Automation) en el subproceso de la interfaz de usuario.
-   Los métodos [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) y [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) generan los eventos [**Recognition**](inkrecognizercontext-recognition.md) y [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) en el subproceso de reconocimiento en segundo plano.

### <a name="pen-input-panel-events"></a>Eventos del panel de entrada de lápiz

Los eventos [**PenInputPanel**](peninputpanel-class.md) se generan en el subproceso en el que se crea el objeto **PenInputPanel** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. Ink. InkCollector. DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft. Ink. InkCollector. AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

