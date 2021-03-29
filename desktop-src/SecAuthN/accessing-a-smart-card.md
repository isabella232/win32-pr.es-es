---
description: Explica los medios por los que una aplicación o un proveedor de servicios se puede conectar a una tarjeta inteligente mediante el subsistema de tarjeta inteligente.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Acceso a una tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652731"
---
# <a name="accessing-a-smart-card"></a>Acceso a una tarjeta inteligente

El subsistema de [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) proporciona varios medios para que una aplicación o un [*proveedor de servicios*](/windows/desktop/SecGloss/c-gly) se conecten a una tarjeta inteligente:

-   Una aplicación puede llamar a [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) para conectarse a una tarjeta que resida en un lector determinado. Esta es la manera más sencilla de establecer comunicación con una tarjeta inteligente.
-   Una aplicación puede buscar una tarjeta inteligente específica dentro de un grupo de lectores determinado. La aplicación identifica la tarjeta por su nombre para mostrar y especifica una lista de los lectores en los que puede aparecer la tarjeta. El [*Administrador de recursos*](/windows/desktop/SecGloss/r-gly) busca en la lista de lectores cualquier tarjeta con una [*cadena ATR*](/windows/desktop/SecGloss/a-gly) que coincida con la tarjeta con nombre y devuelve información de estado a la aplicación. El [*subsistema de tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) nunca coloca una GUI o interactúa con la tarjeta más allá de obtener la cadena ATR. Sin embargo, proporciona información suficiente para que la aplicación o un control común puedan guiar al usuario a través de la búsqueda del tipo de tarjeta o tarjeta deseado. Esto da como resultado la asignación de la solicitud a un lector concreto, al que se dirige más e/s.
-   Una aplicación puede solicitar una lista de tarjetas que admitan un conjunto determinado de interfaces de tarjeta inteligente. A continuación, la aplicación puede usar la lista en el caso anterior. Esto permite que las aplicaciones se conecten a las tarjetas según sus capacidades, sin tener en cuenta sus nombres.

Cuando una aplicación busca una tarjeta, proporciona una matriz de nombres de lector en la que se va a buscar. Para cada elemento de lector de la matriz, Resource Manager proporciona la información siguiente:

-   Si el lector está disponible para que lo use esta aplicación.
-   Si hay una tarjeta insertada en este lector y, en caso afirmativo, cuál es su cadena ATR.
-   Indica si la cadena ATR de la tarjeta coincide con cualquiera de las cadenas ATR de las tarjetas solicitadas.

La aplicación usa la información devuelta para aplicar más filtros a las tarjetas o para pedir al usuario que seleccione la tarjeta deseada. Tenga en cuenta que una o varias de las listas de lectores devueltas se pueden abrir para su uso exclusivo por parte de otras aplicaciones, por lo que no se garantiza el acceso a esta lista de lectores.

 

 
