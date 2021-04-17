---
description: Cada evento puede tener asociados datos específicos del evento.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Datos del evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666704"
---
# <a name="event-data"></a>Datos del evento

Cada evento puede tener asociados datos específicos del evento. El Visor de eventos no interpreta estos datos; solo muestra datos adicionales en formato hexadecimal y de texto combinados. El límite máximo del tamaño de un evento en el registro par es 0x3FFFF bytes. Por lo tanto, use los datos específicos del evento con moderación, incluido solo si está seguro de que será útil para alguien que depure un problema. Por ejemplo, muchos eventos relacionados con la red incluyen bloques de control de red (NCB) como datos específicos del evento.

Cuando se usan datos específicos del evento, la última parte de la cadena de descripción debe proporcionar una nota sobre la información proporcionada como datos específicos del evento. Por ejemplo, el software de red podría proporcionar una nota como: "(el NCB es los datos de evento)". Como Convención, use paréntesis alrededor de estos comentarios, como se indica en este ejemplo.

También puede utilizar datos específicos del evento para almacenar información que la aplicación puede procesar independientemente del Visor de eventos. Por ejemplo, puede escribir un visor específicamente para los eventos o escribir un programa que examine el registro y cree un informe que incluya información de los datos específicos del evento.

 

 



