---
title: Acerca de Windows Web Services
description: La Windows WEB Services API es una API por capas y se puede ver como se muestra a continuación.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574248"
---
# <a name="about-windows-web-services"></a>Acerca de Windows Web Services

La Windows Web Services API es una API en capas y se puede ver como se muestra a continuación.

![Diagrama que muestra las capas y las áreas entre capas de la API Windows Web Services.](images/apistack.png)

WWSAPI es una API por capas. Esperamos que la mayoría de los desarrolladores tengan como destino el modelo de servicio, que es un modelo de programación basado en métodos. En el modelo de servicio, el host de servicio proporciona el modelo de programación del lado servidor, mientras que el proxy de servicio proporciona el modelo de programación del lado cliente.

Cada capa expone un conjunto de API y tipos que se pueden usar con las API de esa capa.

## <a name="service-model"></a>Modelo de servicio

La capa de nivel superior denominada [Modelo de servicio](service-model-layer-overview.md) proporciona un modelo de programación basado en métodos y es el modelo más fácil de usar. En el modelo de servicio, el host de [servicio proporciona](service-host.md) el modelo de programación del lado servidor, mientras que el proxy de [servicio](service-proxy.md) proporciona el modelo de programación del lado cliente. [El](context.md) contexto se usa dentro del modelo de servicio para pasar un estado pertinente disponible para la operación de servicio o la devolución de llamada cuando se invoca. Y [El contrato de](contract.md) servicio se usa para especificar un contrato de servicio en un punto de conexión expuesto en el servicio. Los siguientes componentes y operaciones forman parte de la capa de servicio:

-   [Host de servicio](service-host.md)
-   [Proxy de servicio](service-proxy.md)
-   [Contexto](context.md)
-   [Contrato](contract.md)
-   [Metadatos de servicio](service-metadata.md)

## <a name="channel-layer"></a>Capa de canal

El modelo de servicio se basa en una capa de canal, que proporciona total flexibilidad, pero es más difícil de usar. Los siguientes componentes y operaciones forman parte de la capa de canal:

-   [Mensaje](message.md)
-   [Canal](channel.md)
-   [Agente de escucha](listener.md)
-   [Errores](faults.md)
-   [Url](url.md)
-   [Seguridad](security-overview.md)
-   [Importación de metadatos](metadata-import.md)

## <a name="xml-layer"></a>Capa XML

A su vez, la capa de canal se basa en un marco XML ligero, que incluye la deserialización de tipos de datos de C. Los siguientes componentes y operaciones forman parte de la capa XML:

-   [Escritor XML](xml-writer.md)
-   [Lector XML](xml-reader.md)
-   [Búfer XML](xml-buffer.md)
-   [Serialización](serialization.md)
-   [Compatibilidad con lenguaje XML](xml-language-support.md)

## <a name="common-to-all-layers"></a>Común a todas las capas

A continuación se incluyen temas que se aplican a cualquiera de las tres capas:

-   [Errores](errors.md)
-   [Modelo asincrónico](asynchronous-model.md)
-   [Seguridad para subprocesos](thread-safety.md)
-   [Seguimiento](tracing.md)
-   [Cancelación](cancellation.md)
-   [Utilidades](utilities.md)
-   [Depuración](debugging.md)
-   [Herramienta del compilador de Wsutil](wsutil-compiler-tool.md)
-   [Montón](heap.md)

## <a name="examples"></a>Ejemplos

Para obtener más información sobre los elementos de API, [vea Windows referencia de servicios web](windows-web-services-reference.md). Para obtener ejemplos de uso de la API, consulte [Uso de Windows Web Services](using-windows-web-services.md).

 

 




