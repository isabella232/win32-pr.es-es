---
description: Hay otra clase de eventos asincrónicos además de los descritos anteriormente.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Eventos espontáneos asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687896"
---
# <a name="asynchronous-spontaneous-events"></a><span data-ttu-id="35677-103">Eventos espontáneos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="35677-103">Asynchronous Spontaneous Events</span></span>

<span data-ttu-id="35677-104">Hay otra clase de eventos asincrónicos además de los descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="35677-104">There is another class of asynchronous events besides those described above.</span></span> <span data-ttu-id="35677-105">Estos eventos son "espontáneos" en el sentido de que no son resultados directos de las solicitudes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="35677-105">These events are "spontaneous" in the sense that they are not direct results of corresponding requests.</span></span> <span data-ttu-id="35677-106">Estos eventos se detectan en casos como cuando llega una llamada entrante o cuando una llamada saliente pasa de un "anillo" a un estado de "respuesta".</span><span class="sxs-lookup"><span data-stu-id="35677-106">These events are detected in such cases as when an incoming call arrives, or when an outbound call goes from a "ringing" to an "answering" state.</span></span> <span data-ttu-id="35677-107">Cuando TAPI inicializa por primera vez las interacciones con el TSPI de un dispositivo determinado, pasa un puntero a un procedimiento de devolución de llamada al que se va a llamar para notificar eventos espontáneos.</span><span class="sxs-lookup"><span data-stu-id="35677-107">When TAPI first initializes interactions with the TSPI for a particular device, it passes a pointer to a callback procedure to be called for reporting such spontaneous events.</span></span> <span data-ttu-id="35677-108">Junto con este puntero de procedimiento es un identificador de dispositivo que el proveedor de servicios incluye como uno de los parámetros reales para la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="35677-108">Along with this procedure pointer is a device handle that the service provider includes as one of the actual parameters to the callback.</span></span>

 

 



