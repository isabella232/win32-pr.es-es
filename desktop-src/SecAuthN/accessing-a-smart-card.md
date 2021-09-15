---
description: Explica los medios por los que una aplicación o proveedor de servicios puede conectarse a una tarjeta inteligente mediante el subsistema de tarjeta inteligente.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Acceso a una tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473485"
---
# <a name="accessing-a-smart-card"></a>Acceso a una tarjeta inteligente

El [*subsistema de tarjetas*](/windows/desktop/SecGloss/s-gly) inteligentes proporciona varios medios para que una aplicación o proveedor [*de servicios*](/windows/desktop/SecGloss/c-gly) se conecte a una tarjeta inteligente:

-   Una aplicación puede llamar a [**SCardConnect para**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) conectarse a una tarjeta que reside en un lector determinado. Esta es la manera más sencilla de establecer la comunicación con una tarjeta inteligente.
-   Una aplicación puede buscar una tarjeta inteligente específica dentro de un grupo de lectores determinado. La aplicación identifica la tarjeta por su nombre para mostrar y especifica una lista de lectores en la que puede aparecer la tarjeta. El [*administrador de recursos*](/windows/desktop/SecGloss/r-gly) busca en la lista de lectores las tarjetas con una cadena [*ATR*](/windows/desktop/SecGloss/a-gly) que coincida con la tarjeta con nombre y devuelve información de estado a la aplicación. El [*subsistema de tarjeta*](/windows/desktop/SecGloss/s-gly) inteligente nunca coloca una GUI ni interactúa con la tarjeta más allá de obtener la cadena ATR. Sin embargo, proporciona información suficiente para que la aplicación o un control común puedan ayudar al usuario a buscar el tipo de tarjeta o tarjeta deseado. Esto da como resultado la asignación de la solicitud a un lector específico, al que se dirige más E/S.
-   Una aplicación puede solicitar una lista de tarjetas que admitan un conjunto determinado de interfaces de tarjeta inteligente. A continuación, la aplicación puede usar la lista en el caso anterior. Esto permite a las aplicaciones conectarse a tarjetas en función de sus funcionalidades, sin tener en cuenta sus nombres.

Cuando una aplicación busca una tarjeta, proporciona una matriz de nombres de lector en los que buscar. Para cada elemento de lector de la matriz, el administrador de recursos proporciona la siguiente información:

-   Si el lector está disponible para su uso por esta aplicación.
-   Si hay una tarjeta insertada en este lector y, si es así, cuál es su cadena ATR.
-   Si la cadena ATR de la tarjeta coincide con cualquiera de las cadenas ATR de las tarjetas solicitadas.

La aplicación usa la información devuelta para aplicar filtros adicionales a las tarjetas o para pedir al usuario que seleccione la tarjeta deseada. Tenga en cuenta que es posible que otras aplicaciones abran uno o varios de los lectores devueltos para su uso exclusivo, por lo que no se garantiza el acceso a esta lista de lectores.

 

 
