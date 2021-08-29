---
description: Una cadena de certificados es una colección jerárquida de certificados que conduce desde el usuario final o el equipo a una raíz de confianza, normalmente la entidad de certificación raíz (CA) de una organización.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Cadena de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a6227746690468e934475904fcc0bd895d995e2a674b9a4c6e9d01bc792fdba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904864"
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

 

 



