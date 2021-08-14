---
description: Los conjuntos de estaciones que se supervisan a través de un vínculo de terceros se modela como un dispositivo de línea y, posiblemente, un dispositivo de teléfono asociado.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Estaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad9874542a63f05e124ea5df833aa0a433c03713cc3a2d7bb1ca3a471174e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760727"
---
# <a name="stations"></a>Estaciones

Los conjuntos de estaciones que se supervisan a través de un vínculo de terceros se modela como un dispositivo de línea y, posiblemente, un dispositivo de teléfono asociado. El dispositivo de línea puede tener varias direcciones si el terminal modelado admite más de un número de directorio (DN). Varias apariciones de llamadas en el mismo DN se pueden modelar como una sola dirección que admite varias llamadas.

Las llamadas entre dos estaciones del conmutador tienen dos identificadores de llamada, uno que da la vista de llamada desde la primera estación (en su dispositivo de línea) y el otro que da la vista de llamada desde la segunda estación (en su dispositivo de línea). Por ejemplo, una línea de [**tercerosMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) colocada por una aplicación en el servidor se dirigiría al dispositivo de línea asociado a la estación desde la que se va a marcar la llamada; Se crearía un identificador de llamada en esa línea, en la dirección especificada en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (lo que da control sobre qué DN se usa en un teléfono que admite varios DN). Cuando se ofrece la llamada a la dirección de destino, se crea un nuevo identificador de llamada que muestra una llamada *en* estado de oferta; Las aplicaciones sabrán que se trata de otra vista de la misma llamada por parte del **miembro dwCallID** en [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) siendo igual para ambas llamadas. Ambas llamadas se *inactivan cuando* se ha descartado la llamada. Se podría descartar una llamada de la aplicación de terceros realizando [**una lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) en cualquiera de los identificadores de llamada.

 

 



