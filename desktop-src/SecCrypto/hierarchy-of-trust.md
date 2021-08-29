---
description: La confiabilidad de un certificado digital se establece mediante una jerarquía de confianza.
ms.assetid: 13ee08b4-9c8e-480b-b78d-9472a2d7b566
title: Jerarquía de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67955c9dc94c09cf391f58375ae00f74a1584d536ad299bb2f5d1335dd1aeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006247"
---
# <a name="hierarchy-of-trust"></a>Jerarquía de confianza

Para [*que los certificados digitales*](../secgloss/c-gly.md) sean eficaces, los usuarios de certificados deben tener un alto nivel de confianza en ellos. Hay casos en los que un usuario no confía en el emisor de un certificado. Esto podría ocurrir si el usuario [](../secgloss/c-gly.md) del certificado nunca ha oído hablar de la entidad de certificación y, por lo tanto, no está cómodo con la aceptación de un certificado de ese emisor en el valor de face. Este problema se aborda en el proceso de certificación mediante una jerarquía de confianza.

Una jerarquía de confianza comienza con al menos una entidad de certificación de confianza para todas las entidades de la cadena de certificados. Puede ser un administrador de entidad de certificación interno o una empresa u organización externa especializada en comprobar las identidades y emitir certificados. Esta autoridad se denomina la [*entidad de certificación raíz*](../secgloss/r-gly.md). A continuación, la entidad de certificación raíz certifica otras entidades de certificación, denominadas entidades de certificación de primer nivel, que luego pueden emitir certificados y también certificar entidades de certificación adicionales o de segundo nivel. Esta situación se muestra en la ilustración siguiente.

![jerarquía de confianza](images/trust.png)

La identidad de la entidad de certificación que emite un certificado forma parte de un certificado. Esa entidad de certificación se denomina emisor del certificado. Cuando el emisor de un certificado es una entidad de certificación de nivel 1 o nivel 2, el receptor de ese certificado puede determinar si el emisor del certificado está certificado como una entidad de certificación válida por una entidad de certificación en un nivel por encima de él y que la entidad de certificación de nivel superior está certificada como entidad de certificación válida por una entidad de certificación de nivel superior hasta que se determine que existe una cadena de confianza entre el nivel más bajo. la entidad de certificación y la entidad de certificación raíz.

Por ejemplo, en la ilustración anterior, se puede comprobar que ca 4 se certificó como entidad de certificación por ca 1 y que ca 1 se certificó como entidad de certificación por la CA \# \# \# raíz. Por lo tanto, cuando se pasa un certificado de una entidad de certificación de nivel inferior junto con el mensaje cifrado, se pasa junto con él información sobre todos los certificados de su cadena de confianza hasta la raíz.

La ilustración y la descripción que se acaba de presentar son conceptuales. En el mundo real, la situación de la entidad de certificación está evolucionando y no se ha establecido ni aceptado ninguna entidad raíz única. A corto plazo, las islas de autoridad se desarrollarán como se muestra en la ilustración siguiente.

![islas de autoridad en una jerarquía de confianza](images/trust2.png)

Con el tiempo, las islas raíz, raíz 1 y raíz 2 de la ilustración, podrían convertirse en CA de nivel 1 en una sola CA raíz. En ese momento, la situación tendría de nuevo una única autoridad raíz. Queda por ver cómo evolucionará la imagen real.

 

 
