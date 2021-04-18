---
title: Canalizaciones (RPC)
description: El constructor de tipo de canalización es un mecanismo muy eficaz para pasar grandes cantidades de datos o cualquier cantidad de datos que no esté disponible en la memoria al mismo tiempo.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- RPC llamada a procedimiento remoto, descripción, canalizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488765"
---
# <a name="pipes-rpc"></a>Canalizaciones (RPC)

El constructor de tipo de canalización es un mecanismo muy eficaz para pasar grandes cantidades de datos o cualquier cantidad de datos que no esté disponible en la memoria al mismo tiempo. Mediante el uso de una canalización, el tiempo de ejecución de RPC controla la transferencia de datos real, lo que elimina la sobrecarga asociada a llamadas a procedimiento remoto repetidas.

Una vez que un cliente invoca un procedimiento remoto que tiene un parámetro de canalización, el cliente y el servidor escriben bucles para transferir los datos. Los datos se pueden producir en el cliente o el servidor. En cualquier caso, no es necesario conocer la cantidad de datos (en bytes) de antemano. Los datos se pueden generar o consumir incrementalmente. En el bucle de transferencia de datos, el servidor llama a rutinas de código auxiliar que cargan o descargan un búfer de datos. El cliente llama a los procedimientos definidos por el programador para asignar búferes, cargar datos en los búferes y descargarlos.

En esta sección se proporciona información general sobre el uso de canalizaciones para llamadas a procedimientos remotos. Presenta la información general de los temas siguientes:

-   [Terminología de canalización esencial](essential-pipe-terminology.md)
-   [El estado de la canalización](the-pipe-state.md)
-   [Definir canalizaciones en archivos IDL](defining-pipes-in-idl-files.md)
-   [Implementación de la canalización del lado cliente](client-side-pipe-implementation.md)
-   [Implementación de la canalización del lado servidor](server-side-pipe-implementation.md)
-   [Reglas para varias canalizaciones](rules-for-multiple-pipes.md)
-   [Combinación de parámetros de canalización y no de canalización](combining-pipe-and-nonpipe-parameters.md)

Para obtener más información sobre la sintaxis de canalización y las restricciones, vea [canalización](/windows/desktop/Midl/pipe) en la referencia del lenguaje MIDL. En el programa de ejemplo de CANALIZAciones del kit de desarrollo de software (SDK) de la plataforma \\ , el directorio RPC muestra cómo usar las canalizaciones **\[ in y out \]** para transferir datos entre un cliente y un servidor.

 

 
