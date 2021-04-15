---
description: Estos pasos comprueban la firma de datos firmados.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Comprobación de un mensaje firmado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668478"
---
# <a name="verifying-a-signed-message"></a><span data-ttu-id="cbd44-103">Comprobación de un mensaje firmado</span><span class="sxs-lookup"><span data-stu-id="cbd44-103">Verifying a Signed Message</span></span>

<span data-ttu-id="cbd44-104">Estos pasos comprueban la firma de datos firmados.</span><span class="sxs-lookup"><span data-stu-id="cbd44-104">These steps verify the signature of signed data.</span></span> <span data-ttu-id="cbd44-105">En la ilustración siguiente se muestran las tareas individuales que se deben realizar, tal y como se muestra en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbd44-105">The following illustration depicts the individual tasks that must be accomplished, as shown in the list that follows it.</span></span>

![comprobación de un mensaje firmado](images/verifmsg.png)

<span data-ttu-id="cbd44-107">**Para comprobar la firma de un mensaje firmado**</span><span class="sxs-lookup"><span data-stu-id="cbd44-107">**To verify the signature of a signed message**</span></span>

1.  <span data-ttu-id="cbd44-108">Obtiene un puntero al mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="cbd44-108">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="cbd44-109">Abra un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cbd44-109">Open a [*certificate store*](../secgloss/c-gly.md).</span></span>
3.  <span data-ttu-id="cbd44-110">Con el identificador de firmante incluido en el mensaje, obtenga el certificado del remitente y obtenga un identificador de su [*clave pública*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cbd44-110">Using the signer ID contained in the message, get the sender's certificate and get a handle to its [*public key*](../secgloss/p-gly.md).</span></span>

    <span data-ttu-id="cbd44-111">Como alternativa a los pasos 2 y 3, puede usar el certificado contenido en el mensaje para recuperar la clave pública del firmante.</span><span class="sxs-lookup"><span data-stu-id="cbd44-111">As an alternative to steps 2 and 3, you can use the certificate contained in the message to retrieve the signer's public key.</span></span>

4.  <span data-ttu-id="cbd44-112">Mediante la clave pública del firmante, descifre la firma digital y genere el Resumen original de los datos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbd44-112">Using the signer's public key, decrypt the digital signature, producing the original digest of the data in the message.</span></span>
5.  <span data-ttu-id="cbd44-113">Mediante el algoritmo hash incluido en el mensaje, se [*aplica un algoritmo hash*](../secgloss/h-gly.md) a los datos contenidos en el mensaje, lo que produce una nueva síntesis.</span><span class="sxs-lookup"><span data-stu-id="cbd44-113">Using the hash algorithm contained in the message, [*hash*](../secgloss/h-gly.md) the data contained in the message, yielding a new digest.</span></span>
6.  <span data-ttu-id="cbd44-114">Compare la síntesis recuperada del mensaje con la nueva síntesis que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="cbd44-114">Compare the digest retrieved from the message with the new digest just created.</span></span>
7.  <span data-ttu-id="cbd44-115">Si los dos resúmenes coinciden, se comprueba la firma.</span><span class="sxs-lookup"><span data-stu-id="cbd44-115">If the two digests match, the signature is verified.</span></span> <span data-ttu-id="cbd44-116">Esto significa que la [*clave privada*](../secgloss/p-gly.md) que se usó para firmar los datos coincide con la clave pública que se acaba de usar para descifrar la firma y que los datos no han cambiado desde que se firmaron los datos.</span><span class="sxs-lookup"><span data-stu-id="cbd44-116">This means that the [*private key*](../secgloss/p-gly.md) that was used to sign the data matches the public key just used to decrypt the signature, and that the data has not changed since the data was signed.</span></span>

    <span data-ttu-id="cbd44-117">Si los dos resúmenes no coinciden, no se comprueba la firma y las claves privada y pública no coinciden, o los datos han cambiado desde que se firmaron los datos, o ambos.</span><span class="sxs-lookup"><span data-stu-id="cbd44-117">If the two digests do not match, the signature is not verified, and either the private/public keys do not match, or the data has been changed since the data was signed, or both.</span></span>

<span data-ttu-id="cbd44-118">Se puede usar una sola función, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), para comprobar una firma, como se muestra en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbd44-118">A single function, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), can be used to verify a signature, as shown in the following procedure.</span></span>

<span data-ttu-id="cbd44-119">**Para comprobar un mensaje firmado**</span><span class="sxs-lookup"><span data-stu-id="cbd44-119">**To verify a signed message**</span></span>

1.  <span data-ttu-id="cbd44-120">Obtiene un puntero al mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="cbd44-120">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="cbd44-121">Obtiene el tamaño del mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="cbd44-121">Get the size of the signed message.</span></span>
3.  <span data-ttu-id="cbd44-122">Obtiene un identificador en un proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="cbd44-122">Get a handle on a cryptographic provider.</span></span>
4.  <span data-ttu-id="cbd44-123">Inicialice el [**mensaje de comprobación de cifrado \_ \_ \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) la estructura.</span><span class="sxs-lookup"><span data-stu-id="cbd44-123">Initialize the [**CRYPT\_VERIFY\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) structure.</span></span>
5.  <span data-ttu-id="cbd44-124">Llame a [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) para comprobar la firma.</span><span class="sxs-lookup"><span data-stu-id="cbd44-124">Call [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) to verify the signature.</span></span>

<span data-ttu-id="cbd44-125">El código que implementa este procedimiento se incluye en el [ejemplo C programa: firmar un mensaje y comprobar la firma de un mensaje](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="cbd44-125">Code that implements this procedure is included in [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
