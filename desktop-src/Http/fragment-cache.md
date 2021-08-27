---
title: Caché de fragmentos
description: La API del servidor HTTP proporciona funcionalidad para que los usuarios almacenen fragmentos de datos en una memoria caché para su uso en la forma rápida de respuestas HTTP.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6659ead1139bd1b35a466a56c44357dd1f7f30cbac5fad8669445208be0e5136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047255"
---
# <a name="fragment-cache"></a>Caché de fragmentos

La API del servidor HTTP proporciona funcionalidad para que los usuarios almacenen fragmentos de datos en una memoria caché para su uso en la forma rápida de respuestas HTTP.

Los fragmentos se pueden agregar a la memoria caché mediante una llamada a la [**función HttpAddFragmentToCache.**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) Un fragmento se identifica mediante una dirección URL contenida en el *parámetro pUrlPrefix.* Una llamada a esta función con la dirección URL de un fragmento existente sobrescribe el fragmento existente.

El propietario de la cola de solicitudes que agregó inicialmente el fragmento puede eliminar o sobrescribir un fragmento. La [**función HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) a la que se llama con urlPrefix elimina todos los fragmentos dentro de ese prefijo, así como los descendientes jerárquicos de esa dirección UrlPrefix. La [**función HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) lee todo el fragmento o un intervalo de bytes especificado dentro del fragmento.

> [!Note]  
> Agregar un fragmento a la memoria caché no garantiza que esté disponible para futuras llamadas para enviar una respuesta. Las entradas de caché de fragmentos pueden no estar disponibles en cualquier momento. Se produce un error en una llamada que usa un fragmento que no está disponible. Las aplicaciones que usan la caché de fragmentos deben estar preparadas para controlar este error.

 

## <a name="sending-a-response-with-a-fragment"></a>Envío de una respuesta con un fragmento

Los fragmentos se pueden usar para formar todas o partes de un cuerpo de entidad de respuestas HTTP. Puede enviar una respuesta y un cuerpo de entidad en una llamada a la función [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) especificando una matriz de estructuras [**HTTP DATA \_ \_ CHUNK**](/windows/desktop/api/Http/ns-http-http_data_chunk) en la estructura [**HTTP \_ RESPONSE.**](http-response.md)

Un [**FRAGMENTO DE DATOS \_ \_ HTTP**](/windows/desktop/api/Http/ns-http-http_data_chunk) puede especificar un bloque de memoria, un identificador para un archivo ya abierto o una entrada de caché de fragmentos. Corresponden a los tipos **HTTP \_ DATA \_ CHUNK:** **HttpDataChunkFromMemory,** **HttpDataChunkFromFileHandle** y **HttpDataChunkFromFragmentCache,** respectivamente. Las respuestas completa de la caché HTTP también se pueden usar como fragmentos en la estructura [**HTTP \_ RESPONSE,**](http-response.md) aunque no se recomienda esta práctica.

La [**estructura \_ HTTP RESPONSE**](http-response.md) contiene un puntero a una matriz de estructuras HTTP DATA [**\_ \_ CHUNK**](/windows/desktop/api/Http/ns-http-http_data_chunk) que componen el cuerpo de la entidad de la respuesta. La **estructura \_ HTTP RESPONSE** también contiene un recuento de coincidencias que especifica la dimensión de la matriz de estructuras HTTP DATA **\_ \_ CHUNK.** El valor HttpDataChunkFromFragmentCache de la estructura **HTTP \_ DATA \_ CHUNK** especifica el tipo de caché de fragmentos del fragmento de datos. La **estructura HTTP DATA \_ \_ CHUNK** también especifica el nombre del fragmento.

Una respuesta que contiene un fragmento almacenado en caché produce un error ERROR PATH NOT FOUND si alguna de las entradas de caché de fragmentos \_ \_ no está \_ disponible. Puesto que no se garantiza que las entradas de caché de fragmentos estén disponibles, las aplicaciones deben estar preparadas para controlar este caso. Una manera de controlar este caso es intentar volver a agregar la entrada de caché de fragmentos y volver a enviar la respuesta. Si se producen errores repetidos, la aplicación puede usar fragmentos de datos almacenados en búferes de memoria en lugar de entradas de caché de fragmentos.

Las entradas de caché de fragmentos también se pueden especificar en la [**función HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) El fragmento se agrega al cuerpo de la entidad en la estructura [**HTTP \_ DATA \_ CHUNK,**](/windows/desktop/api/Http/ns-http-http_data_chunk) como se ha descrito anteriormente. De nuevo, el envío puede producir un error si alguna de las entradas de caché de fragmentos especificadas no está disponible.

 

 




