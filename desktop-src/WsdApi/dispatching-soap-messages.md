---
description: Existen muchas formas de controlar la distribución de mensajes SOAP recibidos al servicio adecuado. Los dos mecanismos más sencillos son envío de nivel de transporte y envío de dirección y acción.
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: Enviar mensajes SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a60e896557a64b840ec890ddc5c5d2e2cf8295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545867"
---
# <a name="dispatching-soap-messages"></a>Enviar mensajes SOAP

Existen muchas formas de controlar la distribución de mensajes SOAP recibidos al servicio adecuado. Los dos mecanismos más sencillos son envío de nivel de transporte y envío de dirección y acción.

## <a name="transport-level-dispatch"></a>Envío de nivel de transporte

Con el envío de nivel de transporte, el servidor HTTP subyacente (como la [API http](/windows/desktop/Http/http-api-start-page)) se usa para administrar el enrutamiento de las solicitudes al dispositivo y sus servicios. El servidor proporciona una dirección URL diferente para cada servicio y para el dispositivo, y se registran receptores diferentes para cada dirección URL. Esto permite diseñar el código de forma que cada servicio esté aislado del otro, ya sea en ejecución como componentes independientes en el mismo proceso o en ejecución como procesos independientes.

El envío de nivel de transporte tiene algunas ventajas. Los mensajes se pueden enviar al componente adecuado sin analizar primero la envoltura SOAP o el cuerpo del mensaje. Además, se puede reutilizar el mecanismo existente para enrutar los mensajes proporcionados por la mayoría de las implementaciones de servidor HTTP, lo que significa que el código de distribución personalizado no es necesario. También aísla el código de procesamiento SOAP entre los servicios, lo que proporciona un nivel de seguridad, ya que los servicios seguros evitan que los mensajes viajen a través del código común.

## <a name="address-and-action-dispatch"></a>Envío de dirección y acción

La distribución de la dirección y la acción se basa en los encabezados SOAP para determinar el servicio adecuado al que se envía el mensaje. Este modelo también puede usar información adicional, como parámetros de referencia, para facilitar la distribución.

Este modelo fomenta la reutilización de código en una pila de mensajería por capas, ya que todos los servicios comparten todo el código hasta el procesador SOAP. Además, no se requieren direcciones de transporte diferentes para los servicios, lo que significa que las direcciones UUID se pueden usar para los puntos de conexión de servicio. La distribución de la dirección y la acción también traduce más directamente a un modelo de programación. Los desarrolladores pueden conectar servicios y dispositivos en un único componente que administra el enrutamiento, en lugar de tener que asociarse a una capa HTTP o crear componentes independientes para cada servicio.

 

 
