---
description: Los conjuntos de estaciones que se supervisan a través de un vínculo de terceros se modelan como un dispositivo de línea y, posiblemente, un dispositivo telefónico asociado.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688620"
---
# <a name="stations"></a>Cadenas

Los conjuntos de estaciones que se supervisan a través de un vínculo de terceros se modelan como un dispositivo de línea y, posiblemente, un dispositivo telefónico asociado. El dispositivo de línea puede tener varias direcciones, si el terminal modelado admite más de un número de directorio (DN). Varios aspectos de la llamada en el mismo DN se pueden modelar como una sola dirección que admite varias llamadas.

Las llamadas entre dos estaciones del conmutador tienen dos identificadores de llamada: uno que asigna la vista de llamada de la primera estación (en su dispositivo de línea) y el otro, que proporcionan la vista de llamada de la segunda estación (en su dispositivo de línea). Por ejemplo, una [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) de terceros colocada por una aplicación en el servidor se dirigirá al dispositivo de línea asociado a la estación desde la que se va a marcar la llamada; en esa línea se crearía un identificador de llamada, en la dirección especificada en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (con lo que se proporciona el control sobre qué DN se usa en un teléfono que admite varios DNS). Cuando se ofrece la llamada a la dirección de destino, se crea un nuevo identificador de llamada que muestra una llamada en el estado de la *oferta* . las aplicaciones sabrán que era otra vista de la misma llamada por el miembro **dwCallID** de [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) que es igual para ambas llamadas. Ambas llamadas pasarán a *estar inactivas* cuando se quitó la llamada; una llamada podría quitarse de la aplicación de terceros mediante una [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) en cualquiera de los identificadores de llamada.

 

 



