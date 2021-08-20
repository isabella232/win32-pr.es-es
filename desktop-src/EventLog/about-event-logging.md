---
description: Cuando se produce un error, el administrador del sistema o el representante de soporte técnico deben determinar qué produjo el error, intentar recuperar los datos perdidos e impedir que el error se repita.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Acerca del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9f30e4f8a44594b95215d748ac5cafda6b0633eefa668d0d864362c8f3c5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814262"
---
# <a name="about-event-logging"></a>Acerca del registro de eventos

Cuando se produce un error, el administrador del sistema o el representante de soporte técnico deben determinar qué produjo el error, intentar recuperar los datos perdidos e impedir que el error se repita. Resulta útil si las aplicaciones, el sistema operativo y otros servicios del sistema registran eventos importantes, como condiciones de memoria baja o intentos excesivos de acceder a un disco. A continuación, el administrador del sistema puede usar el registro de eventos para ayudar a determinar qué condiciones provocaron el error e identificar el contexto en el que se produjo. Al ver periódicamente el registro de eventos, el administrador del sistema puede identificar problemas (como un disco duro con errores) antes de que causen daños.

> [!Note]  
> Event Logging API se diseñó para aplicaciones que se ejecutan en Windows Server 2003, Windows XP o Windows sistema operativo 2000. En Windows Vista, se ha rediseñado la infraestructura de registro de eventos. Las aplicaciones diseñadas para ejecutarse en Windows Vista o sistemas operativos posteriores ahora deben usar Windows [de](/windows/desktop/WES/windows-event-log) eventos para registrar eventos.

 
En esta sección se describe la interfaz de programación para escribir y consumir eventos mediante el registro de eventos.

-   [Tipos de evento](event-types.md)
-   [Directrices de registro](logging-guidelines.md)
-   [Elementos de registro de eventos](event-logging-elements.md)
-   [Operaciones de registro de eventos](event-logging-operations.md)
-   [Modelo de registro de eventos](event-logging-model.md)
-   [Seguridad del registro de eventos](event-logging-security.md)

> [!Note]  
> Las aplicaciones que publican eventos de más de 64 kilobytes en un equipo de Windows Server 2003, Windows XP o Windows 2000 no podrán publicar eventos en un equipo Windows Vista o posterior.
