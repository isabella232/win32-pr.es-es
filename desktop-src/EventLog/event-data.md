---
description: Cada evento puede tener asociados datos específicos del evento.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Datos del evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf6809b837d36f4cf2ddc0d74b90fe3a925f5eae7efc96973a9bf845c610bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901485"
---
# <a name="event-data"></a>Datos del evento

Cada evento puede tener asociados datos específicos del evento. El Visor de eventos no interpreta estos datos; muestra datos adicionales solo en un formato hexadecimal y de texto combinado. El límite máximo en el tamaño de un evento en el registro par es 0x3FFFF bytes. Por lo tanto, use datos específicos del evento con moderación, incluyéndolo solo si está seguro de que será útil para alguien que depura un problema. Por ejemplo, muchos eventos relacionados con la red incluyen bloques de control de red (NCB) como datos específicos del evento.

Cuando se usan datos específicos del evento, la última parte de su cadena de descripción debe proporcionar una nota sobre la información proporcionada como datos específicos del evento. Por ejemplo, el software de red podría proporcionar una nota como: "(El NCB son los datos del evento).". Como convención, use paréntesis alrededor de dichos comentarios, como se indica en este ejemplo.

También puede usar datos específicos del evento para almacenar información que la aplicación puede procesar independientemente de la Visor de eventos. Por ejemplo, podría escribir un visor específicamente para los eventos o escribir un programa que examina el registro y crea un informe que incluye información de los datos específicos del evento.

 

 



