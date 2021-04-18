---
description: Una de las ventajas de usar listas de certificados de confianza (CTL) es que se pueden diseñar aplicaciones que pueden comprobar automáticamente los mensajes firmados con respecto a los certificados de confianza sin molestar al usuario con cuadros de diálogo.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Comprobar mensajes firmados mediante CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687584"
---
# <a name="verifying-signed-messages-by-using-ctls"></a><span data-ttu-id="f0180-103">Comprobar mensajes firmados mediante CTL</span><span class="sxs-lookup"><span data-stu-id="f0180-103">Verifying Signed Messages by Using CTLs</span></span>

<span data-ttu-id="f0180-104">Una de las ventajas de usar [*listas de certificados de confianza*](../secgloss/c-gly.md) (CTL) es que se pueden diseñar aplicaciones que pueden comprobar automáticamente los mensajes firmados con respecto a los certificados de confianza sin molestar al usuario con cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f0180-104">One of the advantages of using [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) is that applications can be designed that can automatically verify signed messages against trusted certificates without bothering the user with dialog boxes.</span></span> <span data-ttu-id="f0180-105">También proporciona a un administrador de red orígenes de control de confianza.</span><span class="sxs-lookup"><span data-stu-id="f0180-105">It also gives a network administrator control sources to be trusted.</span></span>

<span data-ttu-id="f0180-106">El siguiente procedimiento se puede usar para comprobar la firma de un mensaje firmado mediante una CTL.</span><span class="sxs-lookup"><span data-stu-id="f0180-106">The following procedure can be used to verify the signature of a signed message by using a CTL.</span></span>

<span data-ttu-id="f0180-107">**Para comprobar un mensaje firmado mediante una CTL**</span><span class="sxs-lookup"><span data-stu-id="f0180-107">**To verify a signed message by using a CTL**</span></span>

1.  <span data-ttu-id="f0180-108">Descodifique el mensaje de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="f0180-108">Decode the message as follows:</span></span>

    1.  <span data-ttu-id="f0180-109">Obtiene un puntero al mensaje recibido (el [*BLOB*](../secgloss/b-gly.md)codificado).</span><span class="sxs-lookup"><span data-stu-id="f0180-109">Get a pointer to the received message (the encoded [*BLOB*](../secgloss/b-gly.md)).</span></span>
    2.  <span data-ttu-id="f0180-110">Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios.</span><span class="sxs-lookup"><span data-stu-id="f0180-110">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
    3.  <span data-ttu-id="f0180-111">Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso b y un puntero a los datos que se van a descodificar.</span><span class="sxs-lookup"><span data-stu-id="f0180-111">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step b and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="f0180-112">Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f0180-112">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>

2.  <span data-ttu-id="f0180-113">Compruebe la firma del mensaje descodificado y firmado y obtenga un puntero al [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)del firmante.</span><span class="sxs-lookup"><span data-stu-id="f0180-113">Verify the signature of the decoded, signed message, and get a pointer to the signer's [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

    <span data-ttu-id="f0180-114">Esto se puede hacer llamando a [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), pasando el identificador de mensaje recuperado en el paso 1C como el parámetro *hCryptMsg* .</span><span class="sxs-lookup"><span data-stu-id="f0180-114">This can be done by calling [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the message handle retrieved in step 1c as the *hCryptMsg* parameter.</span></span> <span data-ttu-id="f0180-115">Si la llamada a la función devuelve **true**, se comprobó la firma y se devuelve un puntero al [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmante en el parámetro *ppSigner* .</span><span class="sxs-lookup"><span data-stu-id="f0180-115">If the function call returns **TRUE**, the signature was verified, and a pointer to the signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

3.  <span data-ttu-id="f0180-116">Confirme que el firmante es una fuente de confianza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f0180-116">Confirm that the signer is a trusted source as follows:</span></span>

    1.  <span data-ttu-id="f0180-117">Abra el almacén de certificados que contiene la CTL adecuada.</span><span class="sxs-lookup"><span data-stu-id="f0180-117">Open the certificate store containing the appropriate CTL.</span></span>
    2.  <span data-ttu-id="f0180-118">Obtiene un puntero al [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) llamando a [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="f0180-118">Get a pointer to the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) by calling [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
    3.  <span data-ttu-id="f0180-119">Para confirmar que el firmante es un origen de confianza, llame a [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), pasando el puntero recuperado en el paso anterior en el parámetro *pCtlContext* , el \_ \_ \_ tipo de sujeto de certificado de CTL en el parámetro *dwSubjectType* y el puntero al [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) recuperado en el paso 2 en el parámetro *pvSubject* .</span><span class="sxs-lookup"><span data-stu-id="f0180-119">To confirm that the signer is a trusted source, call [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passing the pointer retrieved in the previous step in the *pCtlContext* parameter, CTL\_CERT\_SUBJECT\_TYPE in the *dwSubjectType* parameter, and the pointer to the [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) retrieved in step 2 in the *pvSubject* parameter.</span></span> <span data-ttu-id="f0180-120">Si la llamada de función devuelve **true**, **el \_ contexto de certificado** que se pasa a la función es un origen de confianza en la CTL.</span><span class="sxs-lookup"><span data-stu-id="f0180-120">If the function call returns **TRUE**, the **CERT\_CONTEXT** passed to the function is a trusted source in the CTL.</span></span>

 

 
