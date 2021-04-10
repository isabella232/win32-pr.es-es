---
description: Cuando se produce un error, el administrador del sistema o el representante de soporte técnico deben determinar la causa del error, intentar recuperar los datos perdidos y evitar que el error se repita.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Acerca del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082233"
---
# <a name="about-event-logging"></a>Acerca del registro de eventos

Cuando se produce un error, el administrador del sistema o el representante de soporte técnico deben determinar la causa del error, intentar recuperar los datos perdidos y evitar que el error se repita. Resulta útil si las aplicaciones, el sistema operativo y otros servicios del sistema registran eventos importantes, como condiciones de memoria insuficiente o intentos excesivos de obtener acceso a un disco. A continuación, el administrador del sistema puede utilizar el registro de eventos para determinar qué condiciones produjeron el error e identificar el contexto en el que se produjo. Al ver periódicamente el registro de eventos, es posible que el administrador del sistema pueda identificar problemas (por ejemplo, un disco duro con errores) antes de que causen daños.

> [!Note]  
> La API de registro de eventos se diseñó para aplicaciones que se ejecutan en el sistema operativo Windows Server 2003, Windows XP o Windows 2000. En Windows Vista, se ha rediseñado la infraestructura de registro de eventos. Las aplicaciones diseñadas para ejecutarse en Windows Vista o sistemas operativos posteriores ahora deben usar el [registro de eventos de Windows](/windows/desktop/WES/windows-event-log) para registrar los eventos.

 
En esta sección se describe la interfaz de programación para escribir y consumir eventos mediante el registro de eventos.

-   [Tipos de evento](event-types.md)
-   [Instrucciones de registro](logging-guidelines.md)
-   [Elementos de registro de eventos](event-logging-elements.md)
-   [Operaciones de registro de eventos](event-logging-operations.md)
-   [Modelo de registro de eventos](event-logging-model.md)
-   [Seguridad del registro de eventos](event-logging-security.md)

> [!Note]  
> Las aplicaciones que publican eventos de más de 64 kilobytes en un equipo con Windows Server 2003, Windows XP o Windows 2000 no podrán publicar eventos en un equipo con Windows Vista o posterior.
