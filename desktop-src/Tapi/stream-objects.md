---
description: Los objetos de secuencia son una abstracción de la secuencia multimedia o de los flujos asociados a una sesión de llamada.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objetos de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168861"
---
# <a name="stream-objects"></a>Objetos de secuencia

Los objetos de secuencia son una abstracción de la secuencia multimedia o de los flujos asociados a una sesión de llamada. Las interfaces y los métodos expuestos en objetos de secuencia y substream permiten a una aplicación realizar controles muy detallados, como pausar una secuencia, agregar nuevos tipos multimedia a una sesión de comunicaciones o ajustar el volumen de audio de un participante de conferencia determinado.

Los dos tipos principales de secuencia son la secuencia y la substream. Las interfaces y los métodos de una implementación estándar son similares para ambos, pero la substreaming permite un nivel de control inferior. Todos los proveedores de servicios multimedia (MSP) deben implementar las interfaces de control de flujo básicas, pero la compatibilidad con las subdifusión es opcional.

Además, algunos proveedores de servicios implementan [interfaces específicas del proveedor](provider-specific-interfaces.md) para las secuencias. Por ejemplo, el MSP de IPConf proporciona controles de nivel de participante. Consulte [IpConf MSP Interfaces (Interfaces de MSP de IPConf)](ipconf-msp-interfaces.md) para obtener un resumen. Para otras interfaces que se puedan implementar, consulte la documentación del proveedor de servicios.

El MSP y TAPI crean objetos de secuencia para una llamada durante la configuración inicial de una sesión saliente o entrante. La aplicación es responsable de identificar los terminales adecuados para estas secuencias y de seleccionar los terminales en las secuencias.

Tenga en cuenta que, en algunos casos, un MSP puede requerir que la aplicación detenga o pause secuencias antes de determinadas operaciones de sesión de llamada.

Las interfaces de flujo se documentan en la referencia de la interfaz del proveedor de servicios multimedia [(MSPI).](media-service-provider-interface-mspi-reference.md)

El [ejemplo de código Seleccionar un terminal](select-a-terminal.md) muestra un ejemplo de enumeración de secuencias y selección de terminales en ellas.

 

 



