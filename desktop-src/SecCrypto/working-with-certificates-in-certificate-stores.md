---
description: Varias funciones agregan un contexto de certificado o un vínculo a un contexto a un \[ Kit de desarrollo de software (SDK) de plataforma de almacén \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Trabajar con certificados en almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361131"
---
# <a name="working-with-certificates-in-certificate-stores"></a>Trabajar con certificados en almacenes de certificados

Varias funciones agregan un contexto de certificado o un vínculo a un contexto de un almacén.

Para certificados que ya están en forma de contexto de certificado:

-   [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [**CertAddCRLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [**CertAddCTLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

Para los certificados que están en forma codificada pero no con contextos de certificado completos:

-   [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

Las siguientes funciones eliminan un certificado, una CRL o una CTL de un almacén mediante la reducción de su recuento de referencias en uno. Si esto hace que el recuento de referencias sea cero, se libera la memoria usada para almacenar el certificado, la CRL o la CTL.

-   [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



