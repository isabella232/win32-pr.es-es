---
title: Client-Side implementación de canalización
description: Implementación de canalización del lado cliente en llamada a procedimiento remoto (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161052"
---
# <a name="client-side-pipe-implementation"></a>Client-Side implementación de canalización

La aplicación cliente debe implementar los procedimientos siguientes, a los que llamará el código auxiliar de cliente durante la transferencia de datos:

-   Procedimiento de extracción (para una canalización de entrada)
-   Procedimiento de inserción (para una canalización de salida)
-   Procedimiento de asignación para asignar un búfer para los datos de transferencia

Todos estos procedimientos deben usar los argumentos especificados por el archivo de encabezado generado por MIDL. Además, la aplicación cliente debe tener una variable de estado para identificar dónde buscar o colocar los datos.

El procedimiento de aoc también puede ser tan sencillo o tan complejo como sea necesario. Por ejemplo, puede devolver un puntero al mismo búfer cada vez que el código auxiliar llama a la función o puede asignar una cantidad de memoria diferente cada vez. Si los datos ya están en el formato adecuado (una matriz de elementos de canalización, por ejemplo), puede coordinar el procedimiento de asignación con el procedimiento de extracción para asignar un búfer que ya contiene los datos. En ese caso, el procedimiento de extracción podría ser una rutina vacía.

La asignación del búfer debe estar en bytes. Por otro lado, los procedimientos de inserción y extracción manipulan elementos cuyo tamaño en bytes depende de cómo se definieron.

En esta sección se describe la implementación de cliente de canalizaciones de entrada y salida en las secciones siguientes:

-   [Implementar canalizaciones de entrada en el cliente](implementing-input-pipes-on-the-client.md)
-   [Implementar canalizaciones de salida en el cliente](implementing-output-pipes-on-the-client.md)

 

 




