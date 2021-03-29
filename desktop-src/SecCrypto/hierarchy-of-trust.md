---
description: La confiabilidad de un certificado digital se establece mediante una jerarquía de confianza.
ms.assetid: 13ee08b4-9c8e-480b-b78d-9472a2d7b566
title: Jerarquía de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485c721493a93c7ea55b1993345e8168ccab319b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912025"
---
# <a name="hierarchy-of-trust"></a>Jerarquía de confianza

Para que los [*certificados digitales*](../secgloss/c-gly.md) sean efectivos, los usuarios de certificados deben tener un alto nivel de confianza en ellos. Hay casos en los que un usuario no confía en el emisor de un certificado. Esto podría ocurrir si el usuario del certificado nunca ha oído hablar de la [*entidad de certificación*](../secgloss/c-gly.md) y, por lo tanto, no se siente incómodo al aceptar un certificado de ese emisor en el valor de la superficie. Este problema se soluciona en el proceso de certificación mediante una jerarquía de confianza.

Una jerarquía de confianza comienza con al menos una entidad de certificación que sea de confianza para todas las entidades de la cadena de certificados. Puede ser un administrador de entidad de certificación interno o una empresa u organización externa especializada en la comprobación de identidades y la emisión de certificados. Esta autoridad se denomina [*entidad de certificación raíz*](../secgloss/r-gly.md). La entidad emisora raíz certifica entonces a otras entidades de certificación, denominadas entidades de certificación de primer nivel, que pueden emitir certificados y también certifican entidades de certificación adicionales o de segundo nivel. Esta situación se muestra en la siguiente ilustración.

![jerarquía de confianza](images/trust.png)

La identidad de la entidad de certificación que emite un certificado forma parte de un certificado. Esa entidad de certificación se denomina emisor del certificado. Cuando el emisor de un certificado es una entidad de certificación de nivel 1 o nivel 2, el receptor de ese certificado puede determinar si el emisor del certificado está certificado como una entidad de certificación válida por una entidad de certificación en un nivel superior, y que la entidad de certificación de nivel superior está certificada como entidad de certificación válida a través de una entidad de certificación de nivel superior hasta que se determina que existe una cadena de confianza entre la entidad de certificación de nivel más bajo y la raíz entidad de certificación.

Por ejemplo, en la ilustración anterior, se puede comprobar que la CA \# 4 se ha certificado como entidad de certificación por CA \# 1 y que \# la CA raíz ha certificado la CA 1 como entidad de certificación. Por lo tanto, cuando se pasa un certificado de una entidad de certificación de nivel inferior junto con el mensaje cifrado, la información sobre todos los certificados de su cadena de confianza hasta la raíz se pasa junto con él.

La ilustración y la descripción que se acaban de presentar son conceptuales. En el mundo real, la situación de la entidad de certificación está evolucionando y no se ha establecido o aceptado ninguna entidad raíz única. A corto plazo, se desarrollarán islas de autoridad tal como se muestra en la siguiente ilustración.

![Islas de autoridad en una jerarquía de confianza](images/trust2.png)

En el tiempo, las islas raíz 1 y raíz 2 de la ilustración se pueden convertir en entidades de certificación de nivel 1 a una CA raíz única. En ese momento, la situación tendría que volver a tener una entidad raíz única. Sigue apareciendo cómo evolucionará la imagen real.

 

 
