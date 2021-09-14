---
title: Establecer propiedades para objetos animados o en movimiento
description: Para los controles de animación, como el control de animación que se muestra al copiar archivos, use el rol de objeto ROLE \_ SYSTEM \_ ANIMATION.
ms.assetid: 8c5ebbc3-4066-452b-8f37-2fb595adea53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1551899305968471bf1425b5cc043be8329c2bd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070630"
---
# <a name="setting-properties-for-animated-or-moving-objects"></a>Establecer propiedades para objetos animados o en movimiento

Para los controles de animación, como el control de animación que se muestra al copiar archivos, use el rol de objeto [**ROLE \_ SYSTEM \_ ANIMATION.**](object-roles.md) Para los gráficos que se animan en ocasiones, use el rol de objeto [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md) con [**el**](state-property.md) estado establecido en STATE [**SYSTEM \_ \_ ANIMATED**](object-state-constants.md).

Use la [**marca STATE \_ SYSTEM \_ ANIMATED**](object-state-constants.md) para marcar un objeto cuya apariencia cambia rápidamente. Los clientes usan esta marca para evitar notificar repetidamente a los usuarios lo que realmente es una serie única de cambios visuales.

Un ejemplo de esto es el texto de marquesina, que se revela progresivamente a medida que se desplaza por la pantalla. Estos objetos reciben el atributo [**de STATE \_ SYSTEM \_ ANIMATED.**](object-state-constants.md) En la mayoría de los casos, la cadena [**Value**](value-property.md) del objeto refleja todo el texto, incluso la parte no visible actualmente. No se **recomienda** cambiar la cadena Value con frecuencia para que se corresponda con el texto actualmente visible porque da como resultado demasiados eventos [**EVENT OBJECT \_ \_ VALUECHANGE**](event-constants.md) que no transmiten información útil.

Por ejemplo, en una ventana que contiene una región rectangular que muestra la palabra "Sí". al moverse en un [](role-property.md) patrón de figura ocho, el rol es [**ROLE \_ SYSTEM \_ GRAPHIC,**](object-roles.md)la propiedad [**Value**](value-property.md) es la cadena mostrada, la propiedad [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) es el rectángulo delimitador alrededor del texto y se establece la marca de atributo STATE [**SYSTEM \_ \_ ANIMATED.**](object-state-constants.md) La [**descripción**](description-property.md) es "The word 'Yes!' (La palabra 'Sí!' se mueve por la pantalla en un patrón de figura ocho". El servidor solo genera eventos [**EVENT \_ OBJECT \_ STATECHANGE**](event-constants.md) cuando el objeto inicia o deja de animación.

 

 




