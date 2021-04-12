---
description: Las nubes se usan en las infraestructuras de agrupación y gráficos del mismo nivel.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Nubes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156541"
---
# <a name="clouds"></a>Nubes

Las nubes se usan en las infraestructuras de [agrupación](grouping-api.md) y [gráficos](graphing-api.md) del mismo nivel. El [Protocolo de resolución de nombres de mismo nivel (PNRP)](pnrp-namespace-provider-api.md) identifica una nube como un conjunto de elementos del mismo nivel que pueden comunicarse en el mismo ámbito de IPv6. Las nubes están estrechamente relacionadas con los ámbitos IPv6. En la siguiente lista se identifican algunas de las características únicas de la nube:

-   Una nube se identifica mediante un nombre y las nubes disponibles se pueden enumerar mediante [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).
-   Si un equipo está conectado a Internet, forma parte de una nube global, que se identifica mediante la cadena "global \_ ".
-   Si un equipo está conectado a una o más redes de área local (LAN), las nubes individuales estarán disponibles para cada vínculo.
-   Un equipo puede estar conectado a muchas redes con varios adaptadores de red o mediante una red privada virtual (VPN), lo que significa que un equipo con una interfaz puede estar visible en muchas nubes.
-   Puede usar PNRP para registrar y resolver nombres de mismo nivel en una nube específica.

 

 



