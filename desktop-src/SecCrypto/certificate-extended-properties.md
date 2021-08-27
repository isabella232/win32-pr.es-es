---
description: Los datos de un contexto de certificado, lista de revocación de certificados (CRL) o lista de certificados de confianza (CTL), incluidas las extensiones, son de solo lectura y no se pueden cambiar.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Propiedades extendidas del certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37eaf192d4c236a4f12898ece2bded86d467404c5eceedd98f1deb976b8857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127095"
---
# <a name="certificate-extended-properties"></a>Propiedades extendidas del certificado

Los datos de un contexto [*de*](../secgloss/c-gly.md)certificado, lista [*de revocación*](../secgloss/c-gly.md) de certificados (CRL) [](../secgloss/c-gly.md)o lista de confianza de certificados (CTL), incluidas las extensiones, son de solo lectura y no se pueden cambiar. [](../secgloss/c-gly.md) Sin embargo, en las plataformas de Microsoft, los certificados CryptoAPI también tienen propiedades extendidas dinámicas que se pueden agregar y cambiar.

> [!Note]  
> Las propiedades extendidas están asociadas a un certificado y no forman parte de un certificado emitido por una entidad [*de certificación*](../secgloss/c-gly.md) (CA). Las propiedades extendidas no están disponibles en un certificado cuando se usa en una plataforma que no es de Microsoft.

 

Estas propiedades incluyen datos que:

-   Pertenece a la clave privada que se va a usar con el certificado.
-   Indica el tipo de hash que se va a realizar en el certificado.
-   Proporciona información definida por el usuario asociada al certificado.

En las plataformas de Microsoft, los valores de estas propiedades se adjuntan al certificado y se mueven con él. Las propiedades predefinidas actualmente identificadas con los IDs de propiedad incluyen las siguientes propiedades:

-   Estas propiedades vinculan un certificado a un CSP determinado y, dentro de ese CSP, a una clave privada determinada:
    -   IDENTIFICADOR \_ DE PROP DE CERT KEY \_ PROV \_ HANDLE \_ \_
    -   IDENTIFICADOR \_ DE PROP DE LA INFORMACIÓN DE CERT KEY \_ \_ \_ \_ PROV
    -   IDENTIFICADOR DE \_ PROP DE CONTEXTO DE CLAVE DE \_ \_ \_ CERTIFICADO
-   Estas propiedades indican el algoritmo hash que se va a usar cuando se realiza una operación de hash:
    -   ID. \_ DE PROP DE HASH \_ SHA1 DE \_ \_ CERT
    -   ID. \_ DE PROP DE HASH \_ \_ MD5 DE \_ CERT

Para obtener listas completas de propiedades de certificado extendidas definidas actualmente y descripciones del significado y uso de cada propiedad, vea [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
