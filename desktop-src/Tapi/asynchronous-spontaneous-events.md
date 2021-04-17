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
# <a name="asynchronous-spontaneous-events"></a>Eventos espontáneos asincrónicos

Hay otra clase de eventos asincrónicos además de los descritos anteriormente. Estos eventos son "espontáneos" en el sentido de que no son resultados directos de las solicitudes correspondientes. Estos eventos se detectan en casos como cuando llega una llamada entrante o cuando una llamada saliente pasa de un "anillo" a un estado de "respuesta". Cuando TAPI inicializa por primera vez las interacciones con el TSPI de un dispositivo determinado, pasa un puntero a un procedimiento de devolución de llamada al que se va a llamar para notificar eventos espontáneos. Junto con este puntero de procedimiento es un identificador de dispositivo que el proveedor de servicios incluye como uno de los parámetros reales para la devolución de llamada.

 

 



