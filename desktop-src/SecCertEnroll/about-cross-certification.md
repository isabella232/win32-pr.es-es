---
description: La certificación cruzada permite a las entidades de una infraestructura de clave pública (PKI) confiar en entidades de otra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificación cruzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277966"
---
# <a name="cross-certification"></a>Certificación cruzada

La certificación cruzada permite a las entidades de una infraestructura de clave pública (PKI) confiar en entidades de otra PKI. Esta relación de confianza mutua normalmente es compatible con un acuerdo de certificación cruzada entre las entidades de certificación (CA) de cada PKI. El acuerdo establece las responsabilidades y responsabilidad de cada entidad.

Una relación de confianza mutua entre dos CA requiere que cada CA emita un certificado al otro para establecer la relación en ambas direcciones. La ruta de acceso de confianza no es jerárquica (ninguna de las entidades de certificación de control está subordinada al otro), aunque las PKI independientes pueden ser jerarquías de certificados. Una vez que se han establecido dos CA y se han especificado las condiciones de confianza y los certificados emitidos entre sí, las entidades dentro de PKI independientes pueden interactuar de acuerdo con las directivas especificadas en los certificados.

![diagrama de certificación cruzada](images/cross-certification.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de confianza](about-trust-models.md)
</dt> </dl>

 

 



