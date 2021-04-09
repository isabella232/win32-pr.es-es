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
# <a name="certificate-extended-properties"></a>Propiedades extendidas del certificado

Los datos de un [*certificado*](../secgloss/c-gly.md), una [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL) o un [*contexto*](../secgloss/c-gly.md)de lista de [*certificados de confianza*](../secgloss/c-gly.md) (CTL), incluidas las extensiones, son de solo lectura y no se pueden cambiar. Sin embargo, en las plataformas de Microsoft, los certificados CryptoAPI también tienen propiedades extendidas dinámicas que se pueden agregar y cambiar.

> [!Note]  
> Las propiedades extendidas están asociadas a un certificado y no forman parte de un certificado emitido por una [*entidad de certificación*](../secgloss/c-gly.md) (CA). Las propiedades extendidas no están disponibles en un certificado cuando se usa en una plataforma que no es de Microsoft.

 

Estas propiedades incluyen datos que:

-   Pertenece a la clave privada que se va a usar con el certificado.
-   Indica el tipo de hash que se va a realizar en el certificado.
-   Proporciona información definida por el usuario asociada al certificado.

En las plataformas de Microsoft, los valores de estas propiedades se adjuntan y se mueven con el certificado. Actualmente, las propiedades predefinidas identificadas con identificadores de propiedad incluyen las siguientes propiedades:

-   Estas propiedades unen un certificado a un CSP determinado y, dentro de ese CSP, a una clave privada determinada:
    -   \_identificador de \_ \_ prop de \_ identificador \_ de la clave de certificado
    -   \_ \_ \_ \_ \_ ID. de prop de clave de certificado
    -   \_ \_ \_ ID. de prop de contexto de clave de certificado \_
-   Estas propiedades indican el algoritmo hash que se utilizará cuando se realice una operación de hash:
    -   \_Identificador de \_ \_ prop hash SHA1 del \_ certificado
    -   \_Identificador de \_ \_ prop hash \_ de certificado MD5

Para obtener una lista completa de las propiedades de certificado extendido definidas actualmente y las descripciones del significado y el uso de cada propiedad, vea [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

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

 

 
