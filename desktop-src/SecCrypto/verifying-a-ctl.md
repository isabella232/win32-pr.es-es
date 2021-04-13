---
description: Para que un interloper sea más difícil de sustituir una lista de certificados de confianza (CTL) ficticia de una existente, Compruebe la firma en la CTL cada vez que se use la CTL.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Comprobar una CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543510"
---
# <a name="verifying-a-ctl"></a><span data-ttu-id="da975-103">Comprobar una CTL</span><span class="sxs-lookup"><span data-stu-id="da975-103">Verifying a CTL</span></span>

<span data-ttu-id="da975-104">Para que un interloper sea más difícil de sustituir una lista de [*certificados de confianza*](../secgloss/c-gly.md) (CTL) ficticia de una existente, Compruebe la firma en la CTL cada vez que se use la CTL.</span><span class="sxs-lookup"><span data-stu-id="da975-104">To make it more difficult for an interloper to substitute a bogus [*certificate trust list*](../secgloss/c-gly.md) (CTL) for an existing one, verify the signature on the CTL each time the CTL is used.</span></span> <span data-ttu-id="da975-105">No use una CTL que no contenga una firma de confianza.</span><span class="sxs-lookup"><span data-stu-id="da975-105">Do not use a CTL that does not contain a trusted signature.</span></span>

<span data-ttu-id="da975-106">**Para comprobar una firma de CTL**</span><span class="sxs-lookup"><span data-stu-id="da975-106">**To verify a CTL signature**</span></span>

1.  <span data-ttu-id="da975-107">Abra el [*almacén de certificados*](../secgloss/c-gly.md) que contiene la CTL deseada.</span><span class="sxs-lookup"><span data-stu-id="da975-107">Open the [*certificate store*](../secgloss/c-gly.md) containing the desired CTL.</span></span>
2.  <span data-ttu-id="da975-108">Obtiene un identificador de un [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) para la CTL.</span><span class="sxs-lookup"><span data-stu-id="da975-108">Get a handle to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) for the CTL.</span></span> <span data-ttu-id="da975-109">Para ello, puede llamar a cualquiera de las funciones que devuelven un identificador **al \_ contexto CTL**, como [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="da975-109">This can be done by calling any of the functions that return a handle to the **CTL\_CONTEXT**, such as [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
3.  <span data-ttu-id="da975-110">Llame a [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), pasando [**el \_ contexto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) recuperado en el paso 2 en el parámetro *hCryptMsg* , un identificador para el almacén de certificados que contiene el certificado de la fuente de confianza para las CTL en el parámetro *rghSignerStore* y la \_ marca CMSG Trusted \_ Signer \_ en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="da975-110">Call [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) retrieved in step 2 in the *hCryptMsg* parameter, a handle to the certificate store containing the certificate of the trusted source for CTLs in the *rghSignerStore* parameter, and the CMSG\_TRUSTED\_SIGNER\_FLAG in the *dwFlags* parameter.</span></span> <span data-ttu-id="da975-111">Si la función devuelve **true**, se comprobó la firma y se devuelve un puntero al [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmante CTL en el parámetro *ppSigner* .</span><span class="sxs-lookup"><span data-stu-id="da975-111">If the function returns **TRUE**, the signature was verified, and a pointer to the CTL signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

 

 
