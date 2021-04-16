---
description: Proceso para descodificar los datos firmados.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Descodificar datos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666405"
---
# <a name="decoding-signed-data"></a><span data-ttu-id="0b661-103">Descodificar datos firmados</span><span class="sxs-lookup"><span data-stu-id="0b661-103">Decoding Signed Data</span></span>

<span data-ttu-id="0b661-104">El siguiente proceso general descodifica un tipo de [*datos con signo*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0b661-104">The following general process decodes a [*signed data*](../secgloss/s-gly.md) type.</span></span>

<span data-ttu-id="0b661-105">**Para descodificar un mensaje firmado**</span><span class="sxs-lookup"><span data-stu-id="0b661-105">**To decode a signed message**</span></span>

1.  <span data-ttu-id="0b661-106">Obtiene un puntero al objeto binario codificado.</span><span class="sxs-lookup"><span data-stu-id="0b661-106">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="0b661-107">Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios.</span><span class="sxs-lookup"><span data-stu-id="0b661-107">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="0b661-108">Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se van a descodificar.</span><span class="sxs-lookup"><span data-stu-id="0b661-108">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="0b661-109">Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b661-109">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="0b661-110">Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 2 y los tipos de parámetro adecuados para tener acceso a los datos descodificados.</span><span class="sxs-lookup"><span data-stu-id="0b661-110">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and the appropriate parameter types to access the decoded data.</span></span> <span data-ttu-id="0b661-111">Por ejemplo, pase \_ el parámetro de contenido CMSG \_ para obtener un puntero al contenido descodificado.</span><span class="sxs-lookup"><span data-stu-id="0b661-111">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="0b661-112">En el siguiente proceso general se comprueba la firma de un mensaje con firma descodificado.</span><span class="sxs-lookup"><span data-stu-id="0b661-112">The following general process verifies the signature of a decoded, signed message.</span></span>

<span data-ttu-id="0b661-113">**Para comprobar la firma de un mensaje descodificado firmado**</span><span class="sxs-lookup"><span data-stu-id="0b661-113">**To verify the signature of a decoded, signed message**</span></span>

1.  <span data-ttu-id="0b661-114">Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el parámetro de información del certificado del firmante CMSG y el identificador de mensaje \_ \_ \_ \_ para obtener [**la \_ información del certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmante del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b661-114">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the message handle and CMSG\_SIGNER\_CERT\_INFO\_PARAM to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the message.</span></span>
2.  <span data-ttu-id="0b661-115">Llame a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir un almacén temporal que se inicializa con los certificados del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b661-115">Call [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open a temporary store that is initialized with the certificates from the message.</span></span>
3.  <span data-ttu-id="0b661-116">Llame a [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) para obtener la información del [**certificado \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmante de los certificados incluidos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b661-116">Call [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the certificates included in the message.</span></span>
4.  <span data-ttu-id="0b661-117">Llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), pasando CMSG \_ Ctrl \_ Verify \_ Signature para comprobar las firmas.</span><span class="sxs-lookup"><span data-stu-id="0b661-117">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_SIGNATURE to verify the signatures.</span></span>
5.  <span data-ttu-id="0b661-118">Llame a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b661-118">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="0b661-119">El resultado de estos procedimientos es que se comprueba la firma y se recupera un puntero al contenido del mensaje descodificado obtenido en el paso 4 del procedimiento para descodificar un mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="0b661-119">The result of these procedures is that the signature is verified and a pointer is retrieved to the decoded message content obtained in step 4 of the procedure for decoding a signed message.</span></span>

<span data-ttu-id="0b661-120">Para obtener información detallada sobre la codificación en C, vea [ejemplo de programa c: firma, codificación, descodificación y comprobación de un mensaje](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="0b661-120">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
