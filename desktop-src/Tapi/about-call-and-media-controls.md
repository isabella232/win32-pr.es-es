---
description: Los controles de llamada y multimedia de TAPI 3 son un conjunto genérico de objetos COM, interfaces y métodos para realizar llamadas entre dos o más máquinas.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Acerca de los controles de llamada y multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914182"
---
# <a name="about-call-and-media-controls"></a>Acerca de los controles de llamada y multimedia

Los controles de llamada y multimedia de TAPI 3 son un conjunto genérico de objetos COM, interfaces y métodos para realizar llamadas entre dos o más máquinas. En el contexto de TAPI 3, la *llamada* a hace referencia no solo a la transmisión de voz a través de la red telefónica conmutada (RTC), sino a cualquier mecanismo medio y de transporte para el que existan proveedores de servicios: por ejemplo, una conferencia de multidifusión multimedia que se ejecute en una intranet corporativa.

Los cinco objetos principales de la arquitectura de control multimedia y de llamadas TAPI 3 son [TAPI](tapi-object.md), [Dirección](address-object.md), [terminal](terminal-object.md), [llamada](call-object.md)y [CallHub](callhub-object.md). Además, se ha realizado el aprovisionamiento de [interfaces específicas del proveedor](provider-specific-interfaces.md).

En el diagrama siguiente se muestra cómo interactúan estos objetos.

![interacciones entre los objetos de llamada y control multimedia de TAPI 3,0](images/sdkobj2.png)

## <a name="features"></a>Características

-   Abstrae la funcionalidad de llamada y multimedia para permitir que protocolos de comunicación diferentes y aparentemente incompatibles expongan una interfaz común a las aplicaciones.
-   Basado en el modelo de objetos componentes (COM) para que las aplicaciones se puedan escribir prácticamente en cualquier lenguaje. Si necesita información adicional sobre COM, consulte el kit de desarrollo de software (SDK) de la plataforma.
-   Control de llamadas proporcionado por los proveedores de servicios de telefonía (profesionales), que implementan mecanismos específicos del transporte.
-   Control multimedia proporcionado por los proveedores de servicios multimedia (MSP). Los MSP actuales usan DirectShow. DirectShow es un sistema modular de componentes conectables denominado filtros, organizados en una configuración denominada gráfico de filtros. El administrador de gráficos de filtros supervisa la conexión de estos filtros y controla el flujo de datos de la secuencia. Si necesita información adicional sobre DirectShow, consulte el SDK de la plataforma.

 

 



