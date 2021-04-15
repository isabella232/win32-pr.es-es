---
description: Una cadena de certificados es una colección jerárquica de certificados que conduce desde el usuario final o el equipo a una raíz de confianza, normalmente la entidad de certificación (CA) raíz de una organización.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Cadena de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669907"
---
# <a name="certificate-chain"></a>Cadena de certificados

Una cadena de certificados es una colección jerárquica de certificados que conduce desde el usuario final o el equipo a una raíz de confianza, normalmente la entidad de certificación (CA) raíz de una organización. Dado que todas las partes presuponen la confianza del certificado raíz, una entidad puede obtener confianza en un certificado de entidad final comprobando la cadena de certificados. Normalmente, la comprobación requiere el establecimiento de que cada certificado de la cadena:

-   Está firmado por la clave pública del certificado anterior.
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

 

 



