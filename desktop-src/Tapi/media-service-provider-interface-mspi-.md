---
description: La interfaz del proveedor de servicios multimedia (MSPI) es un conjunto de interfaces y métodos implementados por un MSP para permitir un control de aplicaciones TAPI 3 sobre el transporte multimedia durante una sesión de comunicaciones.
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: Interfaz del proveedor de servicios multimedia (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b99f78d62c0784e38ede7a4019eef40cf8a48cf9480a4326c5d7b7129ca971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073015"
---
# <a name="media-service-provider-interface-mspi"></a>Interfaz del proveedor de servicios multimedia (MSPI)

La interfaz del proveedor de servicios multimedia (MSPI) es un conjunto de interfaces y métodos implementados por un MSP para permitir un control de aplicaciones TAPI 3 sobre el transporte multimedia durante una sesión de comunicaciones. Un MSP controla los mecanismos específicos del dispositivo y específicos del protocolo necesarios para aplicar estos controles, y se comunica con su TSP emparejado o una aplicación mediante el uso de los métodos proporcionados en MSPI.

En la sección siguiente (Referencia de la interfaz del proveedor de servicios multimedia [(MSPI) )](media-service-provider-interface-mspi-reference.md)se detallan las interfaces que expone un MSP para interactuar con el entorno de telefonía de Microsoft.

Además, un MSP puede exponer métodos y interfaces privadas específicos del proveedor para ayudar aún más en el control multimedia. Por ejemplo, el [MSP de la conferencia IP](ipconf-msp.md) expone interfaces que proporcionan el control del participante. Consulte [Interfaces específicas del proveedor para](provider-specific-interfaces.md) obtener información sobre cómo funcionan los objetos privados e Interfaces MSP de [IPConf](ipconf-msp-interfaces.md) para obtener una lista de referencia de IPConf.

La mayor parte del esfuerzo de programación para crear un MSP es muy específico de una plataforma, un dispositivo y un protocolo de transporte determinados, y está fuera del ámbito de este documento. Sin embargo, Microsoft proporciona un conjunto de clases base msp, que serán útiles para la mayoría de los autores de MSP. Consulte [Clases base de MSP de TAPI 3](tapi-3-msp-base-classes.md) para obtener información sobre el uso de estas clases.

La [**interfaz ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) representa un proveedor de servicios multimedia para el archivo DLL de TAPI. Esta interfaz no la usa ni se expone a una aplicación de usuario final. El archivo DLL de TAPI 3 llama **a CoCreateInstance** en esta interfaz para crear el objeto MSP principal. Los métodos de este objeto permiten a una aplicación cargar y descargar el MSP, recibir información de un TSP y crear la interfaz [**ITStreamControl,**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) que se expone en el objeto de llamada.

Las [**interfaces ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) e [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) proporcionan métodos paralelos con respecto a las substreams. La compatibilidad con substream es opcional. Todas las demás interfaces deben implementarse mediante un MSP.

> [!Note]  
> Las operaciones implementadas por un par TSP/MSP deben encontrarse en un archivo DLL para permitir que un usuario actualice el proveedor de servicios sin reiniciar su sistema.

 

 

 
