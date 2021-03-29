---
description: CryptoAPI proporciona funciones para trabajar con certificados, listas de revocación de certificados (CRL) y listas de certificados de confianza (CTL).
ms.assetid: 23460329-44ed-4bcb-9727-5c841070f093
title: Operaciones con certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2f9f5d6d541b452741f2e4634752b979f26107
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912014"
---
# <a name="operations-with-certificates"></a>Operaciones con certificados

[*CryptoAPI*](../secgloss/c-gly.md) proporciona funciones para trabajar con [*certificados*](../secgloss/c-gly.md), [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) y [*listas de certificados de confianza*](../secgloss/c-gly.md) (CTL). Incluyen funciones para convertir tipos codificados en tipos de contexto, funciones que duplican objetos y funciones que liberan estos objetos. Estas funciones codifican la información en contextos, pero no agregan este contexto a ningún almacén. Estas funciones son [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)y [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext). Utilice la función CertFree adecuada para liberar los contextos creados por una de estas funciones.

Las funciones de CryptoAPI para duplicar certificados, CRL y CTL incrementan el [*contador de referencias*](../secgloss/r-gly.md) en el contexto especificado y devuelven un puntero al contexto. Las funciones de duplicación no asignan espacio adicional ni copian los datos de un contexto en una nueva ubicación de memoria. Estas funciones son [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext), [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)y [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext). Los contextos creados con cualquiera de estas funciones se deben liberar con la función CertFree adecuada.

Las funciones de CryptoAPI que liberan certificados, CRL y CTL son [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)y [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext). Cada una de estas funciones disminuye el [*recuento de referencias*](../secgloss/r-gly.md) en un contexto. Si el recuento de referencias llega a cero, se libera la memoria asignada para el contexto.

Para obtener listas completas de funciones para trabajar con certificados, CRL y CTL, consulte [funciones de mantenimiento del almacén](cryptography-functions.md)de certificados y certificados, [funciones de certificados](cryptography-functions.md), funciones de [lista de revocación de certificados](cryptography-functions.md)y funciones de lista de certificados de [confianza](cryptography-functions.md).

 

 
