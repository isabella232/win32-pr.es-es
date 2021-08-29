---
description: Los objetos de secuencia son una abstracción de la secuencia multimedia o secuencias asociadas a una sesión de llamada.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objetos stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49adf4b5073937ae12e86a60a07c64e9f9e9694b8ff65f7b03a49ed3af9fe805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080455"
---
# <a name="stream-objects"></a>Objetos stream

Los objetos de secuencia son una abstracción de la secuencia multimedia o secuencias asociadas a una sesión de llamada. Las interfaces y los métodos expuestos en objetos de secuencia y substream permiten a una aplicación realizar controles muy detallados, como pausar una secuencia, agregar nuevos tipos multimedia a una sesión de comunicaciones o ajustar el volumen de audio de un participante de conferencia determinado.

Los dos tipos principales de secuencia son la secuencia y la subsección. Las interfaces y los métodos de una implementación estándar son similares para ambos, pero el substreaming permite un nivel de control inferior. Todos los proveedores de servicios multimedia (MSP) deben implementar las interfaces básicas de control de secuencias, pero la compatibilidad con substreams es opcional.

Además, algunos proveedores de servicios implementan [interfaces específicas del proveedor](provider-specific-interfaces.md) para secuencias. Por ejemplo, el MSP de IPConf proporciona controles de nivel de participante. Consulte [IpConf MSP Interfaces (Interfaces de MSP de IPConf)](ipconf-msp-interfaces.md) para obtener un resumen. Para otras interfaces que se pueden implementar, consulte la documentación del proveedor de servicios.

Msp y TAPI crean objetos de secuencia para una llamada durante la configuración inicial de una sesión saliente o entrante. La aplicación es responsable de identificar los terminales adecuados para estas secuencias y de seleccionar los terminales en las secuencias.

Tenga en cuenta que, en algunos casos, un MSP puede requerir que la aplicación detenga o pause los flujos antes de determinadas operaciones de sesión de llamada.

Las interfaces de flujo se documentan en la Referencia de la interfaz del proveedor de servicios multimedia [(MSPI).](media-service-provider-interface-mspi-reference.md)

El [ejemplo de código Seleccionar un terminal](select-a-terminal.md) muestra un ejemplo de enumeración de secuencias y selección de terminales en ellos.

 

 



