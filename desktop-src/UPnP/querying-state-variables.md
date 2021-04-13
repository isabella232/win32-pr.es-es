---
title: Consultar variables de estado
description: La interfaz IUPnPService proporciona el método QueryStateVariable, que devuelve el valor de una variable de estado especificada.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357001"
---
# <a name="querying-state-variables"></a>Consultar variables de estado

La interfaz [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) proporciona el método [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , que devuelve el valor de una variable de estado especificada.

El foro de UPnP desaconseja el uso de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable). Se recomienda que los escritores de dispositivos escriban las acciones adecuadas para proporcionar esta información. Los escritores de dispositivos no tienen ninguna obligación de implementar **QueryStateVariable**.

Vea la sección [invocación de acciones](invoking-actions.md).

 

 




