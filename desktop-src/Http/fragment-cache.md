---
title: Caché de fragmentos
description: La API del servidor HTTP proporciona funcionalidad para que los usuarios almacenen fragmentos de datos en una memoria caché para su uso en respuestas HTTP de forma rápida.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3979fb03c4f8898644329fd27eafb7007adbcc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994016"
---
# <a name="fragment-cache"></a>Caché de fragmentos

La API del servidor HTTP proporciona funcionalidad para que los usuarios almacenen fragmentos de datos en una memoria caché para su uso en respuestas HTTP de forma rápida.

Los fragmentos se pueden agregar a la memoria caché mediante una llamada a la función [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) . Un fragmento se identifica mediante una dirección URL contenida en el parámetro *pUrlPrefix* . Una llamada a esta función con la dirección URL de un fragmento existente sobrescribe el fragmento existente.

El propietario de la cola de solicitudes que agregó inicialmente el fragmento puede eliminar o sobrescribir un fragmento. La función [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) llamada a UrlPrefix elimina todos los fragmentos de ese prefijo, así como los descendientes jerárquicos de ese UrlPrefix. La función [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) lee el fragmento completo o un intervalo de bytes especificado dentro del fragmento.

> [!Note]  
> Al agregar un fragmento a la memoria caché, no se garantiza que esté disponible para futuras llamadas para enviar una respuesta. Las entradas de la caché de fragmentos pueden dejar de estar disponibles en cualquier momento. Se produce un error en una llamada que utiliza un fragmento que no está disponible. Las aplicaciones que usan la memoria caché de fragmentos deben estar preparadas para controlar este error.

 

## <a name="sending-a-response-with-a-fragment"></a>Enviar una respuesta con un fragmento

Los fragmentos se pueden usar para formar todas o partes de un cuerpo de entidad de respuestas HTTP. Puede enviar una respuesta y un cuerpo de entidad en una llamada a la función [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) especificando una matriz de estructuras de [**\_ \_ fragmentos de datos http**](/windows/desktop/api/Http/ns-http-http_data_chunk) en la estructura de [**\_ respuesta http**](http-response.md) .

Un [**\_ \_ fragmento de datos http**](/windows/desktop/api/Http/ns-http-http_data_chunk) puede especificar un bloque de memoria, un identificador de un archivo ya abierto o una entrada de la caché de fragmentos. Estos se corresponden con los tipos de **\_ \_ fragmentos de datos http** : **HttpDataChunkFromMemory**, **HttpDataChunkFromFileHandle** y **HttpDataChunkFromFragmentCache**, respectivamente. Las respuestas completas en la memoria caché HTTP también se pueden usar como fragmentos en la estructura de [**\_ respuesta http**](http-response.md) , aunque no se recomienda esta práctica.

La estructura de [**\_ respuesta http**](http-response.md) contiene un puntero a una matriz de estructuras de [**\_ \_ fragmentos de datos http**](/windows/desktop/api/Http/ns-http-http_data_chunk) que componen el cuerpo de la entidad de la respuesta. La estructura de **\_ respuesta http** también contiene un recuento coincidente que especifica la dimensión de la matriz de estructuras de **\_ \_ fragmentos de datos http** . El valor HttpDataChunkFromFragmentCache de la estructura de **\_ \_ fragmentos de datos http** especifica el tipo de caché de fragmentos del fragmento de datos. La estructura de **\_ \_ fragmentos de datos http** también especifica el nombre del fragmento.

Se produce un ERROR en una respuesta que contiene un fragmento en caché con una \_ ruta \_ de acceso no \_ encontrada si alguna de las entradas de la caché de fragmentos no está disponible. Dado que no se garantiza que las entradas de la caché de fragmentos estén disponibles, las aplicaciones deben estar preparadas para controlar este caso. Una manera de controlar este caso es intentar volver a agregar la entrada de caché de fragmentos y reenviar la respuesta. Si se producen errores repetidos, la aplicación puede usar fragmentos de datos almacenados en búferes de memoria en lugar de entradas de caché de fragmentos.

Las entradas de la caché de fragmentos también se pueden especificar en la función [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) . El fragmento se agrega al cuerpo de la entidad en la estructura de [**\_ \_ fragmentos de datos http**](/windows/desktop/api/Http/ns-http-http_data_chunk) tal y como se ha descrito anteriormente. De nuevo, el envío puede producir un error si alguna de las entradas de caché de fragmentos especificadas no está disponible.

 

 




