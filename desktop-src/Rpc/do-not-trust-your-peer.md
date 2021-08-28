---
title: No confiar en el mismo nivel
description: '\ 0034;Do not trust your peer \ 0034; es una regla de seguridad básica, pero a menudo se pasa por alto.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf9235e8b01b6c7b10be96b1d34ed989b27421420d15489441aea948445cfde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021774"
---
# <a name="do-not-trust-your-peer"></a>No confiar en el mismo nivel

"No confiar en el mismo nivel" es una regla de seguridad básica, pero a menudo se pasa por alto. No suponga que la otra parte de una comunicación se comportará correctamente y no suponga que el mismo nivel pasará los datos que espera. MIDL y RPC realizan algunas comprobaciones en su nombre, pero no todas.

Sepa qué aspecto de los parámetros comprueba MIDL o RPC, y qué aspectos debe comprobar usted mismo. Por ejemplo, para los identificadores de contexto de entrada y salida, RPC comprueba que el identificador de contexto no es un valor no null no válido. Permite valores NULL y valores válidos, pero muchos desarrolladores no saben que los valores NULL se permiten. Esto es algo que se debe comprobar.

Incluso si generalmente confía en su homólogo, asegúrese de no introducir nuevas rutas de acceso por las que una máquina o cuenta principal en peligro pueda atacar a otras máquinas. Imagine que un usuario elige su fecha de nacimiento como contraseña y lo adivina un atacante. Incluso después de que se autentiquen las solicitudes del usuario y se permita el acceso a sus datos, asegúrese de que no existen vulnerabilidades vulnerables, tales saturaciones de pila que pueden permitir que un atacante tome el control del servidor y extienda la infracción de seguridad.

 

 




