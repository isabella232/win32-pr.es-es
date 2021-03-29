---
description: En un protocolo simple mediante la autenticación de clave secreta, un cliente presenta un mensaje de autenticador en forma de información cifrada en la clave de sesión.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Mensajes del autenticador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e76cf171d163ac2f1d0d4a7fcaab53a7fa0ace0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277346"
---
# <a name="authenticator-messages"></a>Mensajes del autenticador

En un protocolo simple mediante la autenticación de clave secreta, un cliente presenta un mensaje de autenticador en forma de información cifrada en la [*clave de sesión*](/windows/desktop/SecGloss/s-gly). La información del mensaje del autenticador debe ser diferente cada vez que se ejecuta el protocolo de autenticación, o una entidad no autorizada podría reutilizar un mensaje de autenticador cifrado.

Al recibir el mensaje del autenticador, el servidor lo descifra y puede indicar a partir del contenido del mensaje descifrado si el descifrado se realizó correctamente. Si el mensaje descifrado no es galimatías, el servidor sabe que el cliente que presenta el mensaje del autenticador usó la clave correcta para cifrar el mensaje. Solo dos entidades tienen acceso a la [*clave de sesión*](/windows/desktop/SecGloss/s-gly) y, si el servidor es uno de ellos, el cliente que cifró el mensaje del autenticador debe ser el otro.

Para la autenticación mutua, se ejecuta un protocolo similar. El servidor extrae parte de la información del mensaje del autenticador original descifrado, lo cifra con la clave de sesión compartida y envía el mensaje cifrado al cliente. El cliente descifra el mensaje y compara el resultado con el original. Si el mensaje descifrado coincide con la parte correcta del mensaje original, el cliente sabe que el servidor pudo descifrar el mensaje original con la clave de sesión secreta compartida y pudo volver a cifrar una parte de ese mensaje con esa misma clave de [*sesión*](/windows/desktop/SecGloss/s-gly)secreta compartida.

 

 
