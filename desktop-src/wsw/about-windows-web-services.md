---
title: Acerca de los servicios Web de Windows
description: La API de servicios Web de Windows es una API en capas y se puede mostrar como se indica a continuación.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566041"
---
# <a name="about-windows-web-services"></a>Acerca de los servicios Web de Windows

La API de servicios Web de Windows es una API en capas y se puede ilustrar del siguiente modo:

![Diagrama que muestra las capas y las áreas de capas cruzadas de la API de servicios Web de Windows.](images/apistack.png)

WWSAPI es una API en capas. Esperamos que la mayoría de los desarrolladores tengan como destino el modelo de servicio, que es un modelo de programación basado en métodos. En el modelo de servicio, el host de servicio proporciona el modelo de programación del lado servidor, mientras que el proxy de servicio proporciona el modelo de programación del lado cliente.

Cada capa expone un conjunto de API y tipos que se pueden usar con las API de esa capa.

## <a name="service-model"></a>Modelo de servicio

La capa de nivel superior denominada [modelo de servicio](service-model-layer-overview.md) proporciona un modelo de programación basado en métodos y es el modelo más sencillo de usar. En el modelo de servicio, el [host de servicio](service-host.md) proporciona el modelo de programación del lado servidor, mientras que el proxy de [servicio](service-proxy.md) proporciona el modelo de programación del lado cliente. El [contexto](context.md) se usa en el modelo de servicio para pasar un estado relevante disponible para la operación de servicio y/o la devolución de llamada cuando se invoca. Y el [contrato de servicio](contract.md) se usa para especificar un contrato de servicio en un extremo expuesto en el servicio. Los siguientes componentes y operaciones forman parte del nivel de servicio:

-   [Host de servicio](service-host.md)
-   [Proxy de servicio](service-proxy.md)
-   [Contexto](context.md)
-   [DataContract](contract.md)
-   [Metadatos de servicio](service-metadata.md)

## <a name="channel-layer"></a>Nivel de canal

El modelo de servicio se basa en una capa de canal, lo que proporciona una flexibilidad completa, pero es más difícil de usar. Los siguientes componentes y operaciones forman parte de la capa del canal:

-   [Message](message.md)
-   [Canal](channel.md)
-   [Agente de escucha](listener.md)
-   [Errores](faults.md)
-   [Url](url.md)
-   [Seguridad](security-overview.md)
-   [Importación de metadatos](metadata-import.md)

## <a name="xml-layer"></a>Nivel XML

La capa de canales a su vez se basa en un marco XML ligero, que incluye la deserialización de los tipos de datos de C. Los siguientes componentes y operaciones forman parte de la capa XML:

-   [Escritor XML](xml-writer.md)
-   [Lector XML](xml-reader.md)
-   [Búfer XML](xml-buffer.md)
-   [Serialización](serialization.md)
-   [Compatibilidad con el lenguaje XML](xml-language-support.md)

## <a name="common-to-all-layers"></a>Común a todas las capas

A continuación se muestran los temas que se aplican a cualquiera de las tres capas:

-   [Errores](errors.md)
-   [Modelo asincrónico](asynchronous-model.md)
-   [Seguridad para subprocesos](thread-safety.md)
-   [Seguimiento](tracing.md)
-   [Cancelación](cancellation.md)
-   [Utilidades](utilities.md)
-   [Depuración](debugging.md)
-   [Herramienta del compilador Wsutil](wsutil-compiler-tool.md)
-   [Montón](heap.md)

## <a name="examples"></a>Ejemplos

Para obtener más información sobre los elementos de la API, consulte [referencia de servicios Web de Windows](windows-web-services-reference.md). Para obtener ejemplos del uso de la API, vea [uso de servicios Web de Windows](using-windows-web-services.md).

 

 




