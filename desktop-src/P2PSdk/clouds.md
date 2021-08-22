---
description: Las nubes las usan las infraestructuras de agrupación y grafos del mismo nivel.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Nubes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5ecbeee1f5b69d120c5f351f8a5bb200b6e3e5f60e4bacca5a4f5484f402dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932697"
---
# <a name="clouds"></a>Nubes

Las nubes las usan las infraestructuras [de agrupación y](grouping-api.md) [grafos del](graphing-api.md) mismo nivel. El Protocolo de resolución de nombres del mismo nivel [(PNRP)](pnrp-namespace-provider-api.md) identifica una nube como un conjunto de pares que se pueden comunicar dentro del mismo ámbito IPv6. Las nubes están estrechamente relacionadas con los ámbitos IPv6. En la lista siguiente se identifican algunas de las características únicas de la nube:

-   Una nube se identifica mediante un nombre y las nubes disponibles se pueden enumerar mediante [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).
-   Si un equipo está conectado a Internet, forma parte de una nube global, que se identifica mediante la cadena \_ "Global".
-   Si un equipo está conectado a una o varias redes de área local (LAN), hay nubes individuales disponibles para cada vínculo.
-   Un equipo se puede conectar a muchas redes si tiene varios adaptadores de red o mediante una red privada virtual (VPN), lo que significa que un equipo con una interfaz puede ser visible en muchas nubes.
-   Puede usar PNRP para registrar y resolver nombres del mismo nivel en una nube específica.

 

 



