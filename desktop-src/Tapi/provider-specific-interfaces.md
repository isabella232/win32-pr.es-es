---
description: TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite a las aplicaciones aprovechar las ventajas de la funcionalidad específica del proveedor.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Provider-Specific interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160617"
---
# <a name="provider-specific-interfaces"></a>Provider-Specific interfaces

TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite a las aplicaciones aprovechar las ventajas de la funcionalidad específica del proveedor. Además, TAPI 3 permite a los proveedores de servicios entregar eventos específicos del proveedor a las aplicaciones como objetos COM a través de la misma interfaz en la que la aplicación recibe eventos estándar.

TAPI logra esta integración agregando objetos específicos del proveedor con los objetos estándar (TAPI, Address, Terminal, Call y CallHub) y distribuyendo o delegando métodos desconocidos en estos objetos específicos del proveedor.

Por ejemplo, un proveedor de servicios puede permitir que las aplicaciones obtengan información sobre una llamada más allá de lo que expone la [**interfaz ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) El proveedor debe definir una interfaz que permita a las aplicaciones realizar estas consultas adicionales e implementar esa interfaz en un objeto . Este objeto también implementa una interfaz de consulta de información del proveedor para que una aplicación pueda detectar qué tipos de funciones específicas del proveedor podrían estar disponibles.

Cuando la aplicación obtiene una referencia a un objeto de llamada, la aplicación puede usar la nueva interfaz específica del proveedor y sus métodos como si fueran implementados por el propio objeto de llamada.

Consulte Referencia de la interfaz del proveedor de servicios multimedia [(MSPI)](media-service-provider-interface-mspi-reference.md) para obtener una lista de todas las interfaces MSP estándar.

Consulte [IpConf MSP Interfaces (Interfaces MSP de IPConf)](ipconf-msp-interfaces.md) para obtener una lista de todas las interfaces específicas del MSP de IPConf.

 

 



