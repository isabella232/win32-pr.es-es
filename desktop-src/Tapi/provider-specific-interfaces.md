---
description: TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite que las aplicaciones aprovechen las funcionalidades específicas del proveedor.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Provider-Specific interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09290bf6d2ade55a9e9d2b0f51315acfc5488805b6c19b23679e00708ddaed45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060573"
---
# <a name="provider-specific-interfaces"></a>Provider-Specific interfaces

TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite que las aplicaciones aprovechen las funcionalidades específicas del proveedor. Además, TAPI 3 permite a los proveedores de servicios entregar eventos específicos del proveedor a las aplicaciones como objetos COM a través de la misma interfaz en la que la aplicación recibe eventos estándar.

TAPI logra esta integración agregando objetos específicos del proveedor con los objetos estándar (TAPI, Address, Terminal, Call y CallHub) y distribuyendo o delegando métodos desconocidos a estos objetos específicos del proveedor.

Por ejemplo, un proveedor de servicios puede permitir que las aplicaciones obtengan información sobre una llamada más allá de lo que expone la [**interfaz ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) El proveedor debe definir una interfaz que permita a las aplicaciones realizar estas consultas adicionales e implementar esa interfaz en un objeto . Este objeto también implementa una interfaz de consulta de información del proveedor para que una aplicación pueda detectar qué tipos de funciones específicas del proveedor podrían estar disponibles.

Cuando la aplicación obtiene una referencia a un objeto de llamada, la aplicación puede usar la nueva interfaz específica del proveedor y sus métodos como si lo hubiera implementado el propio objeto de llamada.

Vea Referencia de la interfaz del proveedor de servicios multimedia [(MSPI)](media-service-provider-interface-mspi-reference.md) para obtener una lista de todas las interfaces MSP estándar.

Consulte [IpConf MSP Interfaces (Interfaces msp de IPConf)](ipconf-msp-interfaces.md) para obtener una lista de todas las interfaces específicas del MSP de IPConf.

 

 



