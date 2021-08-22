---
title: Canalizaciones (RPC)
description: El constructor de tipo de canalización es un mecanismo muy eficaz para pasar grandes cantidades de datos o cualquier cantidad de datos que no esté disponible en la memoria a la vez.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- Llamada a procedimiento remoto RPC, descrita, canalizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c477dc249e400022efda21fef4055840c5095e74500f4ae0bea375310b1903f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927530"
---
# <a name="pipes-rpc"></a>Canalizaciones (RPC)

El constructor de tipo de canalización es un mecanismo muy eficaz para pasar grandes cantidades de datos o cualquier cantidad de datos que no esté disponible en la memoria a la vez. Mediante el uso de una canalización, el tiempo de ejecución de RPC controla la transferencia de datos real, lo que elimina la sobrecarga asociada a las llamadas a procedimiento remoto repetidas.

Después de que un cliente invoca un procedimiento remoto que tiene un parámetro de canalización, el cliente y el servidor escriben bucles para transferir datos. Los datos se pueden generar en el cliente o en el servidor. En cualquier caso, la cantidad de datos (en bytes) no tiene que conocerse de antemano. Los datos se pueden generar o consumir de forma incremental. Mientras se encuentra en el bucle de transferencia de datos, el servidor llama a rutinas de código auxiliar que cargan o descargan un búfer de datos. El cliente llama a procedimientos definidos por el programador para asignar búferes, cargar datos en y descargar datos de los búferes.

En esta sección se proporciona información general sobre el uso de canalizaciones para llamadas a procedimientos remotos. Presenta la información general en los temas siguientes:

-   [Terminología esencial de canalización](essential-pipe-terminology.md)
-   [Estado de canalización](the-pipe-state.md)
-   [Definir canalizaciones en archivos IDL](defining-pipes-in-idl-files.md)
-   [Implementación de canalización del lado cliente](client-side-pipe-implementation.md)
-   [Implementación de canalización del lado servidor](server-side-pipe-implementation.md)
-   [Reglas para varias canalizaciones](rules-for-multiple-pipes.md)
-   [Combinación de parámetros de canalización y no de canalización](combining-pipe-and-nonpipe-parameters.md)

Para obtener más información sobre la sintaxis y las restricciones de canalización, vea [canalización en](/windows/desktop/Midl/pipe) midl language reference (Referencia del lenguaje MIDL). El programa de ejemplo PIPES del directorio \\ rpc **\[ \]** de ejemplos del Kit de desarrollo de software de plataforma (SDK) muestra cómo usar canalizaciones de entrada y salida para transferir datos entre un cliente y un servidor.

 

 
