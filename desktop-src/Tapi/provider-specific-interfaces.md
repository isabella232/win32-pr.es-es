---
description: TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite que las aplicaciones aprovechen la funcionalidad específica del proveedor.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfaces de Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083178"
---
# <a name="provider-specific-interfaces"></a>Interfaces de Provider-Specific

TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite que las aplicaciones aprovechen la funcionalidad específica del proveedor. Además, TAPI 3 permite que los proveedores de servicios entreguen eventos específicos del proveedor a las aplicaciones como objetos COM en la misma interfaz en la que la aplicación recibe eventos estándar.

TAPI consigue esta integración mediante la agregación de objetos específicos del proveedor con los objetos estándar (TAPI, dirección, terminal, llamada y CallHub) y la distribución o delegación de métodos desconocidos para estos objetos específicos del proveedor.

Por ejemplo, un proveedor de servicios puede permitir que las aplicaciones obtengan información sobre una llamada más allá de lo que expone la interfaz [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) . El proveedor debe definir una interfaz que permita a las aplicaciones realizar estas consultas adicionales e implementar esa interfaz en un objeto. Este objeto también implementa una interfaz de consulta de información de proveedor para que una aplicación pueda detectar qué tipos de funciones específicas del proveedor pueden estar disponibles.

Cuando la aplicación obtiene una referencia a un objeto de llamada, la aplicación puede usar la nueva interfaz específica del proveedor y sus métodos como si se hubieran implementado mediante el propio objeto de llamada.

Consulte [referencia de la interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-reference.md) para obtener una lista de todas las interfaces MSP estándar.

Consulte [interfaces de IPCONF MSP](ipconf-msp-interfaces.md) para obtener una lista de todas las interfaces específicas de IPConf MSP.

 

 



