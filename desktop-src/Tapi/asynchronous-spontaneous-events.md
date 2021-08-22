---
description: Hay otra clase de eventos asincrónicos además de los descritos anteriormente.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Eventos asincrónicos asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785ed97e6538b1baff9af13e64791a094d872e540fc088b74820119629d08b4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871911"
---
# <a name="asynchronous-spontaneous-events"></a>Eventos asincrónicos asincrónicos

Hay otra clase de eventos asincrónicos además de los descritos anteriormente. Estos eventos son "estundos" en el sentido de que no son resultados directos de las solicitudes correspondientes. Estos eventos se detectan en casos como cuando llega una llamada entrante o cuando una llamada saliente pasa de un estado de "timbre" a un estado de "respuesta". Cuando TAPI inicializa por primera vez interacciones con el TSPI para un dispositivo determinado, pasa un puntero a un procedimiento de devolución de llamada al que se va a llamar para notificar estos eventos escotentes. Junto con este puntero de procedimiento hay un identificador de dispositivo que el proveedor de servicios incluye como uno de los parámetros reales para la devolución de llamada.

 

 



