---
description: Muestra cómo enviar un mensaje cifrado.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Intercambios de claves de sesión manual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560619"
---
# <a name="manual-session-key-exchanges"></a><span data-ttu-id="1857e-103">Intercambios de claves de sesión manual</span><span class="sxs-lookup"><span data-stu-id="1857e-103">Manual Session Key Exchanges</span></span>

> [!Note]  
> <span data-ttu-id="1857e-104">En el procedimiento descrito en esta sección se da por supuesto que los usuarios (o los clientes de CryptoAPI) ya poseen su propio conjunto de [*pares de claves pública y privada*](../secgloss/p-gly.md) , y que también han obtenido [*las claves públicas*](../secgloss/p-gly.md)de los demás.</span><span class="sxs-lookup"><span data-stu-id="1857e-104">The procedure described in this section assumes that the users (or CryptoAPI clients) already possess their own set of [*public/private key pairs*](../secgloss/p-gly.md) and have also obtained each other's [*public keys*](../secgloss/p-gly.md).</span></span>

 

<span data-ttu-id="1857e-105">En la ilustración siguiente se muestra cómo usar este procedimiento para enviar un mensaje cifrado.</span><span class="sxs-lookup"><span data-stu-id="1857e-105">The following illustration shows how to use this procedure to send an encrypted message.</span></span>

![envío de un mensaje cifrado](images/capi04.png)

<span data-ttu-id="1857e-107">Este enfoque es vulnerable a al menos una forma común de ataque.</span><span class="sxs-lookup"><span data-stu-id="1857e-107">This approach is vulnerable to at least one common form of attack.</span></span> <span data-ttu-id="1857e-108">Un atacante puede adquirir copias de uno o más mensajes cifrados y claves cifradas.</span><span class="sxs-lookup"><span data-stu-id="1857e-108">An eavesdropper can acquire copies of one or more encrypted messages and the encrypted keys.</span></span> <span data-ttu-id="1857e-109">Después, en algún momento posterior, el espionaje puede enviar uno de estos mensajes al receptor y el receptor no tendrá forma de saber que el mensaje no procedía directamente del remitente original.</span><span class="sxs-lookup"><span data-stu-id="1857e-109">Then, at some later time, the eavesdropper can send one of these messages to the receiver and the receiver will have no way of knowing the message did not come directly from the original sender.</span></span> <span data-ttu-id="1857e-110">Este riesgo puede reducirse con la marca de tiempo de todos los mensajes o mediante el uso de números de serie.</span><span class="sxs-lookup"><span data-stu-id="1857e-110">This risk can be reduced by time-stamping all messages or by using serial numbers.</span></span>

<span data-ttu-id="1857e-111">La manera más fácil de enviar mensajes cifrados a otro usuario es enviar el mensaje cifrado con una clave de sesión aleatoria junto con la clave de sesión cifrada con la clave [*pública de intercambio de claves*](../secgloss/k-gly.md)del receptor.</span><span class="sxs-lookup"><span data-stu-id="1857e-111">The easiest way to send encrypted messages to another user is to send the message encrypted with a random session key along with the session key encrypted with the receiver's [*key exchange public key*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="1857e-112">A continuación se indican los pasos para enviar una clave de sesión cifrada.</span><span class="sxs-lookup"><span data-stu-id="1857e-112">Following are the steps for sending an encrypted session key.</span></span>

<span data-ttu-id="1857e-113">**Para enviar una clave de sesión cifrada**</span><span class="sxs-lookup"><span data-stu-id="1857e-113">**To send an encrypted session key**</span></span>

1.  <span data-ttu-id="1857e-114">Cree una [*clave de sesión*](../secgloss/s-gly.md) aleatoria mediante la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="1857e-114">Create a random [*session key*](../secgloss/s-gly.md) by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>
2.  <span data-ttu-id="1857e-115">Cifre el mensaje mediante la clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="1857e-115">Encrypt the message by using the session key.</span></span> <span data-ttu-id="1857e-116">Este procedimiento se describe en [cifrado y descifrado de datos](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="1857e-116">This procedure is discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>
3.  <span data-ttu-id="1857e-117">Exporte la clave de sesión a un [*BLOB de clave*](../secgloss/k-gly.md) con la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , especificando que la clave se cifrará con la clave pública de intercambio de claves del usuario de destino.</span><span class="sxs-lookup"><span data-stu-id="1857e-117">Export the session key into a [*key BLOB*](../secgloss/k-gly.md) with the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, specifying that the key be encrypted with the destination user's key exchange public key.</span></span>
4.  <span data-ttu-id="1857e-118">Envíe el mensaje cifrado y el BLOB de clave cifrada al usuario de destino.</span><span class="sxs-lookup"><span data-stu-id="1857e-118">Send both the encrypted message and the encrypted key BLOB to the destination user.</span></span>
5.  <span data-ttu-id="1857e-119">El usuario de destino importa el BLOB de clave a su CSP mediante la función [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="1857e-119">The destination user imports the key BLOB into his or her CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span> <span data-ttu-id="1857e-120">Esto descifrará automáticamente la clave de sesión, siempre que se haya especificado la clave pública de intercambio de claves del usuario de destino en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="1857e-120">This will automatically decrypt the session key, provided the destination user's key exchange public key was specified in step 3.</span></span>
6.  <span data-ttu-id="1857e-121">Después, el usuario de destino puede descifrar el mensaje mediante la clave de sesión, siguiendo el procedimiento descrito en [cifrado y descifrado de datos](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="1857e-121">The destination user can then decrypt the message by using the session key, following the procedure discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

 

 
