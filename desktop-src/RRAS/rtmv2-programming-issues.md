---
title: Problemas de programación de RTMv2
description: Las funciones RTMv2 se escriben con las siguientes suposiciones.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemas de programación, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584568fc3c4e7a46a2a2114781b81465d893b80978471aa3149d93d38f0c8c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035595"
---
# <a name="rtmv2-programming-issues"></a>Problemas de programación de RTMv2

Las funciones RTMv2 se escriben con las siguientes suposiciones.

-   Las funciones RTMv2 no asignan memoria para el cliente. El cliente siempre debe asignar memoria.
-   Cuando un cliente anula el registro, debe realizar operaciones de limpieza propiamente dichas, como liberar toda la memoria asignada.
-   Los clientes deben liberar los identificadores correctamente; Pueden producirse pérdidas de memoria si un cliente no observa esta práctica.

 

 




