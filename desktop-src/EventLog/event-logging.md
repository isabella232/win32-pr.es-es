---
description: Muchas aplicaciones registran errores y eventos en registros de errores patentados, cada uno con su propio formato e interfaz de usuario.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Registro de eventos (registro de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688296"
---
# <a name="event-logging-event-logging"></a>Registro de eventos (registro de eventos)

Muchas aplicaciones registran errores y eventos en registros de errores patentados, cada uno con su propio formato e interfaz de usuario. Los datos de aplicaciones diferentes no se pueden combinar fácilmente en un informe completo, lo que requiere que los administradores del sistema o los representantes de soporte técnico comprueben diversos orígenes para diagnosticar problemas.

El registro de eventos proporciona una manera centralizada y estándar para que las aplicaciones (y el sistema operativo) registren eventos importantes de software y hardware. El servicio registro de eventos registra eventos de varios orígenes y los almacena en una sola colección denominada *registro de eventos*. El Visor de eventos permite ver registros; la interfaz de programación también permite examinar los registros.

-   [Acerca del registro de eventos](about-event-logging.md)
-   [Uso del registro de eventos](using-event-logging.md)
-   [Referencia del registro de eventos](event-logging-reference.md)

> [!Note]  
> La API de registro de eventos se diseñó para aplicaciones que se ejecutan en el sistema operativo Windows Server 2003, Windows XP o Windows 2000. En Windows Vista, se ha rediseñado la infraestructura de registro de eventos. Las aplicaciones diseñadas para ejecutarse en Windows Vista o sistemas operativos posteriores deben usar el [registro de eventos de Windows](/windows/desktop/WES/windows-event-log) para registrar los eventos.
