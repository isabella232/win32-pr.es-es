---
description: Hay muchas maneras de controlar el envío de mensajes SOAP recibidos al servicio adecuado. Los dos mecanismos más sencillos son el envío de nivel de transporte y el envío de direcciones y acciones.
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: Envío de mensajes SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579c01d03a76fcadc1ee82a270c8e222cbf68aa739d10bed0749bb82bcda80ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030255"
---
# <a name="dispatching-soap-messages"></a>Envío de mensajes SOAP

Hay muchas maneras de controlar el envío de mensajes SOAP recibidos al servicio adecuado. Los dos mecanismos más sencillos son el envío de nivel de transporte y el envío de direcciones y acciones.

## <a name="transport-level-dispatch"></a>Envío de nivel de transporte

Con la distribución de nivel de transporte, el servidor HTTP subyacente (como la [API HTTP)](/windows/desktop/Http/http-api-start-page)se usa para administrar el enrutamiento de las solicitudes al dispositivo y sus servicios. El servidor proporciona una dirección URL diferente para cada servicio y para el dispositivo y se registran receptores diferentes para cada dirección URL. Esto permite diseñar código de forma que cada servicio esté aislado del otro, ya sea ejecutándose como componentes independientes dentro del mismo proceso o ejecutándose como procesos independientes.

La distribución de nivel de transporte tiene algunas ventajas. Los mensajes se pueden enviar al componente adecuado sin analizar primero el sobre SOAP o el cuerpo del mensaje. Además, se puede reutilizar el mecanismo existente para enrutar los mensajes proporcionados por la mayoría de las implementaciones de servidor HTTP, lo que significa que el código de distribución personalizado no es necesario. También aísla el código de procesamiento SOAP entre servicios, lo que proporciona un nivel de seguridad, ya que los servicios seguros evitan que los mensajes viajen a través del código común.

## <a name="address-and-action-dispatch"></a>Envío de direcciones y acciones

El envío de direcciones y acciones se basa en los encabezados SOAP para determinar el servicio adecuado al que se envía el mensaje. Este modelo también puede usar información adicional, como parámetros de referencia, para ayudar a enviar más información.

Este modelo fomenta la reutilización de código en una pila de mensajería por capas, ya que todos los servicios comparten todo el código hasta el procesador SOAP. Además, no se requieren direcciones de transporte distintas para los servicios, lo que significa que las direcciones UUID se pueden usar para los puntos de conexión de servicio. La distribución de direcciones y acciones también se traduce más directamente en un modelo de programación. Los desarrolladores pueden conectar servicios y dispositivos a un único componente que administra el enrutamiento, en lugar de tener que vincularse a una capa HTTP o crear componentes independientes para cada servicio.

 

 
