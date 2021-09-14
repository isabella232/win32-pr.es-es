---
description: Una cadena de certificados es una colección jerárquida de certificados que conduce desde el usuario final o el equipo a una raíz de confianza, normalmente la entidad de certificación raíz (CA) de una organización.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Cadena de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173362"
---
# <a name="certificate-chain"></a>Cadena de certificados

Una cadena de certificados es una colección jerárquida de certificados que conduce desde el usuario final o el equipo a una raíz de confianza, normalmente la entidad de certificación raíz (CA) de una organización. Dado que todas las partes presumiblemente confían en el certificado raíz, una entidad puede obtener confianza en un certificado de entidad final comprobando la cadena de certificados. La comprobación normalmente requiere establecer que cada certificado de la cadena:

-   Está firmado por la clave pública en el certificado anterior.
-   No ha expirado.
-   No se ha revocado.
-   Se ajusta a las directivas especificadas por los certificados anteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Jerarquía de certificados](about-certificate-hierarchy.md)
</dt> <dt>

[Certificación cruzada](about-cross-certification.md)
</dt> <dt>

[Modelos de confianza](about-trust-models.md)
</dt> </dl>

 

 



