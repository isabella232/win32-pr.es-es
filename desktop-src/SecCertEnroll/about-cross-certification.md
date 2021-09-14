---
description: La certificación cruzada permite que las entidades de una infraestructura de clave pública (PKI) confíen en las entidades de otra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificación cruzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160761"
---
# <a name="cross-certification"></a>Certificación cruzada

La certificación cruzada permite que las entidades de una infraestructura de clave pública (PKI) confíen en las entidades de otra PKI. Esta relación de confianza mutua suele ser compatible con un contrato de certificación cruzada entre las entidades de certificación (CA) de cada PKI. El contrato establece las responsabilidades y responsabilidades de cada parte.

Una relación de confianza mutua entre dos CA requiere que cada ca emita un certificado a la otra para establecer la relación en ambas direcciones. La ruta de acceso de confianza no es jerárquica (ninguna de las CA de control está subordinada a la otra), aunque los PKI independientes pueden ser jerarquías de certificados. Una vez que dos CA han establecido y especificado los términos de confianza y emitidos certificados entre sí, las entidades dentro de los PKI independientes pueden interactuar sujeto a las directivas especificadas en los certificados.

![diagrama de certificación cruzada](images/cross-certification.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de confianza](about-trust-models.md)
</dt> </dl>

 

 



