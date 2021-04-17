---
description: Schannel tiene un conjunto bien definido de comportamientos para la información incompleta o excesiva incluida en los búferes de entrada de estas funciones.
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Búferes adicionales devueltos por Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652989"
---
# <a name="extra-buffers-returned-by-schannel"></a>Búferes adicionales devueltos por Schannel

La información se debe enviar entre el cliente y el servidor mientras se establece un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) y después porque los mensajes seguros se intercambian mediante las características de cifrado y descifrado proporcionadas por Schannel. Las siguientes funciones se usan para realizar estas tareas:

-   [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [**DecryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

Schannel tiene un conjunto bien definido de comportamientos para la información incompleta o excesiva incluida en los búferes de entrada de estas funciones. La información se intercambia entre el cliente y el servidor de la siguiente manera:

1.  La entidad local interactúa con Schannel llamando a una función SSPI y pasando información. Normalmente, la información se recibió de la parte remota.
2.  La función devuelve un código de estado y los búferes de salida que contienen información.
3.  Según el código de estado, los búferes de salida se envían a la parte remota mediante algún mecanismo de comunicación.
4.  La parte remota lee la información enviada por la entidad local.
5.  El bucle se repite, con las partes locales y remotas intercambiadas. (La entidad remota llama a una función SSPI y pasa la información leída en el paso anterior).

Todo funciona según lo esperado cuando el búfer de entrada de la función SSPI contiene exactamente la información necesaria. Sin embargo, debido a la naturaleza orientada a flujos de algunos protocolos de comunicaciones, este podría no ser el caso; un bloque de información recibido de una parte remota puede contener menos datos de los necesarios o más datos de los que puede procesar Schannel en una única llamada de función.

Si el búfer de entrada contiene demasiado poca información, las funciones devuelven un \_ \_ mensaje incompleto de sec \_ . El autor de la llamada debe obtener datos adicionales de la parte remota y volver a llamar a la función.

Cuando los búferes de entrada contienen demasiada información, Schannel no lo trata como un error. La función procesa tanto como sea posible la entrada y devuelve el código de estado para esa actividad de procesamiento. Además, Schannel indica la presencia de información sin procesar en los búferes de entrada devolviendo un búfer de salida de tipo SECBUFFER \_ extra. Probar los búferes de salida para este tipo de búfer es la única manera de detectar esta situación. El campo **cbBuffer** de la estructura de búfer adicional indica el número de bytes de entrada que no se procesaron.

> [!Note]  
> El campo **pvBuffer** del búfer adicional no contiene una copia de los datos sobrantes.

 

Si recibe un búfer adicional de una función SSPI, debe quitar la información ya procesada del búfer de entrada y llamar de nuevo a la función. Schannel puede, y a menudo, devuelve solo el búfer adicional y nada más en los búferes de salida.

 

 
