---
description: Las funciones CertAddCertificateLinkToStore, CertAddCRLLinkToStore y CertAddCTLLinkToStore agregan vínculos a contextos existentes en almacenes de certificados en lugar de agregar copias de esos contextos.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Vínculos de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e73c67acd9aaba8efe21bba829b59b5cad9803beacf146a765636c0d65c0ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127005"
---
# <a name="certificate-links"></a>Vínculos de certificado

Las funciones [**CertAddCertificateLinkToStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore) [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)y [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) agregan [](../secgloss/c-gly.md) vínculos a contextos existentes en almacenes de certificados en lugar de agregar copias de esos contextos. Agregar vínculos a almacenes hace que el mismo [*certificado*](../secgloss/c-gly.md)físico, [*CRL*](../secgloss/c-gly.md)o [*CTL*](../secgloss/c-gly.md) esté disponible a través de varios almacenes diferentes. Los cambios realizados en [](../secgloss/c-gly.md) las propiedades extendidas de un contexto desde el almacén del contexto original, o desde un almacén donde se almacena un vínculo a ese contexto, están disponibles en el almacén que contiene el contexto original y en todos los demás almacenes que tienen vínculos a ese contexto.

Para obtener un ejemplo en el que se [**usa CertAddCertificateLinkToStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)vea Programa C de [ejemplo: Operaciones de almacén de certificados](example-c-program-certificate-store-operations.md).

![vínculos de certificado](images/mancert1.png)

Suponga que los certificados A.1, A.2, A.3 y A.4 se encuentran originalmente en el almacén A, y que los certificados B.1, B.2, B.3 y B.4 están originalmente en el almacén B.

-   El diagrama muestra un vínculo agregado en el almacén B al certificado A.2 y un vínculo agregado en el almacén A al certificado B.2.
-   El original del certificado A.2 todavía está en el almacén A. El original de B.2 todavía está en la tienda B.
-   Los cambios realizados en las propiedades extendidas del certificado A.2 o del certificado B.2 del almacén A o del almacén B estarán disponibles para ambos almacenes.
-   Si se ha realizado y almacenado una copia del certificado A.3 en el almacén B, los cambios realizados en las propiedades extendidas del certificado A.3 original del almacén A no estarán visibles en la nueva copia del almacén B. Si se realizaron cambios en las propiedades extendidas de la copia del certificado A.3 en el almacén B, esos cambios no afectarían al contenido del certificado A.3 original y no serían visibles desde el almacén A.

 

 
