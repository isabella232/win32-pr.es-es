---
description: Un proveedor de servicios multimedia (MSP) de TAPI 3 permite un control considerable de las aplicaciones sobre los medios de un mecanismo de transporte determinado.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Acerca del proveedor de servicios multimedia (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157000"
---
# <a name="about-the-media-service-provider-msp"></a>Acerca del proveedor de servicios multimedia (MSP)

Un proveedor de servicios multimedia (MSP) de TAPI 3 permite un control considerable de las aplicaciones sobre los medios de un mecanismo de transporte determinado. Un MSP siempre existe emparejado con un proveedor de servicios de telefonía (TSP). Del mismo modo que un TSP es una capa de abstracción para el control de llamadas, MSP controla los medios sin necesidad de codificación específica del dispositivo. Para obtener un ejemplo de comunicación de MSP/TSP, consulte [información general del proveedor de servicios TAPI](./tapi-service-provider-overview.md).

Un MSP permite el control de medios mediante el uso de interfaces de terminal, secuencia y subflujo especiales definidas por TAPI. En el diagrama de [acerca de los controles de llamada y multimedia](about-call-and-media-controls.md) se muestra cómo estas interfaces aparecen en una aplicación TAPI 3.

Además, un MSP puede implementar interfaces privadas [específicas del proveedor](provider-specific-interfaces.md), que TAPI agregará a los objetos estándar expuestos a una aplicación. Por ejemplo, Microsoft IPConf MSP, que se instala con Microsoft Windows 2000, implementa la interfaz [**ITParticipant**](itparticipant.md) , que proporciona controles para miembros individuales de una conferencia.

En el siguiente tema se describen brevemente los MSP que se pueden instalar con un sistema operativo de Microsoft. Para más información sobre la configuración y el uso, consulte el kit de recursos de la plataforma de destino.

Se pueden escribir otros proveedores de servicios multimedia de terceros para determinados protocolos o para dispositivos físicos. La [interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-.md) describe las interfaces que se deben implementar para permitir que un MSP interactúe con los componentes de telefonía de Microsoft.

 

 
