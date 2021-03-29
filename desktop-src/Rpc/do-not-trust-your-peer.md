---
title: No confíe en su equipo del mismo nivel
description: '\ 0034; no confíe en su equipo del mismo nivel \ 0034; es una regla de seguridad básica, pero a menudo se pasa por alto.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775499"
---
# <a name="do-not-trust-your-peer"></a>No confíe en su equipo del mismo nivel

"No confiar en el equipo del mismo nivel" es una regla de seguridad básica, pero a menudo se pasa por alto. No asuma que la otra parte de una comunicación se comportará correctamente y no asumirá que el homólogo pasará los datos esperados. MIDL y RPC realizan algunas comprobaciones en su nombre, pero no todas las comprobaciones.

Sepa qué aspecto de los parámetros se comprueban mediante MIDL o RPC, y qué aspectos debe comprobar usted mismo. Por ejemplo, para los identificadores de contexto in/out, RPC comprueba que el identificador de contexto no es un valor no NULL válido. Permite valores NULL y valores válidos, pero muchos desarrolladores no saben que los valores NULL se permiten. Esto es algo que se debe comprobar.

Aunque en general confíe en el equipo del mismo nivel, asegúrese de no introducir nuevas rutas de acceso por las que una máquina principal o máquina en peligro puede atacar a otras máquinas. Imagine que un usuario elige su cumpleaños como su contraseña y lo adivina un atacante. Incluso después de que se autentiquen las solicitudes del usuario y se permita el acceso a sus datos, asegúrese de que las vulnerabilidades explotables no existan, como saturaciones de la pila, lo que puede permitir que un atacante tome el control del servidor y amplíe la brecha de seguridad.

 

 




