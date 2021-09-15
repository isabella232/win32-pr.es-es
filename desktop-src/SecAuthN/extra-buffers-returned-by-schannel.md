---
description: Schannel tiene un conjunto bien definido de comportamientos para obtener información incompleta o excesiva incluida en los búferes de entrada de estas funciones.
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Búferes adicionales devueltos por Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271412"
---
# <a name="extra-buffers-returned-by-schannel"></a>Búferes adicionales devueltos por Schannel

La información debe enviarse entre [](/windows/desktop/SecGloss/s-gly) el cliente y el servidor mientras se establece un contexto de seguridad y posteriormente porque los mensajes seguros se intercambian mediante las características de cifrado y descifrado proporcionadas por Schannel. Las siguientes funciones se usan para realizar estas tareas:

-   [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

Schannel tiene un conjunto bien definido de comportamientos para obtener información incompleta o excesiva incluida en los búferes de entrada de estas funciones. La información se intercambia entre el cliente y el servidor de la siguiente manera:

1.  La entidad local interactúa con Schannel llamando a una función SSPI y pasando información. Normalmente, la información se recibió de la parte remota.
2.  La función devuelve un código de estado y búferes de salida que contienen información.
3.  Según el código de estado, los búferes de salida se envían a la entidad remota mediante algún mecanismo de comunicación.
4.  La entidad remota lee la información enviada por la entidad local.
5.  El bucle se repite, con las partes locales y remotas intercambiadas. (La entidad remota llama a una función SSPI y pasa la información leída en el paso anterior).

Todo funciona según lo previsto cuando el búfer de entrada de la función SSPI contiene exactamente la información necesaria. Sin embargo, debido a la naturaleza orientada a secuencias de algunos protocolos de comunicación, puede que esto no sea así. Un bloque de información recibido de una entidad remota puede contener menos datos de los necesarios o más datos de los que Schannel puede procesar en una sola llamada de función.

Si el búfer de entrada contiene poca información, las funciones devuelven SEC \_ E \_ INCOMPLETE \_ MESSAGE. El autor de la llamada debe obtener datos adicionales de la entidad remota y volver a llamar a la función.

Cuando los búferes de entrada contienen demasiada información, Schannel no lo trata como un error. La función procesa tanto como sea posible la entrada y devuelve el código de estado de esa actividad de procesamiento. Además, Schannel indica la presencia de información sin procesar en los búferes de entrada devolviendo un búfer de salida de tipo SECBUFFER \_ EXTRA. Probar los búferes de salida para este tipo de búfer es la única manera de detectar esta situación. El **campo cbBuffer** de la estructura de búfer adicional indica cuántos bytes de entrada no se procesaron.

> [!Note]  
> El **campo pvBuffer** del búfer adicional no contiene una copia de los datos en exceso.

 

Si recibe un búfer adicional de una función SSPI, debe quitar la información ya procesada del búfer de entrada y volver a llamar a la función. Schannel puede y, a menudo, devolver solo el búfer adicional y nada más en los búferes de salida.

 

 
