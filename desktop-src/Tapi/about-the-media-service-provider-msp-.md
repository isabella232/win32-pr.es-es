---
description: Un proveedor de servicios multimedia (MSP) TAPI 3 permite a una aplicación un control considerable sobre los medios para un mecanismo de transporte determinado.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Acerca del proveedor de Media Service (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f6113fa6c5fcceddaf379894d5680cbdccccec5be228041967dabb11fcc2caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872928"
---
# <a name="about-the-media-service-provider-msp"></a>Acerca del proveedor de Media Service (MSP)

Un proveedor de servicios multimedia (MSP) TAPI 3 permite a una aplicación un control considerable sobre los medios para un mecanismo de transporte determinado. Un MSP siempre existe emparejado con un proveedor de servicios de telefonía (TSP). Al igual que un TSP es una capa de abstracción para el control de llamadas, el MSP controla los medios sin necesidad de codificación específica del dispositivo. Para obtener un ejemplo de comunicación MSP/TSP, vea [Información general del proveedor de servicios TAPI.](./tapi-service-provider-overview.md)

Un MSP habilita el control multimedia mediante el uso de interfaces especiales de terminal, secuencia y substream definidas por TAPI. En el diagrama [de Acerca de los controles de](about-call-and-media-controls.md) llamada y multimedia se muestra cómo aparecen estas interfaces en una aplicación TAPI 3.

Además, un MSP puede implementar interfaces específicas del proveedor privado, que TAPI agregará a los objetos estándar [expuestos](provider-specific-interfaces.md)a una aplicación. Por ejemplo, el MSP de IPConf de Microsoft, que se instala con Microsoft Windows 2000, implementa la interfaz [**ITParticipant,**](itparticipant.md) que proporciona controles para miembros individuales de una conferencia.

En el tema siguiente se describen brevemente los MSP que se pueden instalar con un sistema operativo de Microsoft. Para más información sobre la configuración y el uso, consulte el kit de recursos de la plataforma de destino.

Se pueden escribir proveedores de servicios multimedia de terceros adicionales para protocolos concretos o para dispositivos físicos. La interfaz del proveedor de servicios multimedia [(MSPI)](media-service-provider-interface-mspi-.md) describe las interfaces que se deben implementar para permitir que un MSP interactúe con los componentes de Telefonía de Microsoft.

 

 
