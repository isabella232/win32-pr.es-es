---
description: Las siguientes consideraciones de subprocesos de Tablet PC son específicas de cuando se usan el modelo de objetos componentes (COM) y la automatización.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Consideraciones sobre el subproceso de automatización y COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705445"
---
# <a name="com-and-automation-threading-considerations"></a>Consideraciones sobre el subproceso de automatización y COM

Las siguientes consideraciones de subprocesos de Tablet PC son específicas de cuando se usan el modelo de objetos componentes (COM) y la automatización.

-   [Seguridad para subprocesos](#thread-safety)
-   [Aplicaciones STA y MTA](#sta-and-mta-applications)
-   [InkCollector y InkOverlay](#inkcollector-and-inkoverlay)
-   [Receptores de eventos](#event-sinks)
-   [Excepciones dentro de los controladores de eventos](#exceptions-within-event-handlers)
-   [Temas relacionados](#related-topics)

## <a name="thread-safety"></a>Seguridad para subprocesos

A excepción de los controles [InkPicture](inkpicture-control.md) y [InkEdit](inkedit-control.md) , los objetos de Tablet PC son seguros para subprocesos y se marcan como ambos. Al marcarse como Both, se pueden ejecutar en un contenedor uniproceso (STA) o en un contenedor multiproceso (MTA).

Windows Forms usa el modelo STA porque Windows Forms se basa en ventanas nativas de Win32 que son subprocesos de Apartamento inherentemente.

## <a name="sta-and-mta-applications"></a>Aplicaciones STA y MTA

Si la aplicación se ejecuta en un MTA o usa el contador de referencias de subprocesamiento libre (FTM), debe escribir código seguro para subprocesos; sin embargo, si lo hace, puede mejorar determinados problemas de rendimiento de control de eventos.

## <a name="inkcollector-and-inkoverlay"></a>InkCollector y InkOverlay

La aplicación no debe liberar su referencia final a [**InkCollector**](inkcollector-class.md) o el objeto [**InkOverlay**](inkoverlay-class.md) , de modo que se destruya el objeto directamente del subproceso de entrada manuscrita. En su lugar, la aplicación debe liberar el objeto **InkCollector** o **InkOverlay** de un subproceso de aplicación.

**PRECAUCIÓN:** Una aplicación marcada como MTA o usa el FTM, que permite llamadas directas desde el subproceso de entrada manuscrita al apartamento de la aplicación, puede liberar su referencia final al objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) directamente desde el subproceso de entrada manuscrita; sin embargo, esto provoca un error irrecuperable en la aplicación.

## <a name="event-sinks"></a>Receptores de eventos

Si la aplicación no usa el FTM y un objeto y su receptor de eventos se crean en distintos apartamentos, el evento se ejecuta en el subproceso que atiende al receptor de eventos.

## <a name="exceptions-within-event-handlers"></a>Excepciones dentro de los controladores de eventos

Las excepciones que se inician desde los controladores de eventos de Tablet PC se consumen y no son visibles para el resto o la aplicación. Del mismo modo, los valores HRESULT no se propagan desde los controladores de eventos de Tablet PC. Si una aplicación que utiliza el nivel COM inicia una excepción, el subproceso en segundo plano finaliza y se pierde la excepción. No se llamará a ningún controlador de eventos adicional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de receptores de eventos de C++](c---event-sinks-sample.md)
</dt> <dt>

[Consideraciones generales de subprocesos](general-threading-considerations.md)
</dt> <dt>

[Consideraciones sobre los subprocesos de biblioteca administrada](managed-library-threading-considerations.md)
</dt> </dl>

 

 



