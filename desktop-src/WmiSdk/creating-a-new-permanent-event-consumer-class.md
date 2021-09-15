---
description: Uno de los primeros pasos para crear un consumidor de eventos permanente es crear la clase WMI que describe el consumidor de eventos. En concreto, la clase de consumidor de eventos permanente define los parámetros de la acción implementada por el consumidor físico.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Crear una nueva clase de consumidor de eventos permanente
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f8ae8e1e83abcf3b340398d45aefde4c7141e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569365"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>Crear una nueva clase de consumidor de eventos permanente

Uno de los primeros pasos para crear un consumidor de eventos permanente es crear la clase WMI que describe el consumidor de eventos. En concreto, la clase de consumidor de eventos permanente define los parámetros de la acción implementada por el consumidor físico.

En el procedimiento siguiente se describe cómo crear una clase de consumidor de eventos permanente.

**Para crear una clase de consumidor de eventos permanente**

1.  Derive una clase de la clase del sistema [**\_ \_ EventConsumer.**](--eventconsumer.md)
2.  Implemente los parámetros necesarios para procesar una notificación de eventos.

En el ejemplo siguiente se muestra la sintaxis utilizada para crear la clase SMTPConsumerEvent. Puede usarlo como ejemplo para crear la nueva clase. La [**clase SMTPEventConsumer**](smtpeventconsumer.md) envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento. Esta clase se define en smtpcons.mof.

``` syntax
class SMTPEventConsumer : __EventConsumer
{
  [key] string Name;
  [not_null] string SMTPServer;
  [Template] string Subject;
  [Template] string FromLine;
  [Template] string ReplyToLine;
  [Template] string Message;
  [Template] string ToLine;
  [Template] string CcLine;
  [Template] string BccLine;
  string HeaderFields[];
};
```

Debe poder crear instancias de la clase de consumidor de eventos permanente para describir una o varias maneras de enviar eventos al consumidor físico. Para obtener más información, vea [Crear un consumidor lógico.](creating-a-logical-consumer.md)

 

 



