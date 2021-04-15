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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715838"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a><span data-ttu-id="d7d97-104">Crear una nueva clase de consumidor de eventos permanente</span><span class="sxs-lookup"><span data-stu-id="d7d97-104">Creating a New Permanent Event Consumer Class</span></span>

<span data-ttu-id="d7d97-105">Uno de los primeros pasos para crear un consumidor de eventos permanente es crear la clase WMI que describe el consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7d97-105">One of the first steps in creating a permanent event consumer is to create the WMI class that describes the event consumer.</span></span> <span data-ttu-id="d7d97-106">En concreto, la clase de consumidor de eventos permanente define los parámetros de la acción implementada por el consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="d7d97-106">Specifically, the permanent event consumer class defines the parameters of the action implemented by the physical consumer.</span></span>

<span data-ttu-id="d7d97-107">En el procedimiento siguiente se describe cómo crear una clase de consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="d7d97-107">The following procedure describes how to create a permanent event consumer class.</span></span>

<span data-ttu-id="d7d97-108">**Para crear una clase de consumidor de eventos permanente**</span><span class="sxs-lookup"><span data-stu-id="d7d97-108">**To create a permanent event consumer class**</span></span>

1.  <span data-ttu-id="d7d97-109">Derive una clase de la clase del sistema [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d97-109">Derive a class from the [**\_\_EventConsumer**](--eventconsumer.md) system class.</span></span>
2.  <span data-ttu-id="d7d97-110">Implemente los parámetros necesarios para procesar una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7d97-110">Implement any parameters necessary to process an event notification.</span></span>

<span data-ttu-id="d7d97-111">En el ejemplo siguiente se muestra la sintaxis utilizada para crear la clase SMTPConsumerEvent.</span><span class="sxs-lookup"><span data-stu-id="d7d97-111">The following example shows the syntax used to create the SMTPConsumerEvent class.</span></span> <span data-ttu-id="d7d97-112">Puede utilizarlo como ejemplo para crear la nueva clase.</span><span class="sxs-lookup"><span data-stu-id="d7d97-112">You can use this as an example for creating your new class.</span></span> <span data-ttu-id="d7d97-113">La clase [**SMTPEventConsumer**](smtpeventconsumer.md) envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="d7d97-113">The [**SMTPEventConsumer**](smtpeventconsumer.md) class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="d7d97-114">Esta clase se define en smtpcons. mof.</span><span class="sxs-lookup"><span data-stu-id="d7d97-114">This class is defined in smtpcons.mof.</span></span>

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

<span data-ttu-id="d7d97-115">Debe poder crear instancias de la clase de consumidor de eventos permanente para describir una o varias formas de enviar eventos al consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="d7d97-115">You should be able to create instances of your permanent event consumer class to describe one or more ways to send events to your physical consumer.</span></span> <span data-ttu-id="d7d97-116">Para obtener más información, vea [crear un consumidor lógico](creating-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="d7d97-116">For more information, see [Creating a Logical Consumer](creating-a-logical-consumer.md).</span></span>

 

 



