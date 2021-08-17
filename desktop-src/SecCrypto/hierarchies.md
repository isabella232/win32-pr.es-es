---
description: Servicios de certificados admite jerarquías de entidad de certificación (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Jerarquías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240f2f2fc2920db1a67adb18281ad5c1d67fabdb2996ae3aae8342f96b1810c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006303"
---
# <a name="hierarchies"></a>Jerarquías

Servicios de certificados [*admite jerarquías*](../secgloss/c-gly.md) de entidad de certificación (CA). Una [*jerarquía de CA*](../secgloss/c-gly.md) consta de una CA de nivel superior (denominada CA raíz) con una o varias CA subordinadas que la CA raíz ha emitido certificados. Un posible escenario de jerarquía de CA estaría en una organización con una CA raíz, que se usó para emitir certificados a varias CA subordinadas. A continuación, las CA subordinadas pueden emitir certificados de entidad final, como certificados emitidos a un usuario. El certificado del usuario contendrá una ruta de acceso de confianza para la jerarquía de ca, en este caso, incluido el certificado tanto para la CA subordinada emisora como para la ca raíz.

 

 
