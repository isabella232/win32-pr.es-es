---
description: Muchas aplicaciones registran errores y eventos en registros de errores propietarios, cada una con su propio formato e interfaz de usuario.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Registro de eventos (registro de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8894c7a6d038efdc317611ca6284f62d99c82ebc767b6f96f83931803a887185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927845"
---
# <a name="event-logging-event-logging"></a>Registro de eventos (registro de eventos)

Muchas aplicaciones registran errores y eventos en registros de errores propietarios, cada una con su propio formato e interfaz de usuario. Los datos de diferentes aplicaciones no se pueden combinar fácilmente en un informe completo, lo que requiere que los administradores del sistema o los representantes de soporte técnico comprueben diversos orígenes para diagnosticar problemas.

El registro de eventos proporciona una manera estándar y centralizada para que las aplicaciones (y el sistema operativo) registren eventos importantes de software y hardware. El servicio de registro de eventos registra eventos de varios orígenes y los almacena en una sola colección denominada registro *de eventos*. El Visor de eventos permite ver los registros; la interfaz de programación también le permite examinar los registros.

-   [Acerca del registro de eventos](about-event-logging.md)
-   [Uso del registro de eventos](using-event-logging.md)
-   [Referencia del registro de eventos](event-logging-reference.md)

> [!Note]  
> Event Logging API se diseñó para aplicaciones que se ejecutan en el sistema operativo Windows Server 2003, Windows XP o Windows 2000. En Windows Vista, se ha rediseñado la infraestructura de registro de eventos. Las aplicaciones diseñadas para ejecutarse en Windows Vista o sistemas operativos posteriores deben usar Windows [de eventos](/windows/desktop/WES/windows-event-log) para registrar eventos.
