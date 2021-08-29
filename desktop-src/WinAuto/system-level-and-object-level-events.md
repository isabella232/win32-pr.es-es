---
title: System-Level y Object-Level eventos
description: Microsoft Active Accessibility usa tres clases de nivel de sistema WinEvents, nivel de objeto y consola.
ms.assetid: 3333fe6c-38cd-4e7e-be4b-94c9f824e7e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab93b5780ceb960b7ad15ce220dcc8a7a0801aae8f7fec9cb8211417906b82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133638"
---
# <a name="system-level-and-object-level-events"></a>System-Level y Object-Level eventos

Microsoft Active Accessibility usa tres clases de WinEvents: nivel *de* sistema, *nivel de objeto* y *consola*. Cada tiene uno de los siguientes valores constantes [de evento](event-constants.md) correspondientes:

-   Las constantes de evento que comienzan por EVENT \_ SYSTEM identifican eventos de nivel de sistema. Estos eventos describen situaciones que afectan a todas las aplicaciones del sistema.
-   Las constantes de evento que comienzan por EVENT \_ OBJECT identifican eventos de nivel de objeto. Estos eventos pertenecen a situaciones específicas de objetos dentro de una aplicación.
-   Las constantes de evento que comienzan por EVENT \_ CONSOLE identifican eventos de nivel de consola. Estos eventos indican cambios en las ventanas de consola.

El sistema operativo y las aplicaciones de servidor generan las clases de eventos de nivel de sistema y de objeto. El sistema operativo genera eventos de nivel de sistema y de nivel de objeto para los escenarios siguientes:

-   Notificaciones de todo el sistema sobre los cambios de foco
-   Cambios de activación
-   Eventos relacionados con objetos proporcionados por el sistema, como controles comunes

Las aplicaciones de servidor generan eventos de nivel de sistema para objetos personalizados que replican objetos del sistema, como menús personalizados y barras de desplazamiento.

Las aplicaciones de servidor suelen generar eventos de nivel de objeto para los cambios en los objetos accesibles que contienen, como la creación, destrucción y selección de objetos.

Aunque el sistema genera eventos de nivel de objeto para objetos [**de**](window.md) ventana, los servidores también deben enviar eventos de nivel de objeto para cada objeto accesible contenido en una ventana. Por ejemplo, si una aplicación de servidor registra una clase de ventana definida por la aplicación para crear un control personalizado, el sistema genera eventos de nivel de objeto para la ventana que contiene el control personalizado; el servidor genera eventos de nivel de objeto para el objeto accesible que proporciona información sobre el control.

Los servidores solo generan eventos de nivel de objeto para los controles personalizados para los que implementan la [**interfaz IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Para obtener más información, vea [Custom Interfaz de usuario Elements](custom-user-interface-elements.md).

 

 




