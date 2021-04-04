---
title: Establecer propiedades para objetos animados o en movimiento
description: En el caso de los controles de animación, como el control de animación que se muestra al copiar archivos, use el \_ rol de objeto animación del sistema de roles \_ .
ms.assetid: 8c5ebbc3-4066-452b-8f37-2fb595adea53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1551899305968471bf1425b5cc043be8329c2bd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076183"
---
# <a name="setting-properties-for-animated-or-moving-objects"></a>Establecer propiedades para objetos animados o en movimiento

En el caso de los controles de animación, como el control de animación que se muestra al copiar archivos, use el rol de objeto [**\_ \_ animación del sistema de roles**](object-roles.md) . En el caso de los gráficos que se animan ocasionalmente, use el rol de objeto de [**\_ \_ gráfico sistema de roles**](object-roles.md) con el [**Estado**](state-property.md) establecido en [**estado \_ \_ animado del sistema**](object-state-constants.md).

Use la [**marca \_ \_ animada del sistema de estado**](object-state-constants.md) para marcar un objeto cuya apariencia cambia rápidamente. Los clientes usan esta marca para evitar que los usuarios notifiquen repetidamente lo que realmente es una serie de cambios visuales.

Un ejemplo de esto es el texto de marquesina, que se revela progresivamente a medida que se desplaza por la pantalla. Estos objetos reciben el atributo de [**Estado de \_ sistema \_ animado**](object-state-constants.md). En la mayoría de los casos, la cadena de [**valor**](value-property.md) del objeto refleja todo el texto, incluso la parte no visible actualmente. No se recomienda cambiar la cadena de **valor** con frecuencia para que se corresponda con el texto actualmente visible porque se producen demasiados eventos de [**VALUECHANGE de \_ objeto \_ de evento**](event-constants.md) que no transmiten información útil.

Por ejemplo, en una ventana que contiene una región rectangular que muestra la palabra "sí" Si se mueve en un patrón de figuras-ocho, el [**rol**](role-property.md) es el [**\_ \_ gráfico del sistema de roles**](object-roles.md), la propiedad [**valor**](value-property.md) es la cadena que se muestra, la propiedad [**Ubicación**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) es el rectángulo delimitador alrededor del texto y se establece la marca de atributo [**\_ \_ animado del sistema de estado**](object-state-constants.md) . La [**Descripción**](description-property.md) es "la palabra ' sí! ' se desplaza por la pantalla en un patrón de figuras-ocho. " El servidor solo genera [**eventos \_ \_ STATECHANGE de objeto de evento**](event-constants.md) cuando el objeto inicia o deja de animaciones.

 

 




