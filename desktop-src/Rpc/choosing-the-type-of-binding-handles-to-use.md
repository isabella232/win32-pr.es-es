---
title: Elección del tipo de identificadores de enlace que se va a usar
description: Elección del tipo de identificadores de enlace que se va a usar
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075436"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Elección del tipo de identificadores de enlace que se va a usar

**Procedimiento recomendado:** Si sabe qué servidor usará la aplicación, use identificadores explícitos. Si no es así, use los identificadores explícitos en cada ocasión, o bien use identificadores genéricos con rutinas de **\_ enlace** y **\_ desenlace** .

No use identificadores ni identificadores automáticos. Los identificadores implícitos no son seguros para subprocesos y, aunque la seguridad para subprocesos puede parecer innecesaria, podría ser necesario más adelante. Los identificadores automáticos tienen una gran sobrecarga y requieren una gran cantidad de configuración para funcionar correctamente. Los servicios de Active Directory han reemplazado sus capacidades de búsqueda.

Los identificadores explícitos son muy eficaces y muchas funciones atractivas solo están disponibles para los identificadores explícitos. Por ejemplo, si varias llamadas RPC van al mismo servidor, puede construir el identificador de enlace una vez y realizar todas las llamadas con él. Este enfoque es mucho más eficaz que cualquier otro método. Si no se conoce el servidor al que se va a llamar, construya un identificador de enlace explícito para cada llamada o use identificadores de enlace genéricos.

En Microsoft™ Windows XP, el tiempo de ejecución de RPC es bastante eficaz en las llamadas de reutilización y almacenamiento en caché, por lo que si la llamada *n*+ 1ª termina en el mismo servidor que la llamada *n*, RPC vuelve a usar los recursos asignados para la llamada *n*, evitando la necesidad de almacenar en caché los identificadores de enlace para mejorar el rendimiento.

 

 




