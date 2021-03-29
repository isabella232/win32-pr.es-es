---
description: Una interfaz de tarjeta inteligente consta de un conjunto predefinido de servicios disponibles dentro de una tarjeta inteligente, los protocolos necesarios para invocar los servicios y cualquier suposición relativa al contexto de los servicios.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfaces de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816211"
---
# <a name="smart-card-interfaces"></a>Interfaces de tarjeta inteligente

Una interfaz de [*tarjeta inteligente*](../secgloss/s-gly.md) consta de un conjunto predefinido de servicios disponibles dentro de una *tarjeta inteligente*, los protocolos necesarios para invocar los servicios y cualquier suposición relativa al contexto de los servicios.

Con respecto a las tarjetas inteligentes, el término "interfaz" es similar al modo en que se usa en COM, que a su vez es similar en concepto al identificador de la aplicación ISO 7816/5, pero con un ámbito diferente.

Cada interfaz de tarjeta inteligente se identifica mediante un GUID. Por ejemplo, se puede definir una interfaz que proporcione información de Bioritmo a su titular. Si una tarjeta inteligente determinada es compatible con este servicio, puede que sea compatible con el GUID de la interfaz. Mediante el uso de los GUID de interfaz, una aplicación puede buscar un conjunto determinado de interfaces, localizando cualquier tarjeta que admita ese conjunto, para completar una tarea.

Aunque una interfaz tiene un GUID, podría implementarse de forma diferente en distintas tarjetas. Por ejemplo, la interfaz de Bioritmo mencionada anteriormente puede tener varias implementaciones diferentes, pero se hace referencia a todos con el mismo GUID. Las distintas implementaciones no cambiarían la interacción entre la aplicación y la tarjeta inteligente. sin embargo, la interacción entre el [*proveedor de servicios*](../secgloss/c-gly.md) y las tarjetas inteligentes puede diferir dependiendo de la implementación de la interfaz.

El conjunto de interfaces que admite una tarjeta inteligente se define durante la introducción de tarjetas inteligentes (consulte [Introducción a las tarjetas inteligentes en el sistema](introducing-smart-cards-to-the-system.md)).

 

 
