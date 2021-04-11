---
description: Las funciones CertAddCertificateLinkToStore, CertAddCRLLinkToStore y CertAddCTLLinkToStore agregan vínculos a los contextos existentes en los almacenes de certificados en lugar de agregar copias de esos contextos.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Vínculos de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156292"
---
# <a name="certificate-links"></a>Vínculos de certificado

Las funciones [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)y [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) agregan vínculos a los contextos existentes en los [*almacenes de certificados*](../secgloss/c-gly.md) en lugar de agregar copias de esos contextos. La adición de vínculos a almacenes hace que el mismo [*certificado*](../secgloss/c-gly.md)físico, [*CRL*](../secgloss/c-gly.md)o [*CTL*](../secgloss/c-gly.md) esté disponible a través de varios almacenes diferentes. Los cambios realizados en las propiedades extendidas de un [*contexto*](../secgloss/c-gly.md) desde el almacén del contexto original, o desde un almacén donde se almacena un vínculo a ese contexto, están disponibles en el almacén que contiene el contexto original y en todos los demás almacenes que tienen vínculos a ese contexto.

Para obtener un ejemplo en el que se usa [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), vea [programa C del ejemplo: operaciones del almacén de certificados](example-c-program-certificate-store-operations.md).

![vínculos de certificado](images/mancert1.png)

Suponga que los certificados A. 1, A. 2, A. 3 y A. 4 se encuentran originalmente en el almacén A, y los certificados B. 1, b. 2, B. 3 y B. 4 se encuentran originalmente en la tienda B.

-   En el diagrama se muestra un vínculo agregado en la tienda B al certificado A. 2 y un vínculo agregado en el almacén a al certificado B. 2.
-   El original del certificado A. 2 todavía está en el almacén A. El original de B. 2 todavía está en la tienda B.
-   Cualquier cambio realizado en las propiedades extendidas del certificado A. 2 o del certificado B. 2 de la tienda A o B estará disponible en ambas tiendas.
-   Si se realizó una copia del certificado A. 3 y se almacenó en el almacén B, los cambios que se realicen en las propiedades extendidas del certificado. 3 original creado en el almacén A no estarán visibles en la nueva copia del almacén B. Si se realizaron cambios en las propiedades extendidas de la copia del certificado A. 3 en la tienda B, esos cambios no afectarán al contenido del certificado A. 3 original y no se verán desde el almacén A.

 

 
