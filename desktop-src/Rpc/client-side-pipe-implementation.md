---
title: Implementación de Client-Side Pipe
description: Implementación de la canalización del lado cliente en llamada a procedimiento remoto (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903744"
---
# <a name="client-side-pipe-implementation"></a>Implementación de Client-Side Pipe

La aplicación cliente debe implementar los siguientes procedimientos, a los que llamará el código auxiliar de cliente durante la transferencia de datos:

-   Un procedimiento de extracción (para una canalización de entrada)
-   Un procedimiento de extracción (para una canalización de salida)
-   Un procedimiento de asignación para asignar un búfer para los datos de transferencia

Todos estos procedimientos deben usar los argumentos especificados por el archivo de encabezado generado por MIDL. Además, la aplicación cliente debe tener una variable de estado para identificar dónde ubicar o colocar los datos.

El procedimiento de asignación también puede ser tan simple o tan complejo como sea necesario. Por ejemplo, puede devolver un puntero al mismo búfer cada vez que el código auxiliar llama a la función, o puede asignar una cantidad de memoria diferente cada vez. Si los datos ya tienen el formato adecuado (una matriz de elementos de canalización, por ejemplo), puede coordinar el procedimiento de asignación con el procedimiento de extracción para asignar un búfer que ya contiene los datos. En ese caso, el procedimiento de extracción puede ser una rutina vacía.

La asignación del búfer debe estar en bytes. Los procedimientos de inserción y extracción, por otro lado, manipulan los elementos, cuyo tamaño en bytes depende de cómo se definieron.

En esta sección se describe la implementación del cliente de canalizaciones de entrada y salida en las siguientes secciones:

-   [Implementar canalizaciones de entrada en el cliente](implementing-input-pipes-on-the-client.md)
-   [Implementar canalizaciones de salida en el cliente](implementing-output-pipes-on-the-client.md)

 

 




