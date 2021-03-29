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
# <a name="authenticator-messages"></a><span data-ttu-id="eef1e-103">Mensajes del autenticador</span><span class="sxs-lookup"><span data-stu-id="eef1e-103">Authenticator Messages</span></span>

<span data-ttu-id="eef1e-104">En un protocolo simple mediante la autenticación de clave secreta, un cliente presenta un mensaje de autenticador en forma de información cifrada en la [*clave de sesión*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="eef1e-104">In a simple protocol using secret key authentication, a client presents an authenticator message in the form of a piece of information encrypted in the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="eef1e-105">La información del mensaje del autenticador debe ser diferente cada vez que se ejecuta el protocolo de autenticación, o una entidad no autorizada podría reutilizar un mensaje de autenticador cifrado.</span><span class="sxs-lookup"><span data-stu-id="eef1e-105">The information in the authenticator message must be different each time the authentication protocol is executed, or an encrypted authenticator message could be reused by an unauthorized entity.</span></span>

<span data-ttu-id="eef1e-106">Al recibir el mensaje del autenticador, el servidor lo descifra y puede indicar a partir del contenido del mensaje descifrado si el descifrado se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="eef1e-106">On receiving the authenticator message, the server decrypts it and can tell from the contents of the decrypted message whether decryption was successful.</span></span> <span data-ttu-id="eef1e-107">Si el mensaje descifrado no es galimatías, el servidor sabe que el cliente que presenta el mensaje del autenticador usó la clave correcta para cifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="eef1e-107">If the decrypted message is not gibberish, the server knows that the client presenting the authenticator message used the correct key to encrypt the message.</span></span> <span data-ttu-id="eef1e-108">Solo dos entidades tienen acceso a la [*clave de sesión*](/windows/desktop/SecGloss/s-gly) y, si el servidor es uno de ellos, el cliente que cifró el mensaje del autenticador debe ser el otro.</span><span class="sxs-lookup"><span data-stu-id="eef1e-108">Only two entities have access to the [*session key*](/windows/desktop/SecGloss/s-gly) and if the server is one of those, the client who encrypted the authenticator message must be the other.</span></span>

<span data-ttu-id="eef1e-109">Para la autenticación mutua, se ejecuta un protocolo similar.</span><span class="sxs-lookup"><span data-stu-id="eef1e-109">For mutual authentication, a similar protocol is executed.</span></span> <span data-ttu-id="eef1e-110">El servidor extrae parte de la información del mensaje del autenticador original descifrado, lo cifra con la clave de sesión compartida y envía el mensaje cifrado al cliente.</span><span class="sxs-lookup"><span data-stu-id="eef1e-110">The server extracts part of the information from the decrypted, original authenticator message, encrypts it with the shared session key, and sends the encrypted message to the client.</span></span> <span data-ttu-id="eef1e-111">El cliente descifra el mensaje y compara el resultado con el original.</span><span class="sxs-lookup"><span data-stu-id="eef1e-111">The client decrypts the message and compares the result with the original.</span></span> <span data-ttu-id="eef1e-112">Si el mensaje descifrado coincide con la parte correcta del mensaje original, el cliente sabe que el servidor pudo descifrar el mensaje original con la clave de sesión secreta compartida y pudo volver a cifrar una parte de ese mensaje con esa misma clave de [*sesión*](/windows/desktop/SecGloss/s-gly)secreta compartida.</span><span class="sxs-lookup"><span data-stu-id="eef1e-112">If the decrypted message matches the correct part of the original message, the client knows that the server was able to decrypt the original message with the shared secret session key and was able to re-encrypt a portion of that message with that same shared secret [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>

 

 
