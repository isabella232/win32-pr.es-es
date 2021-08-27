---
description: En un protocolo simple que usa la autenticación de clave secreta, un cliente presenta un mensaje autenticador en forma de un fragmento de información cifrado en la clave de sesión.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Authenticator Mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc21cd87fbf1b725f276f138bcd0bd513658428ddd1296c4016542953bd8b86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035465"
---
# <a name="authenticator-messages"></a>Authenticator Mensajes

En un protocolo simple que usa la autenticación de clave secreta, un cliente presenta un mensaje autenticador en forma de un fragmento de información cifrado en la clave [*de sesión*](/windows/desktop/SecGloss/s-gly). La información del mensaje del autenticador debe ser diferente cada vez que se ejecuta el protocolo de autenticación o una entidad no autorizada podría reutilizar un mensaje autenticador cifrado.

Al recibir el mensaje autenticador, el servidor lo descifra y puede saber desde el contenido del mensaje descifrado si el descifrado se ha realizado correctamente. Si el mensaje descifrado no es descifrado, el servidor sabe que el cliente que presenta el mensaje autenticador usó la clave correcta para cifrar el mensaje. Solo dos entidades tienen [](/windows/desktop/SecGloss/s-gly) acceso a la clave de sesión y, si el servidor es uno de ellos, el cliente que ha cifrado el mensaje del autenticador debe ser el otro.

Para la autenticación mutua, se ejecuta un protocolo similar. El servidor extrae parte de la información del mensaje autenticador original descifrado, lo cifra con la clave de sesión compartida y envía el mensaje cifrado al cliente. El cliente descifra el mensaje y compara el resultado con el original. Si el mensaje descifrado coincide con la parte correcta del mensaje original, el cliente sabe que el servidor pudo descifrar el mensaje original con la clave de sesión secreta compartida y pudo volver a cifrar una parte de ese mensaje con esa misma clave de sesión secreta [*compartida.*](/windows/desktop/SecGloss/s-gly)

 

 
