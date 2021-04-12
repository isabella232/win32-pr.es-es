---
title: Problemas de programación de RTMv2
description: Las funciones de RTMv2 se escriben con los siguientes supuestos.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemas de programación, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357064"
---
# <a name="rtmv2-programming-issues"></a>Problemas de programación de RTMv2

Las funciones de RTMv2 se escriben con los siguientes supuestos.

-   Las funciones RTMv2 no asignan memoria para el cliente. El cliente siempre debe asignar memoria.
-   Cuando se anula el registro de un cliente, debe realizar las operaciones de limpieza, como liberar toda la memoria asignada.
-   Los clientes deben liberar los identificadores correctamente; pueden producirse pérdidas de memoria si un cliente no observa esta práctica.

 

 




