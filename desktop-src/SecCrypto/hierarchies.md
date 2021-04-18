---
description: Los servicios de Certificate Server admiten jerarquías de entidades de certificación (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Jerarquías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668207"
---
# <a name="hierarchies"></a>Jerarquías

Los servicios de Certificate Server admiten jerarquías de [*entidades de certificación*](../secgloss/c-gly.md) (CA). Una [*jerarquía de entidad de certificación*](../secgloss/c-gly.md) consta de una entidad de certificación de nivel superior (denominada entidad de certificación raíz) con una o más CA subordinadas que la CA raíz ha emitido certificados. Un posible escenario de jerarquía de CA sería en una organización con una CA raíz que se usaba para emitir certificados a varias CA subordinadas. A continuación, las CA subordinadas pueden emitir certificados de entidad final, como los certificados emitidos para un usuario. El certificado del usuario contendrá una ruta de acceso de confianza para la jerarquía de la entidad de certificación, en este caso, incluido el certificado para la CA subordinada emisora y la CA raíz.

 

 
