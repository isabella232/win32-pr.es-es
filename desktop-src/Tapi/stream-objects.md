---
description: Los objetos de secuencia son una abstracción de la secuencia de medios o las secuencias asociadas a una sesión de llamada.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objetos de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687803"
---
# <a name="stream-objects"></a>Objetos de secuencia

Los objetos de secuencia son una abstracción de la secuencia de medios o las secuencias asociadas a una sesión de llamada. Las interfaces y los métodos expuestos en los objetos Stream y substream permiten a una aplicación ejercitar controles muy detallados, como pausar una secuencia, agregar nuevos tipos de medios a una sesión de comunicaciones o ajustar el volumen de audio de un participante de conferencia determinado.

Los dos tipos principales de Stream son la secuencia y la subsecuencia. Las interfaces y los métodos de una implementación estándar son similares para ambos, pero el subflujo permite un nivel de control inferior. Todos los proveedores de servicios multimedia (MSP) deben implementar las interfaces básicas de control de secuencias, pero la compatibilidad con subsecuencias es opcional.

Además, algunos proveedores de servicios implementan [interfaces específicas del proveedor](provider-specific-interfaces.md) para las secuencias. Por ejemplo, IPConf MSP proporciona controles de nivel de participante. Consulte [IPCONF MSP interfaces](ipconf-msp-interfaces.md) para obtener un resumen. Para otras interfaces que podrían implementarse, vea la documentación del proveedor de servicios.

MSP y TAPI crean objetos de secuencia para una llamada durante la configuración inicial de una sesión de entrada o de salida. La aplicación es responsable de identificar los terminales adecuados para estos flujos y seleccionar los terminales en los flujos.

Tenga en cuenta que, en algunos casos, un MSP puede requerir que la aplicación detenga o PAUSE las secuencias antes de ciertas operaciones de la sesión de llamada.

Las interfaces de secuencia se documentan en la referencia de la [interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-reference.md).

En el ejemplo de [selección de un](select-a-terminal.md) código de terminal se muestra un ejemplo de cómo enumerar secuencias y seleccionar terminales en ellas.

 

 



