---
description: Las siguientes interfaces se pueden usar para administrar firmas de certificados y claves públicas y privadas.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Firma de certificado e interfaces clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911289"
---
# <a name="certificate-signature-and-key-interfaces"></a><span data-ttu-id="63ca2-103">Firma de certificado e interfaces clave</span><span class="sxs-lookup"><span data-stu-id="63ca2-103">Certificate Signature and Key Interfaces</span></span>

<span data-ttu-id="63ca2-104">Las siguientes interfaces se pueden usar para administrar firmas de certificados y claves públicas y privadas.</span><span class="sxs-lookup"><span data-stu-id="63ca2-104">The following interfaces can be used to manage certificate signatures, and public and private keys.</span></span>



| <span data-ttu-id="63ca2-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="63ca2-105">Interface</span></span>                                                      | <span data-ttu-id="63ca2-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="63ca2-106">Description</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63ca2-107">**ISignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="63ca2-107">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | <span data-ttu-id="63ca2-108">Representa un certificado de firma que le permite firmar una solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="63ca2-108">Represents a signing certificate that enables you to sign a certificate request.</span></span>                  |
| [<span data-ttu-id="63ca2-109">**ISignerCertificates**</span><span class="sxs-lookup"><span data-stu-id="63ca2-109">**ISignerCertificates**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | <span data-ttu-id="63ca2-110">Administra una colección de objetos [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .</span><span class="sxs-lookup"><span data-stu-id="63ca2-110">Manages a collection of [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) objects.</span></span>                 |
| [<span data-ttu-id="63ca2-111">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="63ca2-111">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | <span data-ttu-id="63ca2-112">Representa una clave privada asimétrica que se puede usar para el cifrado, la firma y el acuerdo de claves.</span><span class="sxs-lookup"><span data-stu-id="63ca2-112">Represents an asymmetric private key that can be used for encryption, signing, and key agreement.</span></span> |
| [<span data-ttu-id="63ca2-113">**IX509PublicKey**</span><span class="sxs-lookup"><span data-stu-id="63ca2-113">**IX509PublicKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | <span data-ttu-id="63ca2-114">Representa una clave pública en un par de claves pública y privada.</span><span class="sxs-lookup"><span data-stu-id="63ca2-114">Represents a public key in a public/private key pair.</span></span>                                             |
| [<span data-ttu-id="63ca2-115">**IX509SignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="63ca2-115">**IX509SignatureInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | <span data-ttu-id="63ca2-116">Representa la información utilizada para firmar una solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="63ca2-116">Represents information used to sign a certificate request.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="63ca2-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63ca2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63ca2-118">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="63ca2-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



