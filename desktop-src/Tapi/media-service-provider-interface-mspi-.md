---
description: La interfaz del proveedor de servicios multimedia (MSPI) es un conjunto de interfaces y métodos implementados por un MSP para permitir un control de la aplicación TAPI 3 sobre el transporte multimedia durante una sesión de comunicaciones.
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: Interfaz del proveedor de servicios multimedia (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1ce09e626ede14515c0abbbd5c3a35921026d6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678637"
---
# <a name="media-service-provider-interface-mspi"></a>Interfaz del proveedor de servicios multimedia (MSPI)

La interfaz del proveedor de servicios multimedia (MSPI) es un conjunto de interfaces y métodos implementados por un MSP para permitir un control de la aplicación TAPI 3 sobre el transporte multimedia durante una sesión de comunicaciones. Un MSP controla los mecanismos específicos del dispositivo y específicos del protocolo necesarios para activar estos controles y se comunica con su TSP emparejado o con una aplicación mediante el uso de los métodos proporcionados en MSPI.

En la sección siguiente (referencia de la [interfaz del proveedor de servicios multimedia (MSPI)) se](media-service-provider-interface-mspi-reference.md)detallan las interfaces que expone un MSP para interactuar con el entorno de telefonía de Microsoft.

Además, un MSP puede exponer interfaces y métodos privados específicos del proveedor para ayudar más en el control de medios. Por ejemplo, el [MSP de la Conferencia IP](ipconf-msp.md) expone interfaces que proporcionan control de participantes. Consulte [interfaces específicas del proveedor](provider-specific-interfaces.md) para obtener información sobre cómo funcionan los objetos privados y [IPCONF las interfaces MSP](ipconf-msp-interfaces.md) para obtener una lista de referencia de IPConf.

La mayoría del esfuerzo de programación en la creación de un MSP es muy específico para una plataforma, un dispositivo y un protocolo de transporte determinados, y está fuera del ámbito de este documento. Sin embargo, Microsoft proporciona un conjunto de clases base MSP, que serán útiles para la mayoría de los autores MSP. Consulte [las clases base de TAPI 3 MSP](tapi-3-msp-base-classes.md) para obtener información sobre el uso de estas clases.

La interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) representa un proveedor de servicios multimedia para la dll de TAPI. Esta interfaz no se usa ni se expone a una aplicación de usuario final. La DLL de TAPI 3 llama a **CoCreateInstance** en esta interfaz para crear el objeto MSP principal. Los métodos de este objeto permiten a una aplicación cargar y descargar el MSP, recibir información de un TSP y crear la interfaz [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) , que se expone en el objeto de llamada.

Las interfaces [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) y [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) proporcionan métodos paralelos con respecto a las subsecuencias. La compatibilidad con subsecuencias es opcional. El resto de interfaces debe implementarse mediante un MSP.

> [!Note]  
> Las operaciones implementadas por un par TSP/MSP deben estar ubicadas en una DLL para permitir que un usuario actualice el proveedor de servicios sin reiniciar su sistema.

 

 

 
