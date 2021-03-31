---
description: Muchas formas de autenticación se basan en la idea de que una entidad puede demostrar su identidad si puede demostrar que conoce una clave, como una contraseña, que solo puede conocer.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticación de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277146"
---
# <a name="key-authentication"></a><span data-ttu-id="446f2-103">Autenticación de clave</span><span class="sxs-lookup"><span data-stu-id="446f2-103">Key Authentication</span></span>

<span data-ttu-id="446f2-104">Muchas formas de autenticación se basan en la idea de que una entidad puede demostrar su identidad si puede demostrar que conoce una clave, como una contraseña, que solo puede conocer.</span><span class="sxs-lookup"><span data-stu-id="446f2-104">Many forms of authentication are based on the idea that an entity can prove its identity if it can prove it knows a key, such as a password, that only it can know.</span></span>

<span data-ttu-id="446f2-105">Las técnicas de autenticación que se basan en un secreto, como una contraseña, deben tener una manera de evitar que el secreto se convierta en un conocimiento público.</span><span class="sxs-lookup"><span data-stu-id="446f2-105">Authentication techniques that rely on a secret, such as a password, need to have a way to keep the secret from becoming public knowledge.</span></span> <span data-ttu-id="446f2-106">Un propietario de contraseña no puede recorrer una puerta y proporcionar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="446f2-106">A password owner cannot walk up to a door and give the password.</span></span> <span data-ttu-id="446f2-107">Es posible que alguien además del Doorkeeper esté escuchando; o bien, podría ser la puerta equivocada.</span><span class="sxs-lookup"><span data-stu-id="446f2-107">Someone besides the doorkeeper might be listening; or it might be the wrong door.</span></span> <span data-ttu-id="446f2-108">Con el fin de mantener un secreto, debe haber una manera de demostrar que un usuario conoce la contraseña sin revelar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="446f2-108">In order to keep a secret, there must be a way to prove a user knows the password without revealing the password.</span></span> <span data-ttu-id="446f2-109">Esta es la idea detrás de la autenticación de clave secreta, un método de comprobación utilizado en el [*protocolo Kerberos*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="446f2-109">That is the idea behind secret key authentication, a method of verification used throughout the [*Kerberos protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="446f2-110">Tenga en cuenta que el "secreto" en la autenticación de clave secreta es que el proceso de autenticación tiene lugar "en secreto", es decir, sin revelar realmente el contenido de la clave.</span><span class="sxs-lookup"><span data-stu-id="446f2-110">Notice that the "secret" in secret key authentication is that the authentication process takes place "in secret;" that is, without ever actually revealing the content of the key.</span></span>

<span data-ttu-id="446f2-111">Para que la autenticación de clave secreta funcione, las dos partes de una transacción deben compartir una [*clave de sesión*](../secgloss/s-gly.md) criptográfica, que también es secreta, solo las conoce y no otras.</span><span class="sxs-lookup"><span data-stu-id="446f2-111">For secret key authentication to work, the two parties to a transaction must share a cryptographic [*session key*](../secgloss/s-gly.md) which is also secret, known only to them and to no others.</span></span> <span data-ttu-id="446f2-112">La clave es [*simétrica*](../secgloss/s-gly.md); es decir, es una clave única que se usa para el cifrado y el descifrado.</span><span class="sxs-lookup"><span data-stu-id="446f2-112">The key is [*symmetric*](../secgloss/s-gly.md); that is, it is a single key used for both encryption and decryption.</span></span> <span data-ttu-id="446f2-113">Una parte del proceso de autenticación demuestra su conocimiento de la clave mediante el cifrado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="446f2-113">One party in the authentication process proves its knowledge of the key by encrypting a message.</span></span> <span data-ttu-id="446f2-114">La otra parte demuestra su conocimiento de la clave mediante el descifrado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="446f2-114">The other party proves its knowledge of the key by decrypting the message.</span></span>

 

 
