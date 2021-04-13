---
title: Eventos System-Level y Object-Level
description: Microsoft Active Accessibility usa tres clases de nivel de sistema, nivel de objeto y consola de WinEvents.
ms.assetid: 3333fe6c-38cd-4e7e-be4b-94c9f824e7e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d14a0469527a7654dd3e323adb47d650866ca9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356953"
---
# <a name="system-level-and-object-level-events"></a>Eventos System-Level y Object-Level

Microsoft Active Accessibility usa tres clases de WinEvents: *nivel de sistema*, *nivel de objeto* y *consola*. Cada una de ellas tiene uno de los siguientes valores de [constantes de evento](event-constants.md) correspondientes:

-   Las constantes de evento que comienzan con el sistema de eventos \_ identifican los eventos de nivel de sistema. Estos eventos describen situaciones que afectan a todas las aplicaciones del sistema.
-   Las constantes de evento que comienzan con \_ el objeto de evento identifican los eventos de nivel de objeto. Estos eventos pertenecen a situaciones específicas de objetos dentro de una aplicación.
-   Las constantes de evento que comienzan con la \_ consola de eventos identifican eventos en el nivel de consola. Estos eventos indican cambios en las ventanas de la consola.

El sistema operativo y las aplicaciones de servidor generan las clases de eventos de nivel de objeto y de sistema. El sistema operativo genera eventos de nivel de sistema y de nivel de objeto para los siguientes escenarios:

-   Notificaciones en todo el sistema sobre los cambios de foco
-   Cambios de activación
-   Eventos relacionados con los objetos proporcionados por el sistema, como los controles comunes

Las aplicaciones de servidor generan eventos de nivel de sistema para objetos personalizados que replican objetos del sistema, como menús personalizados y barras de desplazamiento.

Normalmente, las aplicaciones de servidor generan eventos de nivel de objeto para los cambios en los objetos accesibles que contienen, como la creación, la destrucción y la selección de objetos.

Aunque el sistema genera eventos de nivel de objeto para los objetos de [**ventana**](window.md) , los servidores también deben enviar eventos de nivel de objeto para todos los objetos accesibles incluidos en una ventana. Por ejemplo, si una aplicación de servidor registra una clase de ventana definida por la aplicación para crear un control personalizado, el sistema genera eventos de nivel de objeto para la ventana que contiene el control personalizado. el servidor genera eventos de nivel de objeto para el objeto accesible que proporciona información sobre el control.

Los servidores solo generan eventos de nivel de objeto para los controles personalizados para los que implementan la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Para obtener más información, vea elementos de la [interfaz de usuario personalizados](custom-user-interface-elements.md).

 

 




