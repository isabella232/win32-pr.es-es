---
description: Las siguientes consideraciones de subprocesos de Tablet PC son específicas de cuando se usan el modelo de objetos componentes (COM) y la automatización.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Consideraciones sobre subprocesamiento de COM y Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359663"
---
# <a name="com-and-automation-threading-considerations"></a>Consideraciones sobre subprocesamiento de COM y Automation

Las siguientes consideraciones de subprocesos de Tablet PC son específicas de cuando se usan el modelo de objetos componentes (COM) y la automatización.

-   [Seguridad para subprocesos](#thread-safety)
-   [Aplicaciones STA y MTA](#sta-and-mta-applications)
-   [InkCollector y InkOverlay](#inkcollector-and-inkoverlay)
-   [Receptores de eventos](#event-sinks)
-   [Excepciones en controladores de eventos](#exceptions-within-event-handlers)
-   [Temas relacionados](#related-topics)

## <a name="thread-safety"></a>Seguridad para subprocesos

A excepción [de los controles InkPicture](inkpicture-control.md) y [InkEdit,](inkedit-control.md) los objetos de tablet PC son seguros para subprocesos y se marcan como ambos. Al estar marcados como ambos, se pueden ejecutar en un único apartamento con subprocesos (STA) o en un apartamento multiproceso (MTA).

Windows formularios usan el modelo STA porque los formularios Windows Forms se basan en ventanas win32 nativas que son intrínsecamente subprocesos de apartamento.

## <a name="sta-and-mta-applications"></a>Aplicaciones STA y MTA

Si la aplicación se ejecuta en un MTA o usa el serializador de subprocesos libre (FTM), debe escribir código seguro para subprocesos. sin embargo, al hacerlo, puede mejorar ciertos problemas de rendimiento de control de eventos.

## <a name="inkcollector-and-inkoverlay"></a>InkCollector y InkOverlay

La aplicación no debe liberar su referencia final al [**objeto InkCollector**](inkcollector-class.md) o [**InkOverlay,**](inkoverlay-class.md) lo que destruye el objeto directamente desde el subproceso de entrada de lápiz. En su lugar, la aplicación debe liberar **el objeto InkCollector** o **InkOverlay** de un subproceso de aplicación.

**Precaución:** Una aplicación que está marcada como MTA o usa ftm, que permite llamadas directas desde el subproceso de entrada de lápiz al apartamento de la aplicación, puede liberar su referencia final al objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) directamente desde el subproceso de entrada de lápiz. sin embargo, esto provoca un error irrecuperable de la aplicación.

## <a name="event-sinks"></a>Receptores de eventos

Si la aplicación no usa ftm y un objeto y su receptor de eventos se crean en diferentes departamentos, el evento se ejecuta en el subproceso que da servicio al receptor del evento.

## <a name="exceptions-within-event-handlers"></a>Excepciones en controladores de eventos

Las excepciones que se inician desde los controladores de eventos de Tablet PC se consumen y no son visibles para el resto o la aplicación. Del mismo modo, los valores HRESULT no se propagan desde los controladores de eventos de Tablet PC. Si una aplicación que usa la capa COM produce una excepción, el subproceso en segundo plano finaliza y se pierde la excepción. No se llamará a ningún controlador de eventos adicional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de receptores de eventos de C++](c---event-sinks-sample.md)
</dt> <dt>

[Consideraciones generales sobre subprocesos](general-threading-considerations.md)
</dt> <dt>

[Consideraciones sobre subprocesos de biblioteca administrada](managed-library-threading-considerations.md)
</dt> </dl>

 

 



