---
description: Los datos de un certificado, una lista de revocación de certificados (CRL) o un contexto de lista de certificados de confianza (CTL), incluidas las extensiones, son de solo lectura y no se pueden cambiar.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Propiedades extendidas del certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155897"
---
# <a name="certificate-extended-properties"></a><span data-ttu-id="e07c4-103">Propiedades extendidas del certificado</span><span class="sxs-lookup"><span data-stu-id="e07c4-103">Certificate Extended Properties</span></span>

<span data-ttu-id="e07c4-104">Los datos de un [*certificado*](../secgloss/c-gly.md), una [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL) o un [*contexto*](../secgloss/c-gly.md)de lista de [*certificados de confianza*](../secgloss/c-gly.md) (CTL), incluidas las extensiones, son de solo lectura y no se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="e07c4-104">The data in a [*certificate*](../secgloss/c-gly.md), [*certificate revocation list*](../secgloss/c-gly.md) (CRL), or [*certificate trust list*](../secgloss/c-gly.md) (CTL) [*context*](../secgloss/c-gly.md), including any extensions, is read-only and cannot be changed.</span></span> <span data-ttu-id="e07c4-105">Sin embargo, en las plataformas de Microsoft, los certificados CryptoAPI también tienen propiedades extendidas dinámicas que se pueden agregar y cambiar.</span><span class="sxs-lookup"><span data-stu-id="e07c4-105">However, on Microsoft platforms, CryptoAPI certificates also have dynamic extended properties that can be added and changed.</span></span>

> [!Note]  
> <span data-ttu-id="e07c4-106">Las propiedades extendidas están asociadas a un certificado y no forman parte de un certificado emitido por una [*entidad de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="e07c4-106">Extended properties are associated with a certificate and are not part of a certificate as issued by a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span> <span data-ttu-id="e07c4-107">Las propiedades extendidas no están disponibles en un certificado cuando se usa en una plataforma que no es de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e07c4-107">Extended properties are not available on a certificate when it is used on a non-Microsoft platform.</span></span>

 

<span data-ttu-id="e07c4-108">Estas propiedades incluyen datos que:</span><span class="sxs-lookup"><span data-stu-id="e07c4-108">These properties include data that:</span></span>

-   <span data-ttu-id="e07c4-109">Pertenece a la clave privada que se va a usar con el certificado.</span><span class="sxs-lookup"><span data-stu-id="e07c4-109">Pertains to the private key to be used with the certificate.</span></span>
-   <span data-ttu-id="e07c4-110">Indica el tipo de hash que se va a realizar en el certificado.</span><span class="sxs-lookup"><span data-stu-id="e07c4-110">Indicates the type of hashes to be performed on the certificate.</span></span>
-   <span data-ttu-id="e07c4-111">Proporciona información definida por el usuario asociada al certificado.</span><span class="sxs-lookup"><span data-stu-id="e07c4-111">Provides user-defined information associated with the certificate.</span></span>

<span data-ttu-id="e07c4-112">En las plataformas de Microsoft, los valores de estas propiedades se adjuntan y se mueven con el certificado.</span><span class="sxs-lookup"><span data-stu-id="e07c4-112">On Microsoft platforms, values for these properties are attached to and move with the certificate.</span></span> <span data-ttu-id="e07c4-113">Actualmente, las propiedades predefinidas identificadas con identificadores de propiedad incluyen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="e07c4-113">Currently predefined properties identified with property IDs include the following properties:</span></span>

-   <span data-ttu-id="e07c4-114">Estas propiedades unen un certificado a un CSP determinado y, dentro de ese CSP, a una clave privada determinada:</span><span class="sxs-lookup"><span data-stu-id="e07c4-114">These properties tie a certificate to a particular CSP and, within that CSP, to a particular private key:</span></span>
    -   <span data-ttu-id="e07c4-115">\_identificador de \_ \_ prop de \_ identificador \_ de la clave de certificado</span><span class="sxs-lookup"><span data-stu-id="e07c4-115">CERT\_KEY\_PROV\_HANDLE\_PROP\_ID</span></span>
    -   <span data-ttu-id="e07c4-116">\_ \_ \_ \_ \_ ID. de prop de clave de certificado</span><span class="sxs-lookup"><span data-stu-id="e07c4-116">CERT\_KEY\_PROV\_INFO\_PROP\_ID</span></span>
    -   <span data-ttu-id="e07c4-117">\_ \_ \_ ID. de prop de contexto de clave de certificado \_</span><span class="sxs-lookup"><span data-stu-id="e07c4-117">CERT\_KEY\_CONTEXT\_PROP\_ID</span></span>
-   <span data-ttu-id="e07c4-118">Estas propiedades indican el algoritmo hash que se utilizará cuando se realice una operación de hash:</span><span class="sxs-lookup"><span data-stu-id="e07c4-118">These properties indicate the hashing algorithm to be used when a hashing operation is performed:</span></span>
    -   <span data-ttu-id="e07c4-119">\_Identificador de \_ \_ prop hash SHA1 del \_ certificado</span><span class="sxs-lookup"><span data-stu-id="e07c4-119">CERT\_SHA1\_HASH\_PROP\_ID</span></span>
    -   <span data-ttu-id="e07c4-120">\_Identificador de \_ \_ prop hash \_ de certificado MD5</span><span class="sxs-lookup"><span data-stu-id="e07c4-120">CERT\_MD5\_HASH\_PROP\_ID</span></span>

<span data-ttu-id="e07c4-121">Para obtener una lista completa de las propiedades de certificado extendido definidas actualmente y las descripciones del significado y el uso de cada propiedad, vea [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span><span class="sxs-lookup"><span data-stu-id="e07c4-121">For complete lists of currently defined extended certificate properties and descriptions of the meaning and use of each property, see [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e07c4-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e07c4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e07c4-123">**CertGetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="e07c4-123">**CertGetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="e07c4-124">**CertGetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="e07c4-124">**CertGetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[<span data-ttu-id="e07c4-125">**CertSetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="e07c4-125">**CertSetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="e07c4-126">**CertSetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="e07c4-126">**CertSetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
