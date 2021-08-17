---
description: Información general sobre las consideraciones generales de subprocesamiento.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Consideraciones generales sobre subprocesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f4c6f2aa76775d3d88e8ea60c3899a2d8ac47e5ef07fddbbdfaca96196dee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092579"
---
# <a name="general-threading-considerations"></a>Consideraciones generales sobre subprocesamiento

A continuación se presentan consideraciones generales sobre el subprocesamiento al desarrollar para Tablet PC.

-   [Subprocesos de aplicación y que no son de aplicación](#application-and-non-application-threads)
-   [Consideraciones de rendimiento](#performance-considerations)
    -   [Controladores de eventos](#event-handlers)
    -   [Propiedad AutoRedraw](#autoredraw-property)
    -   [Propiedad DynamicRendering](#dynamicrendering-property)
-   [Consideraciones sobre el subprocesamiento de eventos](#event-threading-considerations)
    -   [Eventos de objetos InkCollector y InkOverlay](#inkcollector-and-inkoverlay-objects-events)
    -   [Eventos de colección de objetos ink y trazos](#ink-object-and-strokes-collection-events)
    -   [Eventos de reconocimiento](#recognition-events)
    -   [Eventos del panel de entrada del lápiz](#pen-input-panel-events)
-   [Temas relacionados](#related-topics)

## <a name="application-and-non-application-threads"></a>Subprocesos de aplicación y que no son de aplicación

Todos los eventos de entrada de lápiz se generan en un subproceso de entrada de lápiz independiente de alta prioridad. Esto permite que la entrada de lápiz fluya sin problemas incluso cuando una aplicación se ejecuta lentamente. Sin embargo, los controladores de eventos pueden ralentizar o bloquear la representación de la entrada de lápiz.

Todos los eventos de reconocimiento generados por llamadas a métodos de reconocimiento en segundo plano se controlan en un subproceso de reconocimiento en segundo plano independiente de prioridad normal.

Todos los eventos del mouse se generan en el subproceso de interfaz de usuario (UI) principal de la aplicación.

## <a name="performance-considerations"></a>Consideraciones de rendimiento

### <a name="event-handlers"></a>Controladores de eventos

La interfaz de programación de aplicaciones (API) de tablet PC Platform tiene un modelo interactivo para eventos en lugar de un modelo de notificación. Mantenga el código en controladores de eventos cortos para reducir el tiempo que se bloquea la representación de entrada de lápiz. La colección de entrada de lápiz de Tablet PC no está bloqueada, pero la aplicación no recibe la entrada de lápiz mientras la aplicación está bloqueada.

### <a name="autoredraw-property"></a>Propiedad AutoRedraw

Cuando la aplicación realiza una representación personalizada o cuando la aplicación es sensible a problemas de dibujo, puede controlar el repintado usted mismo y establecer la propiedad [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) en **false** para el objeto [**InkCollector,**](inkcollector-class.md) el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture.](inkpicture-control.md) Use los eventos de la tabla siguiente para controlar el repintado.



| Objeto o control                                            | Evento                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Objeto<br/> | Eventos [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) y [Control.Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del control subyacente.<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Objeto<br/>     | Eventos [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) y [Control.Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del control subyacente.<br/>                                 |
| [InkPicture](inkpicture-control.md) Control<br/>      | Eventos [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) y [Control.Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) heredados del control [InkPicture.](inkpicture-control.md)<br/> |



 

### <a name="dynamicrendering-property"></a>Propiedad DynamicRendering

Cuando la aplicación realiza una representación personalizada o cuando desea la información, pero no la entrada de lápiz, puede controlar la creación de la entrada de lápiz usted mismo y desactivar la representación en tiempo real de la entrada de lápiz estableciendo la propiedad [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) en **false** para el objeto [**InkCollector,**](inkcollector-class.md) el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture.](inkpicture-control.md)

## <a name="event-threading-considerations"></a>Consideraciones sobre el subprocesamiento de eventos

Los eventos de la API de la plataforma de Tablet PC se crean en varios subprocesos.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>Eventos de objetos InkCollector y InkOverlay

La mayoría de los eventos de [**objeto InkCollector**](inkcollector-class.md) y [**InkOverlay**](inkoverlay-class.md) se genera en el subproceso de entrada manuscrita. Solo los eventos del mouse para estos objetos se genera en el subproceso de interfaz de usuario. Por ejemplo, para el objeto **InkCollector,** el evento [**MouseDown**](inkcollector-mousedown.md) se genera en el subproceso de interfaz de usuario y el [**evento CursorDown**](inkcollector-cursordown.md) se genera en el subproceso ink.

### <a name="ink-object-and-strokes-collection-events"></a>Eventos de colección de objetos ink y trazos

Los [**eventos del objeto Ink**](inkdisp-class.md) y de la colección [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) pueden proceder del subproceso de entrada de lápiz o del subproceso de interfaz de usuario. Cuando la aplicación manipula el objeto **Ink** o **la colección Strokes,** el evento se genera en el subproceso de interfaz de usuario. Cuando el [**objeto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) actualiza el objeto **Ink** o la colección **Strokes,** el evento se genera en el subproceso ink.

Los [controles InkPicture](inkpicture-control-reference.md) [y InkEdit](inkedit-control-reference.md) funcionan en un apartamento de un solo subproceso (STA). Cuando el control InkPicture o InkEdit actualiza el objeto [**Ink**](inkdisp-class.md) o la colección [**Strokes,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) el evento se genera en el subproceso de interfaz de usuario.

### <a name="recognition-events"></a>Eventos de reconocimiento

Los eventos de reconocimiento se genera en el subproceso de interfaz de usuario o en el subproceso de reconocimiento en segundo plano.

-   El método Recognize [](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) del control [InkEdit](inkedit-control-reference.md) genera el evento [Recognition](/previous-versions/ms836436(v=msdn.10)) (solo managed library) o [**RecognitionResult**](inkedit-recognitionresult.md) (solo Automation) en el subproceso de la interfaz de usuario.
-   Los métodos [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) y [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) provoca los eventos [**Recognition**](inkrecognizercontext-recognition.md) y [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) en el subproceso de reconocimiento en segundo plano.

### <a name="pen-input-panel-events"></a>Eventos del panel de entrada del lápiz

[**Los eventos PenInputPanel**](peninputpanel-class.md) se genera en el subproceso en el que se crea el objeto **PenInputPanel.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft.Ink.InkCollector.DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft.Ink.InkCollector.AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

